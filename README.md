# linearregression
Linear regression

#import the required libraries

import pandas as pd
import matplotlib.pyplot as plt
from sklearn import linear_model

#read the data 

data=pd.read_csv('data location') #for a CSV file

data=pd.read_excel('data location')#for an excel file

#check the number of rows and columns
data.shape

#plot the graph, choose graph type based on your requirement
data.plot(kind='graph type' x='x axis' y='axis')
plt.show #displays the plot

data.corr() #find the correlation coefficents

#convert to dataframe
xnew=pd.DataFrame(data['x axis'])
ynew=pd.DataFrame(data['y axis'])

#apply linear regression
lm= linear_model.LinearRegression() 
model= lm.fit(xnew,ynew)

model.coef_ #model coefficent 
model.intercept_ #model intercept
model.score(xnew,ynew) #model score
model.predict([['prediction value']]) #prediction for new value

Check linearregression.ipynb for a worked out model
 
