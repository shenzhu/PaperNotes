# Using Twitter to Recommend Real-Time Topical News
---
## Keyword
***Content-based recommendations***, ***News recommendations***, ***Real-time recommendations***, ***Social recommendations***, ***Twitter***

## Introduction
Current recommender systems are limited in their ability to identify such stories because, typically, they rely on a **critical mass** of **user comsumption**, before such stories can be recognised. In this paper, we harnessing a popular **micro-blogging service** such as Twitter as a source of current and topical news. 

## Recommending Topical News
RSS is a **data format** that is designed to provide **access to frequently updated content**.

Twitter is so-called **micro-blogging** service.

We have the idea that **mining tweets** can provide access to emerging topics and breaking events and that this information can be used as the basis for a novel approach to ranking RSS news feeds so that topical articles can be effectively **promoted**.

### Recommendation Approach & Architecture
The Buzzer system comprises 3 basic components:

1. Web-based configuration interface: for users to provide their Twitter account and RSS. Providing Twitter account is **optional**, we can use Twitter's **public timeline** as source of news.
2. Lucene Indexer: mining and indexing tweets and RSS information.
3. Recommendation Engine: generates a ranked list of RSS stories based on the co-occurence of popular terms within the user's RSS and Twitter indexes.

*see the Buzzer architecture picture in the paper*
*see the algorithm picture in the paper*

### Example Session & User Interface
Three options for user:

1. Public-Rank: mine tweets from the Twitter **public timeline**
2. Friends-Rank: mine tweets from the **users' friends**
3. Content-Rank: score articles according to the frequency of occurence of the top-100 RSS terms.

The Buzzer page also shows a standard **term/frequency tag cloud** that includes terms ordered and sized based on the **frequency of each item**.This is also useful in **explaining to the user**.

## Preliminary Evaluation
We see that these usage results suggest a preference for the **Friends-Rank recommendations** compared to the recommendations derived from **Twitter's Public Timeline**.This suggests that users are more likely to tune in to the themes and topics of interest to their friends than those that might be of interest to the Twitter public at large.

There is a strong preference for the **Public-Rank** articles.

We also found a **correlation coefficient** of **-0.89**, suggesting that users with more friends tend to benefit more so from the **Friends-Rank recommendations**.

## Conclusions

## Question & Ideas
- There are also many ways in which the content-based recommendation technique may be improved: moving from single terms to **more complex phrases**, which may improve the recommendation ranking.
- Focus on **perfecting the scoring techniques**.
- Provide additional recommendation services such as **recommending new RSS feeds** to users or **recommending relevant people** to follow on Twitter

## Location
***D:\Papers\ACM RecSys.2009.Owen Phelan.pdf***

## Date
**2013.10.9**