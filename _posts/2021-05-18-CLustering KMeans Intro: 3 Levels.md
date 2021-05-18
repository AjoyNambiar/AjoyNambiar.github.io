---
published: false
---
## 3 Levels to undestand KMeans Algorithm

Clustering as name suggest if the acitivty of grouping and finding themes within the objects. We do it all the time without thinking about it, one unpacks their grocery bag and stores veggies in veggie tray, sugar goes in the cupboard sits next to tea. You get the idea.


Here I try to break down a a Machine Learning algorithm called KMeans which does clustering in 3 steps. I think of it as levels of thinking each progressively more detail than the previous so if you want a preview or wants to start clusteing your data with python this can be good starting point.

Before we begin lets state logic behind clustering. It is to maximize the **similarity** of data within cluster and maximise the **dissimiarity** between clusters

1. Level 1: Whats the use case of clustering?

- _Customer Segmentation_. Business want to cluster their customers so they can improve the customer experience. Think about the Netflix or Amazon recommender system, here consumers are clustered from the shopping/ viewing behaviour and recommender uses it to next recommendation. Here the clustering will bring better customer experience retaining existing consumer or convert a prospect.

- _Document Classification_. With increasing amount of digital text and books an efficient way to catgegorize the those books is needed. Here clustering algorithm can help classifying using frequency of words, exisiting book tags into clusters. This increases the correct audience to reach the books efficiently.

- _Credit Card Fraud Detection_. This is part of outlier detection. Here a 'normal' credit card usage say paying utility bills, usage at grocery stores is compared against the 'odd' usage like high amount usage in overseas country may be flagged as possible fraud and trigger a validation response leading to increased authentication checks like calling the client to verify the transaction.

I have listed a few of the top business use cases where business can use data to generate the clustering alorithm to gain insights. Here I want to point out that the interpreation of cluster is key hence involvement of domain specialist is important to give context. In many cases the cluster results may be useless and one should be ok to live with it. 
On a more general note these algorithm can help people cluster their data and help then fix patterns when they are exploring the data


Enter text in [Markdown](http://daringfireball.net/projects/markdown/). Use the toolbar above, or click the **?** button for formatting help.
