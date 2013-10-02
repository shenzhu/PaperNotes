# The YouTube Video Recommendation System
---

## Keyword
***Information Storage and Retrieval***, ***Information System Applications***

## Introduction

### Goals
- Provide personalized recommendations that help users find high quality videos relevant to their interests.
- Recommendations are updated regularly and reflect a user's recent activity on the site.
- Top-N recommender.
- Maintain user privacy and provide explicit control over personalized user data.

### Challenges
- Videos uploaded by user are often have no or very poor metadata.
- The video corpus size is roughly on the same order or magnitude as the number of active users.
- Videos on YouTube are mostly short form.
- User interactions are thus relatively short and noisy.
- Many of the interesting videos on YouTube have a short life cycle going from upload to viral in the order of days requiring constant freshness of recommendation.

## System Design ##
1. We want recommendations to be reasonably recent and fresh as well as diverse and relevant to the user's recent actions.
2. Users understand why a video was recommended to users.
3. Using user's personal activity as seeds and expanding the set of videos by traversing a co-visitation based graph of videos.

### Input data

### Related Videos
We define a user is likely to watch after having watched the given seed video v.

*see formula in the paper pdf file*

### Generating Recommendation Candidates
In practice, the related videos for any videos that are very similar to the seed video.

*see formula in the paper pdf file*

### Ranking
- Video quality
- User specificity
- Diversification
Use a ***liner combination*** of these signals. 

### User Interface

### System Implementation
We choose a ***batch-oriented pre-computation*** approach rather than on-demand calculation of recommendations.

**Three parts of YouTube's recommendation system:**

- Data collection
- Recommendation generation
- Recommendation serving

## Evaluation
**We use a combination of different metrics. The primary metrics we consider include click through rate, long CTR, session length, time until first long watch and recommendation coverage.**

## Results
*see the graph in the paper pdf file*

## Location
***D:\Papers\ACM RecSys.2010.James Davidson.pdf***

---