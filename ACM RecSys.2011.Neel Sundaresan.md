# Recommender Systems at the Long Tail
---
## Keyword
***Algorithms***, ***Economics***, ***Human Factors***, ***Measurement***

## 1. Introduction
Recommender systems are **information filtering systems** where users are recommended "relevant" information items at the **right context** at the **right time** with the goal of **pleasing the user** and **generating revenue** for the system.

## 2. The Market Place

### 2.1 The Scale
Items are listed in **explicitly defined hierarchy** of categories and there are over 30000 nodes in this category tree.

### 2.2 Product Dimension

### 2.3 Buyer Dimension

### 2.4 The Seller Dimension 

### 2.5 Buyer-Seller Handshake
Buyers who search for products may use a **different language** than users, there is a **gap** between them.

While this gap introduces **additional stress** in the **search system**, it opens up **opportunities** for recommender system to fill the gap by using the knowledge **mined** from **savvy buyers** and helping other buyers.

### 2.6 Opportunities and Challenges
***Opportunities:***:

- There are a number of stages the buyers need to go through, **searching**, **finding**, **watching**, **revisiting**, **bidding**, **buying** and **paying for items**. Each of the stages offer opportunities for the recommender system.
- Recommendations may involve **queries**, **categories**, **products** or **items** and even **sellers** to buyers

***Challenges:***

- **Long tail**, **transient nature** of the inventory, the **diversity** in condition and format, **multi-seller market**
- All of these introduce **super sparsity** in **any relationship matrix** and applying well-known algorithms as is(**content-based,=**, **collaborative** or **neighborhood** algorithms) difficult. 

## 3. Six Senses: 5 Ws and An H
Recommender fill the **gap** between **what the buyer needs**, says **what she needs**, and **what is **available**.

### 3.1 The What
*see in 2.6 - opportunities*

### 3.2 The Where
The right context determines the right recommendations, we may recommend **different items** for **different scenarios**. For instance, the search results, the bid page, the checking page, the post-transaction scenario and even in non-transaction flow.

### 3.3 The When
We incorporate a **time window factor** into the standard recommender system model. The time window factor indicates the **time difference** between the purchase time and the recommendation time.

### 3.4 The Why
Why dimension is required to reason to the user **why certain recommendations are presented**.

### 3.5 The Who
- This dimension addresses the **personalization aspect** of recommender system.
- For casual buyers recommender systems work much better than for a power buyer, over-recommending is likely to cause **user fatigue**.
- Capturing appropriate buyer dimension into the recommender system becomes important.
- Typical personalization in recommender systems user **supervised** or **semi-supervised** approaches to fit the model parameters to some predined user profile attributes.

### 3.6 The How
***see the techniques that are used in eBay in the paper***

## 4. The eBay Space

### 4.1 Trust

### 4.2 The Robinhood Approach
We discussed user diversity and varying expertise. Another way to smooth is to take advantage of the **user expertise**. This can be used to the **benefit of inexperienced** users.

Simply by relating queries that are typed in the same session a graph of query relations is built, the graph mining combines **linguistic and behavior relationship** between queries accounting for user expertise. For instance, "apple ipod mp3 player" and "creative mp3 player" are linked.

*see the picture and table in the paper*

### 4.3 Cross-Category Recommendation

### 4.4 Of Populars and the Serendipitous
Recommending **buzzing**, **trending** or **popular inventory** can generate buying activity, also the unique one-of-a-kind nature of the inventory lends itself to building **novel serendipitous** experience.

### 4.5 The Elephant helps scale
All of our algorithms are built over a large scale **Hadoop Map-Reduce** infrastructure.

Since most matrix operations are reduction operations are **data-parallelizable** it is possible to combine **Hadoop with such GPU-based data parallel** local compute-intensive operations.

## 5. Conclusion Remarks

## Questions & Ideas
***Questions:***

- The algorithms used in eBay, which is the 3.6 part of the paper.

***Ideas:***

- As e-commerce grows more social and mobile, new dimensions get added like **location-aware** or ** app-based** or **game-based** recommender system. The future for this space is bright and vibrant and should provide amazing research opportunities.

## Location
***D:\Papers\ACM RecSys2011.Neel Sundaresan.pdf***

## Date
**2013.10.11**
---