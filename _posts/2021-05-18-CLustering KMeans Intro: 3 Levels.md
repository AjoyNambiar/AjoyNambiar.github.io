---
published: true
---
## 3 Levels to undestand KMeans Algorithm

Clustering as name suggest if the acitivty of grouping and finding themes within the objects. We do it all the time without thinking about it, one unpacks their grocery bag and stores veggies in veggie tray, sugar goes in the cupboard sits next to tea. You get the idea.


Here I try to break down a a Machine Learning algorithm called KMeans which does clustering in 3 steps. I think of it as levels of thinking each progressively more detail than the previous so if you want a preview or wants to start clusteing your data with python this can be good starting point.

Before we begin lets state logic behind clustering. It is to maximize the **similarity** of data within cluster and maximise the **dissimiarity** between clusters

**Level 1**: Whats the use case of clustering?

- _Customer Segmentation_. Business want to cluster their customers so they can improve the customer experience. Think about the Netflix or Amazon recommender system, here consumers are clustered from the shopping/ viewing behaviour and recommender uses it to next recommendation. Here the clustering will bring better customer experience retaining existing consumer or convert a prospect.

- _Document Classification_. With increasing amount of digital text and books an efficient way to catgegorize the those books is needed. Here clustering algorithm can help classifying using frequency of words, exisiting book tags into clusters. This increases the correct audience to reach the books efficiently.

- _Credit Card Fraud Detection_. This is part of outlier detection. Here a 'normal' credit card usage say paying utility bills, usage at grocery stores is compared against the 'odd' usage like high amount usage in overseas country may be flagged as possible fraud and trigger a validation response leading to increased authentication checks like calling the client to verify the transaction.

So these were some cases business can use data to generate the clustering alorithm to gain insights. Here I want to point out that the interpreation of cluster is key hence involvement of domain specialist is important to give context. In many cases the cluster results may be useless and one should be ok to live with it. 
While business use case gives some background, personally I think more day to day usage is for data analyst using these technique to cluster their data and help find patterns or themes when they are exploring the data and understand it better especially when size of dataset is big.

**Level 2**: What does the  KMeans Clusering do?

Follow 
1. User loads the dataset n datapoints and inputs K random points the initial cluster centres - this is where user hands over control to machine.
2. Machine assigns each data point to their nearest cluster centre. The most common way of measuring the distance between the points is the Euclidean distance
3. For each cluster, compute the new cluster centre which will be the mean of all cluster members
4. Now re-assign all the data points to the diffrent clusters by taking into account the new cluster centres
5. Keep iterating through the step 3 & 4 until there are no further changes possible

![Capture1.JPG]({{site.baseurl}}/_posts/Capture1.JPG)


![Capture1.JPG]({{site.baseurl}}/_posts/Capture1.JPG)


If you are wondering what centroid is think of it as mean/ avergae or its the same as center of gravity from high school physics. Essentially what we have done is the found clusters whose centroids are 'Close' (similar) to points within cluster and 'Far' (dissimilar) from points from points from other cluster.

On side note here the example shows a 2-D clustering problem, in real world the data points can have several feature making it hard to visualize cluster but algorithm works the same.

**Level 3**: Hands on with a Code in Python

Lets start by importing the relvant libararies. The one in focus is KMeans from sklearn.cluster package.

<script src="https://gist.github.com/AjoyNambiar/a694f35e11e3cf4b2a482016b34e0205.js"></script>

Load the data. here I have used open source California housing data from 1990 census, [see kaggle link](https://www.kaggle.com/camnugent/california-housing-prices). It has data for residential housing in California of a 'block' with location - lat/ long, median income of household and other house characteristics.


<script src="https://gist.github.com/AjoyNambiar/edb302de420e8ce6e0a2d8ffe45d1b32.js"></script>

Now for illustration can we cluser this dataset based on median income and housing location. In other words is there a pattern or theme in income and where people live. Let data tells us.

<script src="https://gist.github.com/AjoyNambiar/f684b1a3c14970b49d2a1a7d34cfb427.js"></script>

So what we have here is KMeans has clustered the data and we added the cluster label back to original data, see last column. Now comes the hardest part interpreting if these labels make any sense or not. For this lets go ahead an visualize data with cluser. First lets look at the map using location vs cluster label and next will be income compared with cluster label. Is there a theme here?

![Map.JPG]({{site.baseurl}}/_posts/Map.JPG)

![income.JPG]({{site.baseurl}}/_posts/income.JPG)


With this  
0- Mid income group living in North California in suburbs of San Fracisco

1- Low income living in Suburb of LA or border towns, Mexico

2 -High income living in downtown LA or San Francisco (Hollywood stars?)
