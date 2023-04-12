
## Project Goal

Leveraging machine learning algorithms, this program aims to improve the existing trading signals for a top financial advisory firm.

---

## Technologies

Python 3.9.16

Google Colab

SKLearn

Pandas Library

---


## Installation Guide

Make sure to run the appropriate imports:

`import pandas as pd`

`import numpy as np`

`from pathlib import Path`

`import hvplot.pandas`

`import matplotlib.pyplot as plt`

`from sklearn import svm`

`from sklearn.preprocessing import StandardScaler`

`from pandas.tseries.offsets import DateOffset`

`from sklearn.metrics import classification_report`

`from sklearn.tree import DecisionTreeClassifier`

---


## Analysis


The graph below illustrates the cumulative returns that were actually earned and those that were predicted during a three-month training period. It indicates that the returns expected by the strategy were marginally higher than the actual returns.

![1](https://github.com/sg3956/Machine_Learning_Trading_Bot/blob/1692d26884a927d2a797d57351d55c191beb3da1/3_4_100.png)


The graph presented below depicts a comparison of cumulative returns during a two-month training period. It suggests that the returns expected by the strategy did not differ significantly from those obtained during the three-month training period.
![2](https://github.com/sg3956/Machine_Learning_Trading_Bot/blob/1692d26884a927d2a797d57351d55c191beb3da1/2_4_100.png)


The graph below displays the cumulative returns obtained from an 8-month training window. The graph indicates that the predicted returns aligned with the actual returns for a longer period compared to the 2-month and 3-month training periods. However, there was a phase where the predicted returns were lower than the actual returns. Towards the end of the data, the predictions picked up again and were higher than before.

![3](https://github.com/sg3956/Machine_Learning_Trading_Bot/blob/1692d26884a927d2a797d57351d55c191beb3da1/8_4_100.png)


Judging solely from the three graphs presented, it seems that the strategy that used a 3 month training window exhibited the least amount of volatility.


This graph illustrates a 3 month training period, previously mentioned, where the short Simple Moving Average (SMA) is configured to 7 days and the long SMA is set to 200 days.

![4](https://github.com/sg3956/Machine_Learning_Trading_Bot/blob/1692d26884a927d2a797d57351d55c191beb3da1/7_200.png)


This graph illustrates a 3 month training period, previously mentioned, where the short Simple Moving Average (SMA) is configured to 7 days and the long SMA is set to 150 days.


![5](https://github.com/sg3956/Machine_Learning_Trading_Bot/blob/1692d26884a927d2a797d57351d55c191beb3da1/7_150.png)


From these graphs, it seems that utilizing a short window of 7 days and a long window of 150 days produces slightly improved predictions with reduced volatility, compared to the initial approach that employed a 4-day short window and a 100-day long window. Based on this analysis, this is the strategy that I would suggest.

The graph presented below displays the cumulative returns obtained using a Decision Tree Classifier Model, with a 3-month training period and Simple Moving Averages (SMAs) configured to a 4-day short window and a 100-day long window.


![6](https://github.com/sg3956/Machine_Learning_Trading_Bot/blob/1692d26884a927d2a797d57351d55c191beb3da1/Actual_vs_DTC.png)

This graphic suggests that the returns obtained from the Decision Tree Classifier Model, with a 3-month training period and SMAs configured to a 4-day short window and a 100-day long window, exhibit higher volatility and ultimately result in lower returns compared to the actual returns. Based on this analysis, I would recommend using the SVM strategy as it produced the most accurate predicted returns with the least amount of volatility.

---


## Contributor

Soheil Gityforoze

sg3956@columbia.edu


---

## Licenses

MIT

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
