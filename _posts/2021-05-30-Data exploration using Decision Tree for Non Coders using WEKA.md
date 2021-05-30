---
published: true
---

### ![DT](/images/DT.PNG)


Decision Tree may help explore relationship between variable and check for data consistency. The tree comes from Machine Learning algorithm and If there is a strong theme in data the tree will have high accuracy. The advantage of Decision Tree is simplicity, they help in visualizing the relationship.
In this post I show a way to do it in WEKA open source no-code / GUI based data analysis and machine learning application. GUI is intuitive and users with no background in coding and machine learning can come with their Decision Tree for their data
Just to clarify the goal is not to predict anything, it is to spotlight the dataset.

**Why a decision tree?**
A decision tree is a visual representation of ‘decision’ that is taken based on input data, essentially an in-then-else. Business loves it is very easy to go through and to communicate. The tree starts with a root node which is the first question and then carries down decision nodes, the follow up questions before finally reaching a prediction. 
Above is weird Decision Tree which predicts if one is man or woman based shoes one owns. :)

### Decision Tree for Non-Coders using WEKA
**Here are the steps to build decision tree in WEKA**
Here are I have loaded training file from Titanic data set from Kaggle https://www.kaggle.com/c/titanic
Data shows passenger data – Age, Sex, Name, Travelling Class, Boarding port and finally if they survived the accident. If we are curious in understanding main factors in  passenger survival, Decision Tree can be a good option. 

_Step 1_: Prepare the datset into .csv file for Weka, using Explorer and Open File in Preprocess There are other file formats which WEKA can accept. Once csv file is loaded it you can click each attribute and see the its statistics on middle right – mean, std dev, min, max, distinct and also number of missing values are show. A histogram is shown in bottom right of the attribute and split with a nominal attribute can be plotted – here the split of nominal attribute is show. Blue is people who did not survive and red are one who lived.

![Preprocess](/images/Preprocess.PNG)
 

_Step 2:_ Click Classify on top tab and then choose J48 from tree classifer. Choose the default Cross-validation 10 fold. Choose the main attribute of interest. In this case it is Survived attribute and click Start. The result of the algorithm shows up in output window. Main thing to notice is accuracy – higher means there is presence of a strong theme. There are other metrics here but since our aim is not to predict we can go into reviewing the decision tree.
 
 ![Crossval_result](/images/Crossval_result.PNG)

_Step 3:_ Click visualize tree by right clicking on Result list and then click fit to screen

  ![Viz_tree](/images/Viz_tree.PNG)


_Step 4:_ For illustration a simplified tree is shows below to see what relationship exist between Age, Sex, Plcass attributes against Survive attribute.
So starting from root at the top (root is on top and nodes below – think of it as upside down tree) we see Sex of passenger is very important variable. If passenger is Male and greater than 9 years of age then DT predicts they will NOT survive – it predicts 545 of such passenger will die of which it is not correct for 90 passenger shown as number 945/90 i.e. approx. 10% incorrect. Similarly, for Females who were in cabin class 2 or lower are most likely to survive as shown by number 170/9 – approx. 5% incorrect. It also flags up very inaccurate branch like Females in class>2 and with age less than 38 is precited survived Yes 132 time of which 61 times is incorrect.
The main idea is using few clicks in Weka and very little data processing the decision tree is able to highlight here strong connection between attributes Sex, then Age and PClass on passenger’s survival. The higher the attribute shows up in tree it effect is higher the lower the it is on branch lesser role it plays with key/ main attribute.

  ![Titanic Tree](/images/Titanic Tree.PNG)
