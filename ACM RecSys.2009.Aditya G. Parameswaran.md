# Recommendations with Prerequisites

## Keyword
***Recommendation Algorithm***, ***Graph Theory***

## 1. Introduction
A prerequisite of an item i is another item j that must be taken or consumed **in advance** of i. Thus, it makes sense to consider prerequisites with making recommendations.

**CourseRank** is a social tool developed in our InfoLab and used by students to evaluate courses and plan their academic program.

Although our focus is a on prerequisites in an academic environment, prerequisites also arise in other recommendation contexts.

## 2. The Problem of Prerequisites
Defines the variables and notations used in this paper.

## 3. The 3 Algorithm
Since the problem of recommendation with prerequisites is **NP-Hard**, we can only provide **approximate solution**.

### 3.1 Illustrative Example

### 3.2 Definition 
We define **boundary**(A) of a set A as the set of items in A that can be deleted, without violating the **prerequisites** of any other items in the set.

We define **external**(A) of a set A as the set of items that **are not in** A and can be potentially added to A without **violating prerequisites**.

### 3.3 Algorithm 1: Breadth-first Pickings

#### 3.3.1 Example
#### 3.3.2 Description of the Algorithm
As listed in Algorithm 1, we initialize the set A with the best k items by picking **greedily the best item** from among the items whose prerequisites **have been satisfied**, but are not already in the set A.(line 2-4)

We then **greedily** try to replace items from **boundary(A)**, i.e., the items that are non-essential to A, with those from **external(A)**, those whose prerequisites have been satisfied(line 7-14). However, we make sure that we do not delete the **parent** of a child(line 8).

*see the pseudo code of Algorithm 1 in the paper*

### 3.4 Algorithm 2: Greedy-value pickings
We use a **max-priority-queue** for this algorithm, and insert sets of items into the queue.

#### 3.4.1 Example

#### 3.4.2 Description of the Algorithm
We insert all **sub-chains** present in graph into the queue(line 3-7), sorted on average **score**.

Now, as long as we have not picked enough items in A, we keep picking chains by **popping sets from the queue**(line 8-9). If the popped set is small enough to be accommodated in A(line 10), we add it to A(line 11), and update the values of other sets that correspond to **super-chains**(line 12-16) and **sub-chains**(line 17-19). Super-chains will now get truncated given that the set corresponding to the current chain has been picked. Sub-chains can **no longer** be picked, since the current chain has been picked.

*see the pseudo code of Algorithm 2 in the paper*

### 3.5 Algorithm 3: Top-down pickings

#### 3.5.1 Example

#### 3.5.2 Description of the Algorithm
Initially let a be the **top-k** and B to be the set of items already considered.

We start off with the **best set** of items of size k(line 1), and try to **incrementally add prerequisites**. We keep track of items that we have already added prerequisites for in B(line 6), and never let such items be **deleted**.

We pick the items in order of decreasing scores from A-B, i.e., the items that have not been examined already(line 4). We then check if the prerequisites of the item are already present in A(line 7), if so, we examine the next item.

If there are still some s prerequisites required(line 8), we replace items from A if possible(line 11-14,18). These items are picked from **boundary(A)**, but should not be present in the items already consider B(line 12-13).

IF sufficient items cannot be found we replace the item under consideration with and item form **external(A)**(line 16), i.e., those items that be potentially added because their prerequisites are present.


*see the pseudo code of Algorithm 3 in the paper*

## 4. Related Work

## 5. Conclusions
- We studied how prerequisites affect the problem of recommendations . We focused on the problem of recommending a set of items with **high score**, while **satisfying prerequisites**. We proved that this problem is **NP-Hard**.
- We found that the **greedy value pickings algorithm** consistently performs better than the other two algorithms, and performs even better if we **increase the number** of items picked relative to the number of chains. However, this algorithm may be more **expensive computationally** than the other two
- We also found that there are cases where the **breadth first picking algorithm** does better than the **top down pickings algorithm**, specially when the number of items is **small** relative to the number of chains.

## Questions & Ideas
This paper chose a good perspective of recommendations, we may do some further research in the field.

## Location
***D:\Papers\ACM RecSys.2009.Aditya G. Parameswaran.pdf***

## Date
**2013.10.15**