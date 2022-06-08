**OTUS Machine Learning Advanced**

### **Homework 5**

### Building a model to predict protein expression from PPI graph data

![proteins](https://user-images.githubusercontent.com/73858914/172504903-f533b8ea-4135-4c2d-9dd3-463fc14a10d1.png)

**Goals:**

- Predict proteins expression given a graph of PPI   

**Means**:

- Notebook relies mostly on [networkx](https://github.com/networkx/networkx) and [node2vec](https://github.com/eliorc/node2vec) libraries

**Data source**:
  
Dataset represents a graph of PPI. Proteins are nodes and their interactions are edges.

Proteins' expression data is split in [`train`](https://raw.githubusercontent.com/a-milenkin/Otus_HW_protein_expression/main/train.csv) and [`test`](https://raw.githubusercontent.com/a-milenkin/Otus_HW_protein_expression/main/test.csv) sets. 
Interaction information is provided in [`edges`](https://raw.githubusercontent.com/a-milenkin/Otus_HW_protein_expression/main/edges.csv).   
    
**Approach to the problem**:

1. We will build the graph's embedding in 128-dimensional space
2. Using this embedding as a feature space and protein expression as target variable,   
we will apply support vector regressor (`SVR` from sklearn) with `rbf` kernel for prediction.

**Binder notebook:**

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/oort77/OTUS_ADV_HW5/main)
