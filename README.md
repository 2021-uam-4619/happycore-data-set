import pandas as pd

import numpy as pn

#import seaborn as sns

import matplotlib.pyplot as plt

import statistics as state

d=pd.read_csv('happyscore_income.csv')

d

plt.plot(d.country.head(),d.adjusted_satisfaction.head(),color='red')

plt.barh(d.country.head(),d.adjusted_satisfaction.head(),color=['r','g','b','y','m'])

colors=[1,2,3,4,5]


plt.scatter(d.country.head(),d.adjusted_satisfaction.head(),c=colors)

print("mean of adjusted_satisfaction=",state.mean(d.adjusted_satisfaction))

print("median of adjusted_satisfaction=",state.median(d.adjusted_satisfaction))

d.corr().head(6).round(2)#corelation 

colors=[1,2,3,4,5]

plt.scatter(d.happyScore.head(),d.GDP.head(),c=colors)

plt.colorbar(label="asim",extend='both',shrink=1,pad=0.12,format="%.3f")#when give arrow shape use extend function

plt.clim(1,10)#given couting of color bar

#shrink use bar size change

#pad use graph size change


#when take foemate of bar using format function
