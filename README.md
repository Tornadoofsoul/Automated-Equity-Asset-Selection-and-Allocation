# This repository is sperated into four parts:

## 1. Data Preprocessing

crawl ticker list and basic stock from http://www.nasdaq.com/screening/company-list.aspx

crawl financial statement from http://www.morningstar.com/

crawl historical stock prices from  https://finance.yahoo.com/

```python
./crawl.py
```

## 2. Feature engineering

```python
./feature engineering.py
```
### 2.1 Feature Engineering

		Basic feature filter to delete useless features

		format basic information to the (sample_n, feature_m) matrix

	    [ feature1_sample_1, feature2_sample_1, ... feature_m_sample_1]

	    ...

	    [ feature1_sample_m, feature2_sample_m, ... feature_m_sample_n]

## 3. Stock classification based on stock price

```python
./learning.py
```

### 3.1 Train the model

#### 3.1.1	Take financial ratios (2006 - Dec.2014) to train the model

#### 3.1.2 Label based on Sortino ratio and CVaR with time between Jan, 2014 and Jan, 2015

#### 3.1.3 Select best parameters for us.

### 3.2 Predict data and make comparison

#### 3.2.1 Predict the performance based on financial ratios (2007 - Dec.2015)

#### 3.2.2 Check if the selected group is sigficant better than the rest
	




Use SVM in sklearn to train the model and use cross-validation to pick the best parameters (missing value problem, maybe handled by cubic spline)

Get a roughly desired stock sets


## 4. Optimize the best weight for your portfolio

```python
./mean_variance_optimization.py
```

Do a brute-force method to randomly pick 15 stocks from the stock sets and implement mean-variance portfolio with no short constraint

Delelte the portfolio with the worst CVAR 



