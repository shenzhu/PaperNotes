# Self-adjusting Hybrid Recommenders Based on Social Network Analysis

## Keyword
***Hybrid recommender system***, ***Social Networks***, ***Graph Theory***, ***Link Analysis***

## 1. Introduction
Although social recommenders perform very well in some situations, they usually can not provide any suggestion to users without a **social context**(social **cold start**).

One of the most common forms of ensemble recommenders simply consists in a **liner combination** of recommenders. In this approach, the weights in the linear combination are generally the **same** for all users.

We explore the **adaptive adjustments** of the **ensemble coefficients** on a user basis. We also explore a new approach for **self-adjusting** the weight of each recommender by using **social network analysis** to balance the influence of each recommender.

## 2. Self-Adjusting Recommenders
We mainly focus on **weighted hybrid recommenders**, in which the scores of n individual techniques are aggregated by a **linear combination**, and usually, the weights is static, so recommendations from each technique recieve the **same** weight independent of the **target user**.

The traditional static way has two main drawbacks:

- Firstly, the optimal weight has to be **found empirically** by relving on current recommender performance, dataset characteristics.
- Second, the optimal weight may not be the same for all users since the system gathers a **different amount** of information from each user.

We explore a **self-adjusting hybrid recommendation** approach that makes user of **adjusting factors** to boost one of the combined recommenders for certain users.

We analyze a particular hybrid configuration in which we combine **social and CF** recommenders. In this context, we propose to user **graph-based** measures as **adjusting factors** of the users' strength in the network, by balancing the influence of each recommender.

## 3. Experiments
*see the result table in the paper*

Finally, it is worth noting that single approaches obtain **lower accuracy** values than hybrids on equal terms since they **deal poorly** with the social cold start situation.

The empirical results thus suggest that significant improvements can be drawn from the **proposed self-adjustment** strategy based on **graph-based** social factors.

## Questions & Ideas
***Questions:***

- The paper does not describe **the whole** algorithm, it just says the idea, so if we want to use the system in the future, we need to **figure out** the algorithm.


***Ideas:***
- In this paper, researchers use **degree**, **average neighbordegree**, **two-hop neighborhood**, **PageRank** and **HITS** scores, we may use other things as adjusting factors to fortify the system.

## Location
***D:\Papers\ACM SIGIR.2011.Alejandro Bellogin.pdf***

## Date
**2013.10.12**

