# SLackathon-Optimize-Supply-Chain-Inventory-Good-Boy-Simba
IBM SLACKATHON
# Optimize Supply Chain Inventory
## Contents
  - [Contents](#contents)
  
  - [Short description](#short-description)
   

  
    - [What's the problem?](#whats-the-problem)
    - [How can technology help?](#how-can-technology-help)
    - [The idea](#the-idea)

## Short description
### What's the problem?

There are multiple problems holding inventory as there are a lot of factors that are involved in it from a Manufacturing to transportation to warehouse to expiry and sales of that product. Some of them are mentioned below that play a critical role in inventory and need to be optimized in order for a company to have good revenue and sales.

 1. Limited Visibility
 2. Over stocking
 3. Changing Demand
 4. Overstocking
 5. Production planning
 

### How can technology help?

Machine learning will allow us to identify the demand and keep relevant stock accordingly which will help reduce the cost of the products.


### The Idea 

The Idea is to build a model that will help companies maintain a fair amount of stock that does not increase their warehouse cost and keeping in mind that there is not shortage of inventory either. Remove limited visibility in warehouse of the inventory and keeping inventory as per the trend.

### The Code

import numpy as np
import pandas as pd
from matplotlib import pyplot as plt

cvv = lambda x: np.std(x, ddof=0) / np.mean(x) * 100

df = pd.DataFrame({'Dist 1 ':[83,67,85,74,62,82],
                   'Dist 2 ':[83,85,82,75,69,69],
                   'Dist 3 ':[85,66,77,84,69,75],
                   'Dist 4 ':[73,91,82,85,76,83],
                   'Dist 5 ':[81,82,76,74,70,61],
                   'Factory':[405,391,402,392,346,370]})

max= np.max(df)
mean1=np.mean(df)
std1= np.std(df) #mistake i made earlies was i was using 'df.std()'

zmax= (max-mean1)/std1

 
dfs=df.apply(cvv)  




std1.plot()

plt.show()
mean1.plot()
plt.show()
zmax.plot()
plt.show()
dfs.plot()
plt.show

### The Graph

![image](https://user-images.githubusercontent.com/84643666/198098407-62f3bc1e-007f-4020-a47c-30e31a66d778.png)
![image](https://user-images.githubusercontent.com/84643666/198098539-2276d468-d976-4527-8554-b3d91b9b5123.png)
![image](https://user-images.githubusercontent.com/84643666/198098587-60c9401b-29a2-49c6-bd18-ab8b415e117d.png)


