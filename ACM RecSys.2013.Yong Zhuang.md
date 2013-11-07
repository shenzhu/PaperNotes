# A Fast Parallel SGD for Matrix Factorization in Shared Memory Systems

## Keyword
***Recommender system***, ***Matrix factorization***, ***Stochastic gradient descent***, ***Parallel and vector implementations***

## Problem
There have been some **parallel algorithms** using **stochastic gradient descent** to optimize **matrix factorization**, thus making recommendations for users, such as **HogWild** and **DSGD**, but the algorithms has two shortcomings: **data discontinuity** and **block imbalance**.

- **Locking problem**: For a parallel algorithm, to maximize the performance, keeping **all threads busy** is important. A simple to make blocks of matrix more balanced is **random shuffling**, but the amount of ratings in each block may still not be exactly the same. Further, even if each block contains the same amount of ratings, the computing time of each code can still be slightly different.
- **Memory Discontinuity**: When a program accesses data in memory discontinuously, it suffers from a **high cache-miss rate** and **performance degradation**

## Improvements 
- **Lock-Free Scheduling**: For a block, if it is independent from all blocks being processed, then we call it a **free block**. When a thread finishes processing a block, the scheduler assigns a new block that meets the following conditions:
	- It is a **free block**
	- Its number of past updates (processing time) is the **smallest** among all free blocks
Therefore, we can always assign a free block to a thread when it finishes updating the previous one.


- **Partial Random Method**: Partial random method selects ratings in a block orderly but **randomizes** the selection of blocks, the randomness can be enhanced by griding matrix into **more blocks**.

## Summary
This paper describes the fast parallel SGD for matrix factorization, it is mainly about using **parallel computing** in recommendation algorithms.

- Ideas: We may use the **lock-free scheduling** and **partial random method** techniques to improve other recommendation algorithms.

## Location
***D:\Papers\ACM RecSys.2013.Yong Zhuang.pdf***

## Date
**2013.11.6**