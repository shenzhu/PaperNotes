# Dynamic Personalized Recommendation of Comment-Eliciting Stories
---

## Keyword
***Collaborative filtering***, ***user comments***, ***personalization***

## Introduction
A common feature of many present-day media sites is their attempt to enrich user engagement by **soliciting** and **distributing** user generated comment(**UCG**), and in particular users' comments on content.

This work aims to present to each commenting user a personalized **list of stories** that may engage the user to the point of commenting on them.

Using a combination of **story vocabulary** and **collaborative filtering** signals that utilize **co-commenting patterns** of users, a **latent factor model** was shown to have a good predictive signal.

***Contributions:***

1. Extend the traditional train-test analysis with a **continuous, dynamic approach** that enables personalized recommendation of stories in **real time**.
2. Demonstrate the strong effect of a media site's structure and the ephemeral nature of the news articles on the **commenting patters** of users. At any moment only a **small subset** of stories is heavily clicked, read and eventually commented on. This **presentation bias**  obscures the ideal commenting preferences of users, who end up commenting on the **"better of what's featured"** rather than **"best of what's available"**
3. Results show that we are able to overcome the site's **inherent presentation bias** and outperform the strong baseline above as **users' commenting history grows**.
4. We develop a **framework** for prediction that simulates on **on-line scenario** using **off-line data**.

## Problem Settings
Stories that are highly trending now may be **far less relevant** in an hour. **Time** play a **major role** in our experiments, which simulate **real-time** recommendations using **only historical off-line** data.

### Data Description
Tuples***(user, story, creation time)***

### Prediction Problem Definition 
**four points, see it in the paper**

### Evaluation Metrics
1. **Mean Reciprocal Rank(mrr)** - the average of the inverse ranks 
2. **Recall@K** - the ratio of comments from **C***test* with rank lower or equal K

## Baseline Predictor
### Description
The baseline predictor we applied is based on **recent commenting trends** which we denote as the **Trending Score(TS)**, the **normalized version of the trending score** called **NTS**. 

*see the formulas in the paper*

### Baseline Results
- For low values of *l* the results are **worse**, as **every comment written** by some user has a strong effect on the **story NTS**.
- For higher values of *l*, recall results are **better and more stable**.
- The value of *l* = 15 exhibited the **best results**
- We see that **'heavy commenters'** are **harder to predict** using the **trending score baseline**.

## Personalized Predictor
Our system learns a **latent factor** of dimension *d* for each **user, tag and co-commenter**.

When a user comments on a **non-trending story**, our model should have evidence of a strong link between this paper and the story.

### Prediction Mechanics
***see the description and formulas in the paper***

For the final formula, its left part is responsible for the **temporal dynamics**, its right additive is the **personalization part**.

### Error Function
In the training stage we train **all latent factor vectors in order** to **minimize a cost function**. The cost function for minimization is an **aggregation** of a **loss function**, **computed per all user-story scores** over the training period.

*see the formula in the paper*

We train our model by **employing stochastic gradient descent** with **early stopping**. Each iteration **enumerates all training comments**, updating both the **trending score** for all stories and the various latent factor models.

### Continuous Learning
Every **user-story score** changes during simulation because:

1. The trending score is **constantly changing**.
2. When comments are **added to a story**, **its representation changes**, also affecting **the user-story score**.

## Results
*see the result graphs in the paper*
### Content Vs. Collaboration
- Results are best when combing the **tag** and **co-commenting data**.
- We see that the additional signals significantly improve over the **non-personalized baseline**, especially for stories that have yet to **accumulate many comments**.

### Advantage of prior user information
The baseline predictor **deteriorates** for users **with longer history**

### Continuous learning results
The **tag + commenters with additional learning after 60 days** method  
coincides with the **tag + commenters** for the first simulation period, and outperforms it afterwards once additional learning is performed.

## Conclusion and Future Work
This work presented a **dynamic, real-time latent factor modeling approach** for prediction of stories that users are **likely to comment on**.

## Questions & Ideas
***Questions:***

- ***"***For low values of *l* the results are **worse**, as **every comment written** by some user has a strong effect on the **story NTS*****"***
- The **cost function** in **Error Function**

***Ideas:***

- The method can be further improved by **re-training of the model** over time.
- We plan to further **tune the presonalization factor** in an **on-line experiment** of the proposed user experience.

## Location
***D:\Papers\ACM RecSys.2012.Michal Aharon.pdf***

## Date
**2013.10.10**
---


