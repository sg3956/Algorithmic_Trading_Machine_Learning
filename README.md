
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


The following graph shows the actual and predicted cumulative returns for a 3 month training period. This graph shows that the predicted strategy returns performed just slightly better than the actual returns.

![1](https://github.com/sg3956/Machine_Learning_Trading_Bot/blob/1692d26884a927d2a797d57351d55c191beb3da1/3_4_100.png)


The following graph shows the cumulative returns comparison with a 2 month training period. This graph shows that the predicted strategy returns did not perform much differently than the 2 month training period.

![2](https://github.com/sg3956/Machine_Learning_Trading_Bot/blob/1692d26884a927d2a797d57351d55c191beb3da1/2_4_100.png)


The following graph shows the cumulative returns with a 6 month training window. This graph shows that the predictions matched with the actual returns for longer than the 2 and 3 month training periods, but then predicted lower for a period of time before having higher predictions towards the end of the data. 

![3](https://github.com/sg3956/Machine_Learning_Trading_Bot/blob/1692d26884a927d2a797d57351d55c191beb3da1/8_4_100.png)


Based in these three graphs alone, it appears that the 3 month window strategy has the least amount of volatility.


The following graph shows a 3 month training period from above with the short SMA set to 7 days and the long SMA set to 200 days.

![4](https://github.com/sg3956/Machine_Learning_Trading_Bot/blob/1692d26884a927d2a797d57351d55c191beb3da1/7_200.png)


The following graph shows a 3 month training period from above with the short SMA set to 7 days and the long SMA set to 150 days.

![5](https://github.com/sg3956/Machine_Learning_Trading_Bot/blob/1692d26884a927d2a797d57351d55c191beb3da1/7_150.png)


As you can see from these graphs, it appears that using a short window of 7 days and a long window of 150 days predicts slightly better with less volatility than the original 4 day short window and 100 day long window. This will be the strategy that I recommend.


The final graph below shows the cumulative returns with a 3 month training period, 4 day short window and 100 day long window SMAs using a Decision Tree Classifier Model.

![6](https://github.com/sg3956/Machine_Learning_Trading_Bot/blob/1692d26884a927d2a797d57351d55c191beb3da1/Actual_vs_DTC.png)

We can see from this graphic that the returns are a little more volatile and end up lower than the actual returns. Therefore my recommendation is to use the SVM strategy as it had the best predicted returns with the least amount of volatility.

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
