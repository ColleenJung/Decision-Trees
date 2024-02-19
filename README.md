# Decision-Trees
#CART algorithm

<img width="723" alt="Screenshot 2024-02-19 at 1 43 33 PM" src="https://github.com/ColleenJung/Decision-Trees/assets/119357849/07760569-2176-4b8d-824f-28823a9f8e6a">

# Terminoglogy of a Decision Tree

- Each box in the tree diagram is called a **Node.**
- Each line in the tree diagram is called a **Branch or a Split.**
- A tree diagram is displayed in layers, the number of layers minus one is the **Depth** (e.g., this tree has 3 layers but only 2 levels deep)
- The feature used to create a branch is called the **Branching Variable or the Splitting Variable**
  1. `DEBTINC` is the splitting variable in the first level
  2. `DELINQ` is a splitting variable in the second level and DEBTINC is used again as another splitting variable

<img width="579" alt="image" src="https://github.com/ColleenJung/Decision-Trees/assets/119357849/9528635d-0deb-43c6-9ff3-daba0dd8953a">

- A **Parent Node** is a node where the branch comes from.
- A **Child Nod**e is a node where the branch goes into.
- The **Root Node** is the node where there are no branches that go into it.
- There is only one Root Node in a Tree Diagram.
- The Root Node is at Level 0
- A **Terminal Node** is a node where there no branches that come from it.

# Two popular Decision Tree Algorithms
1. CART – Classification And Regression Trees
Leo Breiman, Jerome Friedman, Charles J. Stone, Richard A. Olshen (1984). Classification and Regression Trees, Belmont, California: Wadsworth International Group.

2. CHAID – CHi-squared Automatic Interaction Detector
Gordon V. Kass (1980). An Explanatory Technique for Investigating Large Quantities of Categorical Data, Applied Statistics (Journal of the Royal Statistical Society, Series C), volume 29, number 2, pages 119-127.
![image](https://github.com/ColleenJung/Decision-Trees/assets/119357849/895e962c-c160-4d44-895e-8a2a3823eb3a)

# Make Consequences as Distinctive as Possible(Impurity Metric)

<img width="486" alt="Screenshot 2024-02-19 at 3 54 15 PM" src="https://github.com/ColleenJung/Decision-Trees/assets/119357849/9efb2dba-b381-4513-bba0-7d977d79f802">

# Entropy and Gini Index for a Split

<img width="443" alt="Screenshot 2024-02-19 at 3 55 00 PM" src="https://github.com/ColleenJung/Decision-Trees/assets/119357849/6a78cece-6f5d-4978-bcee-4d09a6bc4256">

<img width="468" alt="Screenshot 2024-02-19 at 3 55 44 PM" src="https://github.com/ColleenJung/Decision-Trees/assets/119357849/ba6c20a0-50f5-41e2-98c6-56daa656aee0">


# Example Datasets
1. A BinaryClassification Tree
2. A Multi-ClassClassification Tree
3. Describe Clusters With a Classification Tree


# Issues in Training Decision Trees(Stopping Rules)
<img width="479" alt="Screenshot 2024-02-19 at 3 56 56 PM" src="https://github.com/ColleenJung/Decision-Trees/assets/119357849/171a3064-92b6-4969-967b-f376028e89ba">

1. Predictor Missing Values Handling
<img width="481" alt="Screenshot 2024-02-19 at 3 58 04 PM" src="https://github.com/ColleenJung/Decision-Trees/assets/119357849/805989d3-945e-4115-b943-292aa2040933">

2. Temptation to Overfit the Data

<img width="481" alt="Screenshot 2024-02-19 at 3 58 29 PM" src="https://github.com/ColleenJung/Decision-Trees/assets/119357849/1c250f3d-0c72-47a5-ab47-06976e71addf">

# Scikit-Learn Decision Tree Module
https://scikit-learn.org/stable/modules/classes.html#module-sklearn.tree 
- tree.DecisionTreeClassifier()	A decision tree classifier
- tree.DecisionTreeRegressor()	A decision tree regressor
- tree.plot_tree()			Draw a tree diagram

# tree.DecisionTreeRegressor()
<img width="839" alt="image" src="https://github.com/ColleenJung/Decision-Trees/assets/119357849/c870ebad-7517-43a1-9a0c-528ac4ef78f4">

# Cutoff Values From sklearn.tree
- The sklearn.tree module calculates its cutoff value by taking the average of the optimal value and the next higher unique value.
  1. In Step 1, we found the optimal cutoff value is 29.5.  The next higher unique value is 30.68.  Thus, the average is (29.5 + 30.68)/2 = 30.09.
  2. In Step 2, we found the optimal cutoff values are 17.83 and 64.92. Their next higher unique values are 18.26 and 65.37.  Thus, their averages are (17.83 + 18.26)/2 = 18.045 and (64.92 + 65.37)/2 = 65.145.
- The sklearn.tree module uses these cutoff values to avoid machine nuisances in comparing floating point numbers.









