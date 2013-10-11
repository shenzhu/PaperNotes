# Estimating the Magic Barrier of Recommender Systems: A User Study

## Keyword
***recommender systems***, ***evaluation***, ***noise***

## Main Problem
**Current evaluation methods of recommender system may not be appropriate because of the inherent noise of user data**

## 1. Introduction
The magic barrier is a **theoretical boundary** for the level of optimization that can be performed on a recommender algorithm on known transactional data.

The evaluation models assume that recorded transactions, whether ratings on movies or purchases of items reflect a ***ground truth***: that the historical transactions users have performed are **free of noise**.

Most RS evaluation still uses traditional information retrieval measures and methods, even though these might not always reflect the **actual quality** of the recommendation.

The study is intended to capture the **natural level** of noise in **users' ratings**. The initial results from the study confirm the notion that users' ratings are **inherently noisy**, and that the ratings should not be seen as an **absolute truth**.

## 2. Estimating the Magic Barrier

## 3. User Study
The study was performed through a webpage mimicking the look-and-feel of the moviepilot website, on this page users were presented with a random selection of movies they had previously rated, with the ratings **withheld**. Users who chose to participate in the study was asked to give ***opinion*** on movies, the term opinion was used in order to mitigate the implicit meaning of **re-rating***.

## 4. Results and Discussion
- The study collected only **one** opinion **per user-movie** pair, which could introduce potential noise in the opinion values. In a more thorough study collecting **several opinions** of a user about the same item, we expect to reach a lower estimate of the magic barrier due to **lower noise** when **averaging several user-opinion pairs**.
- The results showed that only if the rating and opinion had been performed within **a very short timespan** of each user did the RMSE become **lower**, in other cases, the RMSE stayed at a **constant level**. Due to the temporal aspect being of little difference in terms of RMSE, the results of the study argue for the fact that difference between ratings and opinions were **not introduced by time**.


## 5. Conclusion & Future Work
The so-called **magic barrier** of recommender systems can be better assessed by **noise estimation** in scenarios similar to ours, seems to hold.

## Questions & Ideas
***Ideas:***

- We are currently in the process of processing the data from the study, and preparing a larger scale study in a similar environment in order to gain **enough empirical data** for a final model for magic barrier estimation.

## Location
***D:\Papers\ACM SIGIR.2012.Alan Said.pdf***

## Date
**2013.10.11**


 