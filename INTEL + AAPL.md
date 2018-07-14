

```python
import pandas as pd
pd.core.common.is_list_like = pd.api.types.is_list_like
pd.set_option('display.max_columns', None)  
pd.set_option('display.max_rows', None) 
```


```python
import pandas_datareader.data as web
```


```python
import matplotlib.pylab as plt
```


```python
import scipy.stats as stats
```


```python
from scipy.stats import ttest_ind
```


```python
import matplotlib.pyplot as plt
```


```python
import mpl_finance as mpl
```


```python
import seaborn as seb
```


```python
from mpl_finance import candlestick_ohlc
```


```python
import matplotlib.dates as mdates
```


```python
from matplotlib.dates import date2num
```


```python
from matplotlib import style
```


```python
%matplotlib inline
```


```python
import bs4 #beautifulsoup4
```


```python
import sklearn #scikit_learn
```


```python
import numpy as np
```


```python
import datetime as dt
```


```python
from mpl_toolkits.mplot3d import Axes3D
```


```python
from scipy.stats import ttest_ind
```


```python
style.use('ggplot')
```


```python
start_07 = dt.datetime(2007,1,1)
```


```python
end_07 = dt.datetime(2007,12,31)
```


```python
start_08 = dt.datetime(2008,1,1)
```


```python
end_08 = dt.datetime(2008,12,31)
```


```python
start_09 = dt.datetime(2009,1,1)
```


```python
end_09 = dt.datetime(2009,12,31)
```


```python
start_10 = dt.datetime(2010,1,1)
```


```python
end_10 = dt.datetime(2010,12,31)
```


```python
start_11 = dt.datetime(2011,1,1)
```


```python
end_11 = dt.datetime(2011,12,31)
```


```python
start_12 = dt.datetime(2012,1,1)
```


```python
end_12 = dt.datetime(2012,12,31)
```


```python
start_13 = dt.datetime(2013,1,1)
```


```python
end_13 = dt.datetime(2013,12,31)
```


```python
start_14 = dt.datetime(2014,1,1)
```


```python
end_14 = dt.datetime(2014,12,31)
```


```python
start_15 = dt.datetime(2015,1,1)
```


```python
end_15 = dt.datetime(2015,12,31)
```


```python
start_16 = dt.datetime(2016,1,1)
```


```python
end_16 = dt.datetime(2016,12,31)
```


```python
start_17 = dt.datetime(2017,1,1)
```


```python
end_17 = dt.datetime(2017,12,31)
```


```python
start_18 = dt.datetime(2018,1,1)
```


```python
end_18 = dt.datetime(2018,12,31)
```


```python
df_INTC_07 = web.DataReader('INTC','quandl', start_07,end_07)
```


```python
df_INTC_08 = web.DataReader('INTC','quandl', start_08,end_08)
```


```python
df_INTC_09 = web.DataReader('INTC','quandl', start_09,end_09)
```


```python
df_INTC_10 = web.DataReader('INTC','quandl', start_10,end_10)
```


```python
df_INTC_11 = web.DataReader('INTC','quandl', start_11,end_11)
```


```python
df_INTC_12 = web.DataReader('INTC','quandl', start_12,end_12)
```


```python
df_INTC_13 = web.DataReader('INTC','quandl', start_13,end_13)
```


```python
df_INTC_14 = web.DataReader('INTC','quandl', start_14,end_14)
```


```python
df_INTC_15 = web.DataReader('INTC','quandl', start_15,end_15)
```


```python
df_INTC_16 = web.DataReader('INTC','quandl', start_16,end_16)
```


```python
df_INTC_17 = web.DataReader('INTC','quandl', start_17,end_17)
```


```python
#---------------------------------------------------------------------------------------------------------------------------
```


```python
df_AAPL_07 = web.DataReader('AAPL','quandl', start_07,end_07)
```


```python
df_AAPL_07 = web.DataReader('AAPL','quandl', start_07,end_07)
```


```python
df_AAPL_08 = web.DataReader('AAPL','quandl', start_08,end_08)
```


```python
df_AAPL_09 = web.DataReader('AAPL','quandl', start_09,end_09)
```


```python
df_AAPL_10 = web.DataReader('AAPL','quandl', start_10,end_10)
```


```python
df_AAPL_11 = web.DataReader('AAPL','quandl', start_11,end_11)
```


```python
df_AAPL_12 = web.DataReader('AAPL','quandl', start_12,end_12)
```


```python
df_AAPL_13 = web.DataReader('AAPL','quandl', start_13,end_13)
```


```python
df_AAPL_14 = web.DataReader('AAPL','quandl', start_14,end_14)
```


```python
df_AAPL_15 = web.DataReader('AAPL','quandl', start_15,end_15)
```


```python
df_AAPL_16 = web.DataReader('AAPL','quandl', start_16,end_16)
```


```python
df_AAPL_17 = web.DataReader('AAPL','quandl', start_17,end_17)
```


```python
plt.plot(df_INTC_07.index,df_INTC_07['AdjClose'], c='r')
plt.plot(df_AAPL_07.index,df_AAPL_07['AdjClose'], c='g')
plt.show()
```


![png](output_68_0.png)



```python
plt.plot(df_INTC_08.index,df_INTC_08['AdjClose'], c='r')
plt.plot(df_AAPL_08.index,df_AAPL_08['AdjClose'], c='g')
plt.show()
```


![png](output_69_0.png)



```python
plt.plot(df_INTC_09.index,df_INTC_09['AdjClose'], c='r')
plt.plot(df_AAPL_09.index,df_AAPL_09['AdjClose'], c='g')
plt.show()
```


![png](output_70_0.png)



```python
plt.plot(df_INTC_10.index,df_INTC_10['AdjClose'], c='r')
plt.plot(df_AAPL_10.index,df_AAPL_10['AdjClose'], c='g')
plt.show()
```


![png](output_71_0.png)



```python
plt.plot(df_INTC_11.index,df_INTC_11['AdjClose'], c='r')
plt.plot(df_AAPL_11.index,df_AAPL_11['AdjClose'], c='g')
plt.show()
```


![png](output_72_0.png)



```python
plt.plot(df_INTC_12.index,df_INTC_12['AdjClose'], c='r')
plt.plot(df_AAPL_12.index,df_AAPL_12['AdjClose'], c='g')
plt.show()
```


![png](output_73_0.png)



```python
plt.plot(df_INTC_13.index,df_INTC_13['AdjClose'], c='r')
plt.plot(df_AAPL_13.index,df_AAPL_13['AdjClose'], c='g')
plt.show()
```


![png](output_74_0.png)



```python
plt.plot(df_INTC_14.index,df_INTC_14['AdjClose'], c='r')
plt.plot(df_AAPL_14.index,df_AAPL_14['AdjClose'], c='g')
plt.show()
```


![png](output_75_0.png)



```python
plt.plot(df_INTC_15.index,df_INTC_15['AdjClose'], c='r')
plt.plot(df_AAPL_15.index,df_AAPL_15['AdjClose'], c='g')
plt.show()
```


![png](output_76_0.png)



```python
plt.plot(df_INTC_16.index,df_INTC_16['AdjClose'], c='r')
plt.plot(df_AAPL_16.index,df_AAPL_16['AdjClose'], c='g')
plt.show()
```


![png](output_77_0.png)



```python
plt.plot(df_INTC_17.index,df_INTC_17['AdjClose'], c='r')
plt.plot(df_AAPL_17.index,df_AAPL_17['AdjClose'], c='g')
plt.show()
```


![png](output_78_0.png)



```python
df_INTC_07.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Close</th>
      <th>Volume</th>
      <th>ExDividend</th>
      <th>SplitRatio</th>
      <th>AdjOpen</th>
      <th>AdjHigh</th>
      <th>AdjLow</th>
      <th>AdjClose</th>
      <th>AdjVolume</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2007-12-31</th>
      <td>26.63</td>
      <td>27.00</td>
      <td>26.59</td>
      <td>26.66</td>
      <td>23687800.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>19.218702</td>
      <td>19.485728</td>
      <td>19.189834</td>
      <td>19.240352</td>
      <td>23687800.0</td>
    </tr>
    <tr>
      <th>2007-12-28</th>
      <td>27.11</td>
      <td>27.27</td>
      <td>26.65</td>
      <td>26.76</td>
      <td>35391400.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>19.565115</td>
      <td>19.680586</td>
      <td>19.233135</td>
      <td>19.312522</td>
      <td>35391400.0</td>
    </tr>
    <tr>
      <th>2007-12-27</th>
      <td>27.36</td>
      <td>27.42</td>
      <td>26.77</td>
      <td>26.83</td>
      <td>29577500.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>19.745538</td>
      <td>19.788840</td>
      <td>19.319739</td>
      <td>19.363040</td>
      <td>29577500.0</td>
    </tr>
    <tr>
      <th>2007-12-26</th>
      <td>27.20</td>
      <td>27.47</td>
      <td>27.13</td>
      <td>27.45</td>
      <td>21346200.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>19.630067</td>
      <td>19.824924</td>
      <td>19.579548</td>
      <td>19.810490</td>
      <td>21346200.0</td>
    </tr>
    <tr>
      <th>2007-12-24</th>
      <td>26.82</td>
      <td>27.37</td>
      <td>26.75</td>
      <td>27.31</td>
      <td>22486400.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>19.355823</td>
      <td>19.752755</td>
      <td>19.305305</td>
      <td>19.709453</td>
      <td>22486400.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_AAPL_07.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Close</th>
      <th>Volume</th>
      <th>ExDividend</th>
      <th>SplitRatio</th>
      <th>AdjOpen</th>
      <th>AdjHigh</th>
      <th>AdjLow</th>
      <th>AdjClose</th>
      <th>AdjVolume</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2007-12-31</th>
      <td>199.50</td>
      <td>200.50</td>
      <td>197.7500</td>
      <td>198.08</td>
      <td>19261900.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>25.638531</td>
      <td>25.767044</td>
      <td>25.413631</td>
      <td>25.456041</td>
      <td>134833300.0</td>
    </tr>
    <tr>
      <th>2007-12-28</th>
      <td>200.59</td>
      <td>201.56</td>
      <td>196.8801</td>
      <td>199.83</td>
      <td>24987400.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>25.778611</td>
      <td>25.903269</td>
      <td>25.301837</td>
      <td>25.680940</td>
      <td>174911800.0</td>
    </tr>
    <tr>
      <th>2007-12-27</th>
      <td>198.95</td>
      <td>202.96</td>
      <td>197.8000</td>
      <td>198.57</td>
      <td>28411700.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>25.567848</td>
      <td>26.083189</td>
      <td>25.420057</td>
      <td>25.519013</td>
      <td>198881900.0</td>
    </tr>
    <tr>
      <th>2007-12-26</th>
      <td>199.01</td>
      <td>200.96</td>
      <td>196.8200</td>
      <td>198.95</td>
      <td>25133300.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>25.575559</td>
      <td>25.826161</td>
      <td>25.294113</td>
      <td>25.567848</td>
      <td>175933100.0</td>
    </tr>
    <tr>
      <th>2007-12-24</th>
      <td>195.03</td>
      <td>199.33</td>
      <td>194.7900</td>
      <td>198.80</td>
      <td>17150100.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>25.064073</td>
      <td>25.616683</td>
      <td>25.033230</td>
      <td>25.548571</td>
      <td>120050700.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_INTC_07['Diff'] = df_INTC_07['AdjClose'] - df_INTC_07['AdjClose'].shift(1)
df_INTC_08['Diff'] = df_INTC_08['AdjClose'] - df_INTC_08['AdjClose'].shift(1)
df_INTC_09['Diff'] = df_INTC_09['AdjClose'] - df_INTC_09['AdjClose'].shift(1)
df_INTC_10['Diff'] = df_INTC_10['AdjClose'] - df_INTC_10['AdjClose'].shift(1)
df_INTC_11['Diff'] = df_INTC_11['AdjClose'] - df_INTC_11['AdjClose'].shift(1)
df_INTC_12['Diff'] = df_INTC_12['AdjClose'] - df_INTC_12['AdjClose'].shift(1)
df_INTC_13['Diff'] = df_INTC_13['AdjClose'] - df_INTC_13['AdjClose'].shift(1)
df_INTC_14['Diff'] = df_INTC_14['AdjClose'] - df_INTC_14['AdjClose'].shift(1)
df_INTC_15['Diff'] = df_INTC_15['AdjClose'] - df_INTC_15['AdjClose'].shift(1)
df_INTC_16['Diff'] = df_INTC_16['AdjClose'] - df_INTC_16['AdjClose'].shift(1)
df_INTC_17['Diff'] = df_INTC_17['AdjClose'] - df_INTC_17['AdjClose'].shift(1)
df_INTC_07.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Close</th>
      <th>Volume</th>
      <th>ExDividend</th>
      <th>SplitRatio</th>
      <th>AdjOpen</th>
      <th>AdjHigh</th>
      <th>AdjLow</th>
      <th>AdjClose</th>
      <th>AdjVolume</th>
      <th>Diff</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2007-12-31</th>
      <td>26.63</td>
      <td>27.00</td>
      <td>26.59</td>
      <td>26.66</td>
      <td>23687800.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>19.218702</td>
      <td>19.485728</td>
      <td>19.189834</td>
      <td>19.240352</td>
      <td>23687800.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2007-12-28</th>
      <td>27.11</td>
      <td>27.27</td>
      <td>26.65</td>
      <td>26.76</td>
      <td>35391400.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>19.565115</td>
      <td>19.680586</td>
      <td>19.233135</td>
      <td>19.312522</td>
      <td>35391400.0</td>
      <td>0.072169</td>
    </tr>
    <tr>
      <th>2007-12-27</th>
      <td>27.36</td>
      <td>27.42</td>
      <td>26.77</td>
      <td>26.83</td>
      <td>29577500.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>19.745538</td>
      <td>19.788840</td>
      <td>19.319739</td>
      <td>19.363040</td>
      <td>29577500.0</td>
      <td>0.050519</td>
    </tr>
    <tr>
      <th>2007-12-26</th>
      <td>27.20</td>
      <td>27.47</td>
      <td>27.13</td>
      <td>27.45</td>
      <td>21346200.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>19.630067</td>
      <td>19.824924</td>
      <td>19.579548</td>
      <td>19.810490</td>
      <td>21346200.0</td>
      <td>0.447450</td>
    </tr>
    <tr>
      <th>2007-12-24</th>
      <td>26.82</td>
      <td>27.37</td>
      <td>26.75</td>
      <td>27.31</td>
      <td>22486400.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>19.355823</td>
      <td>19.752755</td>
      <td>19.305305</td>
      <td>19.709453</td>
      <td>22486400.0</td>
      <td>-0.101037</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_AAPL_07['Diff'] = df_AAPL_07['AdjClose'] - df_AAPL_07['AdjClose'].shift(1)
df_AAPL_08['Diff'] = df_AAPL_08['AdjClose'] - df_AAPL_08['AdjClose'].shift(1)
df_AAPL_09['Diff'] = df_AAPL_09['AdjClose'] - df_AAPL_09['AdjClose'].shift(1)
df_AAPL_10['Diff'] = df_AAPL_10['AdjClose'] - df_AAPL_10['AdjClose'].shift(1)
df_AAPL_11['Diff'] = df_AAPL_11['AdjClose'] - df_AAPL_11['AdjClose'].shift(1)
df_AAPL_12['Diff'] = df_AAPL_12['AdjClose'] - df_AAPL_12['AdjClose'].shift(1)
df_AAPL_13['Diff'] = df_AAPL_13['AdjClose'] - df_AAPL_13['AdjClose'].shift(1)
df_AAPL_14['Diff'] = df_AAPL_14['AdjClose'] - df_AAPL_14['AdjClose'].shift(1)
df_AAPL_15['Diff'] = df_AAPL_15['AdjClose'] - df_AAPL_15['AdjClose'].shift(1)
df_AAPL_16['Diff'] = df_AAPL_16['AdjClose'] - df_AAPL_16['AdjClose'].shift(1)
df_AAPL_17['Diff'] = df_AAPL_17['AdjClose'] - df_AAPL_17['AdjClose'].shift(1)
df_AAPL_07.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Close</th>
      <th>Volume</th>
      <th>ExDividend</th>
      <th>SplitRatio</th>
      <th>AdjOpen</th>
      <th>AdjHigh</th>
      <th>AdjLow</th>
      <th>AdjClose</th>
      <th>AdjVolume</th>
      <th>Diff</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2007-12-31</th>
      <td>199.50</td>
      <td>200.50</td>
      <td>197.7500</td>
      <td>198.08</td>
      <td>19261900.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>25.638531</td>
      <td>25.767044</td>
      <td>25.413631</td>
      <td>25.456041</td>
      <td>134833300.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2007-12-28</th>
      <td>200.59</td>
      <td>201.56</td>
      <td>196.8801</td>
      <td>199.83</td>
      <td>24987400.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>25.778611</td>
      <td>25.903269</td>
      <td>25.301837</td>
      <td>25.680940</td>
      <td>174911800.0</td>
      <td>0.224899</td>
    </tr>
    <tr>
      <th>2007-12-27</th>
      <td>198.95</td>
      <td>202.96</td>
      <td>197.8000</td>
      <td>198.57</td>
      <td>28411700.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>25.567848</td>
      <td>26.083189</td>
      <td>25.420057</td>
      <td>25.519013</td>
      <td>198881900.0</td>
      <td>-0.161928</td>
    </tr>
    <tr>
      <th>2007-12-26</th>
      <td>199.01</td>
      <td>200.96</td>
      <td>196.8200</td>
      <td>198.95</td>
      <td>25133300.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>25.575559</td>
      <td>25.826161</td>
      <td>25.294113</td>
      <td>25.567848</td>
      <td>175933100.0</td>
      <td>0.048835</td>
    </tr>
    <tr>
      <th>2007-12-24</th>
      <td>195.03</td>
      <td>199.33</td>
      <td>194.7900</td>
      <td>198.80</td>
      <td>17150100.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>25.064073</td>
      <td>25.616683</td>
      <td>25.033230</td>
      <td>25.548571</td>
      <td>120050700.0</td>
      <td>-0.019277</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_AAPL_17
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Close</th>
      <th>Volume</th>
      <th>ExDividend</th>
      <th>SplitRatio</th>
      <th>AdjOpen</th>
      <th>AdjHigh</th>
      <th>AdjLow</th>
      <th>AdjClose</th>
      <th>AdjVolume</th>
      <th>Diff</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2017-12-29</th>
      <td>170.5200</td>
      <td>170.5900</td>
      <td>169.2200</td>
      <td>169.2300</td>
      <td>25643711.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>170.520000</td>
      <td>170.590000</td>
      <td>169.220000</td>
      <td>169.230000</td>
      <td>25643711.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2017-12-28</th>
      <td>171.0000</td>
      <td>171.8500</td>
      <td>170.4800</td>
      <td>171.0800</td>
      <td>15997739.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>171.000000</td>
      <td>171.850000</td>
      <td>170.480000</td>
      <td>171.080000</td>
      <td>15997739.0</td>
      <td>1.850000</td>
    </tr>
    <tr>
      <th>2017-12-27</th>
      <td>170.1000</td>
      <td>170.7800</td>
      <td>169.7100</td>
      <td>170.6000</td>
      <td>21672062.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>170.100000</td>
      <td>170.780000</td>
      <td>169.710000</td>
      <td>170.600000</td>
      <td>21672062.0</td>
      <td>-0.480000</td>
    </tr>
    <tr>
      <th>2017-12-26</th>
      <td>170.8000</td>
      <td>171.4700</td>
      <td>169.6790</td>
      <td>170.5700</td>
      <td>32968167.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>170.800000</td>
      <td>171.470000</td>
      <td>169.679000</td>
      <td>170.570000</td>
      <td>32968167.0</td>
      <td>-0.030000</td>
    </tr>
    <tr>
      <th>2017-12-22</th>
      <td>174.6800</td>
      <td>175.4240</td>
      <td>174.5000</td>
      <td>175.0100</td>
      <td>16052615.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>174.680000</td>
      <td>175.424000</td>
      <td>174.500000</td>
      <td>175.010000</td>
      <td>16052615.0</td>
      <td>4.440000</td>
    </tr>
    <tr>
      <th>2017-12-21</th>
      <td>174.1700</td>
      <td>176.0200</td>
      <td>174.1000</td>
      <td>175.0100</td>
      <td>20356826.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>174.170000</td>
      <td>176.020000</td>
      <td>174.100000</td>
      <td>175.010000</td>
      <td>20356826.0</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2017-12-20</th>
      <td>174.8700</td>
      <td>175.4200</td>
      <td>173.2500</td>
      <td>174.3500</td>
      <td>23000392.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>174.870000</td>
      <td>175.420000</td>
      <td>173.250000</td>
      <td>174.350000</td>
      <td>23000392.0</td>
      <td>-0.660000</td>
    </tr>
    <tr>
      <th>2017-12-19</th>
      <td>175.0300</td>
      <td>175.3900</td>
      <td>174.0900</td>
      <td>174.5400</td>
      <td>27078872.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>175.030000</td>
      <td>175.390000</td>
      <td>174.090000</td>
      <td>174.540000</td>
      <td>27078872.0</td>
      <td>0.190000</td>
    </tr>
    <tr>
      <th>2017-12-18</th>
      <td>174.8800</td>
      <td>177.2000</td>
      <td>174.8600</td>
      <td>176.4200</td>
      <td>28831533.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>174.880000</td>
      <td>177.200000</td>
      <td>174.860000</td>
      <td>176.420000</td>
      <td>28831533.0</td>
      <td>1.880000</td>
    </tr>
    <tr>
      <th>2017-12-15</th>
      <td>173.6300</td>
      <td>174.1700</td>
      <td>172.4600</td>
      <td>173.8700</td>
      <td>37054632.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>173.630000</td>
      <td>174.170000</td>
      <td>172.460000</td>
      <td>173.870000</td>
      <td>37054632.0</td>
      <td>-2.550000</td>
    </tr>
    <tr>
      <th>2017-12-14</th>
      <td>172.4000</td>
      <td>173.1300</td>
      <td>171.6500</td>
      <td>172.2200</td>
      <td>20219307.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>172.400000</td>
      <td>173.130000</td>
      <td>171.650000</td>
      <td>172.220000</td>
      <td>20219307.0</td>
      <td>-1.650000</td>
    </tr>
    <tr>
      <th>2017-12-13</th>
      <td>172.5000</td>
      <td>173.5400</td>
      <td>172.0000</td>
      <td>172.2700</td>
      <td>23142242.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>172.500000</td>
      <td>173.540000</td>
      <td>172.000000</td>
      <td>172.270000</td>
      <td>23142242.0</td>
      <td>0.050000</td>
    </tr>
    <tr>
      <th>2017-12-12</th>
      <td>172.1500</td>
      <td>172.3900</td>
      <td>171.4610</td>
      <td>171.7000</td>
      <td>18945457.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>172.150000</td>
      <td>172.390000</td>
      <td>171.461000</td>
      <td>171.700000</td>
      <td>18945457.0</td>
      <td>-0.570000</td>
    </tr>
    <tr>
      <th>2017-12-11</th>
      <td>169.2000</td>
      <td>172.8900</td>
      <td>168.7900</td>
      <td>172.6700</td>
      <td>33092051.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>169.200000</td>
      <td>172.890000</td>
      <td>168.790000</td>
      <td>172.670000</td>
      <td>33092051.0</td>
      <td>0.970000</td>
    </tr>
    <tr>
      <th>2017-12-08</th>
      <td>170.4900</td>
      <td>171.0000</td>
      <td>168.8200</td>
      <td>169.3700</td>
      <td>23096872.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>170.490000</td>
      <td>171.000000</td>
      <td>168.820000</td>
      <td>169.370000</td>
      <td>23096872.0</td>
      <td>-3.300000</td>
    </tr>
    <tr>
      <th>2017-12-07</th>
      <td>169.0300</td>
      <td>170.4400</td>
      <td>168.9100</td>
      <td>169.4520</td>
      <td>24469613.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>169.030000</td>
      <td>170.440000</td>
      <td>168.910000</td>
      <td>169.452000</td>
      <td>24469613.0</td>
      <td>0.082000</td>
    </tr>
    <tr>
      <th>2017-12-06</th>
      <td>167.5000</td>
      <td>170.2047</td>
      <td>166.4600</td>
      <td>169.0100</td>
      <td>28224357.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>167.500000</td>
      <td>170.204700</td>
      <td>166.460000</td>
      <td>169.010000</td>
      <td>28224357.0</td>
      <td>-0.442000</td>
    </tr>
    <tr>
      <th>2017-12-05</th>
      <td>169.0600</td>
      <td>171.5200</td>
      <td>168.4000</td>
      <td>169.6400</td>
      <td>27008428.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>169.060000</td>
      <td>171.520000</td>
      <td>168.400000</td>
      <td>169.640000</td>
      <td>27008428.0</td>
      <td>0.630000</td>
    </tr>
    <tr>
      <th>2017-12-04</th>
      <td>172.4800</td>
      <td>172.6200</td>
      <td>169.6300</td>
      <td>169.8000</td>
      <td>32115052.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>172.480000</td>
      <td>172.620000</td>
      <td>169.630000</td>
      <td>169.800000</td>
      <td>32115052.0</td>
      <td>0.160000</td>
    </tr>
    <tr>
      <th>2017-12-01</th>
      <td>169.9500</td>
      <td>171.6700</td>
      <td>168.5000</td>
      <td>171.0500</td>
      <td>39590080.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>169.950000</td>
      <td>171.670000</td>
      <td>168.500000</td>
      <td>171.050000</td>
      <td>39590080.0</td>
      <td>1.250000</td>
    </tr>
    <tr>
      <th>2017-11-30</th>
      <td>170.4300</td>
      <td>172.1400</td>
      <td>168.4400</td>
      <td>171.8500</td>
      <td>40172368.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>170.430000</td>
      <td>172.140000</td>
      <td>168.440000</td>
      <td>171.850000</td>
      <td>40172368.0</td>
      <td>0.800000</td>
    </tr>
    <tr>
      <th>2017-11-29</th>
      <td>172.6300</td>
      <td>172.9200</td>
      <td>167.1600</td>
      <td>169.4800</td>
      <td>40788324.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>172.630000</td>
      <td>172.920000</td>
      <td>167.160000</td>
      <td>169.480000</td>
      <td>40788324.0</td>
      <td>-2.370000</td>
    </tr>
    <tr>
      <th>2017-11-28</th>
      <td>174.3000</td>
      <td>174.8700</td>
      <td>171.8600</td>
      <td>173.0700</td>
      <td>25468442.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>174.300000</td>
      <td>174.870000</td>
      <td>171.860000</td>
      <td>173.070000</td>
      <td>25468442.0</td>
      <td>3.590000</td>
    </tr>
    <tr>
      <th>2017-11-27</th>
      <td>175.0500</td>
      <td>175.0800</td>
      <td>173.3400</td>
      <td>174.0900</td>
      <td>20536313.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>175.050000</td>
      <td>175.080000</td>
      <td>173.340000</td>
      <td>174.090000</td>
      <td>20536313.0</td>
      <td>1.020000</td>
    </tr>
    <tr>
      <th>2017-11-24</th>
      <td>175.1000</td>
      <td>175.5000</td>
      <td>174.6459</td>
      <td>174.9700</td>
      <td>14026519.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>175.100000</td>
      <td>175.500000</td>
      <td>174.645900</td>
      <td>174.970000</td>
      <td>14026519.0</td>
      <td>0.880000</td>
    </tr>
    <tr>
      <th>2017-11-22</th>
      <td>173.3600</td>
      <td>175.0000</td>
      <td>173.0500</td>
      <td>174.9600</td>
      <td>24997274.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>173.360000</td>
      <td>175.000000</td>
      <td>173.050000</td>
      <td>174.960000</td>
      <td>24997274.0</td>
      <td>-0.010000</td>
    </tr>
    <tr>
      <th>2017-11-21</th>
      <td>170.7800</td>
      <td>173.7000</td>
      <td>170.7800</td>
      <td>173.1400</td>
      <td>24875471.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>170.780000</td>
      <td>173.700000</td>
      <td>170.780000</td>
      <td>173.140000</td>
      <td>24875471.0</td>
      <td>-1.820000</td>
    </tr>
    <tr>
      <th>2017-11-20</th>
      <td>170.2900</td>
      <td>170.5600</td>
      <td>169.5600</td>
      <td>169.9800</td>
      <td>15974387.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>170.290000</td>
      <td>170.560000</td>
      <td>169.560000</td>
      <td>169.980000</td>
      <td>15974387.0</td>
      <td>-3.160000</td>
    </tr>
    <tr>
      <th>2017-11-17</th>
      <td>171.0400</td>
      <td>171.3900</td>
      <td>169.6400</td>
      <td>170.1500</td>
      <td>21665811.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>171.040000</td>
      <td>171.390000</td>
      <td>169.640000</td>
      <td>170.150000</td>
      <td>21665811.0</td>
      <td>0.170000</td>
    </tr>
    <tr>
      <th>2017-11-16</th>
      <td>171.1800</td>
      <td>171.8700</td>
      <td>170.3000</td>
      <td>171.1000</td>
      <td>23497326.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>171.180000</td>
      <td>171.870000</td>
      <td>170.300000</td>
      <td>171.100000</td>
      <td>23497326.0</td>
      <td>0.950000</td>
    </tr>
    <tr>
      <th>2017-11-15</th>
      <td>169.9700</td>
      <td>170.3197</td>
      <td>168.3800</td>
      <td>169.0800</td>
      <td>28702351.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>169.970000</td>
      <td>170.319700</td>
      <td>168.380000</td>
      <td>169.080000</td>
      <td>28702351.0</td>
      <td>-2.020000</td>
    </tr>
    <tr>
      <th>2017-11-14</th>
      <td>173.0400</td>
      <td>173.4800</td>
      <td>171.1800</td>
      <td>171.3400</td>
      <td>23588451.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>173.040000</td>
      <td>173.480000</td>
      <td>171.180000</td>
      <td>171.340000</td>
      <td>23588451.0</td>
      <td>2.260000</td>
    </tr>
    <tr>
      <th>2017-11-13</th>
      <td>173.5000</td>
      <td>174.5000</td>
      <td>173.4000</td>
      <td>173.9700</td>
      <td>16828025.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>173.500000</td>
      <td>174.500000</td>
      <td>173.400000</td>
      <td>173.970000</td>
      <td>16828025.0</td>
      <td>2.630000</td>
    </tr>
    <tr>
      <th>2017-11-10</th>
      <td>175.1100</td>
      <td>175.3800</td>
      <td>174.2700</td>
      <td>174.6700</td>
      <td>25061183.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>175.110000</td>
      <td>175.380000</td>
      <td>174.270000</td>
      <td>174.670000</td>
      <td>25061183.0</td>
      <td>0.700000</td>
    </tr>
    <tr>
      <th>2017-11-09</th>
      <td>175.1100</td>
      <td>176.0950</td>
      <td>173.1400</td>
      <td>175.8800</td>
      <td>28636531.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>175.110000</td>
      <td>176.095000</td>
      <td>173.140000</td>
      <td>175.880000</td>
      <td>28636531.0</td>
      <td>1.210000</td>
    </tr>
    <tr>
      <th>2017-11-07</th>
      <td>173.9100</td>
      <td>175.2500</td>
      <td>173.6000</td>
      <td>174.8100</td>
      <td>23910914.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>173.910000</td>
      <td>175.250000</td>
      <td>173.600000</td>
      <td>174.810000</td>
      <td>23910914.0</td>
      <td>-1.070000</td>
    </tr>
    <tr>
      <th>2017-11-06</th>
      <td>172.3650</td>
      <td>174.9900</td>
      <td>171.7200</td>
      <td>174.2500</td>
      <td>34242566.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>172.365000</td>
      <td>174.990000</td>
      <td>171.720000</td>
      <td>174.250000</td>
      <td>34242566.0</td>
      <td>-0.560000</td>
    </tr>
    <tr>
      <th>2017-11-03</th>
      <td>174.0000</td>
      <td>174.2600</td>
      <td>171.1200</td>
      <td>172.5000</td>
      <td>58683826.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>174.000000</td>
      <td>174.260000</td>
      <td>171.120000</td>
      <td>172.500000</td>
      <td>58683826.0</td>
      <td>-1.750000</td>
    </tr>
    <tr>
      <th>2017-11-02</th>
      <td>167.6400</td>
      <td>168.5000</td>
      <td>165.2800</td>
      <td>168.1100</td>
      <td>32710040.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>167.640000</td>
      <td>168.500000</td>
      <td>165.280000</td>
      <td>168.110000</td>
      <td>32710040.0</td>
      <td>-4.390000</td>
    </tr>
    <tr>
      <th>2017-11-01</th>
      <td>169.8700</td>
      <td>169.9400</td>
      <td>165.6100</td>
      <td>166.8900</td>
      <td>33100847.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>169.870000</td>
      <td>169.940000</td>
      <td>165.610000</td>
      <td>166.890000</td>
      <td>33100847.0</td>
      <td>-1.220000</td>
    </tr>
    <tr>
      <th>2017-10-31</th>
      <td>167.9000</td>
      <td>169.6499</td>
      <td>166.9400</td>
      <td>169.0400</td>
      <td>35474672.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>167.900000</td>
      <td>169.649900</td>
      <td>166.940000</td>
      <td>169.040000</td>
      <td>35474672.0</td>
      <td>2.150000</td>
    </tr>
    <tr>
      <th>2017-10-30</th>
      <td>163.8900</td>
      <td>168.0700</td>
      <td>163.7200</td>
      <td>166.7200</td>
      <td>43923292.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>163.890000</td>
      <td>168.070000</td>
      <td>163.720000</td>
      <td>166.720000</td>
      <td>43923292.0</td>
      <td>-2.320000</td>
    </tr>
    <tr>
      <th>2017-10-27</th>
      <td>159.2900</td>
      <td>163.6000</td>
      <td>158.7000</td>
      <td>163.0500</td>
      <td>43904150.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>159.290000</td>
      <td>163.600000</td>
      <td>158.700000</td>
      <td>163.050000</td>
      <td>43904150.0</td>
      <td>-3.670000</td>
    </tr>
    <tr>
      <th>2017-10-26</th>
      <td>157.2300</td>
      <td>157.8295</td>
      <td>156.7800</td>
      <td>157.4100</td>
      <td>16751691.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>157.230000</td>
      <td>157.829500</td>
      <td>156.780000</td>
      <td>157.410000</td>
      <td>16751691.0</td>
      <td>-5.640000</td>
    </tr>
    <tr>
      <th>2017-10-25</th>
      <td>156.9100</td>
      <td>157.5500</td>
      <td>155.2700</td>
      <td>156.4050</td>
      <td>20126554.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>156.910000</td>
      <td>157.550000</td>
      <td>155.270000</td>
      <td>156.405000</td>
      <td>20126554.0</td>
      <td>-1.005000</td>
    </tr>
    <tr>
      <th>2017-10-24</th>
      <td>156.2900</td>
      <td>157.4200</td>
      <td>156.2000</td>
      <td>157.1000</td>
      <td>17137731.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>156.290000</td>
      <td>157.420000</td>
      <td>156.200000</td>
      <td>157.100000</td>
      <td>17137731.0</td>
      <td>0.695000</td>
    </tr>
    <tr>
      <th>2017-10-23</th>
      <td>156.8900</td>
      <td>157.6900</td>
      <td>155.5000</td>
      <td>156.1700</td>
      <td>21654461.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>156.890000</td>
      <td>157.690000</td>
      <td>155.500000</td>
      <td>156.170000</td>
      <td>21654461.0</td>
      <td>-0.930000</td>
    </tr>
    <tr>
      <th>2017-10-20</th>
      <td>156.6100</td>
      <td>157.7500</td>
      <td>155.9600</td>
      <td>156.1600</td>
      <td>23612246.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>156.610000</td>
      <td>157.750000</td>
      <td>155.960000</td>
      <td>156.160000</td>
      <td>23612246.0</td>
      <td>-0.010000</td>
    </tr>
    <tr>
      <th>2017-10-19</th>
      <td>156.7500</td>
      <td>157.0800</td>
      <td>155.0200</td>
      <td>155.9800</td>
      <td>42111326.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>156.750000</td>
      <td>157.080000</td>
      <td>155.020000</td>
      <td>155.980000</td>
      <td>42111326.0</td>
      <td>-0.180000</td>
    </tr>
    <tr>
      <th>2017-10-18</th>
      <td>160.4200</td>
      <td>160.7100</td>
      <td>159.6000</td>
      <td>159.7600</td>
      <td>16158659.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>160.420000</td>
      <td>160.710000</td>
      <td>159.600000</td>
      <td>159.760000</td>
      <td>16158659.0</td>
      <td>3.780000</td>
    </tr>
    <tr>
      <th>2017-10-17</th>
      <td>159.7800</td>
      <td>160.8700</td>
      <td>159.2300</td>
      <td>160.4700</td>
      <td>18816438.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>159.780000</td>
      <td>160.870000</td>
      <td>159.230000</td>
      <td>160.470000</td>
      <td>18816438.0</td>
      <td>0.710000</td>
    </tr>
    <tr>
      <th>2017-10-16</th>
      <td>157.9000</td>
      <td>160.0000</td>
      <td>157.6500</td>
      <td>159.8800</td>
      <td>23894630.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>157.900000</td>
      <td>160.000000</td>
      <td>157.650000</td>
      <td>159.880000</td>
      <td>23894630.0</td>
      <td>-0.590000</td>
    </tr>
    <tr>
      <th>2017-10-13</th>
      <td>156.7300</td>
      <td>157.2800</td>
      <td>156.4100</td>
      <td>156.9900</td>
      <td>16287608.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>156.730000</td>
      <td>157.280000</td>
      <td>156.410000</td>
      <td>156.990000</td>
      <td>16287608.0</td>
      <td>-2.890000</td>
    </tr>
    <tr>
      <th>2017-10-12</th>
      <td>156.3500</td>
      <td>157.3700</td>
      <td>155.7299</td>
      <td>156.0000</td>
      <td>16045720.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>156.350000</td>
      <td>157.370000</td>
      <td>155.729900</td>
      <td>156.000000</td>
      <td>16045720.0</td>
      <td>-0.990000</td>
    </tr>
    <tr>
      <th>2017-10-11</th>
      <td>155.9700</td>
      <td>156.9800</td>
      <td>155.7500</td>
      <td>156.5500</td>
      <td>16607693.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>155.970000</td>
      <td>156.980000</td>
      <td>155.750000</td>
      <td>156.550000</td>
      <td>16607693.0</td>
      <td>0.550000</td>
    </tr>
    <tr>
      <th>2017-10-10</th>
      <td>156.0550</td>
      <td>158.0000</td>
      <td>155.1000</td>
      <td>155.9000</td>
      <td>15456331.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>156.055000</td>
      <td>158.000000</td>
      <td>155.100000</td>
      <td>155.900000</td>
      <td>15456331.0</td>
      <td>-0.650000</td>
    </tr>
    <tr>
      <th>2017-10-09</th>
      <td>155.8100</td>
      <td>156.7300</td>
      <td>155.4850</td>
      <td>155.8400</td>
      <td>16200129.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>155.810000</td>
      <td>156.730000</td>
      <td>155.485000</td>
      <td>155.840000</td>
      <td>16200129.0</td>
      <td>-0.060000</td>
    </tr>
    <tr>
      <th>2017-10-06</th>
      <td>154.9700</td>
      <td>155.4900</td>
      <td>154.5600</td>
      <td>155.3000</td>
      <td>16423749.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>154.970000</td>
      <td>155.490000</td>
      <td>154.560000</td>
      <td>155.300000</td>
      <td>16423749.0</td>
      <td>-0.540000</td>
    </tr>
    <tr>
      <th>2017-10-05</th>
      <td>154.1800</td>
      <td>155.4400</td>
      <td>154.0500</td>
      <td>155.3900</td>
      <td>21032800.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>154.180000</td>
      <td>155.440000</td>
      <td>154.050000</td>
      <td>155.390000</td>
      <td>21032800.0</td>
      <td>0.090000</td>
    </tr>
    <tr>
      <th>2017-10-04</th>
      <td>153.6300</td>
      <td>153.8600</td>
      <td>152.4600</td>
      <td>153.4508</td>
      <td>19844177.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>153.630000</td>
      <td>153.860000</td>
      <td>152.460000</td>
      <td>153.450800</td>
      <td>19844177.0</td>
      <td>-1.939200</td>
    </tr>
    <tr>
      <th>2017-10-03</th>
      <td>154.0100</td>
      <td>155.0900</td>
      <td>153.9100</td>
      <td>154.4800</td>
      <td>16146388.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>154.010000</td>
      <td>155.090000</td>
      <td>153.910000</td>
      <td>154.480000</td>
      <td>16146388.0</td>
      <td>1.029200</td>
    </tr>
    <tr>
      <th>2017-10-02</th>
      <td>154.2600</td>
      <td>154.4500</td>
      <td>152.7200</td>
      <td>153.8100</td>
      <td>18524860.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>154.260000</td>
      <td>154.450000</td>
      <td>152.720000</td>
      <td>153.810000</td>
      <td>18524860.0</td>
      <td>-0.670000</td>
    </tr>
    <tr>
      <th>2017-09-29</th>
      <td>153.2100</td>
      <td>154.1300</td>
      <td>152.0000</td>
      <td>154.1200</td>
      <td>25856530.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>153.210000</td>
      <td>154.130000</td>
      <td>152.000000</td>
      <td>154.120000</td>
      <td>25856530.0</td>
      <td>0.310000</td>
    </tr>
    <tr>
      <th>2017-09-28</th>
      <td>153.8900</td>
      <td>154.2800</td>
      <td>152.7000</td>
      <td>153.2800</td>
      <td>21896592.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>153.890000</td>
      <td>154.280000</td>
      <td>152.700000</td>
      <td>153.280000</td>
      <td>21896592.0</td>
      <td>-0.840000</td>
    </tr>
    <tr>
      <th>2017-09-27</th>
      <td>153.8000</td>
      <td>154.7189</td>
      <td>153.5400</td>
      <td>154.2300</td>
      <td>24959552.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>153.800000</td>
      <td>154.718900</td>
      <td>153.540000</td>
      <td>154.230000</td>
      <td>24959552.0</td>
      <td>0.950000</td>
    </tr>
    <tr>
      <th>2017-09-26</th>
      <td>151.7800</td>
      <td>153.9200</td>
      <td>151.6900</td>
      <td>153.1400</td>
      <td>35470985.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>151.780000</td>
      <td>153.920000</td>
      <td>151.690000</td>
      <td>153.140000</td>
      <td>35470985.0</td>
      <td>-1.090000</td>
    </tr>
    <tr>
      <th>2017-09-25</th>
      <td>149.9900</td>
      <td>151.8300</td>
      <td>149.1600</td>
      <td>150.5500</td>
      <td>43922334.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>149.990000</td>
      <td>151.830000</td>
      <td>149.160000</td>
      <td>150.550000</td>
      <td>43922334.0</td>
      <td>-2.590000</td>
    </tr>
    <tr>
      <th>2017-09-22</th>
      <td>152.0200</td>
      <td>152.2700</td>
      <td>150.5600</td>
      <td>151.8900</td>
      <td>46114424.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>152.020000</td>
      <td>152.270000</td>
      <td>150.560000</td>
      <td>151.890000</td>
      <td>46114424.0</td>
      <td>1.340000</td>
    </tr>
    <tr>
      <th>2017-09-21</th>
      <td>155.8000</td>
      <td>155.8000</td>
      <td>152.7500</td>
      <td>153.3900</td>
      <td>36643382.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>155.800000</td>
      <td>155.800000</td>
      <td>152.750000</td>
      <td>153.390000</td>
      <td>36643382.0</td>
      <td>1.500000</td>
    </tr>
    <tr>
      <th>2017-09-20</th>
      <td>157.9000</td>
      <td>158.2600</td>
      <td>153.8300</td>
      <td>156.0700</td>
      <td>51693239.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>157.900000</td>
      <td>158.260000</td>
      <td>153.830000</td>
      <td>156.070000</td>
      <td>51693239.0</td>
      <td>2.680000</td>
    </tr>
    <tr>
      <th>2017-09-19</th>
      <td>159.5100</td>
      <td>159.7700</td>
      <td>158.4400</td>
      <td>158.7300</td>
      <td>20347352.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>159.510000</td>
      <td>159.770000</td>
      <td>158.440000</td>
      <td>158.730000</td>
      <td>20347352.0</td>
      <td>2.660000</td>
    </tr>
    <tr>
      <th>2017-09-18</th>
      <td>160.1100</td>
      <td>160.5000</td>
      <td>157.9950</td>
      <td>158.6700</td>
      <td>27939718.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>160.110000</td>
      <td>160.500000</td>
      <td>157.995000</td>
      <td>158.670000</td>
      <td>27939718.0</td>
      <td>-0.060000</td>
    </tr>
    <tr>
      <th>2017-09-15</th>
      <td>158.4700</td>
      <td>160.9700</td>
      <td>158.0000</td>
      <td>159.8800</td>
      <td>48203642.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>158.470000</td>
      <td>160.970000</td>
      <td>158.000000</td>
      <td>159.880000</td>
      <td>48203642.0</td>
      <td>1.210000</td>
    </tr>
    <tr>
      <th>2017-09-14</th>
      <td>158.9900</td>
      <td>159.4000</td>
      <td>158.0900</td>
      <td>158.2800</td>
      <td>23073646.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>158.990000</td>
      <td>159.400000</td>
      <td>158.090000</td>
      <td>158.280000</td>
      <td>23073646.0</td>
      <td>-1.600000</td>
    </tr>
    <tr>
      <th>2017-09-13</th>
      <td>159.8700</td>
      <td>159.9600</td>
      <td>157.9100</td>
      <td>159.6500</td>
      <td>44393752.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>159.870000</td>
      <td>159.960000</td>
      <td>157.910000</td>
      <td>159.650000</td>
      <td>44393752.0</td>
      <td>1.370000</td>
    </tr>
    <tr>
      <th>2017-09-12</th>
      <td>162.6100</td>
      <td>163.9600</td>
      <td>158.7700</td>
      <td>160.8200</td>
      <td>71139119.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>162.610000</td>
      <td>163.960000</td>
      <td>158.770000</td>
      <td>160.820000</td>
      <td>71139119.0</td>
      <td>1.170000</td>
    </tr>
    <tr>
      <th>2017-09-11</th>
      <td>160.5000</td>
      <td>162.0500</td>
      <td>159.8900</td>
      <td>161.5000</td>
      <td>31028926.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>160.500000</td>
      <td>162.050000</td>
      <td>159.890000</td>
      <td>161.500000</td>
      <td>31028926.0</td>
      <td>0.680000</td>
    </tr>
    <tr>
      <th>2017-09-08</th>
      <td>160.8600</td>
      <td>161.1500</td>
      <td>158.5300</td>
      <td>158.6300</td>
      <td>28183159.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>160.860000</td>
      <td>161.150000</td>
      <td>158.530000</td>
      <td>158.630000</td>
      <td>28183159.0</td>
      <td>-2.870000</td>
    </tr>
    <tr>
      <th>2017-09-07</th>
      <td>162.0900</td>
      <td>162.2400</td>
      <td>160.3600</td>
      <td>161.2600</td>
      <td>21722995.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>162.090000</td>
      <td>162.240000</td>
      <td>160.360000</td>
      <td>161.260000</td>
      <td>21722995.0</td>
      <td>2.630000</td>
    </tr>
    <tr>
      <th>2017-09-06</th>
      <td>162.7100</td>
      <td>162.9900</td>
      <td>160.5200</td>
      <td>161.9100</td>
      <td>21179047.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>162.710000</td>
      <td>162.990000</td>
      <td>160.520000</td>
      <td>161.910000</td>
      <td>21179047.0</td>
      <td>0.650000</td>
    </tr>
    <tr>
      <th>2017-09-05</th>
      <td>163.7500</td>
      <td>164.2500</td>
      <td>160.5600</td>
      <td>162.0800</td>
      <td>29317054.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>163.750000</td>
      <td>164.250000</td>
      <td>160.560000</td>
      <td>162.080000</td>
      <td>29317054.0</td>
      <td>0.170000</td>
    </tr>
    <tr>
      <th>2017-09-01</th>
      <td>164.8000</td>
      <td>164.9400</td>
      <td>163.6300</td>
      <td>164.0500</td>
      <td>16508568.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>164.800000</td>
      <td>164.940000</td>
      <td>163.630000</td>
      <td>164.050000</td>
      <td>16508568.0</td>
      <td>1.970000</td>
    </tr>
    <tr>
      <th>2017-08-31</th>
      <td>163.6400</td>
      <td>164.5200</td>
      <td>163.4800</td>
      <td>164.0000</td>
      <td>26412439.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>163.640000</td>
      <td>164.520000</td>
      <td>163.480000</td>
      <td>164.000000</td>
      <td>26412439.0</td>
      <td>-0.050000</td>
    </tr>
    <tr>
      <th>2017-08-30</th>
      <td>163.8000</td>
      <td>163.8900</td>
      <td>162.6100</td>
      <td>163.3500</td>
      <td>26973946.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>163.800000</td>
      <td>163.890000</td>
      <td>162.610000</td>
      <td>163.350000</td>
      <td>26973946.0</td>
      <td>-0.650000</td>
    </tr>
    <tr>
      <th>2017-08-29</th>
      <td>160.1000</td>
      <td>163.1200</td>
      <td>160.0000</td>
      <td>162.9100</td>
      <td>29307862.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>160.100000</td>
      <td>163.120000</td>
      <td>160.000000</td>
      <td>162.910000</td>
      <td>29307862.0</td>
      <td>-0.440000</td>
    </tr>
    <tr>
      <th>2017-08-28</th>
      <td>160.1400</td>
      <td>162.0000</td>
      <td>159.9300</td>
      <td>161.4700</td>
      <td>25279674.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>160.140000</td>
      <td>162.000000</td>
      <td>159.930000</td>
      <td>161.470000</td>
      <td>25279674.0</td>
      <td>-1.440000</td>
    </tr>
    <tr>
      <th>2017-08-25</th>
      <td>159.6500</td>
      <td>160.5600</td>
      <td>159.2700</td>
      <td>159.8600</td>
      <td>25015218.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>159.650000</td>
      <td>160.560000</td>
      <td>159.270000</td>
      <td>159.860000</td>
      <td>25015218.0</td>
      <td>-1.610000</td>
    </tr>
    <tr>
      <th>2017-08-24</th>
      <td>160.4300</td>
      <td>160.7400</td>
      <td>158.5500</td>
      <td>159.2700</td>
      <td>19029621.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>160.430000</td>
      <td>160.740000</td>
      <td>158.550000</td>
      <td>159.270000</td>
      <td>19029621.0</td>
      <td>-0.590000</td>
    </tr>
    <tr>
      <th>2017-08-23</th>
      <td>159.0700</td>
      <td>160.4700</td>
      <td>158.8800</td>
      <td>159.9800</td>
      <td>19198189.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>159.070000</td>
      <td>160.470000</td>
      <td>158.880000</td>
      <td>159.980000</td>
      <td>19198189.0</td>
      <td>0.710000</td>
    </tr>
    <tr>
      <th>2017-08-22</th>
      <td>158.2300</td>
      <td>160.0000</td>
      <td>158.0200</td>
      <td>159.7800</td>
      <td>21297812.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>158.230000</td>
      <td>160.000000</td>
      <td>158.020000</td>
      <td>159.780000</td>
      <td>21297812.0</td>
      <td>-0.200000</td>
    </tr>
    <tr>
      <th>2017-08-21</th>
      <td>157.5000</td>
      <td>157.8900</td>
      <td>155.1101</td>
      <td>157.2100</td>
      <td>26145653.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>157.500000</td>
      <td>157.890000</td>
      <td>155.110100</td>
      <td>157.210000</td>
      <td>26145653.0</td>
      <td>-2.570000</td>
    </tr>
    <tr>
      <th>2017-08-18</th>
      <td>157.8600</td>
      <td>159.5000</td>
      <td>156.7200</td>
      <td>157.5000</td>
      <td>27012525.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>157.860000</td>
      <td>159.500000</td>
      <td>156.720000</td>
      <td>157.500000</td>
      <td>27012525.0</td>
      <td>0.290000</td>
    </tr>
    <tr>
      <th>2017-08-17</th>
      <td>160.5200</td>
      <td>160.7100</td>
      <td>157.8400</td>
      <td>157.8700</td>
      <td>26925694.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>160.520000</td>
      <td>160.710000</td>
      <td>157.840000</td>
      <td>157.870000</td>
      <td>26925694.0</td>
      <td>0.370000</td>
    </tr>
    <tr>
      <th>2017-08-16</th>
      <td>161.9400</td>
      <td>162.5100</td>
      <td>160.1500</td>
      <td>160.9500</td>
      <td>27321761.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>161.940000</td>
      <td>162.510000</td>
      <td>160.150000</td>
      <td>160.950000</td>
      <td>27321761.0</td>
      <td>3.080000</td>
    </tr>
    <tr>
      <th>2017-08-15</th>
      <td>160.6600</td>
      <td>162.1950</td>
      <td>160.1400</td>
      <td>161.6000</td>
      <td>27936774.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>160.660000</td>
      <td>162.195000</td>
      <td>160.140000</td>
      <td>161.600000</td>
      <td>27936774.0</td>
      <td>0.650000</td>
    </tr>
    <tr>
      <th>2017-08-14</th>
      <td>159.3200</td>
      <td>160.2100</td>
      <td>158.7500</td>
      <td>159.8500</td>
      <td>21754810.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>159.320000</td>
      <td>160.210000</td>
      <td>158.750000</td>
      <td>159.850000</td>
      <td>21754810.0</td>
      <td>-1.750000</td>
    </tr>
    <tr>
      <th>2017-08-11</th>
      <td>156.6000</td>
      <td>158.5728</td>
      <td>156.0700</td>
      <td>157.4800</td>
      <td>25943187.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>156.600000</td>
      <td>158.572800</td>
      <td>156.070000</td>
      <td>157.480000</td>
      <td>25943187.0</td>
      <td>-2.370000</td>
    </tr>
    <tr>
      <th>2017-08-10</th>
      <td>159.9000</td>
      <td>160.0000</td>
      <td>154.6300</td>
      <td>155.2700</td>
      <td>39081017.0</td>
      <td>0.63</td>
      <td>1.0</td>
      <td>159.900000</td>
      <td>160.000000</td>
      <td>154.630000</td>
      <td>155.270000</td>
      <td>39081017.0</td>
      <td>-2.210000</td>
    </tr>
    <tr>
      <th>2017-08-09</th>
      <td>159.2600</td>
      <td>161.2700</td>
      <td>159.1100</td>
      <td>161.0600</td>
      <td>25640394.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>158.616422</td>
      <td>160.618300</td>
      <td>158.467028</td>
      <td>160.409148</td>
      <td>25640394.0</td>
      <td>5.139148</td>
    </tr>
    <tr>
      <th>2017-08-08</th>
      <td>158.6000</td>
      <td>161.8300</td>
      <td>158.2700</td>
      <td>160.0800</td>
      <td>35775675.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>157.959089</td>
      <td>161.176037</td>
      <td>157.630423</td>
      <td>159.433108</td>
      <td>35775675.0</td>
      <td>-0.976040</td>
    </tr>
    <tr>
      <th>2017-08-04</th>
      <td>156.0700</td>
      <td>157.4000</td>
      <td>155.6900</td>
      <td>156.3900</td>
      <td>20349532.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>155.439313</td>
      <td>156.763938</td>
      <td>155.060849</td>
      <td>155.758020</td>
      <td>20349532.0</td>
      <td>-3.675089</td>
    </tr>
    <tr>
      <th>2017-08-03</th>
      <td>157.0500</td>
      <td>157.2100</td>
      <td>155.0200</td>
      <td>155.5700</td>
      <td>26000738.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>156.415353</td>
      <td>156.574706</td>
      <td>154.393556</td>
      <td>154.941334</td>
      <td>26000738.0</td>
      <td>-0.816686</td>
    </tr>
    <tr>
      <th>2017-08-02</th>
      <td>159.2800</td>
      <td>159.7500</td>
      <td>156.1600</td>
      <td>157.1400</td>
      <td>69222793.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>158.636341</td>
      <td>159.104442</td>
      <td>155.528949</td>
      <td>156.504989</td>
      <td>69222793.0</td>
      <td>1.563656</td>
    </tr>
    <tr>
      <th>2017-08-01</th>
      <td>149.1000</td>
      <td>150.2200</td>
      <td>148.4100</td>
      <td>150.0500</td>
      <td>24725526.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>148.497479</td>
      <td>149.612953</td>
      <td>147.810267</td>
      <td>149.443640</td>
      <td>24725526.0</td>
      <td>-7.061349</td>
    </tr>
    <tr>
      <th>2017-07-31</th>
      <td>149.9000</td>
      <td>150.3300</td>
      <td>148.1300</td>
      <td>148.8500</td>
      <td>19422655.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>149.294246</td>
      <td>149.722509</td>
      <td>147.531399</td>
      <td>148.248489</td>
      <td>19422655.0</td>
      <td>-1.195151</td>
    </tr>
    <tr>
      <th>2017-07-28</th>
      <td>149.8900</td>
      <td>150.2300</td>
      <td>149.1900</td>
      <td>149.5000</td>
      <td>16832947.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>149.284287</td>
      <td>149.622913</td>
      <td>148.587115</td>
      <td>148.895863</td>
      <td>16832947.0</td>
      <td>0.647373</td>
    </tr>
    <tr>
      <th>2017-07-27</th>
      <td>153.7500</td>
      <td>153.9900</td>
      <td>147.3000</td>
      <td>150.5600</td>
      <td>32175875.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>153.128688</td>
      <td>153.367718</td>
      <td>146.704753</td>
      <td>149.951579</td>
      <td>32175875.0</td>
      <td>1.055716</td>
    </tr>
    <tr>
      <th>2017-07-26</th>
      <td>153.3500</td>
      <td>153.9300</td>
      <td>153.0600</td>
      <td>153.4600</td>
      <td>15172136.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>152.730305</td>
      <td>153.307961</td>
      <td>152.441477</td>
      <td>152.839860</td>
      <td>15172136.0</td>
      <td>2.888281</td>
    </tr>
    <tr>
      <th>2017-07-25</th>
      <td>151.8000</td>
      <td>153.8400</td>
      <td>151.8000</td>
      <td>152.7400</td>
      <td>18612649.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>151.186568</td>
      <td>153.218325</td>
      <td>151.186568</td>
      <td>152.122770</td>
      <td>18612649.0</td>
      <td>-0.717090</td>
    </tr>
    <tr>
      <th>2017-07-24</th>
      <td>150.5800</td>
      <td>152.4400</td>
      <td>149.9000</td>
      <td>152.0900</td>
      <td>21122730.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>149.971498</td>
      <td>151.823982</td>
      <td>149.294246</td>
      <td>151.475396</td>
      <td>21122730.0</td>
      <td>-0.647373</td>
    </tr>
    <tr>
      <th>2017-07-21</th>
      <td>149.9900</td>
      <td>150.4400</td>
      <td>148.8800</td>
      <td>150.2700</td>
      <td>24671002.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>149.383883</td>
      <td>149.832064</td>
      <td>148.278368</td>
      <td>149.662751</td>
      <td>24671002.0</td>
      <td>-1.812645</td>
    </tr>
    <tr>
      <th>2017-07-20</th>
      <td>151.5000</td>
      <td>151.7400</td>
      <td>150.1900</td>
      <td>150.3400</td>
      <td>17053326.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>150.887781</td>
      <td>151.126811</td>
      <td>149.583074</td>
      <td>149.732468</td>
      <td>17053326.0</td>
      <td>0.069717</td>
    </tr>
    <tr>
      <th>2017-07-19</th>
      <td>150.4800</td>
      <td>151.4200</td>
      <td>149.9500</td>
      <td>151.0200</td>
      <td>20615419.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>149.871903</td>
      <td>150.808104</td>
      <td>149.344044</td>
      <td>150.409720</td>
      <td>20615419.0</td>
      <td>0.677252</td>
    </tr>
    <tr>
      <th>2017-07-18</th>
      <td>149.2000</td>
      <td>150.1300</td>
      <td>148.6700</td>
      <td>150.0800</td>
      <td>17713795.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>148.597075</td>
      <td>149.523317</td>
      <td>148.069217</td>
      <td>149.473519</td>
      <td>17713795.0</td>
      <td>-0.936201</td>
    </tr>
    <tr>
      <th>2017-07-17</th>
      <td>148.8200</td>
      <td>150.9000</td>
      <td>148.5700</td>
      <td>149.5600</td>
      <td>23243713.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>148.218611</td>
      <td>150.290205</td>
      <td>147.969621</td>
      <td>148.955620</td>
      <td>23243713.0</td>
      <td>-0.517899</td>
    </tr>
    <tr>
      <th>2017-07-14</th>
      <td>147.9700</td>
      <td>149.3300</td>
      <td>147.3300</td>
      <td>149.0400</td>
      <td>19961788.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>147.372046</td>
      <td>148.726550</td>
      <td>146.734632</td>
      <td>148.437722</td>
      <td>19961788.0</td>
      <td>-0.517899</td>
    </tr>
    <tr>
      <th>2017-07-13</th>
      <td>145.5000</td>
      <td>148.4900</td>
      <td>145.4400</td>
      <td>147.7700</td>
      <td>24922788.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>144.912027</td>
      <td>147.889944</td>
      <td>144.852269</td>
      <td>147.172854</td>
      <td>24922788.0</td>
      <td>-1.264868</td>
    </tr>
    <tr>
      <th>2017-07-12</th>
      <td>145.8700</td>
      <td>146.1800</td>
      <td>144.8200</td>
      <td>145.7400</td>
      <td>23617964.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>145.280532</td>
      <td>145.589279</td>
      <td>144.234775</td>
      <td>145.151057</td>
      <td>23617964.0</td>
      <td>-2.021797</td>
    </tr>
    <tr>
      <th>2017-07-11</th>
      <td>144.7300</td>
      <td>145.8500</td>
      <td>144.3800</td>
      <td>145.5300</td>
      <td>18311156.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>144.145139</td>
      <td>145.260613</td>
      <td>143.796553</td>
      <td>144.941906</td>
      <td>18311156.0</td>
      <td>-0.209151</td>
    </tr>
    <tr>
      <th>2017-07-10</th>
      <td>144.1100</td>
      <td>145.9500</td>
      <td>143.3700</td>
      <td>145.0600</td>
      <td>21030466.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>143.527644</td>
      <td>145.360208</td>
      <td>142.790634</td>
      <td>144.473805</td>
      <td>21030466.0</td>
      <td>-0.468101</td>
    </tr>
    <tr>
      <th>2017-07-07</th>
      <td>142.9000</td>
      <td>144.7500</td>
      <td>142.9000</td>
      <td>144.1800</td>
      <td>18505351.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>142.322534</td>
      <td>144.165058</td>
      <td>142.322534</td>
      <td>143.597361</td>
      <td>18505351.0</td>
      <td>-0.876444</td>
    </tr>
    <tr>
      <th>2017-07-06</th>
      <td>143.0200</td>
      <td>143.5000</td>
      <td>142.4100</td>
      <td>142.7300</td>
      <td>23374374.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>142.442049</td>
      <td>142.920109</td>
      <td>141.834514</td>
      <td>142.153221</td>
      <td>23374374.0</td>
      <td>-1.444140</td>
    </tr>
    <tr>
      <th>2017-07-05</th>
      <td>143.6900</td>
      <td>144.7900</td>
      <td>142.7237</td>
      <td>144.0900</td>
      <td>20758795.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>143.109341</td>
      <td>144.204896</td>
      <td>142.146946</td>
      <td>143.507725</td>
      <td>20758795.0</td>
      <td>1.354504</td>
    </tr>
    <tr>
      <th>2017-07-03</th>
      <td>144.8800</td>
      <td>145.3001</td>
      <td>143.1000</td>
      <td>143.5000</td>
      <td>14276812.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>144.294532</td>
      <td>144.712935</td>
      <td>142.521725</td>
      <td>142.920109</td>
      <td>14276812.0</td>
      <td>-0.587616</td>
    </tr>
    <tr>
      <th>2017-06-30</th>
      <td>144.4500</td>
      <td>144.9600</td>
      <td>143.7800</td>
      <td>144.0200</td>
      <td>22328979.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>143.866270</td>
      <td>144.374209</td>
      <td>143.198978</td>
      <td>143.438008</td>
      <td>22328979.0</td>
      <td>0.517899</td>
    </tr>
    <tr>
      <th>2017-06-29</th>
      <td>144.7100</td>
      <td>145.1300</td>
      <td>142.2800</td>
      <td>143.6800</td>
      <td>31116980.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>144.125219</td>
      <td>144.543522</td>
      <td>141.705039</td>
      <td>143.099382</td>
      <td>31116980.0</td>
      <td>-0.338626</td>
    </tr>
    <tr>
      <th>2017-06-28</th>
      <td>144.4900</td>
      <td>146.1100</td>
      <td>143.1601</td>
      <td>145.8300</td>
      <td>21915939.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>143.906108</td>
      <td>145.519562</td>
      <td>142.581583</td>
      <td>145.240693</td>
      <td>21915939.0</td>
      <td>2.141312</td>
    </tr>
    <tr>
      <th>2017-06-27</th>
      <td>145.0100</td>
      <td>146.1600</td>
      <td>143.6200</td>
      <td>143.7400</td>
      <td>24423643.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>144.424007</td>
      <td>145.569360</td>
      <td>143.039624</td>
      <td>143.159139</td>
      <td>24423643.0</td>
      <td>-2.081554</td>
    </tr>
    <tr>
      <th>2017-06-26</th>
      <td>147.1700</td>
      <td>148.2800</td>
      <td>145.3800</td>
      <td>145.8200</td>
      <td>25524661.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>146.575278</td>
      <td>147.680793</td>
      <td>144.792512</td>
      <td>145.230734</td>
      <td>25524661.0</td>
      <td>2.071595</td>
    </tr>
    <tr>
      <th>2017-06-23</th>
      <td>145.1300</td>
      <td>147.1600</td>
      <td>145.1100</td>
      <td>146.3500</td>
      <td>25997976.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>144.543522</td>
      <td>146.565319</td>
      <td>144.523603</td>
      <td>145.758592</td>
      <td>25997976.0</td>
      <td>0.527858</td>
    </tr>
    <tr>
      <th>2017-06-22</th>
      <td>145.7700</td>
      <td>146.7000</td>
      <td>145.1199</td>
      <td>145.6300</td>
      <td>18673365.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>145.180936</td>
      <td>146.107178</td>
      <td>144.533463</td>
      <td>145.041502</td>
      <td>18673365.0</td>
      <td>-0.717090</td>
    </tr>
    <tr>
      <th>2017-06-21</th>
      <td>145.5200</td>
      <td>146.0693</td>
      <td>144.6100</td>
      <td>145.8700</td>
      <td>21064679.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>144.931946</td>
      <td>145.479026</td>
      <td>144.025623</td>
      <td>145.280532</td>
      <td>21064679.0</td>
      <td>0.239030</td>
    </tr>
    <tr>
      <th>2017-06-20</th>
      <td>146.8700</td>
      <td>146.8700</td>
      <td>144.9400</td>
      <td>145.0100</td>
      <td>24572170.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>146.276491</td>
      <td>146.276491</td>
      <td>144.354290</td>
      <td>144.424007</td>
      <td>24572170.0</td>
      <td>-0.856525</td>
    </tr>
    <tr>
      <th>2017-06-19</th>
      <td>143.6600</td>
      <td>146.7400</td>
      <td>143.6600</td>
      <td>146.3400</td>
      <td>31449132.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>143.079462</td>
      <td>146.147016</td>
      <td>143.079462</td>
      <td>145.748632</td>
      <td>31449132.0</td>
      <td>1.324625</td>
    </tr>
    <tr>
      <th>2017-06-16</th>
      <td>143.7800</td>
      <td>144.5000</td>
      <td>142.2000</td>
      <td>142.2700</td>
      <td>49180748.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>143.198978</td>
      <td>143.916068</td>
      <td>141.625362</td>
      <td>141.695080</td>
      <td>49180748.0</td>
      <td>-4.053553</td>
    </tr>
    <tr>
      <th>2017-06-15</th>
      <td>143.3200</td>
      <td>144.4798</td>
      <td>142.2100</td>
      <td>144.2900</td>
      <td>31348832.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>142.740836</td>
      <td>143.895950</td>
      <td>141.635322</td>
      <td>143.706917</td>
      <td>31348832.0</td>
      <td>2.011837</td>
    </tr>
    <tr>
      <th>2017-06-14</th>
      <td>147.5000</td>
      <td>147.5000</td>
      <td>143.8400</td>
      <td>145.1600</td>
      <td>31224203.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>146.903945</td>
      <td>146.903945</td>
      <td>143.258735</td>
      <td>144.573401</td>
      <td>31224203.0</td>
      <td>0.866484</td>
    </tr>
    <tr>
      <th>2017-06-13</th>
      <td>147.1600</td>
      <td>147.4500</td>
      <td>145.1500</td>
      <td>146.5900</td>
      <td>33749154.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>146.565319</td>
      <td>146.854147</td>
      <td>144.563441</td>
      <td>145.997622</td>
      <td>33749154.0</td>
      <td>1.424221</td>
    </tr>
    <tr>
      <th>2017-06-12</th>
      <td>145.7400</td>
      <td>146.0900</td>
      <td>142.5100</td>
      <td>145.3200</td>
      <td>71563614.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>145.151057</td>
      <td>145.499643</td>
      <td>141.934110</td>
      <td>144.732754</td>
      <td>71563614.0</td>
      <td>-1.264868</td>
    </tr>
    <tr>
      <th>2017-06-09</th>
      <td>155.1900</td>
      <td>155.1900</td>
      <td>146.0200</td>
      <td>148.9800</td>
      <td>64176149.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>154.562869</td>
      <td>154.562869</td>
      <td>145.429926</td>
      <td>148.377964</td>
      <td>64176149.0</td>
      <td>3.645210</td>
    </tr>
    <tr>
      <th>2017-06-08</th>
      <td>155.2500</td>
      <td>155.5400</td>
      <td>154.4000</td>
      <td>154.9900</td>
      <td>20771367.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>154.622627</td>
      <td>154.911455</td>
      <td>153.776062</td>
      <td>154.363677</td>
      <td>20771367.0</td>
      <td>5.985713</td>
    </tr>
    <tr>
      <th>2017-06-07</th>
      <td>155.0200</td>
      <td>155.9800</td>
      <td>154.4800</td>
      <td>155.3700</td>
      <td>20678772.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>154.393556</td>
      <td>155.349677</td>
      <td>153.855738</td>
      <td>154.742142</td>
      <td>20678772.0</td>
      <td>0.378464</td>
    </tr>
    <tr>
      <th>2017-06-06</th>
      <td>153.9000</td>
      <td>155.8100</td>
      <td>153.7800</td>
      <td>154.4500</td>
      <td>26249630.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>153.278082</td>
      <td>155.180364</td>
      <td>153.158567</td>
      <td>153.825860</td>
      <td>26249630.0</td>
      <td>-0.916282</td>
    </tr>
    <tr>
      <th>2017-06-05</th>
      <td>154.3400</td>
      <td>154.4500</td>
      <td>153.4600</td>
      <td>153.9300</td>
      <td>24803858.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>153.716304</td>
      <td>153.825860</td>
      <td>152.839860</td>
      <td>153.307961</td>
      <td>24803858.0</td>
      <td>-0.517899</td>
    </tr>
    <tr>
      <th>2017-06-02</th>
      <td>153.5800</td>
      <td>155.4500</td>
      <td>152.8900</td>
      <td>155.4500</td>
      <td>27285861.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>152.959375</td>
      <td>154.821818</td>
      <td>152.272164</td>
      <td>154.821818</td>
      <td>27285861.0</td>
      <td>1.513858</td>
    </tr>
    <tr>
      <th>2017-06-01</th>
      <td>153.1700</td>
      <td>153.3300</td>
      <td>152.2200</td>
      <td>153.1800</td>
      <td>16180143.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>152.551032</td>
      <td>152.710386</td>
      <td>151.604871</td>
      <td>152.560992</td>
      <td>16180143.0</td>
      <td>-2.260827</td>
    </tr>
    <tr>
      <th>2017-05-31</th>
      <td>153.9700</td>
      <td>154.1700</td>
      <td>152.3800</td>
      <td>152.7600</td>
      <td>23162873.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>153.347799</td>
      <td>153.546991</td>
      <td>151.764225</td>
      <td>152.142689</td>
      <td>23162873.0</td>
      <td>-0.418303</td>
    </tr>
    <tr>
      <th>2017-05-30</th>
      <td>153.4200</td>
      <td>154.4300</td>
      <td>153.3300</td>
      <td>153.6700</td>
      <td>20034934.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>152.800022</td>
      <td>153.805940</td>
      <td>152.710386</td>
      <td>153.049012</td>
      <td>20034934.0</td>
      <td>0.906323</td>
    </tr>
    <tr>
      <th>2017-05-26</th>
      <td>154.0000</td>
      <td>154.2400</td>
      <td>153.3100</td>
      <td>153.6100</td>
      <td>21632202.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>153.377678</td>
      <td>153.616708</td>
      <td>152.690466</td>
      <td>152.989254</td>
      <td>21632202.0</td>
      <td>-0.059758</td>
    </tr>
    <tr>
      <th>2017-05-25</th>
      <td>153.7300</td>
      <td>154.3500</td>
      <td>153.0300</td>
      <td>153.8700</td>
      <td>19044463.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>153.108769</td>
      <td>153.726264</td>
      <td>152.411598</td>
      <td>153.248203</td>
      <td>19044463.0</td>
      <td>0.258949</td>
    </tr>
    <tr>
      <th>2017-05-24</th>
      <td>153.8400</td>
      <td>154.1700</td>
      <td>152.6700</td>
      <td>153.3400</td>
      <td>19118319.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>153.218325</td>
      <td>153.546991</td>
      <td>152.053053</td>
      <td>152.720345</td>
      <td>19118319.0</td>
      <td>-0.527858</td>
    </tr>
    <tr>
      <th>2017-05-23</th>
      <td>154.9000</td>
      <td>154.9000</td>
      <td>153.3100</td>
      <td>153.8000</td>
      <td>19430358.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>154.274041</td>
      <td>154.274041</td>
      <td>152.690466</td>
      <td>153.178486</td>
      <td>19430358.0</td>
      <td>0.458141</td>
    </tr>
    <tr>
      <th>2017-05-22</th>
      <td>154.0000</td>
      <td>154.5800</td>
      <td>152.9100</td>
      <td>153.9900</td>
      <td>22340069.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>153.377678</td>
      <td>153.955334</td>
      <td>152.292083</td>
      <td>153.367718</td>
      <td>22340069.0</td>
      <td>0.189232</td>
    </tr>
    <tr>
      <th>2017-05-19</th>
      <td>153.3800</td>
      <td>153.9800</td>
      <td>152.6300</td>
      <td>152.9600</td>
      <td>26733798.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>152.760183</td>
      <td>153.357759</td>
      <td>152.013214</td>
      <td>152.341881</td>
      <td>26733798.0</td>
      <td>-1.025838</td>
    </tr>
    <tr>
      <th>2017-05-18</th>
      <td>151.2700</td>
      <td>153.3400</td>
      <td>151.1300</td>
      <td>152.5400</td>
      <td>33159664.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>150.658710</td>
      <td>152.720345</td>
      <td>150.519276</td>
      <td>151.923578</td>
      <td>33159664.0</td>
      <td>-0.418303</td>
    </tr>
    <tr>
      <th>2017-05-17</th>
      <td>153.6000</td>
      <td>154.5700</td>
      <td>149.7100</td>
      <td>150.2500</td>
      <td>49482818.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>152.979294</td>
      <td>153.945375</td>
      <td>149.105014</td>
      <td>149.642832</td>
      <td>49482818.0</td>
      <td>-2.280746</td>
    </tr>
    <tr>
      <th>2017-05-16</th>
      <td>155.9400</td>
      <td>156.0600</td>
      <td>154.7200</td>
      <td>155.4700</td>
      <td>19904679.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>155.309838</td>
      <td>155.429353</td>
      <td>154.094768</td>
      <td>154.841738</td>
      <td>19904679.0</td>
      <td>5.198906</td>
    </tr>
    <tr>
      <th>2017-05-15</th>
      <td>156.0100</td>
      <td>156.6500</td>
      <td>155.0500</td>
      <td>155.7000</td>
      <td>25700983.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>155.379555</td>
      <td>156.016969</td>
      <td>154.423435</td>
      <td>155.070808</td>
      <td>25700983.0</td>
      <td>0.229071</td>
    </tr>
    <tr>
      <th>2017-05-12</th>
      <td>154.7000</td>
      <td>156.4200</td>
      <td>154.6700</td>
      <td>156.1000</td>
      <td>32221756.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>154.074849</td>
      <td>155.787899</td>
      <td>154.044970</td>
      <td>155.469192</td>
      <td>32221756.0</td>
      <td>0.398384</td>
    </tr>
    <tr>
      <th>2017-05-11</th>
      <td>152.4500</td>
      <td>154.0700</td>
      <td>152.3100</td>
      <td>153.9500</td>
      <td>25596687.0</td>
      <td>0.63</td>
      <td>1.0</td>
      <td>151.833942</td>
      <td>153.447395</td>
      <td>151.694507</td>
      <td>153.327880</td>
      <td>25596687.0</td>
      <td>-2.141312</td>
    </tr>
    <tr>
      <th>2017-05-10</th>
      <td>153.6300</td>
      <td>153.9400</td>
      <td>152.1100</td>
      <td>153.2600</td>
      <td>25670456.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>152.385575</td>
      <td>152.693064</td>
      <td>150.877887</td>
      <td>152.018572</td>
      <td>25670456.0</td>
      <td>-1.309308</td>
    </tr>
    <tr>
      <th>2017-05-09</th>
      <td>153.8700</td>
      <td>154.8800</td>
      <td>153.4500</td>
      <td>153.9600</td>
      <td>35942435.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>152.623631</td>
      <td>153.625450</td>
      <td>152.207033</td>
      <td>152.712902</td>
      <td>35942435.0</td>
      <td>0.694330</td>
    </tr>
    <tr>
      <th>2017-05-08</th>
      <td>149.0300</td>
      <td>153.7000</td>
      <td>149.0300</td>
      <td>153.0000</td>
      <td>48339210.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>147.822836</td>
      <td>152.455008</td>
      <td>147.822836</td>
      <td>151.760678</td>
      <td>48339210.0</td>
      <td>-0.952224</td>
    </tr>
    <tr>
      <th>2017-05-05</th>
      <td>146.7600</td>
      <td>148.9800</td>
      <td>146.7600</td>
      <td>148.9600</td>
      <td>26787359.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>145.571223</td>
      <td>147.773241</td>
      <td>145.571223</td>
      <td>147.753403</td>
      <td>26787359.0</td>
      <td>-4.007275</td>
    </tr>
    <tr>
      <th>2017-05-04</th>
      <td>146.5200</td>
      <td>147.1400</td>
      <td>145.8100</td>
      <td>146.5300</td>
      <td>23275690.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>145.333167</td>
      <td>145.948145</td>
      <td>144.628918</td>
      <td>145.343086</td>
      <td>23275690.0</td>
      <td>-2.410317</td>
    </tr>
    <tr>
      <th>2017-05-03</th>
      <td>145.5900</td>
      <td>147.4900</td>
      <td>144.2700</td>
      <td>147.0600</td>
      <td>45142806.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>144.410700</td>
      <td>146.295310</td>
      <td>143.101393</td>
      <td>145.868793</td>
      <td>45142806.0</td>
      <td>0.525707</td>
    </tr>
    <tr>
      <th>2017-05-02</th>
      <td>147.5400</td>
      <td>148.0900</td>
      <td>146.8400</td>
      <td>147.5100</td>
      <td>39752670.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>146.344905</td>
      <td>146.890450</td>
      <td>145.650575</td>
      <td>146.315148</td>
      <td>39752670.0</td>
      <td>0.446355</td>
    </tr>
    <tr>
      <th>2017-05-01</th>
      <td>145.1000</td>
      <td>147.2000</td>
      <td>144.9600</td>
      <td>146.6000</td>
      <td>32818760.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>143.924669</td>
      <td>146.007659</td>
      <td>143.785803</td>
      <td>145.412519</td>
      <td>32818760.0</td>
      <td>-0.902629</td>
    </tr>
    <tr>
      <th>2017-04-28</th>
      <td>144.0900</td>
      <td>144.3000</td>
      <td>143.2700</td>
      <td>143.6500</td>
      <td>20247187.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>142.922851</td>
      <td>143.131150</td>
      <td>142.109493</td>
      <td>142.486415</td>
      <td>20247187.0</td>
      <td>-2.926105</td>
    </tr>
    <tr>
      <th>2017-04-27</th>
      <td>143.9225</td>
      <td>144.1600</td>
      <td>143.3100</td>
      <td>143.7900</td>
      <td>13948980.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>142.756707</td>
      <td>142.992284</td>
      <td>142.149169</td>
      <td>142.625281</td>
      <td>13948980.0</td>
      <td>0.138866</td>
    </tr>
    <tr>
      <th>2017-04-26</th>
      <td>144.4700</td>
      <td>144.6000</td>
      <td>143.3762</td>
      <td>143.6508</td>
      <td>19614287.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>143.299772</td>
      <td>143.428719</td>
      <td>142.214832</td>
      <td>142.487208</td>
      <td>19614287.0</td>
      <td>-0.138072</td>
    </tr>
    <tr>
      <th>2017-04-25</th>
      <td>143.9100</td>
      <td>144.9000</td>
      <td>143.8700</td>
      <td>144.5400</td>
      <td>18216472.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>142.744309</td>
      <td>143.726289</td>
      <td>142.704633</td>
      <td>143.369205</td>
      <td>18216472.0</td>
      <td>0.881997</td>
    </tr>
    <tr>
      <th>2017-04-24</th>
      <td>143.5000</td>
      <td>143.9500</td>
      <td>143.1800</td>
      <td>143.6400</td>
      <td>17116599.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>142.337630</td>
      <td>142.783985</td>
      <td>142.020222</td>
      <td>142.476496</td>
      <td>17116599.0</td>
      <td>-0.892710</td>
    </tr>
    <tr>
      <th>2017-04-21</th>
      <td>142.4400</td>
      <td>142.6800</td>
      <td>141.8500</td>
      <td>142.2700</td>
      <td>17320928.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>141.286216</td>
      <td>141.524272</td>
      <td>140.700995</td>
      <td>141.117593</td>
      <td>17320928.0</td>
      <td>-1.358903</td>
    </tr>
    <tr>
      <th>2017-04-20</th>
      <td>141.2200</td>
      <td>142.9200</td>
      <td>141.1600</td>
      <td>142.4400</td>
      <td>23319562.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>140.076098</td>
      <td>141.762328</td>
      <td>140.016584</td>
      <td>141.286216</td>
      <td>23319562.0</td>
      <td>0.168623</td>
    </tr>
    <tr>
      <th>2017-04-19</th>
      <td>141.8800</td>
      <td>142.0000</td>
      <td>140.4500</td>
      <td>140.6800</td>
      <td>17328375.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>140.730752</td>
      <td>140.849780</td>
      <td>139.312335</td>
      <td>139.540472</td>
      <td>17328375.0</td>
      <td>-1.745744</td>
    </tr>
    <tr>
      <th>2017-04-18</th>
      <td>141.4100</td>
      <td>142.0400</td>
      <td>141.1100</td>
      <td>141.2000</td>
      <td>14697544.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>140.264559</td>
      <td>140.889456</td>
      <td>139.966989</td>
      <td>140.056260</td>
      <td>14697544.0</td>
      <td>0.515788</td>
    </tr>
    <tr>
      <th>2017-04-17</th>
      <td>141.4800</td>
      <td>141.8800</td>
      <td>140.8700</td>
      <td>141.8300</td>
      <td>16582094.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>140.333992</td>
      <td>140.730752</td>
      <td>139.728933</td>
      <td>140.681157</td>
      <td>16582094.0</td>
      <td>0.624897</td>
    </tr>
    <tr>
      <th>2017-04-13</th>
      <td>141.9100</td>
      <td>142.3800</td>
      <td>141.0500</td>
      <td>141.0500</td>
      <td>17822880.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>140.760509</td>
      <td>141.226702</td>
      <td>139.907475</td>
      <td>139.907475</td>
      <td>17822880.0</td>
      <td>-0.773682</td>
    </tr>
    <tr>
      <th>2017-04-12</th>
      <td>141.6000</td>
      <td>142.1500</td>
      <td>141.0100</td>
      <td>141.8000</td>
      <td>20350000.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>140.453020</td>
      <td>140.998565</td>
      <td>139.867799</td>
      <td>140.651400</td>
      <td>20350000.0</td>
      <td>0.743925</td>
    </tr>
    <tr>
      <th>2017-04-11</th>
      <td>142.9400</td>
      <td>143.3500</td>
      <td>140.0600</td>
      <td>141.6300</td>
      <td>30379376.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>141.782166</td>
      <td>142.188845</td>
      <td>138.925494</td>
      <td>140.482777</td>
      <td>30379376.0</td>
      <td>-0.168623</td>
    </tr>
    <tr>
      <th>2017-04-10</th>
      <td>143.6000</td>
      <td>143.8792</td>
      <td>142.9000</td>
      <td>143.1700</td>
      <td>18933397.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>142.436820</td>
      <td>142.713758</td>
      <td>141.742490</td>
      <td>142.010303</td>
      <td>18933397.0</td>
      <td>1.527526</td>
    </tr>
    <tr>
      <th>2017-04-07</th>
      <td>143.7300</td>
      <td>144.1800</td>
      <td>143.2700</td>
      <td>143.3400</td>
      <td>16658543.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>142.565767</td>
      <td>143.012122</td>
      <td>142.109493</td>
      <td>142.178926</td>
      <td>16658543.0</td>
      <td>0.168623</td>
    </tr>
    <tr>
      <th>2017-04-06</th>
      <td>144.2900</td>
      <td>144.5200</td>
      <td>143.4500</td>
      <td>143.6600</td>
      <td>21149034.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>143.121231</td>
      <td>143.349367</td>
      <td>142.288035</td>
      <td>142.496334</td>
      <td>21149034.0</td>
      <td>0.317408</td>
    </tr>
    <tr>
      <th>2017-04-05</th>
      <td>144.2200</td>
      <td>145.4600</td>
      <td>143.8100</td>
      <td>144.0200</td>
      <td>27717854.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>143.051798</td>
      <td>144.281753</td>
      <td>142.645119</td>
      <td>142.853418</td>
      <td>27717854.0</td>
      <td>0.357084</td>
    </tr>
    <tr>
      <th>2017-04-04</th>
      <td>143.2500</td>
      <td>144.8900</td>
      <td>143.1700</td>
      <td>144.7700</td>
      <td>19891354.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>142.089655</td>
      <td>143.716370</td>
      <td>142.010303</td>
      <td>143.597342</td>
      <td>19891354.0</td>
      <td>0.743925</td>
    </tr>
    <tr>
      <th>2017-04-03</th>
      <td>143.7100</td>
      <td>144.1200</td>
      <td>143.0500</td>
      <td>143.7000</td>
      <td>19985714.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>142.545929</td>
      <td>142.952608</td>
      <td>141.891275</td>
      <td>142.536010</td>
      <td>19985714.0</td>
      <td>-1.061333</td>
    </tr>
    <tr>
      <th>2017-03-31</th>
      <td>143.7200</td>
      <td>144.2700</td>
      <td>143.0100</td>
      <td>143.6600</td>
      <td>19661651.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>142.555848</td>
      <td>143.101393</td>
      <td>141.851599</td>
      <td>142.496334</td>
      <td>19661651.0</td>
      <td>-0.039676</td>
    </tr>
    <tr>
      <th>2017-03-30</th>
      <td>144.1900</td>
      <td>144.5000</td>
      <td>143.5000</td>
      <td>143.9300</td>
      <td>21207252.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>143.022041</td>
      <td>143.329529</td>
      <td>142.337630</td>
      <td>142.764147</td>
      <td>21207252.0</td>
      <td>0.267813</td>
    </tr>
    <tr>
      <th>2017-03-29</th>
      <td>143.6800</td>
      <td>144.4900</td>
      <td>143.1900</td>
      <td>144.1200</td>
      <td>29189955.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>142.516172</td>
      <td>143.319610</td>
      <td>142.030141</td>
      <td>142.952608</td>
      <td>29189955.0</td>
      <td>0.188461</td>
    </tr>
    <tr>
      <th>2017-03-28</th>
      <td>140.9100</td>
      <td>144.0400</td>
      <td>140.6200</td>
      <td>143.8000</td>
      <td>33374805.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>139.768609</td>
      <td>142.873256</td>
      <td>139.480958</td>
      <td>142.635200</td>
      <td>33374805.0</td>
      <td>-0.317408</td>
    </tr>
    <tr>
      <th>2017-03-27</th>
      <td>139.3900</td>
      <td>141.2200</td>
      <td>138.6200</td>
      <td>140.8800</td>
      <td>23575094.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>138.260921</td>
      <td>140.076098</td>
      <td>137.497158</td>
      <td>139.738852</td>
      <td>23575094.0</td>
      <td>-2.896348</td>
    </tr>
    <tr>
      <th>2017-03-24</th>
      <td>141.5000</td>
      <td>141.7400</td>
      <td>140.3500</td>
      <td>140.6400</td>
      <td>22395563.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>140.353830</td>
      <td>140.591886</td>
      <td>139.213145</td>
      <td>139.500796</td>
      <td>22395563.0</td>
      <td>-0.238056</td>
    </tr>
    <tr>
      <th>2017-03-23</th>
      <td>141.2600</td>
      <td>141.5844</td>
      <td>140.6100</td>
      <td>140.9200</td>
      <td>20346301.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>140.115774</td>
      <td>140.437546</td>
      <td>139.471039</td>
      <td>139.778528</td>
      <td>20346301.0</td>
      <td>0.277732</td>
    </tr>
    <tr>
      <th>2017-03-22</th>
      <td>139.8450</td>
      <td>141.6000</td>
      <td>139.7600</td>
      <td>141.4200</td>
      <td>25860165.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>138.712236</td>
      <td>140.453020</td>
      <td>138.627924</td>
      <td>140.274478</td>
      <td>25860165.0</td>
      <td>0.495950</td>
    </tr>
    <tr>
      <th>2017-03-21</th>
      <td>142.1100</td>
      <td>142.8000</td>
      <td>139.7300</td>
      <td>139.8400</td>
      <td>39529912.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>140.958889</td>
      <td>141.643300</td>
      <td>138.598167</td>
      <td>138.707276</td>
      <td>39529912.0</td>
      <td>-1.567202</td>
    </tr>
    <tr>
      <th>2017-03-20</th>
      <td>140.4000</td>
      <td>141.5000</td>
      <td>140.2300</td>
      <td>141.4600</td>
      <td>21542038.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>139.262740</td>
      <td>140.353830</td>
      <td>139.094117</td>
      <td>140.314154</td>
      <td>21542038.0</td>
      <td>1.606878</td>
    </tr>
    <tr>
      <th>2017-03-17</th>
      <td>141.0000</td>
      <td>141.0000</td>
      <td>139.8900</td>
      <td>139.9900</td>
      <td>43884952.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>139.857880</td>
      <td>139.857880</td>
      <td>138.756871</td>
      <td>138.856061</td>
      <td>43884952.0</td>
      <td>-1.458093</td>
    </tr>
    <tr>
      <th>2017-03-16</th>
      <td>140.7200</td>
      <td>141.0200</td>
      <td>140.2600</td>
      <td>140.6900</td>
      <td>19231998.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>139.580148</td>
      <td>139.877718</td>
      <td>139.123874</td>
      <td>139.550391</td>
      <td>19231998.0</td>
      <td>0.694330</td>
    </tr>
    <tr>
      <th>2017-03-15</th>
      <td>139.4100</td>
      <td>140.7501</td>
      <td>139.0250</td>
      <td>140.4600</td>
      <td>25691774.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>138.280759</td>
      <td>139.610004</td>
      <td>137.898878</td>
      <td>139.322254</td>
      <td>25691774.0</td>
      <td>-0.228137</td>
    </tr>
    <tr>
      <th>2017-03-14</th>
      <td>139.3000</td>
      <td>139.6500</td>
      <td>138.8400</td>
      <td>138.9900</td>
      <td>15309065.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>138.171650</td>
      <td>138.518815</td>
      <td>137.715376</td>
      <td>137.864161</td>
      <td>15309065.0</td>
      <td>-1.458093</td>
    </tr>
    <tr>
      <th>2017-03-13</th>
      <td>138.8500</td>
      <td>139.4300</td>
      <td>138.8200</td>
      <td>139.2000</td>
      <td>17421717.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>137.725295</td>
      <td>138.300597</td>
      <td>137.695538</td>
      <td>138.072460</td>
      <td>17421717.0</td>
      <td>0.208299</td>
    </tr>
    <tr>
      <th>2017-03-10</th>
      <td>139.2500</td>
      <td>139.3571</td>
      <td>138.6400</td>
      <td>139.1400</td>
      <td>19612801.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>138.122055</td>
      <td>138.228288</td>
      <td>137.516996</td>
      <td>138.012946</td>
      <td>19612801.0</td>
      <td>-0.059514</td>
    </tr>
    <tr>
      <th>2017-03-09</th>
      <td>138.7400</td>
      <td>138.7900</td>
      <td>137.0500</td>
      <td>138.6800</td>
      <td>22155904.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>137.616186</td>
      <td>137.665781</td>
      <td>135.939876</td>
      <td>137.556672</td>
      <td>22155904.0</td>
      <td>-0.456274</td>
    </tr>
    <tr>
      <th>2017-03-08</th>
      <td>138.9500</td>
      <td>139.8000</td>
      <td>138.8200</td>
      <td>139.0000</td>
      <td>18707236.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>137.824485</td>
      <td>138.667600</td>
      <td>137.695538</td>
      <td>137.874080</td>
      <td>18707236.0</td>
      <td>0.317408</td>
    </tr>
    <tr>
      <th>2017-03-07</th>
      <td>139.0600</td>
      <td>139.9800</td>
      <td>138.7900</td>
      <td>139.5200</td>
      <td>17446297.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>137.933594</td>
      <td>138.846142</td>
      <td>137.665781</td>
      <td>138.389868</td>
      <td>17446297.0</td>
      <td>0.515788</td>
    </tr>
    <tr>
      <th>2017-03-06</th>
      <td>139.3650</td>
      <td>139.7700</td>
      <td>138.5959</td>
      <td>139.3400</td>
      <td>21750044.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>138.236124</td>
      <td>138.637843</td>
      <td>137.473254</td>
      <td>138.211326</td>
      <td>21750044.0</td>
      <td>-0.178542</td>
    </tr>
    <tr>
      <th>2017-03-03</th>
      <td>138.7800</td>
      <td>139.8300</td>
      <td>138.5900</td>
      <td>139.7800</td>
      <td>21571121.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>137.655862</td>
      <td>138.697357</td>
      <td>137.467401</td>
      <td>138.647762</td>
      <td>21571121.0</td>
      <td>0.436436</td>
    </tr>
    <tr>
      <th>2017-03-02</th>
      <td>140.0000</td>
      <td>140.2786</td>
      <td>138.7600</td>
      <td>138.9600</td>
      <td>26210984.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>138.865980</td>
      <td>139.142323</td>
      <td>137.636024</td>
      <td>137.834404</td>
      <td>26210984.0</td>
      <td>-0.813358</td>
    </tr>
    <tr>
      <th>2017-03-01</th>
      <td>137.8900</td>
      <td>140.1500</td>
      <td>137.5950</td>
      <td>139.7900</td>
      <td>36414585.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>136.773071</td>
      <td>139.014765</td>
      <td>136.480461</td>
      <td>138.657681</td>
      <td>36414585.0</td>
      <td>0.823277</td>
    </tr>
    <tr>
      <th>2017-02-28</th>
      <td>137.0800</td>
      <td>137.4350</td>
      <td>136.7000</td>
      <td>136.9900</td>
      <td>23482860.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>135.969633</td>
      <td>136.321757</td>
      <td>135.592711</td>
      <td>135.880362</td>
      <td>23482860.0</td>
      <td>-2.777320</td>
    </tr>
    <tr>
      <th>2017-02-27</th>
      <td>137.1400</td>
      <td>137.4350</td>
      <td>136.2800</td>
      <td>136.9300</td>
      <td>20257426.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>136.029147</td>
      <td>136.321757</td>
      <td>135.176113</td>
      <td>135.820848</td>
      <td>20257426.0</td>
      <td>-0.059514</td>
    </tr>
    <tr>
      <th>2017-02-24</th>
      <td>135.9100</td>
      <td>136.6600</td>
      <td>135.2800</td>
      <td>136.6600</td>
      <td>21776585.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>134.809110</td>
      <td>135.553035</td>
      <td>134.184213</td>
      <td>135.553035</td>
      <td>21776585.0</td>
      <td>-0.267813</td>
    </tr>
    <tr>
      <th>2017-02-23</th>
      <td>137.3800</td>
      <td>137.4800</td>
      <td>136.3000</td>
      <td>136.5300</td>
      <td>20788186.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>136.267202</td>
      <td>136.366392</td>
      <td>135.195951</td>
      <td>135.424088</td>
      <td>20788186.0</td>
      <td>-0.128947</td>
    </tr>
    <tr>
      <th>2017-02-22</th>
      <td>136.4300</td>
      <td>137.1200</td>
      <td>136.1100</td>
      <td>137.1100</td>
      <td>20836932.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>135.324898</td>
      <td>136.009309</td>
      <td>135.007490</td>
      <td>135.999390</td>
      <td>20836932.0</td>
      <td>0.575302</td>
    </tr>
    <tr>
      <th>2017-02-21</th>
      <td>136.2300</td>
      <td>136.7500</td>
      <td>135.9800</td>
      <td>136.7000</td>
      <td>24507156.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>135.126518</td>
      <td>135.642306</td>
      <td>134.878543</td>
      <td>135.592711</td>
      <td>24507156.0</td>
      <td>-0.406679</td>
    </tr>
    <tr>
      <th>2017-02-17</th>
      <td>135.1000</td>
      <td>135.8300</td>
      <td>135.1000</td>
      <td>135.7200</td>
      <td>22198197.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>134.005671</td>
      <td>134.729758</td>
      <td>134.005671</td>
      <td>134.620649</td>
      <td>22198197.0</td>
      <td>-0.972062</td>
    </tr>
    <tr>
      <th>2017-02-16</th>
      <td>135.6700</td>
      <td>135.9000</td>
      <td>134.8398</td>
      <td>135.3450</td>
      <td>22584555.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>134.571054</td>
      <td>134.799191</td>
      <td>133.747578</td>
      <td>134.248686</td>
      <td>22584555.0</td>
      <td>-0.371962</td>
    </tr>
    <tr>
      <th>2017-02-15</th>
      <td>135.5200</td>
      <td>136.2700</td>
      <td>134.6200</td>
      <td>135.5100</td>
      <td>35623100.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>134.422269</td>
      <td>135.166194</td>
      <td>133.529559</td>
      <td>134.412350</td>
      <td>35623100.0</td>
      <td>0.163663</td>
    </tr>
    <tr>
      <th>2017-02-14</th>
      <td>133.4700</td>
      <td>135.0900</td>
      <td>133.2500</td>
      <td>135.0200</td>
      <td>33226223.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>132.388874</td>
      <td>133.995752</td>
      <td>132.170656</td>
      <td>133.926319</td>
      <td>33226223.0</td>
      <td>-0.486031</td>
    </tr>
    <tr>
      <th>2017-02-13</th>
      <td>133.0800</td>
      <td>133.8200</td>
      <td>132.7500</td>
      <td>133.2900</td>
      <td>23035421.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>132.002033</td>
      <td>132.736039</td>
      <td>131.674706</td>
      <td>132.210332</td>
      <td>23035421.0</td>
      <td>-1.715987</td>
    </tr>
    <tr>
      <th>2017-02-10</th>
      <td>132.4600</td>
      <td>132.9400</td>
      <td>132.0500</td>
      <td>132.1200</td>
      <td>20065458.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>131.387055</td>
      <td>131.863167</td>
      <td>130.980376</td>
      <td>131.049809</td>
      <td>20065458.0</td>
      <td>-1.160523</td>
    </tr>
    <tr>
      <th>2017-02-09</th>
      <td>131.6500</td>
      <td>132.4450</td>
      <td>131.1200</td>
      <td>132.4200</td>
      <td>28349859.0</td>
      <td>0.57</td>
      <td>1.0</td>
      <td>130.583616</td>
      <td>131.372177</td>
      <td>130.057909</td>
      <td>131.347379</td>
      <td>28349859.0</td>
      <td>0.297570</td>
    </tr>
    <tr>
      <th>2017-02-08</th>
      <td>131.3500</td>
      <td>132.2200</td>
      <td>131.2200</td>
      <td>132.0400</td>
      <td>23004072.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>129.727636</td>
      <td>130.586890</td>
      <td>129.599241</td>
      <td>130.409113</td>
      <td>23004072.0</td>
      <td>-0.938266</td>
    </tr>
    <tr>
      <th>2017-02-07</th>
      <td>130.5400</td>
      <td>132.0900</td>
      <td>130.4500</td>
      <td>131.5300</td>
      <td>38183841.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>128.927640</td>
      <td>130.458496</td>
      <td>128.838752</td>
      <td>129.905412</td>
      <td>38183841.0</td>
      <td>-0.503701</td>
    </tr>
    <tr>
      <th>2017-02-06</th>
      <td>129.1300</td>
      <td>130.5000</td>
      <td>128.9000</td>
      <td>130.2900</td>
      <td>26845924.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>127.535056</td>
      <td>128.888134</td>
      <td>127.307897</td>
      <td>128.680728</td>
      <td>26845924.0</td>
      <td>-1.224684</td>
    </tr>
    <tr>
      <th>2017-02-03</th>
      <td>128.3100</td>
      <td>129.1900</td>
      <td>128.1600</td>
      <td>129.0800</td>
      <td>24507301.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>126.725184</td>
      <td>127.594315</td>
      <td>126.577037</td>
      <td>127.485673</td>
      <td>24507301.0</td>
      <td>-1.195055</td>
    </tr>
    <tr>
      <th>2017-02-02</th>
      <td>127.9750</td>
      <td>129.3900</td>
      <td>127.7800</td>
      <td>128.5300</td>
      <td>33710411.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>126.394322</td>
      <td>127.791844</td>
      <td>126.201730</td>
      <td>126.942467</td>
      <td>33710411.0</td>
      <td>-0.543207</td>
    </tr>
    <tr>
      <th>2017-02-01</th>
      <td>127.0300</td>
      <td>130.4900</td>
      <td>127.0100</td>
      <td>128.7500</td>
      <td>111985040.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>125.460994</td>
      <td>128.878258</td>
      <td>125.441241</td>
      <td>127.159749</td>
      <td>111985040.0</td>
      <td>0.217283</td>
    </tr>
    <tr>
      <th>2017-01-31</th>
      <td>121.1500</td>
      <td>121.3900</td>
      <td>120.6200</td>
      <td>121.3500</td>
      <td>49200993.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>119.653620</td>
      <td>119.890656</td>
      <td>119.130167</td>
      <td>119.851150</td>
      <td>49200993.0</td>
      <td>-7.308599</td>
    </tr>
    <tr>
      <th>2017-01-30</th>
      <td>120.9300</td>
      <td>121.6300</td>
      <td>120.6600</td>
      <td>121.6300</td>
      <td>30377503.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>119.436338</td>
      <td>120.127692</td>
      <td>119.169673</td>
      <td>120.127692</td>
      <td>30377503.0</td>
      <td>0.276542</td>
    </tr>
    <tr>
      <th>2017-01-27</th>
      <td>122.1400</td>
      <td>122.3500</td>
      <td>121.6000</td>
      <td>121.9500</td>
      <td>20562944.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>120.631393</td>
      <td>120.838799</td>
      <td>120.098062</td>
      <td>120.443739</td>
      <td>20562944.0</td>
      <td>0.316048</td>
    </tr>
    <tr>
      <th>2017-01-26</th>
      <td>121.6700</td>
      <td>122.4400</td>
      <td>121.6000</td>
      <td>121.9400</td>
      <td>26337576.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>120.167198</td>
      <td>120.927687</td>
      <td>120.098062</td>
      <td>120.433863</td>
      <td>26337576.0</td>
      <td>-0.009876</td>
    </tr>
    <tr>
      <th>2017-01-25</th>
      <td>120.4200</td>
      <td>122.1000</td>
      <td>120.2800</td>
      <td>121.8800</td>
      <td>32586673.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>118.932637</td>
      <td>120.591887</td>
      <td>118.794366</td>
      <td>120.374604</td>
      <td>32586673.0</td>
      <td>-0.059259</td>
    </tr>
    <tr>
      <th>2017-01-24</th>
      <td>119.5500</td>
      <td>120.1000</td>
      <td>119.5000</td>
      <td>119.9700</td>
      <td>23211038.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>118.073383</td>
      <td>118.616590</td>
      <td>118.024000</td>
      <td>118.488195</td>
      <td>23211038.0</td>
      <td>-1.886409</td>
    </tr>
    <tr>
      <th>2017-01-23</th>
      <td>120.0000</td>
      <td>120.8100</td>
      <td>119.7700</td>
      <td>120.0800</td>
      <td>22050218.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>118.517825</td>
      <td>119.317820</td>
      <td>118.290666</td>
      <td>118.596837</td>
      <td>22050218.0</td>
      <td>0.108641</td>
    </tr>
    <tr>
      <th>2017-01-20</th>
      <td>120.4500</td>
      <td>120.4500</td>
      <td>119.7346</td>
      <td>120.0000</td>
      <td>32597892.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>118.962267</td>
      <td>118.962267</td>
      <td>118.255703</td>
      <td>118.517825</td>
      <td>32597892.0</td>
      <td>-0.079012</td>
    </tr>
    <tr>
      <th>2017-01-19</th>
      <td>119.4000</td>
      <td>120.0900</td>
      <td>119.3700</td>
      <td>119.7800</td>
      <td>25597291.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>117.925236</td>
      <td>118.606713</td>
      <td>117.895606</td>
      <td>118.300542</td>
      <td>25597291.0</td>
      <td>-0.217283</td>
    </tr>
    <tr>
      <th>2017-01-18</th>
      <td>120.0000</td>
      <td>120.5000</td>
      <td>119.7100</td>
      <td>119.9900</td>
      <td>23712961.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>118.517825</td>
      <td>119.011649</td>
      <td>118.231407</td>
      <td>118.507948</td>
      <td>23712961.0</td>
      <td>0.207406</td>
    </tr>
    <tr>
      <th>2017-01-17</th>
      <td>118.3400</td>
      <td>120.2400</td>
      <td>118.2200</td>
      <td>120.0000</td>
      <td>34439843.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>116.878328</td>
      <td>118.754860</td>
      <td>116.759810</td>
      <td>118.517825</td>
      <td>34439843.0</td>
      <td>0.009876</td>
    </tr>
    <tr>
      <th>2017-01-13</th>
      <td>119.1100</td>
      <td>119.6200</td>
      <td>118.8100</td>
      <td>119.0400</td>
      <td>26111948.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>117.638817</td>
      <td>118.142518</td>
      <td>117.342523</td>
      <td>117.569682</td>
      <td>26111948.0</td>
      <td>-0.948143</td>
    </tr>
    <tr>
      <th>2017-01-12</th>
      <td>118.8950</td>
      <td>119.3000</td>
      <td>118.2100</td>
      <td>119.2500</td>
      <td>27086220.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>117.426473</td>
      <td>117.826471</td>
      <td>116.749934</td>
      <td>117.777088</td>
      <td>27086220.0</td>
      <td>0.207406</td>
    </tr>
    <tr>
      <th>2017-01-11</th>
      <td>118.7400</td>
      <td>119.9300</td>
      <td>118.6000</td>
      <td>119.7500</td>
      <td>27588593.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>117.273388</td>
      <td>118.448689</td>
      <td>117.135117</td>
      <td>118.270913</td>
      <td>27588593.0</td>
      <td>0.493824</td>
    </tr>
    <tr>
      <th>2017-01-10</th>
      <td>118.7700</td>
      <td>119.3800</td>
      <td>118.3000</td>
      <td>119.1100</td>
      <td>24462051.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>117.303017</td>
      <td>117.905483</td>
      <td>116.838822</td>
      <td>117.638817</td>
      <td>24462051.0</td>
      <td>-0.632095</td>
    </tr>
    <tr>
      <th>2017-01-09</th>
      <td>117.9500</td>
      <td>119.4300</td>
      <td>117.9400</td>
      <td>118.9900</td>
      <td>33561948.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>116.493145</td>
      <td>117.954865</td>
      <td>116.483269</td>
      <td>117.520300</td>
      <td>33561948.0</td>
      <td>-0.118518</td>
    </tr>
    <tr>
      <th>2017-01-06</th>
      <td>116.7800</td>
      <td>118.1600</td>
      <td>116.4700</td>
      <td>117.9100</td>
      <td>31751900.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>115.337596</td>
      <td>116.700551</td>
      <td>115.031425</td>
      <td>116.453639</td>
      <td>31751900.0</td>
      <td>-1.066660</td>
    </tr>
    <tr>
      <th>2017-01-05</th>
      <td>115.9200</td>
      <td>116.8642</td>
      <td>115.8100</td>
      <td>116.6100</td>
      <td>22193587.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>114.488219</td>
      <td>115.420756</td>
      <td>114.379577</td>
      <td>115.169696</td>
      <td>22193587.0</td>
      <td>-1.283943</td>
    </tr>
    <tr>
      <th>2017-01-04</th>
      <td>115.8500</td>
      <td>116.5100</td>
      <td>115.7500</td>
      <td>116.0200</td>
      <td>21118116.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>114.419083</td>
      <td>115.070931</td>
      <td>114.320318</td>
      <td>114.586983</td>
      <td>21118116.0</td>
      <td>-0.582713</td>
    </tr>
    <tr>
      <th>2017-01-03</th>
      <td>115.8000</td>
      <td>116.3300</td>
      <td>114.7600</td>
      <td>116.1500</td>
      <td>28781865.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>114.369701</td>
      <td>114.893155</td>
      <td>113.342546</td>
      <td>114.715378</td>
      <td>28781865.0</td>
      <td>0.128394</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_INTC_17.drop(pd.to_datetime('2017-08-07'), inplace = True)
df_INTC_17
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    <ipython-input-85-74e36643edc9> in <module>()
    ----> 1 df_INTC_17.drop(pd.to_datetime('2017-08-07'), inplace = True)
          2 df_INTC_17


    ~/anaconda3/lib/python3.6/site-packages/pandas/core/frame.py in drop(self, labels, axis, index, columns, level, inplace, errors)
       3695                                            index=index, columns=columns,
       3696                                            level=level, inplace=inplace,
    -> 3697                                            errors=errors)
       3698 
       3699     @rewrite_axis_style_signature('mapper', [('copy', True),


    ~/anaconda3/lib/python3.6/site-packages/pandas/core/generic.py in drop(self, labels, axis, index, columns, level, inplace, errors)
       3109         for axis, labels in axes.items():
       3110             if labels is not None:
    -> 3111                 obj = obj._drop_axis(labels, axis, level=level, errors=errors)
       3112 
       3113         if inplace:


    ~/anaconda3/lib/python3.6/site-packages/pandas/core/generic.py in _drop_axis(self, labels, axis, level, errors)
       3141                 new_axis = axis.drop(labels, level=level, errors=errors)
       3142             else:
    -> 3143                 new_axis = axis.drop(labels, errors=errors)
       3144             result = self.reindex(**{axis_name: new_axis})
       3145 


    ~/anaconda3/lib/python3.6/site-packages/pandas/core/indexes/base.py in drop(self, labels, errors)
       4402             if errors != 'ignore':
       4403                 raise KeyError(
    -> 4404                     '{} not found in axis'.format(labels[mask]))
       4405             indexer = indexer[~mask]
       4406         return self.delete(indexer)


    KeyError: "[Timestamp('2017-08-07 00:00:00')] not found in axis"



```python
n_7_m = df_INTC_07['Diff'].max()
n_7_i = df_INTC_07['Diff'].idxmax()
n_8_m = df_INTC_08['Diff'].max()
n_8_i = df_INTC_08['Diff'].idxmax()
n_9_m = df_INTC_09['Diff'].max()
n_9_i = df_INTC_09['Diff'].idxmax()
n_10_m = df_INTC_10['Diff'].max()
n_10_i = df_INTC_10['Diff'].idxmax()
n_11_m = df_INTC_11['Diff'].max()
n_11_i = df_INTC_11['Diff'].idxmax()
n_12_m = df_INTC_12['Diff'].max()
n_12_i = df_INTC_12['Diff'].idxmax()
n_13_m = df_INTC_13['Diff'].max()
n_13_i = df_INTC_13['Diff'].idxmax()
n_14_m = df_INTC_14['Diff'].max()
n_14_i = df_INTC_14['Diff'].idxmax()
n_15_m = df_INTC_15['Diff'].max()
n_15_i = df_INTC_15['Diff'].idxmax()
n_16_m = df_INTC_16['Diff'].max()
n_16_i = df_INTC_16['Diff'].idxmax()
n_17_m = df_INTC_17['Diff'].max()
n_17_i = df_INTC_17['Diff'].idxmax()
INTC_max_index_data = {n_7_m:n_7_i, n_8_m:n_8_i, n_9_m:n_9_i, n_10_m:n_10_i, n_11_m:n_11_i, n_12_m:n_12_i, n_13_m:n_13_i, n_14_m:n_14_i, n_15_m:n_15_i,n_16_m:n_16_i, n_17_m:n_17_i}
for i in INTC_max_index_data:
    print (i,INTC_max_index_data[i])
y = INTC_max_index_data.keys()
x = INTC_max_index_data.values()
plt.plot(x,y)
```


```python
a_7_m = df_AAPL_07['Diff'].max()
a_7_i = df_AAPL_07['Diff'].idxmax()
a_8_m = df_AAPL_08['Diff'].max()
a_8_i = df_AAPL_08['Diff'].idxmax()
a_9_m = df_AAPL_09['Diff'].max()
a_9_i = df_AAPL_09['Diff'].idxmax()
a_10_m = df_AAPL_10['Diff'].max()
a_10_i = df_AAPL_10['Diff'].idxmax()
a_11_m = df_AAPL_11['Diff'].max()
a_11_i = df_AAPL_11['Diff'].idxmax()
a_12_m = df_AAPL_12['Diff'].max()
a_12_i = df_AAPL_12['Diff'].idxmax()
a_13_m = df_AAPL_13['Diff'].max()
a_13_i = df_AAPL_13['Diff'].idxmax()
a_14_m = df_AAPL_14['Diff'].max()
a_14_i = df_AAPL_14['Diff'].idxmax()
a_15_m = df_AAPL_15['Diff'].max()
a_15_i = df_AAPL_15['Diff'].idxmax()
a_16_m = df_AAPL_16['Diff'].max()
a_16_i = df_AAPL_16['Diff'].idxmax()
a_17_m = df_AAPL_17['Diff'].max()
a_17_i = df_AAPL_17['Diff'].idxmax()
AAPL_max_index_data = {a_7_m:a_7_i, a_8_m:a_8_i, a_9_m:a_9_i, a_10_m:a_10_i, a_11_m:a_11_i, a_12_m:a_12_i, a_13_m:a_13_i, a_14_m:a_14_i, a_15_m:a_15_i, a_16_m:a_16_i, a_17_m:a_17_i}
for i in AAPL_max_index_data:
    print (i,AAPL_max_index_data[i])
y = AAPL_max_index_data.keys()
x = AAPL_max_index_data.values()
plt.plot(x,y)
```

    1.492046816123004 2007-11-09 00:00:00
    2.9532502872100004 2008-09-26 00:00:00
    1.0088344105570002 2009-10-29 00:00:00
    1.5588740637009977 2010-06-28 00:00:00
    3.035499207305989 2011-10-18 00:00:00
    4.804879811891013 2012-12-04 00:00:00
    8.23504355787 2013-01-23 00:00:00
    5.848590068169997 2014-01-27 00:00:00
    6.628260469329987 2015-08-20 00:00:00
    6.3475968238060005 2016-01-26 00:00:00
    5.985713277740018 2017-06-08 00:00:00





    [<matplotlib.lines.Line2D at 0x1a19f13c88>]




![png](output_86_2.png)



```python
df_INTC_07.corrwith(df_AAPL_07['AdjClose'])
```




    Open          0.921150
    High          0.919998
    Low           0.918280
    Close         0.918312
    Volume       -0.148249
    ExDividend   -0.009703
    SplitRatio         NaN
    AdjOpen       0.926971
    AdjHigh       0.925864
    AdjLow        0.924499
    AdjClose      0.924618
    AdjVolume    -0.148249
    Diff          0.039168
    dtype: float64




```python
df_INTC_08.corrwith(df_AAPL_08['AdjClose'])
```




    Open          0.915694
    High          0.920165
    Low           0.917016
    Close         0.919402
    Volume       -0.238773
    ExDividend    0.010813
    SplitRatio         NaN
    AdjOpen       0.918703
    AdjHigh       0.923565
    AdjLow        0.920047
    AdjClose      0.922661
    AdjVolume    -0.238773
    Diff          0.068765
    dtype: float64




```python
df_INTC_09.corrwith(df_AAPL_09['AdjClose'])
```




    Open          0.956915
    High          0.956611
    Low           0.960027
    Close         0.956705
    Volume       -0.221292
    ExDividend   -0.004061
    SplitRatio         NaN
    AdjOpen       0.963314
    AdjHigh       0.963159
    AdjLow        0.965882
    AdjClose      0.963263
    AdjVolume    -0.221292
    Diff          0.009224
    dtype: float64




```python
df_INTC_10.corrwith(df_AAPL_10['AdjClose'])
```




    Open         -0.006534
    High         -0.020317
    Low           0.024247
    Close         0.004865
    Volume       -0.231794
    ExDividend   -0.007094
    SplitRatio         NaN
    AdjOpen       0.121975
    AdjHigh       0.109308
    AdjLow        0.153739
    AdjClose      0.133771
    AdjVolume    -0.231794
    Diff          0.028734
    dtype: float64




```python
df_INTC_11.corrwith(df_AAPL_11['AdjClose'])
```




    Open          0.479484
    High          0.501755
    Low           0.472235
    Close         0.494299
    Volume       -0.066835
    ExDividend    0.049183
    SplitRatio         NaN
    AdjOpen       0.543157
    AdjHigh       0.561637
    AdjLow        0.537581
    AdjClose      0.556415
    AdjVolume    -0.066835
    Diff          0.046088
    dtype: float64




```python
df_INTC_12.corrwith(df_AAPL_12['AdjClose'])
```




    Open         -0.096990
    High         -0.099652
    Low          -0.099747
    Close        -0.104946
    Volume       -0.094223
    ExDividend   -0.028373
    SplitRatio         NaN
    AdjOpen      -0.055870
    AdjHigh      -0.058607
    AdjLow       -0.059212
    AdjClose     -0.064876
    AdjVolume    -0.094223
    Diff          0.168851
    dtype: float64




```python
df_INTC_13.corrwith(df_AAPL_13['AdjClose'])
```




    Open          0.305879
    High          0.299572
    Low           0.324370
    Close         0.312240
    Volume       -0.299786
    ExDividend    0.003359
    SplitRatio         NaN
    AdjOpen       0.380807
    AdjHigh       0.375593
    AdjLow        0.396739
    AdjClose      0.386779
    AdjVolume    -0.299786
    Diff         -0.021691
    dtype: float64




```python
df_INTC_14.corrwith(df_AAPL_14['AdjClose'])
```




    Open          0.933217
    High          0.935565
    Low           0.934279
    Close         0.936469
    Volume       -0.059399
    ExDividend   -0.016352
    SplitRatio         NaN
    AdjOpen       0.939974
    AdjHigh       0.942090
    AdjLow        0.940996
    AdjClose      0.943015
    AdjVolume    -0.059399
    Diff         -0.029293
    dtype: float64




```python
df_INTC_15.corrwith(df_AAPL_15['AdjClose'])
```




    Open         -0.048288
    High         -0.064714
    Low          -0.033028
    Close        -0.047482
    Volume       -0.073629
    ExDividend    0.005904
    SplitRatio         NaN
    AdjOpen      -0.088185
    AdjHigh      -0.106000
    AdjLow       -0.072547
    AdjClose     -0.087674
    AdjVolume    -0.073629
    Diff          0.118686
    dtype: float64




```python
df_INTC_16.corrwith(df_AAPL_16['AdjClose'])
```




    Open          0.817863
    High          0.818174
    Low           0.816990
    Close         0.817321
    Volume       -0.200592
    ExDividend   -0.051402
    SplitRatio         NaN
    AdjOpen       0.824018
    AdjHigh       0.823944
    AdjLow        0.822423
    AdjClose      0.822861
    AdjVolume    -0.200592
    Diff          0.054387
    dtype: float64




```python
df_INTC_17.corrwith(df_AAPL_17['AdjClose'])
```




    Open          0.628222
    High          0.630202
    Low           0.630384
    Close         0.631530
    Volume        0.072810
    ExDividend    0.009343
    SplitRatio         NaN
    AdjOpen       0.673429
    AdjHigh       0.674889
    AdjLow        0.675841
    AdjClose      0.676317
    AdjVolume     0.072810
    Diff         -0.058678
    dtype: float64




```python
df_INTC_07_AdjClose = df_INTC_07['AdjClose']
df_INTC_07_AdjClose.head()
```




    Date
    2007-12-31    19.240352
    2007-12-28    19.312522
    2007-12-27    19.363040
    2007-12-26    19.810490
    2007-12-24    19.709453
    Name: AdjClose, dtype: float64




```python
df_AAPL_07_AdjClose = df_AAPL_07['AdjClose']
df_AAPL_07_AdjClose.head()
```




    Date
    2007-12-31    25.456041
    2007-12-28    25.680940
    2007-12-27    25.519013
    2007-12-26    25.567848
    2007-12-24    25.548571
    Name: AdjClose, dtype: float64




```python
df_INTC_07_AdjClose.rename(index='Date')
df_INTC_07_AdjClose.to_frame()
df_INTC_07_AdjClose.head()
```




    Date
    2007-12-31    19.240352
    2007-12-28    19.312522
    2007-12-27    19.363040
    2007-12-26    19.810490
    2007-12-24    19.709453
    Name: AdjClose, dtype: float64




```python
df_AAPL_07_AdjClose.rename(index='Date')
df_INTC_07_AdjClose.head()
```




    Date
    2007-12-31    19.240352
    2007-12-28    19.312522
    2007-12-27    19.363040
    2007-12-26    19.810490
    2007-12-24    19.709453
    Name: AdjClose, dtype: float64




```python
merged_07 = pd.concat([df_INTC_07_AdjClose, df_AAPL_07_AdjClose], axis=1, join_axes=[df_INTC_07_AdjClose.index])
merged_07.columns = ['INTC_07', 'AAPL_07']
merged_07.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>INTC_07</th>
      <th>AAPL_07</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2007-12-31</th>
      <td>19.240352</td>
      <td>25.456041</td>
    </tr>
    <tr>
      <th>2007-12-28</th>
      <td>19.312522</td>
      <td>25.680940</td>
    </tr>
    <tr>
      <th>2007-12-27</th>
      <td>19.363040</td>
      <td>25.519013</td>
    </tr>
    <tr>
      <th>2007-12-26</th>
      <td>19.810490</td>
      <td>25.567848</td>
    </tr>
    <tr>
      <th>2007-12-24</th>
      <td>19.709453</td>
      <td>25.548571</td>
    </tr>
  </tbody>
</table>
</div>




```python
correlation = merged_07.corr()
correlation
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>INTC_07</th>
      <th>AAPL_07</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>INTC_07</th>
      <td>1.000000</td>
      <td>0.924618</td>
    </tr>
    <tr>
      <th>AAPL_07</th>
      <td>0.924618</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
plt.scatter(df_INTC_07['Diff'], df_AAPL_07['Diff'], marker = 'x', c='g')
plt.xlabel = ('Intel price change per day')
plt.ylabel = ('Apple price change per day')
```


![png](output_104_0.png)



```python
seb.regplot(df_INTC_07['Diff'], df_AAPL_07['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a19c8bba8>




![png](output_105_1.png)



```python
seb.regplot(df_INTC_08['Diff'], df_AAPL_08['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a19b4a9e8>




![png](output_106_1.png)



```python
seb.regplot(df_INTC_09['Diff'], df_AAPL_09['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a19c3bba8>




![png](output_107_1.png)



```python
seb.regplot(df_INTC_10['Diff'], df_AAPL_10['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a220c6780>




![png](output_108_1.png)



```python
seb.regplot(df_INTC_11['Diff'], df_AAPL_11['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a19f63f98>




![png](output_109_1.png)



```python
seb.regplot(df_INTC_12['Diff'], df_AAPL_12['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a19bd5b70>




![png](output_110_1.png)



```python
seb.regplot(df_INTC_13['Diff'], df_AAPL_13['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a1a15a860>




![png](output_111_1.png)



```python
seb.regplot(df_INTC_14['Diff'], df_AAPL_14['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a1a371be0>




![png](output_112_1.png)



```python
seb.regplot(df_INTC_15['Diff'], df_AAPL_15['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a22906ef0>




![png](output_113_1.png)



```python
seb.regplot(df_INTC_16['Diff'], df_AAPL_16['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a2299e048>




![png](output_114_1.png)



```python
seb.regplot(df_INTC_17['Diff'], df_INTC_17['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a22afedd8>




![png](output_115_1.png)



```python
stats.ttest_ind(df_INTC_17['Diff'], df_AAPL_17['Diff'], equal_var=False)
```




    Ttest_indResult(statistic=nan, pvalue=nan)




```python
df_AAPL_07.loc[:,"Diff"].std()
```




    0.4235193094924471




```python
df_AAPL_08.loc[:,"Diff"].std()
```




    0.6085329189686448




```python
df_AAPL_09.loc[:,"Diff"].std()
```




    0.35409004776653596




```python
df_AAPL_10.loc[:,"Diff"].std()
```




    0.5426277184493238




```python
df_AAPL_11.loc[:,"Diff"].std()
```




    0.7823461228285264




```python
df_AAPL_12.loc[:,"Diff"].std()
```




    1.3645132158955302




```python
df_AAPL_13.loc[:,"Diff"].std()
```




    1.11578520846419




```python
df_AAPL_14.loc[:,"Diff"].std()
```




    1.169183458769323




```python
df_AAPL_15.loc[:,"Diff"].std()
```




    1.8880552633201841




```python
df_AAPL_16.loc[:,"Diff"].std()
```




    1.4623297059678657




```python
df_AAPL_17.loc[:,"Diff"].std()
```




    1.693111088548734




```python
df_INTC_07.loc[:,"Diff"].std()
```




    0.28440530669658537




```python
df_INTC_08.loc[:,"Diff"].std()
```




    0.4428521650140902




```python
df_INTC_09.loc[:,"Diff"].std()
```




    0.2703082857458853




```python
df_INTC_10.loc[:,"Diff"].std()
```




    0.25826567030984704




```python
df_INTC_11.loc[:,"Diff"].std()
```




    0.3085419888161559




```python
df_INTC_12.loc[:,"Diff"].std()
```




    0.27599110640299696




```python
df_INTC_13.loc[:,"Diff"].std()
```




    0.2575237021656122




```python
df_INTC_14.loc[:,"Diff"].std()
```




    0.39641141839468863




```python
df_INTC_15.loc[:,"Diff"].std()
```




    0.4491501760926653




```python
df_INTC_16.loc[:,"Diff"].std()
```




    0.4470358215350684




```python
df_INTC_17.loc[:,"Diff"].std()
```




    0.4260715163180908




```python
df_AAPL_07.loc[:,"Diff"].cov(df_INTC_07.loc[:,"Diff"])
```




    0.05514810885772115




```python
df_AAPL_08.loc[:,"Diff"].cov(df_INTC_08.loc[:,"Diff"])
```




    0.1630848333540226




```python
df_AAPL_09.loc[:,"Diff"].cov(df_INTC_09.loc[:,"Diff"])
```




    0.05132885504529746




```python
df_AAPL_10.loc[:,"Diff"].cov(df_INTC_10.loc[:,"Diff"])
```




    0.07939143269792041




```python
df_AAPL_11.loc[:,"Diff"].cov(df_INTC_11.loc[:,"Diff"])
```




    0.12137180770045401




```python
df_AAPL_12.loc[:,"Diff"].cov(df_INTC_12.loc[:,"Diff"])
```




    0.11835670321083182




```python
df_AAPL_13.loc[:,"Diff"].cov(df_INTC_13.loc[:,"Diff"])
```




    0.04241454876409036




```python
df_AAPL_14.loc[:,"Diff"].cov(df_INTC_14.loc[:,"Diff"])
```




    0.12068850469707701




```python
df_AAPL_15.loc[:,"Diff"].cov(df_INTC_15.loc[:,"Diff"])
```




    0.3597098097952122




```python
df_AAPL_16.loc[:,"Diff"].cov(df_INTC_16.loc[:,"Diff"])
```




    0.2921007074134525




```python
df_AAPL_17.loc[:,"Diff"].cov(df_INTC_17.loc[:,"Diff"])
```




    0.2454890316611117




```python
df_INTC_07['Diff'].mean()
```




    -0.019339106173584




```python
df_AAPL_07['Diff'].mean()
```




    -0.05874629117882




```python
INTC_07_mean=df_INTC_07['Diff'].mean()
INTC_07_mean
```




    -0.019339106173584




```python
INTC_08_mean = df_INTC_08['Diff'].mean()
INTC_08_mean
```




    0.02943822643919842




```python
INTC_09_mean = df_INTC_09['Diff'].mean()
INTC_09_mean
```




    -0.01742839473882868




```python
INTC_10_mean = df_INTC_10['Diff'].mean()
INTC_10_mean
```




    -0.0024347304154940176




```python
INTC_11_mean = df_INTC_11['Diff'].mean()
INTC_11_mean
```




    -0.013376083637832667




```python
INTC_12_mean = df_INTC_12['Diff'].mean()
INTC_12_mean
```




    0.010544306359831333




```python
INTC_13_mean = df_INTC_13['Diff'].mean()
INTC_13_mean
```




    -0.018913973485948202




```python
INTC_14_mean = df_INTC_14['Diff'].mean()
INTC_14_mean
```




    -0.04090674189856972




```python
INTC_15_mean = df_INTC_15['Diff'].mean()
INTC_15_mean
```




    0.0031603476999721176




```python
INTC_16_mean = df_INTC_16['Diff'].mean()
INTC_16_mean
```




    -0.012995493215342619




```python
INTC_17_mean = df_INTC_17['Diff'].mean()
INTC_17_mean
```




    -0.043419667238600815




```python
AAPL_07_mean=df_AAPL_07['Diff'].mean()
AAPL_07_mean
```




    -0.05874629117882




```python
AAPL_08_mean=df_AAPL_08['Diff'].mean()
AAPL_08_mean
```




    0.05583726600539285




```python
AAPL_09_mean=df_AAPL_09['Diff'].mean()
AAPL_09_mean
```




    -0.061431710227844605




```python
AAPL_10_mean=df_AAPL_10['Diff'].mean()
AAPL_10_mean
```




    -0.05557843797596813




```python
AAPL_11_mean=df_AAPL_11['Diff'].mean()
AAPL_11_mean
```




    -0.03862074229872907




```python
AAPL_12_mean=df_AAPL_12['Diff'].mean()
AAPL_12_mean
```




    -0.06490364702983135




```python
AAPL_13_mean=df_AAPL_13['Diff'].mean()
AAPL_13_mean
```




    -0.013451928329549766




```python
AAPL_14_mean=df_AAPL_14['Diff'].mean()
AAPL_14_mean
```




    -0.1248527424291952




```python
AAPL_15_mean=df_AAPL_15['Diff'].mean()
AAPL_15_mean
```




    0.008634052766414341




```python
AAPL_16_mean=df_AAPL_16['Diff'].mean()
AAPL_16_mean
```




    -0.05022187412944234




```python
AAPL_17_mean=df_AAPL_17['Diff'].mean()
AAPL_17_mean
```




    -0.2198170249938709




```python
def gendata_07(loc1=0, loc2=0):
    population_n_07 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_07 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_07, population_a_07
population_n_07, population_a_07 = gendata_07(loc1=INTC_07_mean, loc2=AAPL_07_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_07)), population_n_07, label="INTC 07")
plt.scatter(range(len(population_a_07)), population_a_07, label="AAPL 07")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_07, 10, density=True, alpha=0.5, label="INTC 07")
plt.hist(population_a_07, 10, density=True, alpha=0.5, label="AAPL 07")
plt.axvline(population_n_07.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_07.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a1a4504a8>




![png](output_174_1.png)



```python
stats.ttest_ind(population_n_07, population_a_07, equal_var=False)
```




    Ttest_indResult(statistic=0.43085278050611286, pvalue=0.6667618394372116)




```python
def gendata_08(loc1=0, loc2=0):
    population_n_08 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_08 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_08, population_a_08
population_n_08, population_a_08 = gendata_08(loc1=INTC_08_mean, loc2=AAPL_08_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_08)), population_n_08, label="INTC 08")
plt.scatter(range(len(population_a_08)), population_a_08, label="AAPL 08")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_08, 10, density=True, alpha=0.5, label="INTC 08")
plt.hist(population_a_08, 10, density=True, alpha=0.5, label="AAPL 08")
plt.axvline(population_n_08.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_08.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a22c75da0>




![png](output_176_1.png)



```python
stats.ttest_ind(population_n_08, population_a_08, equal_var=False)
```




    Ttest_indResult(statistic=-0.2886300962191162, pvalue=0.7729845603007193)




```python
def gendata_09(loc1=0, loc2=0):
    population_n_09 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_09 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_09, population_a_09
population_n_09, population_a_09 = gendata_09(loc1=INTC_09_mean, loc2=AAPL_09_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_09)), population_n_09, label="population1")
plt.scatter(range(len(population_a_09)), population_a_09, label="population2")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_09, 10, density=True, alpha=0.5, label="population1")
plt.hist(population_a_09, 10, density=True, alpha=0.5, label="population2")
plt.axvline(population_n_09.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_09.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a22dff2e8>




![png](output_178_1.png)



```python
stats.ttest_ind(population_n_09, population_a_09, equal_var=False)
```




    Ttest_indResult(statistic=0.48110391106117223, pvalue=0.6306539567001321)




```python
def gendata_10(loc1=0, loc2=0):
    population_n_10 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_10 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_10, population_a_10
population_n_10, population_a_10 = gendata_10(loc1=INTC_10_mean, loc2=AAPL_10_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_10)), population_n_10, label="population1")
plt.scatter(range(len(population_a_10)), population_a_10, label="population2")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_10, 10, density=True, alpha=0.5, label="population1")
plt.hist(population_a_10, 10, density=True, alpha=0.5, label="population2")
plt.axvline(population_n_10.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_10.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a22f7c748>




![png](output_180_1.png)



```python
stats.ttest_ind(population_n_10, population_a_10, equal_var=False)
```




    Ttest_indResult(statistic=0.5810390710676672, pvalue=0.561476983284986)




```python
def gendata_11(loc1=0, loc2=0):
    population_n_11 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_11 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_11, population_a_11
population_n_11, population_a_11 = gendata_11(loc1=INTC_11_mean, loc2=AAPL_11_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_11)), population_n_11, label="population1")
plt.scatter(range(len(population_a_11)), population_a_11, label="population2")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_11, 10, density=True, alpha=0.5, label="population1")
plt.hist(population_a_11, 10, density=True, alpha=0.5, label="population2")
plt.axvline(population_n_11.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_11.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a230faba8>




![png](output_182_1.png)



```python
stats.ttest_ind(population_n_11, population_a_11, equal_var=False)
```




    Ttest_indResult(statistic=0.2760088388838162, pvalue=0.7826557761493751)




```python
def gendata_12(loc1=0, loc2=0):
    population_n_12 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_12 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_12, population_a_12
population_n_12, population_a_12 = gendata_12(loc1=INTC_12_mean, loc2=AAPL_12_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_12)), population_n_12, label="population1")
plt.scatter(range(len(population_a_12)), population_a_12, label="population2")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_12, 10, density=True, alpha=0.5, label="population1")
plt.hist(population_a_12, 10, density=True, alpha=0.5, label="population2")
plt.axvline(population_n_12.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_12.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a2327f080>




![png](output_184_1.png)



```python
stats.ttest_ind(population_n_12, population_a_12, equal_var=False)
```




    Ttest_indResult(statistic=0.8248993298331925, pvalue=0.4098236872408483)




```python
def gendata_13(loc1=0, loc2=0):
    population_n_13 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_13 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_13, population_a_13
population_n_13, population_a_13 = gendata_13(loc1=INTC_13_mean, loc2=AAPL_13_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_13)), population_n_13, label="population1")
plt.scatter(range(len(population_a_13)), population_a_13, label="population2")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_13, 10, density=True, alpha=0.5, label="population1")
plt.hist(population_a_13, 10, density=True, alpha=0.5, label="population2")
plt.axvline(population_n_13.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_13.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a233ff4a8>




![png](output_186_1.png)



```python
stats.ttest_ind(population_n_13, population_a_13, equal_var=False)
```




    Ttest_indResult(statistic=-0.059718483889969455, pvalue=0.9524038063950677)




```python
def gendata_14(loc1=0, loc2=0):
    population_n_14 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_14 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_14, population_a_14
population_n_14, population_a_14 = gendata_14(loc1=INTC_14_mean, loc2=AAPL_14_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_14)), population_n_14, label="population1")
plt.scatter(range(len(population_a_14)), population_a_14, label="population2")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_14, 10, density=True, alpha=0.5, label="population1")
plt.hist(population_a_14, 10, density=True, alpha=0.5, label="population2")
plt.axvline(population_n_14.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_14.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a2357e908>




![png](output_188_1.png)



```python
stats.ttest_ind(population_n_14, population_a_14, equal_var=False)
```




    Ttest_indResult(statistic=0.9178115040742434, pvalue=0.35916183960261727)




```python
def gendata_15(loc1=0, loc2=0):
    population_n_15 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_15 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_15, population_a_15
population_n_15, population_a_15 = gendata_15(loc1=INTC_15_mean, loc2=AAPL_15_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_15)), population_n_15, label="population1")
plt.scatter(range(len(population_a_15)), population_a_15, label="population2")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_15, 10, density=True, alpha=0.5, label="population1")
plt.hist(population_a_15, 10, density=True, alpha=0.5, label="population2")
plt.axvline(population_n_15.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_15.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a236f7d68>




![png](output_190_1.png)



```python
stats.ttest_ind(population_n_15, population_a_15, equal_var=False)
```




    Ttest_indResult(statistic=-0.05984596583678021, pvalue=0.9523023234393042)




```python
def gendata_16(loc1=0, loc2=0):
    population_n_16 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_16 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_16, population_a_16
population_n_16, population_a_16 = gendata_16(loc1=INTC_16_mean, loc2=AAPL_16_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_16)), population_n_16, label="population1")
plt.scatter(range(len(population_a_16)), population_a_16, label="population2")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_16, 10, density=True, alpha=0.5, label="population1")
plt.hist(population_a_16, 10, density=True, alpha=0.5, label="population2")
plt.axvline(population_n_16.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_16.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a23767080>




![png](output_192_1.png)



```python
stats.ttest_ind(population_n_16, population_a_16, equal_var=False)
```




    Ttest_indResult(statistic=0.4070092731284522, pvalue=0.6841760527981722)




```python
def gendata_17(loc1=0, loc2=0):
    population_n_17 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_17 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_17, population_a_17
population_n_17, population_a_17 = gendata_17(loc1=INTC_17_mean, loc2=AAPL_17_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_17)), population_n_17, label="population1")
plt.scatter(range(len(population_a_17)), population_a_17, label="population2")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_17, 10, density=True, alpha=0.5, label="population1")
plt.hist(population_a_17, 10, density=True, alpha=0.5, label="population2")
plt.axvline(population_n_17.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_17.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a23a014e0>




![png](output_194_1.png)



```python
stats.ttest_ind(population_n_17, population_a_17, equal_var=False)
```




    Ttest_indResult(statistic=1.928615100334913, pvalue=0.05434670484113653)




```python
critical_value = stats.chi2.ppf(q = 0.95, df = 249)
critical_value
```




    286.807794444232




```python
stats.chisquare(df_INTC_07['Diff'],)
```




    Power_divergenceResult(statistic=nan, pvalue=nan)




```python
data1 = pd.DataFrame(df_INTC_07['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_INTC_08['Diff']).assign(Location=2)
data3 = pd.DataFrame(df_INTC_09['Diff']).assign(Location=3)



cdf = pd.concat([data1, data2, data3])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.072169
    2         1   Diff  0.050519
    3         1   Diff  0.447450
    4         1   Diff -0.101037



![png](output_198_1.png)



```python
data4 = pd.DataFrame(df_INTC_10['Diff']).assign(Location=4)
data5 = pd.DataFrame(df_INTC_11['Diff']).assign(Location=5)
data6 = pd.DataFrame(df_INTC_12['Diff']).assign(Location=6)

cdf = pd.concat([data4, data5, data6])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         4   Diff       NaN
    1         4   Diff -0.007908
    2         4   Diff -0.063266
    3         4   Diff -0.047450
    4         4   Diff -0.031633



![png](output_199_1.png)



```python
data7 = pd.DataFrame(df_INTC_13['Diff']).assign(Location=7)
data8 = pd.DataFrame(df_INTC_14['Diff']).assign(Location=8)
data9 = pd.DataFrame(df_INTC_15['Diff']).assign(Location=9)

cdf = pd.concat([data7, data8, data9])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         7   Diff       NaN
    1         7   Diff -0.092434
    2         7   Diff -0.220081
    3         7   Diff  0.088032
    4         7   Diff -0.237687



![png](output_200_1.png)



```python
data10 = pd.DataFrame(df_INTC_16['Diff']).assign(Location=10)
data11 = pd.DataFrame(df_INTC_17['Diff']).assign(Location=11)


cdf = pd.concat([data10, data11])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0        10   Diff       NaN
    1        10   Diff  0.377127
    2        10   Diff -0.029010
    3        10   Diff  0.425477
    4        10   Diff -0.096699



![png](output_201_1.png)



```python
data1 = pd.DataFrame(df_AAPL_07['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_08['Diff']).assign(Location=2)
data3 = pd.DataFrame(df_AAPL_09['Diff']).assign(Location=3)



cdf = pd.concat([data1, data2, data3])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.224899
    2         1   Diff -0.161928
    3         1   Diff  0.048835
    4         1   Diff -0.019277



![png](output_202_1.png)



```python
data4 = pd.DataFrame(df_AAPL_10['Diff']).assign(Location=4)
data5 = pd.DataFrame(df_AAPL_11['Diff']).assign(Location=5)
data6 = pd.DataFrame(df_AAPL_12['Diff']).assign(Location=6)

cdf = pd.concat([data4, data5, data6])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         4   Diff       NaN
    1         4   Diff  0.141365
    2         4   Diff  0.209478
    3         4   Diff  0.023133
    4         4   Diff -0.101526



![png](output_203_1.png)



```python
data7 = pd.DataFrame(df_AAPL_13['Diff']).assign(Location=7)
data8 = pd.DataFrame(df_AAPL_14['Diff']).assign(Location=8)
data9 = pd.DataFrame(df_AAPL_15['Diff']).assign(Location=9)

cdf = pd.concat([data7, data8, data9])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         7   Diff       NaN
    1         7   Diff -0.863996
    2         7   Diff  0.740378
    3         7   Diff  0.506435
    4         7   Diff  0.501118



![png](output_204_1.png)



```python
data10 = pd.DataFrame(df_AAPL_16['Diff']).assign(Location=10)
data11 = pd.DataFrame(df_AAPL_17['Diff']).assign(Location=11)


cdf = pd.concat([data10, data11])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0        10   Diff       NaN
    1        10   Diff  0.898760
    2        10   Diff  0.029629
    3        10   Diff  0.493824
    4        10   Diff -0.730860



![png](output_205_1.png)



```python
#==================================================================================
```


```python
data1 = pd.DataFrame(df_INTC_07['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_07['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.072169
    2         1   Diff  0.050519
    3         1   Diff  0.447450
    4         1   Diff -0.101037



![png](output_207_1.png)



```python
data1 = pd.DataFrame(df_INTC_08['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_08['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.022258
    2         1   Diff -0.415473
    3         1   Diff  0.037096
    4         1   Diff  0.037096



![png](output_208_1.png)



```python
data1 = pd.DataFrame(df_INTC_09['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_09['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.145775
    2         1   Diff -0.144241
    3         1   Diff -0.078258
    4         1   Diff  0.023017



![png](output_209_1.png)



```python
data1 = pd.DataFrame(df_INTC_10['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_10['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff -0.007908
    2         1   Diff -0.063266
    3         1   Diff -0.047450
    4         1   Diff -0.031633



![png](output_210_1.png)



```python
data1 = pd.DataFrame(df_INTC_11['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_11['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.245519
    2         1   Diff -0.265979
    3         1   Diff  0.274163
    4         1   Diff -0.130943



![png](output_211_1.png)



```python
data1 = pd.DataFrame(df_INTC_12['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_12['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff -0.330193
    2         1   Diff  0.237062
    3         1   Diff  0.118531
    4         1   Diff -0.008466



![png](output_212_1.png)



```python
data1 = pd.DataFrame(df_INTC_12['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_12['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff -0.330193
    2         1   Diff  0.237062
    3         1   Diff  0.118531
    4         1   Diff -0.008466



![png](output_213_1.png)



```python
data1 = pd.DataFrame(df_INTC_13['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_13['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff -0.092434
    2         1   Diff -0.220081
    3         1   Diff  0.088032
    4         1   Diff -0.237687



![png](output_214_1.png)



```python
data1 = pd.DataFrame(df_INTC_14['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_14['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.427016
    2         1   Diff  0.381589
    3         1   Diff  0.336162
    4         1   Diff -0.099940



![png](output_215_1.png)



```python
data1 = pd.DataFrame(df_INTC_15['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_15['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.505381
    2         1   Diff  0.421151
    3         1   Diff -0.477305
    4         1   Diff  0.046795



![png](output_216_1.png)



```python
data1 = pd.DataFrame(df_INTC_16['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_16['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.377127
    2         1   Diff -0.029010
    3         1   Diff  0.425477
    4         1   Diff -0.096699



![png](output_217_1.png)



```python
data1 = pd.DataFrame(df_INTC_17['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_17['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter  value
    0         1   Diff    NaN
    1         1   Diff   0.06
    2         1   Diff  -0.11
    3         1   Diff  -0.03
    4         1   Diff   0.62



![png](output_218_1.png)



```python
#chi square expected should be other stock mean expected returns for year to state if correlation is statistically significant??
```


```python
#for hte multivariate dendrogram heat map, wouldnt PCA reduce the amount of data needed to be shown?
```


```python
#for the ggplot of carats vs price would there be a  better way to represent the data rather than a really densly packed scatter plot?

```
