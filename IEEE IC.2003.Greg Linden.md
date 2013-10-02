# Amazon.com Recommendations Item-to-Item Collaborative Filtering
---
## Keyword
***Collaborative filtering***

## Abstract
Many applications use only the items that customers purchase and explicitly rate to represent their interests, but they can also use other attributes, including ***items viewed***, ***demographic data***, ***subject interests*** and ***favorite artists***.

## Challenges for e-commerce recommendations algorithms
- **Data too large**
- **Realtime high-quality recommendations**
- **Limited information for some customers**
- **Customer data is volatile**

##Recommendation Algorithms
- **Algorithms aggregates items from their similar customers: *Collaborative filtering* and *cluster models***
- **Algorithms focus on finding similar items: *search-based models* and *item-to-item collaborative filtering*** 

### Traditional Collaborative Filtering
N-dimensional vector, cosine of vectors.
Conclusion: O(M + N)(big), hard to simplify(will have bad influence on quality).

### Cluster Models
Divide customers into segments, classification.
Conclusion: Optimal clustering over large data sets is impratical, better performance than TCF

### Search-Based Methods
Search similar items, keywords
Conclusion: Impractical to baser a query on all the items.

#### Item-to-Item Collaborative Filtering
Similar-items table, offline

## Questions && Ideas
- **Can we use several algorithms together to perform a better recommender system?**
- **What is the flaw of Item-to-Item Collaborative Filtering?**

## Location
**D://Papers//IEEE IC.2008.Greg Linden.pdf**

---