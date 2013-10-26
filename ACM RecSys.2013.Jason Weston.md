# Nonlinear Latent Factorization by Embedding Multiple User Interests

## Keyword
***Collaborative filtering***, ***learning to rank***, ***matrix factorization***, ***nonlinear models***

## Improvement
In this paper, the researchers come up with a new method to improve the traditional **latent factor model**. In the traditional latent factor model, both user and item are assigned to a **m-dimensional vector**, researchers think in that way the user has the same capacity as a single item, but in fact, user should is a more complex entity that item.

They model a user with **T** latent vectors, each of dimension m, that model the user's latent tastes. Each item still has a **single m-dimensional** latent feature vector. Then the score between a user and a given item is the maximum match between the user tastes and the given item.

## Questions & Ideas
As it uses the maximum math between the user tastes and the given item, why wouldn't it cause the **overfit problem** ?

Is it really the best way to use the maximum match, what if we use a **weighted average value** ?

Why a overfit problem would happen if we increase the **item embedding dimensionality** ? 

And why increase the user embedding dimensionality does not cause the **memory** problem ?

## Location
***D:\Papers\ACM RecSys.2013.Jason Weston.pdf***

## Date
**2013.10.25** 