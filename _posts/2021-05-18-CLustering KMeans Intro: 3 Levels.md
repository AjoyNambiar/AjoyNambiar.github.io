---
published: false
---
## 3 Levels to undestand KMeans Algorithm

Clustering as name suggest if the acitivty of grouping and finding themes within the objects. We do it all the time without thinking about it, one unpacks their grocery bag and stores veggies in veggie tray, sugar goes in the cupboard sits next to tea. You get the idea.


Here I try to break down a a Machine Learning algorithm called KMeans which does clustering in 3 steps. I think of it as levels of thinking each progressively more detail than the previous so if you want a preview or wants to start clusteing your data with python this can be good starting point.

Before we begin lets state logic behind clustering. It is to maximize the **similarity** of data within cluster and maximise the **dissimiarity** between clusters

Level 1: Whats the use case of clustering?

- _Customer Segmentation_. Business want to cluster their customers so they can improve the customer experience. Think about the Netflix or Amazon recommender system, here consumers are clustered from the shopping/ viewing behaviour and recommender uses it to next recommendation. Here the clustering will bring better customer experience retaining existing consumer or convert a prospect.

- _Document Classification_. With increasing amount of digital text and books an efficient way to catgegorize the those books is needed. Here clustering algorithm can help classifying using frequency of words, exisiting book tags into clusters. This increases the correct audience to reach the books efficiently.

- _Credit Card Fraud Detection_. This is part of outlier detection. Here a 'normal' credit card usage say paying utility bills, usage at grocery stores is compared against the 'odd' usage like high amount usage in overseas country may be flagged as possible fraud and trigger a validation response leading to increased authentication checks like calling the client to verify the transaction.

So these were some cases business can use data to generate the clustering alorithm to gain insights. Here I want to point out that the interpreation of cluster is key hence involvement of domain specialist is important to give context. In many cases the cluster results may be useless and one should be ok to live with it. 
On a more general note these algorithm can help people cluster their data and help then find patterns when they are exploring the data and understand it better.

Level 2: What does the  KMeans Clusering do?

1. Start by choosing K random points the initial cluster centres.
2. Assign each data point to their nearest cluster centre. The most common way of measuring the distance between the points is the Euclidean distance
3. For each cluster, compute the new cluster centre which will be the mean of all cluster members
4. Now re-assign all the data points to the diffrent clusters by taking into account the new cluster centres
5. Keep iterating through the step 3 & 4 until there are no further changes possible

![Capture1.JPG]({{site.baseurl}}/_posts/Capture1.JPG)




<script src="https://gist.github.com/AjoyNambiar/a694f35e11e3cf4b2a482016b34e0205.js"></script>


[https://gist.github.com/AjoyNambiar/a694f35e11e3cf4b2a482016b34e0205](https://gist.github.com/AjoyNambiar/a694f35e11e3cf4b2a482016b34e0205)


Enter text in [Markdown](http://daringfireball.net/projects/markdown/). Use the toolbar above, or click the **?** button for formatting help.
