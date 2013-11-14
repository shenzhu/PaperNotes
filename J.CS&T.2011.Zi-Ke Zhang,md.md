# Tag-Aware Recommender Systems: A State-of-the-art Survey

## Keywords
***social tagging systems***, ***tag-aware recommendation***, ***network-based***, ***tensor-based***, ***topic based methods***


## 1. Overview of Tag-based Recommender Systems
Social tags can be considered as useful resource for designing effective recommendation algorithms:

- Tags are freely associated by users, so it can reflect **personalized preferences**
- Tags express **semantic relations** among items
- The co-occurrence properties of tags can be employed to build both **user communities** and **item clusters**, which be further made use of to find **relevant yet interesting items** for targeted individuals.

Some problems of using tag:

- **Singularity** vs. **plurality**: cat and cats
- **polysemy** vs. **synonymy**: two meanings of apple
- different online tagging systems allow users to give different **formats** of tags


Some effects to solve above issues:

- **Clustering-based** methods can alleviate the word reduction problem
- **Semantic methods** are discussed to use ontology-based to organize tags and reveal the semantic relations among them.
- **Dimension reduction** and **topic-based** methods can solve the **sparsity problem** in large-scale datasets


Three application domains of tag:

- Predicting friends to users
- Recommending items to users
- Pushing interesting topics(tags) to users

## 2. Tag-Aware Recommendation Models
### 2.1 Evaluation Metrics
Partition of datasets: the training set always contains **90%** of entries, and the remaining **10%** of entries, constitute the testing set.

Metrics of Accuracy:

- Ranking Score(RS)
- The area under the ROC curve
- Recall

Metrics of Diversity:

- Inter Diversity(InterD)
- Inner Diversity(InnerD)


### 2.2 Network-based Models
*see this part in the paper*
### 2.3 Tensor-based Models
*see this part in the paper*
### 2.4 Topic-based Models
*see this part in the paper*

## 3. Conclusions and Outlook
**Conclusions:**

Network-based and tensor-based methods can overcome the **sparsity of large-scale data**, hence can be used for designing efficient algorithms. However, they only focus on the network structure, while lack considerations of relations among tags. Comparatively, topic-based methods can **distinguish tags into different topics**, hence can produce more meaningful and understandable recommendations. However, since most of topic-based methods use machine learning to iteratively
refine the results, they require **high efficient** hardwares for computation, and thus consume more computation time. Similar problem lies in tensor-based methods for dimension reduction process. Therefore, a unified model might be considered to fully make use of
their advantages and provide a more promising method in tag-aware recommender systems.

**Challenges:**
- the use of **complete hypergraph** without decomposing any information.
- now system recommend **single type of nodes**, we can recommend **joint node pair**
- **tag clustering methods** and **anti-spam** technique would be both promising ways to reduce the **noise** and help provide high-quality recommendations
- use **probability-based** models to recommend items not just tags to users
- use **multi-layered** network
- most tagging platforms are dynamical systems and evolve over time, thus the study of human dynamics in analyzing the temporal behaviors and interests can provide **real-time** recommendations.

## Ideas
Three models of tagging models have their advantages and drawbacks, so we may use a **hybrid model** that integrates several models to make recommendations. 

## Location
***D:\Papers\J.CS&T.2011.Zi-Ke Zhang.pdf***

## Date
**2013.11.14**