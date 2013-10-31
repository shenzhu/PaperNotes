# Personalized News Recommendation with Context Trees

## Keyword
***online recommender system***, ***personalization***, ***news***

## Improvement
Recommending news has specific challenges: news preferences are subject to trends, users do not want to see multiple articles with similar content, and frequently we have insufficient information to profile the reader.

This paper proposes a new method for recommending news: it combines the **context tree** with a prediction model **expert**.

A context tree defines a **partition tree** organized in a hierarchy of increasingly precise partitions of a space of contexts. They consider as context the **sequence of articles**, **the sequence of topics**, or the **distribution of topics**. Each node int the tree is called **context** and corresponds to a set of sequences or topics distribution within a partition. The main idea if to give **context-dependent** recommendations, with contexts becoming progressively **finer-grained deeper** in the tree.

In this paper, the **expert** prediction model takes into account the **popularity** and **freshness**.

## Questions & Ideas
The main topic of the paper is taking advantage of **context tree** to make recommendations for news. The model is **dynamic**. We may think to use the **context-tree** model on present recommender algorithms based on contents. And the **finer-grained deeper** feature of context tree may be used in somewhere else.

## Location
***D:\Papers\ACM RecSys.2013.Florent Garcin.pdf***

## Date
**2013.10.31** 