# Design and Evaluation of a Group Recommender System
---


## keyword
***Group recommender***, ***Evaluation***, ***Aggregation strategy***

## Introduction
In literature, group recommendations have mostly been generated either by aggregating the users' **individual recommendations** into recommendations for the whole group or by aggregating the users' **individual preference** model into a preference model of the group. 

- Former algorithm: most of them make a decision based on the algorithm's **prediction value**.
- Latter algorithm: combines the group members' preferences into a group preference model using a **social value function**, social value function describes how the opinions and preferences of individuals affect the group's recommendations, but there is still no optimal solution.

## Related Work
A obvious use case for recommendations is a recipe recommender for **families**. 
An evaluation with a number of families showed that the **aggregating preferences strategy** yield slightly better results than the aggregated recommendations lists. This recommender is based on collaborative filtering and the individual data of group members is aggregated in a weighted manner.

## Group Recommender System

## Recommendation Strategy
1. Before calculating the recommendations, the users' ratings are normalized by subtracting the user's **mean rating** and dividing this difference by the **standard deviation** of the user's ratings.
2. The ratings can be **squared** to incorporate the **quadratic effect** of feedback mechanisms, and the further away from the **middle point** of the scale, the larger the differences between subsequent ratings.
3. There three strategies: **aggregating recommendations**, **aggregating preferences** or a **switching strategy**. The switching strategy generates group recommendations based on the aggregating recommendations strategy if the **profile density** of the group is below a certain threshold.
4. In case of the aggregating recommendations strategy, calculates for each item the average of the prediction values of **each group member's recommendation list**.
5. In case of the aggregating preferences strategy, members' individual preferences are aggregated into a group preference by calculating the **average of the members' rating for each item**.
6. If group members have a **unequal importance weight**, a **weighted average is used as aggregation method to take the relative importance of **each group member** into account.

## Experimental Setup
Algorithms: Collaborative Filtering(CF), Content-Based reommender(CB), hybrid recommender(combines the recommendations with the highest rating prediction of the IBCF and the CB recommender into a new recommendation list. The result is an **alternating list** of the best recommendations originating from these **two algorithms**), **SVD Recommender**, **popular recommender** is introduced as a baseline.

Generate group users: Firstly, all users are **randomly assigned** to one group of a specific size, secondly, group recommendations are generated for **each of these groups**, thirdly, the recommendations are evaluated individually as in the classical **single-user case**, by comparing(the rankings of) the recommendations with(the rankings of)the items in the test set of the user.

For each user, the effectiveness of his group recommendations is evaluated base on his **nDCG**.

## Evaluating Strategies
1. This experiment shows that group recommendations are still useful, even for large groups.
2. Shows a **decreasing performance** of the group recommendations as the groups size **increases** for **all algorithms**.
3. The grouping strategy that provides the most accurate recommendations depends on the **used algorithm**. A possible explanation for these differences in accuracy lies in **the way in which the algorithm processes the data**
4. **SVD** and **hybrid** reommender produce the most accurate group recommendations for various group size.
5. These results are only based on the **MovieLens data**, probably the most optimal combination of algorithm and strategy depends on the **data and scenario at hand**.

## Conclusion
The effectiveness of grouping strategies is influenced by the **used algorithm**. The accuracy of the grouping strategies will be compared for groups which are composed so that the group members have a **high similarity**.

## Questions && Ideas
-Investigate the proposed switching strategy to make the results better.

## Location
***D:\\Papers\\ACM RecSys.2012.Toon De Pessemier.pdf***

## Date
**2013.10.8**
