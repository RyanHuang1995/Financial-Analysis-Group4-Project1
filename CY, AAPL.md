

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
df_CY_07 = web.DataReader('CY','quandl', start_07,end_07)
```


```python
df_CY_08 = web.DataReader('CY','quandl', start_08,end_08)
```


```python
df_CY_09 = web.DataReader('CY','quandl', start_09,end_09)
```


```python
df_CY_10 = web.DataReader('CY','quandl', start_10,end_10)
```


```python
df_CY_11 = web.DataReader('CY','quandl', start_11,end_11)
```


```python
df_CY_12 = web.DataReader('CY','quandl', start_12,end_12)
```


```python
df_CY_13 = web.DataReader('CY','quandl', start_13,end_13)
```


```python
df_CY_14 = web.DataReader('CY','quandl', start_14,end_14)
```


```python
df_CY_15 = web.DataReader('CY','quandl', start_15,end_15)
```


```python
df_CY_16 = web.DataReader('CY','quandl', start_16,end_16)
```


```python
df_CY_17 = web.DataReader('CY','quandl', start_17,end_17)
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
plt.plot(df_CY_07.index,df_CY_07['AdjClose'], c='r')
plt.plot(df_AAPL_07.index,df_AAPL_07['AdjClose'], c='g')
plt.show()
```


![png](output_68_0.png)



```python
plt.plot(df_CY_08.index,df_CY_08['AdjClose'], c='r')
plt.plot(df_AAPL_08.index,df_AAPL_08['AdjClose'], c='g')
plt.show()
```


![png](output_69_0.png)



```python
plt.plot(df_CY_09.index,df_CY_09['AdjClose'], c='r')
plt.plot(df_AAPL_09.index,df_AAPL_09['AdjClose'], c='g')
plt.show()
```


![png](output_70_0.png)



```python
plt.plot(df_CY_10.index,df_CY_10['AdjClose'], c='r')
plt.plot(df_AAPL_10.index,df_AAPL_10['AdjClose'], c='g')
plt.show()
```


![png](output_71_0.png)



```python
plt.plot(df_CY_11.index,df_CY_11['AdjClose'], c='r')
plt.plot(df_AAPL_11.index,df_AAPL_11['AdjClose'], c='g')
plt.show()
```


![png](output_72_0.png)



```python
plt.plot(df_CY_12.index,df_CY_12['AdjClose'], c='r')
plt.plot(df_AAPL_12.index,df_AAPL_12['AdjClose'], c='g')
plt.show()
```


![png](output_73_0.png)



```python
plt.plot(df_CY_13.index,df_CY_13['AdjClose'], c='r')
plt.plot(df_AAPL_13.index,df_AAPL_13['AdjClose'], c='g')
plt.show()
```


![png](output_74_0.png)



```python
plt.plot(df_CY_14.index,df_CY_14['AdjClose'], c='r')
plt.plot(df_AAPL_14.index,df_AAPL_14['AdjClose'], c='g')
plt.show()
```


![png](output_75_0.png)



```python
plt.plot(df_CY_15.index,df_CY_15['AdjClose'], c='r')
plt.plot(df_AAPL_15.index,df_AAPL_15['AdjClose'], c='g')
plt.show()
```


![png](output_76_0.png)



```python
plt.plot(df_CY_16.index,df_CY_16['AdjClose'], c='r')
plt.plot(df_AAPL_16.index,df_AAPL_16['AdjClose'], c='g')
plt.show()
```


![png](output_77_0.png)



```python
plt.plot(df_CY_17.index,df_CY_17['AdjClose'], c='r')
plt.plot(df_AAPL_17.index,df_AAPL_17['AdjClose'], c='g')
plt.show()
```


![png](output_78_0.png)



```python
df_CY_07.head()
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
      <td>36.68</td>
      <td>37.0799</td>
      <td>35.90</td>
      <td>36.03</td>
      <td>10833800.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>6.972267</td>
      <td>7.048282</td>
      <td>6.824002</td>
      <td>6.848713</td>
      <td>10833800.0</td>
    </tr>
    <tr>
      <th>2007-12-28</th>
      <td>37.62</td>
      <td>37.7800</td>
      <td>36.54</td>
      <td>36.80</td>
      <td>10789900.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>7.150946</td>
      <td>7.181359</td>
      <td>6.945656</td>
      <td>6.995078</td>
      <td>10789900.0</td>
    </tr>
    <tr>
      <th>2007-12-27</th>
      <td>38.21</td>
      <td>38.8000</td>
      <td>37.20</td>
      <td>37.36</td>
      <td>14505700.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>7.263095</td>
      <td>7.375245</td>
      <td>7.071111</td>
      <td>7.101524</td>
      <td>14505700.0</td>
    </tr>
    <tr>
      <th>2007-12-26</th>
      <td>38.74</td>
      <td>38.9500</td>
      <td>37.59</td>
      <td>38.74</td>
      <td>17807000.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>7.363840</td>
      <td>7.403757</td>
      <td>7.145244</td>
      <td>7.363840</td>
      <td>17807000.0</td>
    </tr>
    <tr>
      <th>2007-12-24</th>
      <td>35.96</td>
      <td>38.0000</td>
      <td>35.96</td>
      <td>37.91</td>
      <td>11622300.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>6.835407</td>
      <td>7.223178</td>
      <td>6.835407</td>
      <td>7.206070</td>
      <td>11622300.0</td>
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
df_CY_07['Diff'] = df_CY_07['AdjClose'] - df_CY_07['AdjClose'].shift(1)
df_CY_08['Diff'] = df_CY_08['AdjClose'] - df_CY_08['AdjClose'].shift(1)
df_CY_09['Diff'] = df_CY_09['AdjClose'] - df_CY_09['AdjClose'].shift(1)
df_CY_10['Diff'] = df_CY_10['AdjClose'] - df_CY_10['AdjClose'].shift(1)
df_CY_11['Diff'] = df_CY_11['AdjClose'] - df_CY_11['AdjClose'].shift(1)
df_CY_12['Diff'] = df_CY_12['AdjClose'] - df_CY_12['AdjClose'].shift(1)
df_CY_13['Diff'] = df_CY_13['AdjClose'] - df_CY_13['AdjClose'].shift(1)
df_CY_14['Diff'] = df_CY_14['AdjClose'] - df_CY_14['AdjClose'].shift(1)
df_CY_15['Diff'] = df_CY_15['AdjClose'] - df_CY_15['AdjClose'].shift(1)
df_CY_16['Diff'] = df_CY_16['AdjClose'] - df_CY_16['AdjClose'].shift(1)
df_CY_17['Diff'] = df_CY_17['AdjClose'] - df_CY_17['AdjClose'].shift(1)
df_CY_07.head()
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
      <td>36.68</td>
      <td>37.0799</td>
      <td>35.90</td>
      <td>36.03</td>
      <td>10833800.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>6.972267</td>
      <td>7.048282</td>
      <td>6.824002</td>
      <td>6.848713</td>
      <td>10833800.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2007-12-28</th>
      <td>37.62</td>
      <td>37.7800</td>
      <td>36.54</td>
      <td>36.80</td>
      <td>10789900.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>7.150946</td>
      <td>7.181359</td>
      <td>6.945656</td>
      <td>6.995078</td>
      <td>10789900.0</td>
      <td>0.146364</td>
    </tr>
    <tr>
      <th>2007-12-27</th>
      <td>38.21</td>
      <td>38.8000</td>
      <td>37.20</td>
      <td>37.36</td>
      <td>14505700.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>7.263095</td>
      <td>7.375245</td>
      <td>7.071111</td>
      <td>7.101524</td>
      <td>14505700.0</td>
      <td>0.106447</td>
    </tr>
    <tr>
      <th>2007-12-26</th>
      <td>38.74</td>
      <td>38.9500</td>
      <td>37.59</td>
      <td>38.74</td>
      <td>17807000.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>7.363840</td>
      <td>7.403757</td>
      <td>7.145244</td>
      <td>7.363840</td>
      <td>17807000.0</td>
      <td>0.262315</td>
    </tr>
    <tr>
      <th>2007-12-24</th>
      <td>35.96</td>
      <td>38.0000</td>
      <td>35.96</td>
      <td>37.91</td>
      <td>11622300.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>6.835407</td>
      <td>7.223178</td>
      <td>6.835407</td>
      <td>7.206070</td>
      <td>11622300.0</td>
      <td>-0.157769</td>
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
df_CY_17.drop(pd.to_datetime('2017-08-07'), inplace = True)
df_CY_17
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
      <td>15.35</td>
      <td>15.3850</td>
      <td>15.2050</td>
      <td>15.240</td>
      <td>3210477.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.350000</td>
      <td>15.385000</td>
      <td>15.205000</td>
      <td>15.240000</td>
      <td>3210477.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2017-12-28</th>
      <td>15.25</td>
      <td>15.3700</td>
      <td>15.2000</td>
      <td>15.290</td>
      <td>3090414.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.250000</td>
      <td>15.370000</td>
      <td>15.200000</td>
      <td>15.290000</td>
      <td>3090414.0</td>
      <td>0.050000</td>
    </tr>
    <tr>
      <th>2017-12-27</th>
      <td>15.22</td>
      <td>15.2600</td>
      <td>15.1550</td>
      <td>15.220</td>
      <td>3018237.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.220000</td>
      <td>15.260000</td>
      <td>15.155000</td>
      <td>15.220000</td>
      <td>3018237.0</td>
      <td>-0.070000</td>
    </tr>
    <tr>
      <th>2017-12-26</th>
      <td>15.21</td>
      <td>15.3700</td>
      <td>15.0400</td>
      <td>15.330</td>
      <td>4159798.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.210000</td>
      <td>15.370000</td>
      <td>15.040000</td>
      <td>15.330000</td>
      <td>4159798.0</td>
      <td>0.110000</td>
    </tr>
    <tr>
      <th>2017-12-22</th>
      <td>15.31</td>
      <td>15.5100</td>
      <td>15.2600</td>
      <td>15.310</td>
      <td>7292003.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.310000</td>
      <td>15.510000</td>
      <td>15.260000</td>
      <td>15.310000</td>
      <td>7292003.0</td>
      <td>-0.020000</td>
    </tr>
    <tr>
      <th>2017-12-21</th>
      <td>15.87</td>
      <td>15.8900</td>
      <td>15.3600</td>
      <td>15.380</td>
      <td>6560836.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.870000</td>
      <td>15.890000</td>
      <td>15.360000</td>
      <td>15.380000</td>
      <td>6560836.0</td>
      <td>0.070000</td>
    </tr>
    <tr>
      <th>2017-12-20</th>
      <td>15.95</td>
      <td>15.9500</td>
      <td>15.6850</td>
      <td>15.830</td>
      <td>4508326.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.950000</td>
      <td>15.950000</td>
      <td>15.685000</td>
      <td>15.830000</td>
      <td>4508326.0</td>
      <td>0.450000</td>
    </tr>
    <tr>
      <th>2017-12-19</th>
      <td>15.69</td>
      <td>15.9500</td>
      <td>15.6800</td>
      <td>15.760</td>
      <td>6531692.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.690000</td>
      <td>15.950000</td>
      <td>15.680000</td>
      <td>15.760000</td>
      <td>6531692.0</td>
      <td>-0.070000</td>
    </tr>
    <tr>
      <th>2017-12-18</th>
      <td>15.39</td>
      <td>15.6200</td>
      <td>15.3100</td>
      <td>15.610</td>
      <td>8562432.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.390000</td>
      <td>15.620000</td>
      <td>15.310000</td>
      <td>15.610000</td>
      <td>8562432.0</td>
      <td>-0.150000</td>
    </tr>
    <tr>
      <th>2017-12-15</th>
      <td>15.05</td>
      <td>15.3600</td>
      <td>14.8800</td>
      <td>15.240</td>
      <td>7005546.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.050000</td>
      <td>15.360000</td>
      <td>14.880000</td>
      <td>15.240000</td>
      <td>7005546.0</td>
      <td>-0.370000</td>
    </tr>
    <tr>
      <th>2017-12-14</th>
      <td>15.25</td>
      <td>15.3250</td>
      <td>15.0400</td>
      <td>15.040</td>
      <td>3796409.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.250000</td>
      <td>15.325000</td>
      <td>15.040000</td>
      <td>15.040000</td>
      <td>3796409.0</td>
      <td>-0.200000</td>
    </tr>
    <tr>
      <th>2017-12-13</th>
      <td>15.34</td>
      <td>15.4463</td>
      <td>15.2200</td>
      <td>15.250</td>
      <td>5890138.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.340000</td>
      <td>15.446300</td>
      <td>15.220000</td>
      <td>15.250000</td>
      <td>5890138.0</td>
      <td>0.210000</td>
    </tr>
    <tr>
      <th>2017-12-12</th>
      <td>15.35</td>
      <td>15.6100</td>
      <td>15.2300</td>
      <td>15.240</td>
      <td>5493738.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.350000</td>
      <td>15.610000</td>
      <td>15.230000</td>
      <td>15.240000</td>
      <td>5493738.0</td>
      <td>-0.010000</td>
    </tr>
    <tr>
      <th>2017-12-11</th>
      <td>15.32</td>
      <td>15.5200</td>
      <td>15.2450</td>
      <td>15.420</td>
      <td>3660563.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.320000</td>
      <td>15.520000</td>
      <td>15.245000</td>
      <td>15.420000</td>
      <td>3660563.0</td>
      <td>0.180000</td>
    </tr>
    <tr>
      <th>2017-12-08</th>
      <td>15.55</td>
      <td>15.6200</td>
      <td>15.3100</td>
      <td>15.320</td>
      <td>5818687.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.550000</td>
      <td>15.620000</td>
      <td>15.310000</td>
      <td>15.320000</td>
      <td>5818687.0</td>
      <td>-0.100000</td>
    </tr>
    <tr>
      <th>2017-12-07</th>
      <td>15.04</td>
      <td>15.3500</td>
      <td>14.9000</td>
      <td>15.320</td>
      <td>9117967.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.040000</td>
      <td>15.350000</td>
      <td>14.900000</td>
      <td>15.320000</td>
      <td>9117967.0</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2017-12-06</th>
      <td>14.70</td>
      <td>14.9400</td>
      <td>14.5500</td>
      <td>14.880</td>
      <td>4888059.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.700000</td>
      <td>14.940000</td>
      <td>14.550000</td>
      <td>14.880000</td>
      <td>4888059.0</td>
      <td>-0.440000</td>
    </tr>
    <tr>
      <th>2017-12-05</th>
      <td>14.76</td>
      <td>15.1200</td>
      <td>14.6400</td>
      <td>14.780</td>
      <td>6386989.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.760000</td>
      <td>15.120000</td>
      <td>14.640000</td>
      <td>14.780000</td>
      <td>6386989.0</td>
      <td>-0.100000</td>
    </tr>
    <tr>
      <th>2017-12-04</th>
      <td>15.36</td>
      <td>15.4800</td>
      <td>14.7400</td>
      <td>14.760</td>
      <td>7090193.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.360000</td>
      <td>15.480000</td>
      <td>14.740000</td>
      <td>14.760000</td>
      <td>7090193.0</td>
      <td>-0.020000</td>
    </tr>
    <tr>
      <th>2017-12-01</th>
      <td>15.68</td>
      <td>15.8100</td>
      <td>14.7400</td>
      <td>15.190</td>
      <td>16504514.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.680000</td>
      <td>15.810000</td>
      <td>14.740000</td>
      <td>15.190000</td>
      <td>16504514.0</td>
      <td>0.430000</td>
    </tr>
    <tr>
      <th>2017-11-30</th>
      <td>15.93</td>
      <td>16.1250</td>
      <td>15.7800</td>
      <td>16.010</td>
      <td>10008577.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.930000</td>
      <td>16.125000</td>
      <td>15.780000</td>
      <td>16.010000</td>
      <td>10008577.0</td>
      <td>0.820000</td>
    </tr>
    <tr>
      <th>2017-11-29</th>
      <td>16.84</td>
      <td>16.9350</td>
      <td>15.6200</td>
      <td>15.690</td>
      <td>13092025.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>16.840000</td>
      <td>16.935000</td>
      <td>15.620000</td>
      <td>15.690000</td>
      <td>13092025.0</td>
      <td>-0.320000</td>
    </tr>
    <tr>
      <th>2017-11-28</th>
      <td>17.00</td>
      <td>17.0750</td>
      <td>16.7900</td>
      <td>16.870</td>
      <td>3622500.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>17.000000</td>
      <td>17.075000</td>
      <td>16.790000</td>
      <td>16.870000</td>
      <td>3622500.0</td>
      <td>1.180000</td>
    </tr>
    <tr>
      <th>2017-11-27</th>
      <td>17.26</td>
      <td>17.3250</td>
      <td>16.9300</td>
      <td>16.950</td>
      <td>5691743.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>17.260000</td>
      <td>17.325000</td>
      <td>16.930000</td>
      <td>16.950000</td>
      <td>5691743.0</td>
      <td>0.080000</td>
    </tr>
    <tr>
      <th>2017-11-24</th>
      <td>17.24</td>
      <td>17.4000</td>
      <td>17.1900</td>
      <td>17.385</td>
      <td>1911007.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>17.240000</td>
      <td>17.400000</td>
      <td>17.190000</td>
      <td>17.385000</td>
      <td>1911007.0</td>
      <td>0.435000</td>
    </tr>
    <tr>
      <th>2017-11-22</th>
      <td>17.36</td>
      <td>17.3700</td>
      <td>17.1500</td>
      <td>17.180</td>
      <td>3696811.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>17.360000</td>
      <td>17.370000</td>
      <td>17.150000</td>
      <td>17.180000</td>
      <td>3696811.0</td>
      <td>-0.205000</td>
    </tr>
    <tr>
      <th>2017-11-21</th>
      <td>17.17</td>
      <td>17.4200</td>
      <td>17.1500</td>
      <td>17.330</td>
      <td>6030624.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>17.170000</td>
      <td>17.420000</td>
      <td>17.150000</td>
      <td>17.330000</td>
      <td>6030624.0</td>
      <td>0.150000</td>
    </tr>
    <tr>
      <th>2017-11-20</th>
      <td>16.80</td>
      <td>17.0900</td>
      <td>16.7500</td>
      <td>17.070</td>
      <td>4877950.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>16.800000</td>
      <td>17.090000</td>
      <td>16.750000</td>
      <td>17.070000</td>
      <td>4877950.0</td>
      <td>-0.260000</td>
    </tr>
    <tr>
      <th>2017-11-17</th>
      <td>16.74</td>
      <td>16.8400</td>
      <td>16.5950</td>
      <td>16.610</td>
      <td>5034900.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>16.740000</td>
      <td>16.840000</td>
      <td>16.595000</td>
      <td>16.610000</td>
      <td>5034900.0</td>
      <td>-0.460000</td>
    </tr>
    <tr>
      <th>2017-11-16</th>
      <td>16.49</td>
      <td>16.7970</td>
      <td>16.4100</td>
      <td>16.610</td>
      <td>6272735.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>16.490000</td>
      <td>16.797000</td>
      <td>16.410000</td>
      <td>16.610000</td>
      <td>6272735.0</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2017-11-15</th>
      <td>16.53</td>
      <td>16.6700</td>
      <td>16.3300</td>
      <td>16.360</td>
      <td>5976340.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>16.530000</td>
      <td>16.670000</td>
      <td>16.330000</td>
      <td>16.360000</td>
      <td>5976340.0</td>
      <td>-0.250000</td>
    </tr>
    <tr>
      <th>2017-11-14</th>
      <td>16.85</td>
      <td>17.1000</td>
      <td>16.7500</td>
      <td>16.780</td>
      <td>7430684.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>16.850000</td>
      <td>17.100000</td>
      <td>16.750000</td>
      <td>16.780000</td>
      <td>7430684.0</td>
      <td>0.420000</td>
    </tr>
    <tr>
      <th>2017-11-13</th>
      <td>16.93</td>
      <td>17.0100</td>
      <td>16.8300</td>
      <td>16.920</td>
      <td>5581899.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>16.930000</td>
      <td>17.010000</td>
      <td>16.830000</td>
      <td>16.920000</td>
      <td>5581899.0</td>
      <td>0.140000</td>
    </tr>
    <tr>
      <th>2017-11-10</th>
      <td>16.93</td>
      <td>17.1500</td>
      <td>16.8350</td>
      <td>16.970</td>
      <td>10404610.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>16.930000</td>
      <td>17.150000</td>
      <td>16.835000</td>
      <td>16.970000</td>
      <td>10404610.0</td>
      <td>0.050000</td>
    </tr>
    <tr>
      <th>2017-11-09</th>
      <td>16.76</td>
      <td>16.9150</td>
      <td>16.5500</td>
      <td>16.730</td>
      <td>5698748.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>16.760000</td>
      <td>16.915000</td>
      <td>16.550000</td>
      <td>16.730000</td>
      <td>5698748.0</td>
      <td>-0.240000</td>
    </tr>
    <tr>
      <th>2017-11-07</th>
      <td>16.45</td>
      <td>16.7700</td>
      <td>16.4400</td>
      <td>16.690</td>
      <td>5996314.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>16.450000</td>
      <td>16.770000</td>
      <td>16.440000</td>
      <td>16.690000</td>
      <td>5996314.0</td>
      <td>-0.040000</td>
    </tr>
    <tr>
      <th>2017-11-06</th>
      <td>16.29</td>
      <td>16.5100</td>
      <td>16.1839</td>
      <td>16.510</td>
      <td>6615985.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>16.290000</td>
      <td>16.510000</td>
      <td>16.183900</td>
      <td>16.510000</td>
      <td>6615985.0</td>
      <td>-0.180000</td>
    </tr>
    <tr>
      <th>2017-11-03</th>
      <td>15.87</td>
      <td>16.1000</td>
      <td>15.7799</td>
      <td>16.100</td>
      <td>5123729.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.870000</td>
      <td>16.100000</td>
      <td>15.779900</td>
      <td>16.100000</td>
      <td>5123729.0</td>
      <td>-0.410000</td>
    </tr>
    <tr>
      <th>2017-11-02</th>
      <td>15.92</td>
      <td>16.0900</td>
      <td>15.8350</td>
      <td>15.930</td>
      <td>10853476.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.920000</td>
      <td>16.090000</td>
      <td>15.835000</td>
      <td>15.930000</td>
      <td>10853476.0</td>
      <td>-0.170000</td>
    </tr>
    <tr>
      <th>2017-11-01</th>
      <td>15.92</td>
      <td>15.9500</td>
      <td>15.3000</td>
      <td>15.570</td>
      <td>7811266.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.920000</td>
      <td>15.950000</td>
      <td>15.300000</td>
      <td>15.570000</td>
      <td>7811266.0</td>
      <td>-0.360000</td>
    </tr>
    <tr>
      <th>2017-10-31</th>
      <td>15.90</td>
      <td>16.1000</td>
      <td>15.7400</td>
      <td>15.860</td>
      <td>7108183.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.900000</td>
      <td>16.100000</td>
      <td>15.740000</td>
      <td>15.860000</td>
      <td>7108183.0</td>
      <td>0.290000</td>
    </tr>
    <tr>
      <th>2017-10-30</th>
      <td>16.06</td>
      <td>16.3400</td>
      <td>16.0400</td>
      <td>16.310</td>
      <td>5597075.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>16.060000</td>
      <td>16.340000</td>
      <td>16.040000</td>
      <td>16.310000</td>
      <td>5597075.0</td>
      <td>0.450000</td>
    </tr>
    <tr>
      <th>2017-10-27</th>
      <td>16.00</td>
      <td>16.2400</td>
      <td>15.8110</td>
      <td>16.120</td>
      <td>10064011.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>16.000000</td>
      <td>16.240000</td>
      <td>15.811000</td>
      <td>16.120000</td>
      <td>10064011.0</td>
      <td>-0.190000</td>
    </tr>
    <tr>
      <th>2017-10-26</th>
      <td>15.70</td>
      <td>15.7800</td>
      <td>15.5100</td>
      <td>15.690</td>
      <td>4015590.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.700000</td>
      <td>15.780000</td>
      <td>15.510000</td>
      <td>15.690000</td>
      <td>4015590.0</td>
      <td>-0.430000</td>
    </tr>
    <tr>
      <th>2017-10-25</th>
      <td>15.78</td>
      <td>15.8100</td>
      <td>15.2900</td>
      <td>15.645</td>
      <td>5406489.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.780000</td>
      <td>15.810000</td>
      <td>15.290000</td>
      <td>15.645000</td>
      <td>5406489.0</td>
      <td>-0.045000</td>
    </tr>
    <tr>
      <th>2017-10-24</th>
      <td>15.90</td>
      <td>15.9900</td>
      <td>15.8400</td>
      <td>15.850</td>
      <td>3232993.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.900000</td>
      <td>15.990000</td>
      <td>15.840000</td>
      <td>15.850000</td>
      <td>3232993.0</td>
      <td>0.205000</td>
    </tr>
    <tr>
      <th>2017-10-23</th>
      <td>15.76</td>
      <td>16.0799</td>
      <td>15.7150</td>
      <td>15.830</td>
      <td>4597587.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.760000</td>
      <td>16.079900</td>
      <td>15.715000</td>
      <td>15.830000</td>
      <td>4597587.0</td>
      <td>-0.020000</td>
    </tr>
    <tr>
      <th>2017-10-20</th>
      <td>15.81</td>
      <td>15.9000</td>
      <td>15.6300</td>
      <td>15.700</td>
      <td>2698543.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.810000</td>
      <td>15.900000</td>
      <td>15.630000</td>
      <td>15.700000</td>
      <td>2698543.0</td>
      <td>-0.130000</td>
    </tr>
    <tr>
      <th>2017-10-19</th>
      <td>15.50</td>
      <td>15.6600</td>
      <td>15.2800</td>
      <td>15.610</td>
      <td>4467309.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.500000</td>
      <td>15.660000</td>
      <td>15.280000</td>
      <td>15.610000</td>
      <td>4467309.0</td>
      <td>-0.090000</td>
    </tr>
    <tr>
      <th>2017-10-18</th>
      <td>15.86</td>
      <td>15.9000</td>
      <td>15.5600</td>
      <td>15.650</td>
      <td>5268925.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.860000</td>
      <td>15.900000</td>
      <td>15.560000</td>
      <td>15.650000</td>
      <td>5268925.0</td>
      <td>0.040000</td>
    </tr>
    <tr>
      <th>2017-10-17</th>
      <td>15.94</td>
      <td>15.9950</td>
      <td>15.8150</td>
      <td>15.860</td>
      <td>2215303.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.940000</td>
      <td>15.995000</td>
      <td>15.815000</td>
      <td>15.860000</td>
      <td>2215303.0</td>
      <td>0.210000</td>
    </tr>
    <tr>
      <th>2017-10-16</th>
      <td>15.85</td>
      <td>15.9350</td>
      <td>15.6839</td>
      <td>15.880</td>
      <td>2486744.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.850000</td>
      <td>15.935000</td>
      <td>15.683900</td>
      <td>15.880000</td>
      <td>2486744.0</td>
      <td>0.020000</td>
    </tr>
    <tr>
      <th>2017-10-13</th>
      <td>15.89</td>
      <td>16.0950</td>
      <td>15.7700</td>
      <td>15.860</td>
      <td>3617017.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.890000</td>
      <td>16.095000</td>
      <td>15.770000</td>
      <td>15.860000</td>
      <td>3617017.0</td>
      <td>-0.020000</td>
    </tr>
    <tr>
      <th>2017-10-12</th>
      <td>15.99</td>
      <td>16.1100</td>
      <td>15.7400</td>
      <td>15.760</td>
      <td>4493795.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.990000</td>
      <td>16.110000</td>
      <td>15.740000</td>
      <td>15.760000</td>
      <td>4493795.0</td>
      <td>-0.100000</td>
    </tr>
    <tr>
      <th>2017-10-11</th>
      <td>15.93</td>
      <td>15.9950</td>
      <td>15.7000</td>
      <td>15.990</td>
      <td>4485311.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.930000</td>
      <td>15.995000</td>
      <td>15.700000</td>
      <td>15.990000</td>
      <td>4485311.0</td>
      <td>0.230000</td>
    </tr>
    <tr>
      <th>2017-10-10</th>
      <td>15.98</td>
      <td>16.0000</td>
      <td>15.7400</td>
      <td>15.940</td>
      <td>6026224.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.980000</td>
      <td>16.000000</td>
      <td>15.740000</td>
      <td>15.940000</td>
      <td>6026224.0</td>
      <td>-0.050000</td>
    </tr>
    <tr>
      <th>2017-10-09</th>
      <td>15.60</td>
      <td>15.7200</td>
      <td>15.4835</td>
      <td>15.530</td>
      <td>3231572.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.600000</td>
      <td>15.720000</td>
      <td>15.483500</td>
      <td>15.530000</td>
      <td>3231572.0</td>
      <td>-0.410000</td>
    </tr>
    <tr>
      <th>2017-10-06</th>
      <td>15.38</td>
      <td>15.6300</td>
      <td>15.3800</td>
      <td>15.510</td>
      <td>3553113.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.380000</td>
      <td>15.630000</td>
      <td>15.380000</td>
      <td>15.510000</td>
      <td>3553113.0</td>
      <td>-0.020000</td>
    </tr>
    <tr>
      <th>2017-10-05</th>
      <td>15.45</td>
      <td>15.5000</td>
      <td>15.2900</td>
      <td>15.480</td>
      <td>2870381.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.450000</td>
      <td>15.500000</td>
      <td>15.290000</td>
      <td>15.480000</td>
      <td>2870381.0</td>
      <td>-0.030000</td>
    </tr>
    <tr>
      <th>2017-10-04</th>
      <td>15.37</td>
      <td>15.4800</td>
      <td>15.2800</td>
      <td>15.410</td>
      <td>3692355.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.370000</td>
      <td>15.480000</td>
      <td>15.280000</td>
      <td>15.410000</td>
      <td>3692355.0</td>
      <td>-0.070000</td>
    </tr>
    <tr>
      <th>2017-10-03</th>
      <td>15.37</td>
      <td>15.4700</td>
      <td>15.1100</td>
      <td>15.420</td>
      <td>5350317.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.370000</td>
      <td>15.470000</td>
      <td>15.110000</td>
      <td>15.420000</td>
      <td>5350317.0</td>
      <td>0.010000</td>
    </tr>
    <tr>
      <th>2017-10-02</th>
      <td>15.05</td>
      <td>15.3200</td>
      <td>14.9950</td>
      <td>15.310</td>
      <td>4674436.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>15.050000</td>
      <td>15.320000</td>
      <td>14.995000</td>
      <td>15.310000</td>
      <td>4674436.0</td>
      <td>-0.110000</td>
    </tr>
    <tr>
      <th>2017-09-29</th>
      <td>14.75</td>
      <td>15.0500</td>
      <td>14.7000</td>
      <td>15.020</td>
      <td>5630336.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.750000</td>
      <td>15.050000</td>
      <td>14.700000</td>
      <td>15.020000</td>
      <td>5630336.0</td>
      <td>-0.290000</td>
    </tr>
    <tr>
      <th>2017-09-28</th>
      <td>14.42</td>
      <td>14.7700</td>
      <td>14.3700</td>
      <td>14.740</td>
      <td>4230191.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.420000</td>
      <td>14.770000</td>
      <td>14.370000</td>
      <td>14.740000</td>
      <td>4230191.0</td>
      <td>-0.280000</td>
    </tr>
    <tr>
      <th>2017-09-27</th>
      <td>14.32</td>
      <td>14.5250</td>
      <td>14.1600</td>
      <td>14.430</td>
      <td>3528346.0</td>
      <td>0.11</td>
      <td>1.0</td>
      <td>14.320000</td>
      <td>14.525000</td>
      <td>14.160000</td>
      <td>14.430000</td>
      <td>3528346.0</td>
      <td>-0.310000</td>
    </tr>
    <tr>
      <th>2017-09-26</th>
      <td>14.28</td>
      <td>14.3250</td>
      <td>14.1400</td>
      <td>14.280</td>
      <td>3171901.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.171967</td>
      <td>14.216627</td>
      <td>14.033026</td>
      <td>14.171967</td>
      <td>3171901.0</td>
      <td>-0.258033</td>
    </tr>
    <tr>
      <th>2017-09-25</th>
      <td>14.35</td>
      <td>14.3953</td>
      <td>14.0500</td>
      <td>14.170</td>
      <td>4779896.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.241437</td>
      <td>14.286395</td>
      <td>13.943707</td>
      <td>14.062799</td>
      <td>4779896.0</td>
      <td>-0.109168</td>
    </tr>
    <tr>
      <th>2017-09-22</th>
      <td>14.15</td>
      <td>14.4800</td>
      <td>14.1007</td>
      <td>14.340</td>
      <td>3427031.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.042950</td>
      <td>14.370454</td>
      <td>13.994023</td>
      <td>14.231513</td>
      <td>3427031.0</td>
      <td>0.168714</td>
    </tr>
    <tr>
      <th>2017-09-21</th>
      <td>14.46</td>
      <td>14.4800</td>
      <td>14.2250</td>
      <td>14.250</td>
      <td>3708030.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.350605</td>
      <td>14.370454</td>
      <td>14.117383</td>
      <td>14.142194</td>
      <td>3708030.0</td>
      <td>-0.089319</td>
    </tr>
    <tr>
      <th>2017-09-20</th>
      <td>14.71</td>
      <td>14.7200</td>
      <td>14.3200</td>
      <td>14.510</td>
      <td>6728891.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.598714</td>
      <td>14.608638</td>
      <td>14.211664</td>
      <td>14.400227</td>
      <td>6728891.0</td>
      <td>0.258033</td>
    </tr>
    <tr>
      <th>2017-09-19</th>
      <td>14.61</td>
      <td>14.7200</td>
      <td>14.3800</td>
      <td>14.690</td>
      <td>5448616.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.499470</td>
      <td>14.608638</td>
      <td>14.271210</td>
      <td>14.578865</td>
      <td>5448616.0</td>
      <td>0.178638</td>
    </tr>
    <tr>
      <th>2017-09-18</th>
      <td>14.43</td>
      <td>14.7900</td>
      <td>14.3800</td>
      <td>14.540</td>
      <td>7570515.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.320832</td>
      <td>14.678109</td>
      <td>14.271210</td>
      <td>14.430000</td>
      <td>7570515.0</td>
      <td>-0.148865</td>
    </tr>
    <tr>
      <th>2017-09-15</th>
      <td>14.35</td>
      <td>14.5100</td>
      <td>14.2650</td>
      <td>14.410</td>
      <td>8639964.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.241437</td>
      <td>14.400227</td>
      <td>14.157080</td>
      <td>14.300983</td>
      <td>8639964.0</td>
      <td>-0.129017</td>
    </tr>
    <tr>
      <th>2017-09-14</th>
      <td>14.10</td>
      <td>14.4300</td>
      <td>14.0200</td>
      <td>14.300</td>
      <td>6880137.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.993329</td>
      <td>14.320832</td>
      <td>13.913934</td>
      <td>14.191816</td>
      <td>6880137.0</td>
      <td>-0.109168</td>
    </tr>
    <tr>
      <th>2017-09-13</th>
      <td>14.11</td>
      <td>14.2500</td>
      <td>13.8550</td>
      <td>14.140</td>
      <td>6604060.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.003253</td>
      <td>14.142194</td>
      <td>13.750182</td>
      <td>14.033026</td>
      <td>6604060.0</td>
      <td>-0.158790</td>
    </tr>
    <tr>
      <th>2017-09-12</th>
      <td>13.85</td>
      <td>14.3500</td>
      <td>13.7700</td>
      <td>14.160</td>
      <td>7025696.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.745220</td>
      <td>14.241437</td>
      <td>13.665825</td>
      <td>14.052875</td>
      <td>7025696.0</td>
      <td>0.019849</td>
    </tr>
    <tr>
      <th>2017-09-11</th>
      <td>13.59</td>
      <td>13.8100</td>
      <td>13.5500</td>
      <td>13.800</td>
      <td>4754701.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.487187</td>
      <td>13.705523</td>
      <td>13.447490</td>
      <td>13.695598</td>
      <td>4754701.0</td>
      <td>-0.357276</td>
    </tr>
    <tr>
      <th>2017-09-08</th>
      <td>13.68</td>
      <td>13.7500</td>
      <td>13.4000</td>
      <td>13.470</td>
      <td>2822401.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.576506</td>
      <td>13.645977</td>
      <td>13.298624</td>
      <td>13.368095</td>
      <td>2822401.0</td>
      <td>-0.327503</td>
    </tr>
    <tr>
      <th>2017-09-07</th>
      <td>13.70</td>
      <td>13.7650</td>
      <td>13.5650</td>
      <td>13.640</td>
      <td>2720756.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.596355</td>
      <td>13.660863</td>
      <td>13.462376</td>
      <td>13.536809</td>
      <td>2720756.0</td>
      <td>0.168714</td>
    </tr>
    <tr>
      <th>2017-09-06</th>
      <td>13.81</td>
      <td>13.8800</td>
      <td>13.6250</td>
      <td>13.710</td>
      <td>2620208.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.705523</td>
      <td>13.774993</td>
      <td>13.521922</td>
      <td>13.606279</td>
      <td>2620208.0</td>
      <td>0.069470</td>
    </tr>
    <tr>
      <th>2017-09-05</th>
      <td>13.81</td>
      <td>13.9100</td>
      <td>13.5700</td>
      <td>13.730</td>
      <td>4087642.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.705523</td>
      <td>13.804766</td>
      <td>13.467338</td>
      <td>13.626128</td>
      <td>4087642.0</td>
      <td>0.019849</td>
    </tr>
    <tr>
      <th>2017-09-01</th>
      <td>13.75</td>
      <td>13.9600</td>
      <td>13.7250</td>
      <td>13.935</td>
      <td>3549189.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.645977</td>
      <td>13.854388</td>
      <td>13.621166</td>
      <td>13.829577</td>
      <td>3549189.0</td>
      <td>0.203449</td>
    </tr>
    <tr>
      <th>2017-08-31</th>
      <td>13.60</td>
      <td>13.7450</td>
      <td>13.5500</td>
      <td>13.690</td>
      <td>3242182.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.497111</td>
      <td>13.641014</td>
      <td>13.447490</td>
      <td>13.586431</td>
      <td>3242182.0</td>
      <td>-0.243146</td>
    </tr>
    <tr>
      <th>2017-08-30</th>
      <td>13.40</td>
      <td>13.6000</td>
      <td>13.3000</td>
      <td>13.580</td>
      <td>4643643.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.298624</td>
      <td>13.497111</td>
      <td>13.199381</td>
      <td>13.477263</td>
      <td>4643643.0</td>
      <td>-0.109168</td>
    </tr>
    <tr>
      <th>2017-08-29</th>
      <td>12.75</td>
      <td>13.4200</td>
      <td>12.5000</td>
      <td>13.370</td>
      <td>13312084.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.653542</td>
      <td>13.318473</td>
      <td>12.405433</td>
      <td>13.268851</td>
      <td>13312084.0</td>
      <td>-0.208411</td>
    </tr>
    <tr>
      <th>2017-08-28</th>
      <td>13.50</td>
      <td>13.5100</td>
      <td>13.2200</td>
      <td>13.280</td>
      <td>7047346.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.397868</td>
      <td>13.407792</td>
      <td>13.119986</td>
      <td>13.179532</td>
      <td>7047346.0</td>
      <td>-0.089319</td>
    </tr>
    <tr>
      <th>2017-08-25</th>
      <td>13.49</td>
      <td>13.5350</td>
      <td>13.2500</td>
      <td>13.400</td>
      <td>4806857.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.387944</td>
      <td>13.432603</td>
      <td>13.149759</td>
      <td>13.298624</td>
      <td>4806857.0</td>
      <td>0.119092</td>
    </tr>
    <tr>
      <th>2017-08-24</th>
      <td>13.45</td>
      <td>13.5950</td>
      <td>13.3300</td>
      <td>13.410</td>
      <td>3888946.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.348246</td>
      <td>13.492149</td>
      <td>13.229154</td>
      <td>13.308549</td>
      <td>3888946.0</td>
      <td>0.009924</td>
    </tr>
    <tr>
      <th>2017-08-23</th>
      <td>13.18</td>
      <td>13.4450</td>
      <td>13.1250</td>
      <td>13.410</td>
      <td>3631764.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.080289</td>
      <td>13.343284</td>
      <td>13.025705</td>
      <td>13.308549</td>
      <td>3631764.0</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2017-08-22</th>
      <td>13.10</td>
      <td>13.4600</td>
      <td>13.0200</td>
      <td>13.320</td>
      <td>6150085.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.000894</td>
      <td>13.358171</td>
      <td>12.921499</td>
      <td>13.219230</td>
      <td>6150085.0</td>
      <td>-0.089319</td>
    </tr>
    <tr>
      <th>2017-08-21</th>
      <td>13.11</td>
      <td>13.1200</td>
      <td>12.8500</td>
      <td>12.940</td>
      <td>4085622.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.010818</td>
      <td>13.020743</td>
      <td>12.752785</td>
      <td>12.842105</td>
      <td>4085622.0</td>
      <td>-0.377125</td>
    </tr>
    <tr>
      <th>2017-08-18</th>
      <td>13.18</td>
      <td>13.2500</td>
      <td>13.0200</td>
      <td>13.120</td>
      <td>5042420.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.080289</td>
      <td>13.149759</td>
      <td>12.921499</td>
      <td>13.020743</td>
      <td>5042420.0</td>
      <td>0.178638</td>
    </tr>
    <tr>
      <th>2017-08-17</th>
      <td>13.64</td>
      <td>13.7382</td>
      <td>13.1100</td>
      <td>13.110</td>
      <td>6153831.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.536809</td>
      <td>13.634266</td>
      <td>13.010818</td>
      <td>13.010818</td>
      <td>6153831.0</td>
      <td>-0.009924</td>
    </tr>
    <tr>
      <th>2017-08-16</th>
      <td>13.56</td>
      <td>13.7900</td>
      <td>13.4300</td>
      <td>13.730</td>
      <td>6791764.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.457414</td>
      <td>13.685674</td>
      <td>13.328398</td>
      <td>13.626128</td>
      <td>6791764.0</td>
      <td>0.615309</td>
    </tr>
    <tr>
      <th>2017-08-15</th>
      <td>13.75</td>
      <td>13.7600</td>
      <td>13.4900</td>
      <td>13.530</td>
      <td>3813639.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.645977</td>
      <td>13.655901</td>
      <td>13.387944</td>
      <td>13.427641</td>
      <td>3813639.0</td>
      <td>-0.198487</td>
    </tr>
    <tr>
      <th>2017-08-14</th>
      <td>13.43</td>
      <td>13.7800</td>
      <td>13.4200</td>
      <td>13.650</td>
      <td>5633403.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.328398</td>
      <td>13.675750</td>
      <td>13.318473</td>
      <td>13.546733</td>
      <td>5633403.0</td>
      <td>0.119092</td>
    </tr>
    <tr>
      <th>2017-08-11</th>
      <td>13.25</td>
      <td>13.3754</td>
      <td>13.1000</td>
      <td>13.280</td>
      <td>5211373.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.149759</td>
      <td>13.274211</td>
      <td>13.000894</td>
      <td>13.179532</td>
      <td>5211373.0</td>
      <td>-0.367201</td>
    </tr>
    <tr>
      <th>2017-08-10</th>
      <td>13.64</td>
      <td>13.6400</td>
      <td>13.1500</td>
      <td>13.220</td>
      <td>8556335.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.536809</td>
      <td>13.536809</td>
      <td>13.050516</td>
      <td>13.119986</td>
      <td>8556335.0</td>
      <td>-0.059546</td>
    </tr>
    <tr>
      <th>2017-08-09</th>
      <td>13.87</td>
      <td>13.9400</td>
      <td>13.6200</td>
      <td>13.730</td>
      <td>4218364.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.765069</td>
      <td>13.834539</td>
      <td>13.516960</td>
      <td>13.626128</td>
      <td>4218364.0</td>
      <td>0.506142</td>
    </tr>
    <tr>
      <th>2017-08-08</th>
      <td>14.17</td>
      <td>14.3900</td>
      <td>13.9750</td>
      <td>14.030</td>
      <td>3901976.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.062799</td>
      <td>14.281135</td>
      <td>13.869274</td>
      <td>13.923858</td>
      <td>3901976.0</td>
      <td>0.297730</td>
    </tr>
    <tr>
      <th>2017-08-04</th>
      <td>14.07</td>
      <td>14.2100</td>
      <td>13.8600</td>
      <td>13.930</td>
      <td>4185008.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.963556</td>
      <td>14.102497</td>
      <td>13.755144</td>
      <td>13.824615</td>
      <td>4185008.0</td>
      <td>-0.267957</td>
    </tr>
    <tr>
      <th>2017-08-03</th>
      <td>14.14</td>
      <td>14.2132</td>
      <td>14.0200</td>
      <td>14.095</td>
      <td>3760052.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.033026</td>
      <td>14.105672</td>
      <td>13.913934</td>
      <td>13.988367</td>
      <td>3760052.0</td>
      <td>0.163752</td>
    </tr>
    <tr>
      <th>2017-08-02</th>
      <td>14.49</td>
      <td>14.5000</td>
      <td>14.0800</td>
      <td>14.160</td>
      <td>4877688.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.380378</td>
      <td>14.390303</td>
      <td>13.973480</td>
      <td>14.052875</td>
      <td>4877688.0</td>
      <td>0.064508</td>
    </tr>
    <tr>
      <th>2017-08-01</th>
      <td>14.21</td>
      <td>14.3900</td>
      <td>14.0300</td>
      <td>14.330</td>
      <td>6785134.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.102497</td>
      <td>14.281135</td>
      <td>13.923858</td>
      <td>14.221589</td>
      <td>6785134.0</td>
      <td>0.168714</td>
    </tr>
    <tr>
      <th>2017-07-31</th>
      <td>14.70</td>
      <td>14.7300</td>
      <td>14.1700</td>
      <td>14.200</td>
      <td>8211368.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.588790</td>
      <td>14.618563</td>
      <td>14.062799</td>
      <td>14.092572</td>
      <td>8211368.0</td>
      <td>-0.129017</td>
    </tr>
    <tr>
      <th>2017-07-28</th>
      <td>14.72</td>
      <td>14.9200</td>
      <td>14.3000</td>
      <td>14.660</td>
      <td>12582885.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.608638</td>
      <td>14.807125</td>
      <td>14.191816</td>
      <td>14.549092</td>
      <td>12582885.0</td>
      <td>0.456520</td>
    </tr>
    <tr>
      <th>2017-07-27</th>
      <td>14.93</td>
      <td>15.1100</td>
      <td>14.2500</td>
      <td>14.640</td>
      <td>10939005.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.817050</td>
      <td>14.995688</td>
      <td>14.142194</td>
      <td>14.529243</td>
      <td>10939005.0</td>
      <td>-0.019849</td>
    </tr>
    <tr>
      <th>2017-07-26</th>
      <td>14.86</td>
      <td>14.8700</td>
      <td>14.5300</td>
      <td>14.760</td>
      <td>6097708.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.747579</td>
      <td>14.757503</td>
      <td>14.420076</td>
      <td>14.648336</td>
      <td>6097708.0</td>
      <td>0.119092</td>
    </tr>
    <tr>
      <th>2017-07-25</th>
      <td>14.44</td>
      <td>14.6700</td>
      <td>14.3200</td>
      <td>14.630</td>
      <td>4966308.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.330757</td>
      <td>14.559017</td>
      <td>14.211664</td>
      <td>14.519319</td>
      <td>4966308.0</td>
      <td>-0.129017</td>
    </tr>
    <tr>
      <th>2017-07-24</th>
      <td>14.65</td>
      <td>14.7700</td>
      <td>14.4800</td>
      <td>14.500</td>
      <td>4898530.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.539168</td>
      <td>14.658260</td>
      <td>14.370454</td>
      <td>14.390303</td>
      <td>4898530.0</td>
      <td>-0.129017</td>
    </tr>
    <tr>
      <th>2017-07-21</th>
      <td>14.75</td>
      <td>14.7525</td>
      <td>14.5050</td>
      <td>14.650</td>
      <td>5841599.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.638411</td>
      <td>14.640892</td>
      <td>14.395265</td>
      <td>14.539168</td>
      <td>5841599.0</td>
      <td>0.148865</td>
    </tr>
    <tr>
      <th>2017-07-20</th>
      <td>14.61</td>
      <td>14.9200</td>
      <td>14.4600</td>
      <td>14.920</td>
      <td>5230038.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.499470</td>
      <td>14.807125</td>
      <td>14.350605</td>
      <td>14.807125</td>
      <td>5230038.0</td>
      <td>0.267957</td>
    </tr>
    <tr>
      <th>2017-07-19</th>
      <td>14.52</td>
      <td>14.7090</td>
      <td>14.4200</td>
      <td>14.590</td>
      <td>7305412.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.410151</td>
      <td>14.597721</td>
      <td>14.310908</td>
      <td>14.479622</td>
      <td>7305412.0</td>
      <td>-0.327503</td>
    </tr>
    <tr>
      <th>2017-07-18</th>
      <td>14.21</td>
      <td>14.4800</td>
      <td>14.1400</td>
      <td>14.440</td>
      <td>5416054.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.102497</td>
      <td>14.370454</td>
      <td>14.033026</td>
      <td>14.330757</td>
      <td>5416054.0</td>
      <td>-0.148865</td>
    </tr>
    <tr>
      <th>2017-07-17</th>
      <td>14.50</td>
      <td>14.5100</td>
      <td>14.1800</td>
      <td>14.290</td>
      <td>4269254.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.390303</td>
      <td>14.400227</td>
      <td>14.072724</td>
      <td>14.181891</td>
      <td>4269254.0</td>
      <td>-0.148865</td>
    </tr>
    <tr>
      <th>2017-07-14</th>
      <td>14.33</td>
      <td>14.4900</td>
      <td>14.3200</td>
      <td>14.470</td>
      <td>4857133.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.221589</td>
      <td>14.380378</td>
      <td>14.211664</td>
      <td>14.360530</td>
      <td>4857133.0</td>
      <td>0.178638</td>
    </tr>
    <tr>
      <th>2017-07-13</th>
      <td>14.00</td>
      <td>14.3500</td>
      <td>13.9100</td>
      <td>14.310</td>
      <td>7235627.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.894085</td>
      <td>14.241437</td>
      <td>13.804766</td>
      <td>14.201740</td>
      <td>7235627.0</td>
      <td>-0.158790</td>
    </tr>
    <tr>
      <th>2017-07-12</th>
      <td>13.95</td>
      <td>14.0500</td>
      <td>13.8850</td>
      <td>13.970</td>
      <td>4844647.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.844464</td>
      <td>13.943707</td>
      <td>13.779955</td>
      <td>13.864312</td>
      <td>4844647.0</td>
      <td>-0.337428</td>
    </tr>
    <tr>
      <th>2017-07-11</th>
      <td>13.72</td>
      <td>13.9500</td>
      <td>13.6800</td>
      <td>13.770</td>
      <td>7179511.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.616204</td>
      <td>13.844464</td>
      <td>13.576506</td>
      <td>13.665825</td>
      <td>7179511.0</td>
      <td>-0.198487</td>
    </tr>
    <tr>
      <th>2017-07-10</th>
      <td>13.86</td>
      <td>13.8750</td>
      <td>13.5500</td>
      <td>13.710</td>
      <td>5854314.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.755144</td>
      <td>13.770031</td>
      <td>13.447490</td>
      <td>13.606279</td>
      <td>5854314.0</td>
      <td>-0.059546</td>
    </tr>
    <tr>
      <th>2017-07-07</th>
      <td>13.44</td>
      <td>13.8800</td>
      <td>13.4200</td>
      <td>13.860</td>
      <td>6249219.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.338322</td>
      <td>13.774993</td>
      <td>13.318473</td>
      <td>13.755144</td>
      <td>6249219.0</td>
      <td>0.148865</td>
    </tr>
    <tr>
      <th>2017-07-06</th>
      <td>13.41</td>
      <td>13.6800</td>
      <td>13.3200</td>
      <td>13.370</td>
      <td>6124318.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.308549</td>
      <td>13.576506</td>
      <td>13.219230</td>
      <td>13.268851</td>
      <td>6124318.0</td>
      <td>-0.486293</td>
    </tr>
    <tr>
      <th>2017-07-05</th>
      <td>13.42</td>
      <td>13.7100</td>
      <td>13.4100</td>
      <td>13.590</td>
      <td>5390695.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.318473</td>
      <td>13.606279</td>
      <td>13.308549</td>
      <td>13.487187</td>
      <td>5390695.0</td>
      <td>0.218336</td>
    </tr>
    <tr>
      <th>2017-07-03</th>
      <td>13.68</td>
      <td>13.8800</td>
      <td>13.3600</td>
      <td>13.370</td>
      <td>3097751.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.576506</td>
      <td>13.774993</td>
      <td>13.258927</td>
      <td>13.268851</td>
      <td>3097751.0</td>
      <td>-0.218336</td>
    </tr>
    <tr>
      <th>2017-06-30</th>
      <td>13.90</td>
      <td>13.9500</td>
      <td>13.6400</td>
      <td>13.650</td>
      <td>3937984.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.794842</td>
      <td>13.844464</td>
      <td>13.536809</td>
      <td>13.546733</td>
      <td>3937984.0</td>
      <td>0.277882</td>
    </tr>
    <tr>
      <th>2017-06-29</th>
      <td>14.30</td>
      <td>14.3400</td>
      <td>13.6000</td>
      <td>13.950</td>
      <td>10797719.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.191816</td>
      <td>14.231513</td>
      <td>13.497111</td>
      <td>13.844464</td>
      <td>10797719.0</td>
      <td>0.297730</td>
    </tr>
    <tr>
      <th>2017-06-28</th>
      <td>13.89</td>
      <td>14.3600</td>
      <td>13.7900</td>
      <td>14.350</td>
      <td>16940651.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.784917</td>
      <td>14.251362</td>
      <td>13.685674</td>
      <td>14.241437</td>
      <td>16940651.0</td>
      <td>0.396974</td>
    </tr>
    <tr>
      <th>2017-06-27</th>
      <td>13.50</td>
      <td>13.6900</td>
      <td>13.1200</td>
      <td>13.200</td>
      <td>10056383.0</td>
      <td>0.11</td>
      <td>1.0</td>
      <td>13.397868</td>
      <td>13.586431</td>
      <td>13.020743</td>
      <td>13.100138</td>
      <td>10056383.0</td>
      <td>-1.141300</td>
    </tr>
    <tr>
      <th>2017-06-26</th>
      <td>13.36</td>
      <td>13.5750</td>
      <td>13.2100</td>
      <td>13.470</td>
      <td>7329800.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.149349</td>
      <td>13.360959</td>
      <td>13.001714</td>
      <td>13.257615</td>
      <td>7329800.0</td>
      <td>0.157477</td>
    </tr>
    <tr>
      <th>2017-06-23</th>
      <td>12.97</td>
      <td>13.3200</td>
      <td>12.8900</td>
      <td>13.310</td>
      <td>6860008.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.765498</td>
      <td>13.109980</td>
      <td>12.686760</td>
      <td>13.100138</td>
      <td>6860008.0</td>
      <td>-0.157477</td>
    </tr>
    <tr>
      <th>2017-06-22</th>
      <td>13.22</td>
      <td>13.2500</td>
      <td>12.9800</td>
      <td>13.010</td>
      <td>6736667.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.011557</td>
      <td>13.041084</td>
      <td>12.775341</td>
      <td>12.804868</td>
      <td>6736667.0</td>
      <td>-0.295270</td>
    </tr>
    <tr>
      <th>2017-06-21</th>
      <td>13.31</td>
      <td>13.5200</td>
      <td>13.1900</td>
      <td>13.270</td>
      <td>4662733.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.100138</td>
      <td>13.306826</td>
      <td>12.982030</td>
      <td>13.060768</td>
      <td>4662733.0</td>
      <td>0.255901</td>
    </tr>
    <tr>
      <th>2017-06-20</th>
      <td>13.36</td>
      <td>13.7950</td>
      <td>13.2100</td>
      <td>13.230</td>
      <td>6663071.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.149349</td>
      <td>13.577490</td>
      <td>13.001714</td>
      <td>13.021399</td>
      <td>6663071.0</td>
      <td>-0.039369</td>
    </tr>
    <tr>
      <th>2017-06-19</th>
      <td>13.30</td>
      <td>13.4900</td>
      <td>13.2000</td>
      <td>13.320</td>
      <td>5160813.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.090295</td>
      <td>13.277299</td>
      <td>12.991872</td>
      <td>13.109980</td>
      <td>5160813.0</td>
      <td>0.088581</td>
    </tr>
    <tr>
      <th>2017-06-16</th>
      <td>13.40</td>
      <td>13.4400</td>
      <td>13.0700</td>
      <td>13.140</td>
      <td>5811401.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.188718</td>
      <td>13.228088</td>
      <td>12.863922</td>
      <td>12.932818</td>
      <td>5811401.0</td>
      <td>-0.177162</td>
    </tr>
    <tr>
      <th>2017-06-15</th>
      <td>13.10</td>
      <td>13.4700</td>
      <td>13.0500</td>
      <td>13.370</td>
      <td>7533348.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.893449</td>
      <td>13.257615</td>
      <td>12.844237</td>
      <td>13.159192</td>
      <td>7533348.0</td>
      <td>0.226374</td>
    </tr>
    <tr>
      <th>2017-06-14</th>
      <td>13.71</td>
      <td>13.8000</td>
      <td>13.0800</td>
      <td>13.270</td>
      <td>11421282.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.493831</td>
      <td>13.582412</td>
      <td>12.873764</td>
      <td>13.060768</td>
      <td>11421282.0</td>
      <td>-0.098423</td>
    </tr>
    <tr>
      <th>2017-06-13</th>
      <td>13.77</td>
      <td>13.9800</td>
      <td>13.6150</td>
      <td>13.770</td>
      <td>7465612.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.552885</td>
      <td>13.759573</td>
      <td>13.400329</td>
      <td>13.552885</td>
      <td>7465612.0</td>
      <td>0.492116</td>
    </tr>
    <tr>
      <th>2017-06-12</th>
      <td>13.41</td>
      <td>13.7950</td>
      <td>13.1799</td>
      <td>13.630</td>
      <td>11732060.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.198561</td>
      <td>13.577490</td>
      <td>12.972089</td>
      <td>13.415092</td>
      <td>11732060.0</td>
      <td>-0.137793</td>
    </tr>
    <tr>
      <th>2017-06-09</th>
      <td>14.27</td>
      <td>14.3265</td>
      <td>13.3600</td>
      <td>13.590</td>
      <td>8955491.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.045001</td>
      <td>14.100610</td>
      <td>13.149349</td>
      <td>13.375723</td>
      <td>8955491.0</td>
      <td>-0.039369</td>
    </tr>
    <tr>
      <th>2017-06-08</th>
      <td>13.85</td>
      <td>14.2400</td>
      <td>13.6900</td>
      <td>14.225</td>
      <td>5013961.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.631623</td>
      <td>14.015474</td>
      <td>13.474146</td>
      <td>14.000710</td>
      <td>5013961.0</td>
      <td>0.624988</td>
    </tr>
    <tr>
      <th>2017-06-07</th>
      <td>14.17</td>
      <td>14.1800</td>
      <td>13.7500</td>
      <td>13.860</td>
      <td>5981684.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.946578</td>
      <td>13.956420</td>
      <td>13.533200</td>
      <td>13.641466</td>
      <td>5981684.0</td>
      <td>-0.359245</td>
    </tr>
    <tr>
      <th>2017-06-06</th>
      <td>14.09</td>
      <td>14.4100</td>
      <td>13.9500</td>
      <td>14.045</td>
      <td>6615198.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.867839</td>
      <td>14.182794</td>
      <td>13.730046</td>
      <td>13.823549</td>
      <td>6615198.0</td>
      <td>0.182083</td>
    </tr>
    <tr>
      <th>2017-06-05</th>
      <td>13.97</td>
      <td>14.2500</td>
      <td>13.9400</td>
      <td>14.160</td>
      <td>6153079.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.749731</td>
      <td>14.025316</td>
      <td>13.720204</td>
      <td>13.936735</td>
      <td>6153079.0</td>
      <td>0.113187</td>
    </tr>
    <tr>
      <th>2017-06-02</th>
      <td>14.20</td>
      <td>14.2300</td>
      <td>13.8700</td>
      <td>13.940</td>
      <td>5903246.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.976105</td>
      <td>14.005632</td>
      <td>13.651308</td>
      <td>13.720204</td>
      <td>5903246.0</td>
      <td>-0.216531</td>
    </tr>
    <tr>
      <th>2017-06-01</th>
      <td>14.03</td>
      <td>14.2900</td>
      <td>13.9100</td>
      <td>14.130</td>
      <td>5307726.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.808785</td>
      <td>14.064686</td>
      <td>13.690677</td>
      <td>13.907208</td>
      <td>5307726.0</td>
      <td>0.187004</td>
    </tr>
    <tr>
      <th>2017-05-31</th>
      <td>14.02</td>
      <td>14.0500</td>
      <td>13.7900</td>
      <td>13.990</td>
      <td>6209902.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.798943</td>
      <td>13.828470</td>
      <td>13.572569</td>
      <td>13.769416</td>
      <td>6209902.0</td>
      <td>-0.137793</td>
    </tr>
    <tr>
      <th>2017-05-30</th>
      <td>13.83</td>
      <td>13.9450</td>
      <td>13.7600</td>
      <td>13.890</td>
      <td>3672567.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.611939</td>
      <td>13.725125</td>
      <td>13.543042</td>
      <td>13.670993</td>
      <td>3672567.0</td>
      <td>-0.098423</td>
    </tr>
    <tr>
      <th>2017-05-26</th>
      <td>14.04</td>
      <td>14.0400</td>
      <td>13.6500</td>
      <td>13.830</td>
      <td>4563025.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.818627</td>
      <td>13.818627</td>
      <td>13.434777</td>
      <td>13.611939</td>
      <td>4563025.0</td>
      <td>-0.059054</td>
    </tr>
    <tr>
      <th>2017-05-25</th>
      <td>14.04</td>
      <td>14.1100</td>
      <td>13.8300</td>
      <td>14.060</td>
      <td>11079689.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.818627</td>
      <td>13.887524</td>
      <td>13.611939</td>
      <td>13.838312</td>
      <td>11079689.0</td>
      <td>0.226374</td>
    </tr>
    <tr>
      <th>2017-05-24</th>
      <td>13.25</td>
      <td>13.9300</td>
      <td>13.1600</td>
      <td>13.900</td>
      <td>11282756.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.041084</td>
      <td>13.710362</td>
      <td>12.952503</td>
      <td>13.680835</td>
      <td>11282756.0</td>
      <td>-0.157477</td>
    </tr>
    <tr>
      <th>2017-05-23</th>
      <td>13.18</td>
      <td>13.1900</td>
      <td>12.8850</td>
      <td>13.040</td>
      <td>4492731.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.972187</td>
      <td>12.982030</td>
      <td>12.681839</td>
      <td>12.834395</td>
      <td>4492731.0</td>
      <td>-0.846440</td>
    </tr>
    <tr>
      <th>2017-05-22</th>
      <td>13.25</td>
      <td>13.2900</td>
      <td>12.9700</td>
      <td>13.140</td>
      <td>4947237.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.041084</td>
      <td>13.080453</td>
      <td>12.765498</td>
      <td>12.932818</td>
      <td>4947237.0</td>
      <td>0.098423</td>
    </tr>
    <tr>
      <th>2017-05-19</th>
      <td>13.18</td>
      <td>13.4000</td>
      <td>13.0900</td>
      <td>13.150</td>
      <td>4655688.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.972187</td>
      <td>13.188718</td>
      <td>12.883606</td>
      <td>12.942660</td>
      <td>4655688.0</td>
      <td>0.009842</td>
    </tr>
    <tr>
      <th>2017-05-18</th>
      <td>12.80</td>
      <td>13.1700</td>
      <td>12.6800</td>
      <td>13.130</td>
      <td>9913783.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.598179</td>
      <td>12.962345</td>
      <td>12.480071</td>
      <td>12.922976</td>
      <td>9913783.0</td>
      <td>-0.019685</td>
    </tr>
    <tr>
      <th>2017-05-17</th>
      <td>13.62</td>
      <td>13.7500</td>
      <td>12.7900</td>
      <td>12.790</td>
      <td>12131568.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.405250</td>
      <td>13.533200</td>
      <td>12.588337</td>
      <td>12.588337</td>
      <td>12131568.0</td>
      <td>-0.334639</td>
    </tr>
    <tr>
      <th>2017-05-16</th>
      <td>13.67</td>
      <td>13.9200</td>
      <td>13.6400</td>
      <td>13.850</td>
      <td>6689072.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.454461</td>
      <td>13.700520</td>
      <td>13.424934</td>
      <td>13.631623</td>
      <td>6689072.0</td>
      <td>1.043287</td>
    </tr>
    <tr>
      <th>2017-05-15</th>
      <td>13.47</td>
      <td>13.8200</td>
      <td>13.4300</td>
      <td>13.640</td>
      <td>4882348.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.257615</td>
      <td>13.602096</td>
      <td>13.218245</td>
      <td>13.424934</td>
      <td>4882348.0</td>
      <td>-0.206689</td>
    </tr>
    <tr>
      <th>2017-05-12</th>
      <td>13.62</td>
      <td>13.6800</td>
      <td>13.3700</td>
      <td>13.450</td>
      <td>2991298.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.405250</td>
      <td>13.464304</td>
      <td>13.159192</td>
      <td>13.237930</td>
      <td>2991298.0</td>
      <td>-0.187004</td>
    </tr>
    <tr>
      <th>2017-05-11</th>
      <td>13.51</td>
      <td>13.7700</td>
      <td>13.3250</td>
      <td>13.630</td>
      <td>3914325.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.296984</td>
      <td>13.552885</td>
      <td>13.114901</td>
      <td>13.415092</td>
      <td>3914325.0</td>
      <td>0.177162</td>
    </tr>
    <tr>
      <th>2017-05-10</th>
      <td>13.53</td>
      <td>13.6000</td>
      <td>13.3900</td>
      <td>13.580</td>
      <td>4034072.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.316669</td>
      <td>13.385565</td>
      <td>13.178876</td>
      <td>13.365880</td>
      <td>4034072.0</td>
      <td>-0.049212</td>
    </tr>
    <tr>
      <th>2017-05-09</th>
      <td>13.31</td>
      <td>13.5250</td>
      <td>13.2000</td>
      <td>13.430</td>
      <td>7582290.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.100138</td>
      <td>13.311748</td>
      <td>12.991872</td>
      <td>13.218245</td>
      <td>7582290.0</td>
      <td>-0.147635</td>
    </tr>
    <tr>
      <th>2017-05-08</th>
      <td>13.45</td>
      <td>13.4800</td>
      <td>13.1300</td>
      <td>13.160</td>
      <td>4954733.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.237930</td>
      <td>13.267457</td>
      <td>12.922976</td>
      <td>12.952503</td>
      <td>4954733.0</td>
      <td>-0.265743</td>
    </tr>
    <tr>
      <th>2017-05-05</th>
      <td>13.32</td>
      <td>13.4900</td>
      <td>13.2100</td>
      <td>13.450</td>
      <td>5817953.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.109980</td>
      <td>13.277299</td>
      <td>13.001714</td>
      <td>13.237930</td>
      <td>5817953.0</td>
      <td>0.285427</td>
    </tr>
    <tr>
      <th>2017-05-04</th>
      <td>13.28</td>
      <td>13.3601</td>
      <td>13.0200</td>
      <td>13.320</td>
      <td>6828497.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.070611</td>
      <td>13.149448</td>
      <td>12.814710</td>
      <td>13.109980</td>
      <td>6828497.0</td>
      <td>-0.127950</td>
    </tr>
    <tr>
      <th>2017-05-03</th>
      <td>13.28</td>
      <td>13.4650</td>
      <td>13.2400</td>
      <td>13.290</td>
      <td>5252892.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.070611</td>
      <td>13.252694</td>
      <td>13.031241</td>
      <td>13.080453</td>
      <td>5252892.0</td>
      <td>-0.029527</td>
    </tr>
    <tr>
      <th>2017-05-02</th>
      <td>13.81</td>
      <td>13.8300</td>
      <td>13.2200</td>
      <td>13.330</td>
      <td>9921307.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.592254</td>
      <td>13.611939</td>
      <td>13.011557</td>
      <td>13.119822</td>
      <td>9921307.0</td>
      <td>0.039369</td>
    </tr>
    <tr>
      <th>2017-05-01</th>
      <td>14.07</td>
      <td>14.1000</td>
      <td>13.6300</td>
      <td>13.800</td>
      <td>7682709.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.848154</td>
      <td>13.877681</td>
      <td>13.415092</td>
      <td>13.582412</td>
      <td>7682709.0</td>
      <td>0.462589</td>
    </tr>
    <tr>
      <th>2017-04-28</th>
      <td>14.20</td>
      <td>14.5800</td>
      <td>13.6500</td>
      <td>14.010</td>
      <td>13802851.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.976105</td>
      <td>14.350113</td>
      <td>13.434777</td>
      <td>13.789100</td>
      <td>13802851.0</td>
      <td>0.206689</td>
    </tr>
    <tr>
      <th>2017-04-27</th>
      <td>14.10</td>
      <td>14.4900</td>
      <td>14.0000</td>
      <td>14.400</td>
      <td>11913612.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.877681</td>
      <td>14.261532</td>
      <td>13.779258</td>
      <td>14.172951</td>
      <td>11913612.0</td>
      <td>0.383851</td>
    </tr>
    <tr>
      <th>2017-04-26</th>
      <td>14.17</td>
      <td>14.2900</td>
      <td>13.8834</td>
      <td>13.980</td>
      <td>6260650.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.946578</td>
      <td>14.064686</td>
      <td>13.664497</td>
      <td>13.759573</td>
      <td>6260650.0</td>
      <td>-0.413378</td>
    </tr>
    <tr>
      <th>2017-04-25</th>
      <td>14.19</td>
      <td>14.3800</td>
      <td>14.0700</td>
      <td>14.240</td>
      <td>5157148.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.966262</td>
      <td>14.153267</td>
      <td>13.848154</td>
      <td>14.015474</td>
      <td>5157148.0</td>
      <td>0.255901</td>
    </tr>
    <tr>
      <th>2017-04-24</th>
      <td>14.15</td>
      <td>14.2900</td>
      <td>13.9100</td>
      <td>14.080</td>
      <td>6695629.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.926893</td>
      <td>14.064686</td>
      <td>13.690677</td>
      <td>13.857997</td>
      <td>6695629.0</td>
      <td>-0.157477</td>
    </tr>
    <tr>
      <th>2017-04-21</th>
      <td>13.96</td>
      <td>14.0700</td>
      <td>13.7650</td>
      <td>13.990</td>
      <td>6342825.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.739889</td>
      <td>13.848154</td>
      <td>13.547963</td>
      <td>13.769416</td>
      <td>6342825.0</td>
      <td>-0.088581</td>
    </tr>
    <tr>
      <th>2017-04-20</th>
      <td>13.91</td>
      <td>14.1200</td>
      <td>13.8500</td>
      <td>14.090</td>
      <td>5796854.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.690677</td>
      <td>13.897366</td>
      <td>13.631623</td>
      <td>13.867839</td>
      <td>5796854.0</td>
      <td>0.098423</td>
    </tr>
    <tr>
      <th>2017-04-19</th>
      <td>13.72</td>
      <td>14.0400</td>
      <td>13.6800</td>
      <td>13.770</td>
      <td>6702315.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.503673</td>
      <td>13.818627</td>
      <td>13.464304</td>
      <td>13.552885</td>
      <td>6702315.0</td>
      <td>-0.314954</td>
    </tr>
    <tr>
      <th>2017-04-18</th>
      <td>13.44</td>
      <td>13.6300</td>
      <td>13.3600</td>
      <td>13.620</td>
      <td>3963255.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.228088</td>
      <td>13.415092</td>
      <td>13.149349</td>
      <td>13.405250</td>
      <td>3963255.0</td>
      <td>-0.147635</td>
    </tr>
    <tr>
      <th>2017-04-17</th>
      <td>13.18</td>
      <td>13.5100</td>
      <td>13.1250</td>
      <td>13.480</td>
      <td>4820787.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.972187</td>
      <td>13.296984</td>
      <td>12.918054</td>
      <td>13.267457</td>
      <td>4820787.0</td>
      <td>-0.137793</td>
    </tr>
    <tr>
      <th>2017-04-13</th>
      <td>13.34</td>
      <td>13.4500</td>
      <td>13.1400</td>
      <td>13.140</td>
      <td>3810871.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.129665</td>
      <td>13.237930</td>
      <td>12.932818</td>
      <td>12.932818</td>
      <td>3810871.0</td>
      <td>-0.334639</td>
    </tr>
    <tr>
      <th>2017-04-12</th>
      <td>13.72</td>
      <td>13.8000</td>
      <td>13.3100</td>
      <td>13.350</td>
      <td>5319369.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.503673</td>
      <td>13.582412</td>
      <td>13.100138</td>
      <td>13.139507</td>
      <td>5319369.0</td>
      <td>0.206689</td>
    </tr>
    <tr>
      <th>2017-04-11</th>
      <td>13.86</td>
      <td>13.9400</td>
      <td>13.4300</td>
      <td>13.750</td>
      <td>10713152.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.641466</td>
      <td>13.720204</td>
      <td>13.218245</td>
      <td>13.533200</td>
      <td>10713152.0</td>
      <td>0.393693</td>
    </tr>
    <tr>
      <th>2017-04-10</th>
      <td>13.77</td>
      <td>13.9800</td>
      <td>13.7600</td>
      <td>13.890</td>
      <td>7636047.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.552885</td>
      <td>13.759573</td>
      <td>13.543042</td>
      <td>13.670993</td>
      <td>7636047.0</td>
      <td>0.137793</td>
    </tr>
    <tr>
      <th>2017-04-07</th>
      <td>13.23</td>
      <td>13.7200</td>
      <td>13.2250</td>
      <td>13.590</td>
      <td>9221997.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.021399</td>
      <td>13.503673</td>
      <td>13.016478</td>
      <td>13.375723</td>
      <td>9221997.0</td>
      <td>-0.295270</td>
    </tr>
    <tr>
      <th>2017-04-06</th>
      <td>13.32</td>
      <td>13.3200</td>
      <td>13.0700</td>
      <td>13.180</td>
      <td>9043518.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.109980</td>
      <td>13.109980</td>
      <td>12.863922</td>
      <td>12.972187</td>
      <td>9043518.0</td>
      <td>-0.403535</td>
    </tr>
    <tr>
      <th>2017-04-05</th>
      <td>13.52</td>
      <td>13.6500</td>
      <td>13.2900</td>
      <td>13.310</td>
      <td>8942874.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.306826</td>
      <td>13.434777</td>
      <td>13.080453</td>
      <td>13.100138</td>
      <td>8942874.0</td>
      <td>0.127950</td>
    </tr>
    <tr>
      <th>2017-04-04</th>
      <td>13.50</td>
      <td>13.6400</td>
      <td>13.3100</td>
      <td>13.420</td>
      <td>6456576.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.287142</td>
      <td>13.424934</td>
      <td>13.100138</td>
      <td>13.208403</td>
      <td>6456576.0</td>
      <td>0.108266</td>
    </tr>
    <tr>
      <th>2017-04-03</th>
      <td>13.78</td>
      <td>13.8500</td>
      <td>13.4000</td>
      <td>13.510</td>
      <td>7922233.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.562727</td>
      <td>13.631623</td>
      <td>13.188718</td>
      <td>13.296984</td>
      <td>7922233.0</td>
      <td>0.088581</td>
    </tr>
    <tr>
      <th>2017-03-31</th>
      <td>13.98</td>
      <td>14.0700</td>
      <td>13.7500</td>
      <td>13.760</td>
      <td>6268579.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.759573</td>
      <td>13.848154</td>
      <td>13.533200</td>
      <td>13.543042</td>
      <td>6268579.0</td>
      <td>0.246058</td>
    </tr>
    <tr>
      <th>2017-03-30</th>
      <td>13.95</td>
      <td>14.1300</td>
      <td>13.8000</td>
      <td>13.970</td>
      <td>12272965.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.730046</td>
      <td>13.907208</td>
      <td>13.582412</td>
      <td>13.749731</td>
      <td>12272965.0</td>
      <td>0.206689</td>
    </tr>
    <tr>
      <th>2017-03-29</th>
      <td>14.59</td>
      <td>14.7900</td>
      <td>14.2200</td>
      <td>14.240</td>
      <td>9520615.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>14.359955</td>
      <td>14.556802</td>
      <td>13.995789</td>
      <td>14.015474</td>
      <td>9520615.0</td>
      <td>0.265743</td>
    </tr>
    <tr>
      <th>2017-03-28</th>
      <td>14.90</td>
      <td>14.9800</td>
      <td>14.3300</td>
      <td>14.470</td>
      <td>14905852.0</td>
      <td>0.11</td>
      <td>1.0</td>
      <td>14.665068</td>
      <td>14.743806</td>
      <td>14.104055</td>
      <td>14.241848</td>
      <td>14905852.0</td>
      <td>0.226374</td>
    </tr>
    <tr>
      <th>2017-03-27</th>
      <td>14.25</td>
      <td>14.8700</td>
      <td>14.0500</td>
      <td>14.840</td>
      <td>13474648.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.919501</td>
      <td>14.525122</td>
      <td>13.724140</td>
      <td>14.495817</td>
      <td>13474648.0</td>
      <td>0.253970</td>
    </tr>
    <tr>
      <th>2017-03-24</th>
      <td>14.24</td>
      <td>14.7600</td>
      <td>14.1800</td>
      <td>14.450</td>
      <td>12285627.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.909733</td>
      <td>14.417673</td>
      <td>13.851125</td>
      <td>14.114863</td>
      <td>12285627.0</td>
      <td>-0.380955</td>
    </tr>
    <tr>
      <th>2017-03-23</th>
      <td>13.87</td>
      <td>14.0800</td>
      <td>13.7600</td>
      <td>14.020</td>
      <td>6602289.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.548314</td>
      <td>13.753444</td>
      <td>13.440866</td>
      <td>13.694836</td>
      <td>6602289.0</td>
      <td>-0.420027</td>
    </tr>
    <tr>
      <th>2017-03-22</th>
      <td>13.93</td>
      <td>13.9700</td>
      <td>13.6400</td>
      <td>13.840</td>
      <td>5900171.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.606923</td>
      <td>13.645995</td>
      <td>13.323649</td>
      <td>13.519010</td>
      <td>5900171.0</td>
      <td>-0.175825</td>
    </tr>
    <tr>
      <th>2017-03-21</th>
      <td>14.28</td>
      <td>14.2900</td>
      <td>13.7500</td>
      <td>13.980</td>
      <td>13960638.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.948805</td>
      <td>13.958573</td>
      <td>13.431098</td>
      <td>13.655763</td>
      <td>13960638.0</td>
      <td>0.136753</td>
    </tr>
    <tr>
      <th>2017-03-20</th>
      <td>14.08</td>
      <td>14.2900</td>
      <td>13.9660</td>
      <td>14.200</td>
      <td>5419586.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.753444</td>
      <td>13.958573</td>
      <td>13.642088</td>
      <td>13.870661</td>
      <td>5419586.0</td>
      <td>0.214898</td>
    </tr>
    <tr>
      <th>2017-03-17</th>
      <td>13.97</td>
      <td>14.0350</td>
      <td>13.8800</td>
      <td>13.980</td>
      <td>6727226.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.645995</td>
      <td>13.709488</td>
      <td>13.558083</td>
      <td>13.655763</td>
      <td>6727226.0</td>
      <td>-0.214898</td>
    </tr>
    <tr>
      <th>2017-03-16</th>
      <td>13.93</td>
      <td>13.9900</td>
      <td>13.7600</td>
      <td>13.910</td>
      <td>4128167.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.606923</td>
      <td>13.665531</td>
      <td>13.440866</td>
      <td>13.587387</td>
      <td>4128167.0</td>
      <td>-0.068376</td>
    </tr>
    <tr>
      <th>2017-03-15</th>
      <td>13.85</td>
      <td>14.0500</td>
      <td>13.7300</td>
      <td>13.930</td>
      <td>6219166.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.528778</td>
      <td>13.724140</td>
      <td>13.411561</td>
      <td>13.606923</td>
      <td>6219166.0</td>
      <td>0.019536</td>
    </tr>
    <tr>
      <th>2017-03-14</th>
      <td>13.77</td>
      <td>13.8700</td>
      <td>13.5700</td>
      <td>13.790</td>
      <td>6879791.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.450634</td>
      <td>13.548314</td>
      <td>13.255272</td>
      <td>13.470170</td>
      <td>6879791.0</td>
      <td>-0.136753</td>
    </tr>
    <tr>
      <th>2017-03-13</th>
      <td>13.45</td>
      <td>13.8900</td>
      <td>13.4300</td>
      <td>13.890</td>
      <td>5873084.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.138055</td>
      <td>13.567851</td>
      <td>13.118519</td>
      <td>13.567851</td>
      <td>5873084.0</td>
      <td>0.097681</td>
    </tr>
    <tr>
      <th>2017-03-10</th>
      <td>13.37</td>
      <td>13.5600</td>
      <td>13.3200</td>
      <td>13.470</td>
      <td>3892235.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.059911</td>
      <td>13.245504</td>
      <td>13.011071</td>
      <td>13.157592</td>
      <td>3892235.0</td>
      <td>-0.410259</td>
    </tr>
    <tr>
      <th>2017-03-09</th>
      <td>13.24</td>
      <td>13.4100</td>
      <td>13.1800</td>
      <td>13.290</td>
      <td>4164388.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.932926</td>
      <td>13.098983</td>
      <td>12.874318</td>
      <td>12.981766</td>
      <td>4164388.0</td>
      <td>-0.175825</td>
    </tr>
    <tr>
      <th>2017-03-08</th>
      <td>13.39</td>
      <td>13.4800</td>
      <td>13.2050</td>
      <td>13.300</td>
      <td>6789628.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.079447</td>
      <td>13.167360</td>
      <td>12.898738</td>
      <td>12.991534</td>
      <td>6789628.0</td>
      <td>0.009768</td>
    </tr>
    <tr>
      <th>2017-03-07</th>
      <td>13.42</td>
      <td>13.5100</td>
      <td>13.3200</td>
      <td>13.360</td>
      <td>3368724.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.108751</td>
      <td>13.196664</td>
      <td>13.011071</td>
      <td>13.050143</td>
      <td>3368724.0</td>
      <td>0.058608</td>
    </tr>
    <tr>
      <th>2017-03-06</th>
      <td>13.34</td>
      <td>13.5100</td>
      <td>13.1100</td>
      <td>13.430</td>
      <td>6649496.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.030607</td>
      <td>13.196664</td>
      <td>12.805941</td>
      <td>13.118519</td>
      <td>6649496.0</td>
      <td>0.068376</td>
    </tr>
    <tr>
      <th>2017-03-03</th>
      <td>13.57</td>
      <td>13.6300</td>
      <td>13.4100</td>
      <td>13.470</td>
      <td>4618298.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.255272</td>
      <td>13.313881</td>
      <td>13.098983</td>
      <td>13.157592</td>
      <td>4618298.0</td>
      <td>0.039072</td>
    </tr>
    <tr>
      <th>2017-03-02</th>
      <td>13.49</td>
      <td>13.8000</td>
      <td>13.4600</td>
      <td>13.520</td>
      <td>8216644.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.177128</td>
      <td>13.479938</td>
      <td>13.147824</td>
      <td>13.206432</td>
      <td>8216644.0</td>
      <td>0.048840</td>
    </tr>
    <tr>
      <th>2017-03-01</th>
      <td>13.42</td>
      <td>13.5000</td>
      <td>13.1900</td>
      <td>13.440</td>
      <td>9215884.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.108751</td>
      <td>13.186896</td>
      <td>12.884086</td>
      <td>13.128287</td>
      <td>9215884.0</td>
      <td>-0.078145</td>
    </tr>
    <tr>
      <th>2017-02-28</th>
      <td>13.52</td>
      <td>13.7700</td>
      <td>13.2050</td>
      <td>13.270</td>
      <td>15937027.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>13.206432</td>
      <td>13.450634</td>
      <td>12.898738</td>
      <td>12.962230</td>
      <td>15937027.0</td>
      <td>-0.166057</td>
    </tr>
    <tr>
      <th>2017-02-27</th>
      <td>12.71</td>
      <td>13.1000</td>
      <td>12.6850</td>
      <td>13.100</td>
      <td>5180718.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.415218</td>
      <td>12.796173</td>
      <td>12.390798</td>
      <td>12.796173</td>
      <td>5180718.0</td>
      <td>-0.166057</td>
    </tr>
    <tr>
      <th>2017-02-24</th>
      <td>12.60</td>
      <td>12.7700</td>
      <td>12.4632</td>
      <td>12.720</td>
      <td>5108634.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.307769</td>
      <td>12.473827</td>
      <td>12.174142</td>
      <td>12.424986</td>
      <td>5108634.0</td>
      <td>-0.371187</td>
    </tr>
    <tr>
      <th>2017-02-23</th>
      <td>13.10</td>
      <td>13.1000</td>
      <td>12.6800</td>
      <td>12.820</td>
      <td>4077361.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.796173</td>
      <td>12.796173</td>
      <td>12.385914</td>
      <td>12.522667</td>
      <td>4077361.0</td>
      <td>0.097681</td>
    </tr>
    <tr>
      <th>2017-02-22</th>
      <td>13.15</td>
      <td>13.1900</td>
      <td>12.9900</td>
      <td>13.110</td>
      <td>3314634.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.845013</td>
      <td>12.884086</td>
      <td>12.688724</td>
      <td>12.805941</td>
      <td>3314634.0</td>
      <td>0.283274</td>
    </tr>
    <tr>
      <th>2017-02-21</th>
      <td>13.00</td>
      <td>13.2799</td>
      <td>12.9100</td>
      <td>13.120</td>
      <td>5865824.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.698492</td>
      <td>12.971901</td>
      <td>12.610580</td>
      <td>12.815709</td>
      <td>5865824.0</td>
      <td>0.009768</td>
    </tr>
    <tr>
      <th>2017-02-17</th>
      <td>12.78</td>
      <td>12.9000</td>
      <td>12.5500</td>
      <td>12.900</td>
      <td>4245951.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.483595</td>
      <td>12.600812</td>
      <td>12.258929</td>
      <td>12.600812</td>
      <td>4245951.0</td>
      <td>-0.214898</td>
    </tr>
    <tr>
      <th>2017-02-16</th>
      <td>12.97</td>
      <td>13.0400</td>
      <td>12.7100</td>
      <td>12.790</td>
      <td>4930748.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.669188</td>
      <td>12.737565</td>
      <td>12.415218</td>
      <td>12.493363</td>
      <td>4930748.0</td>
      <td>-0.107449</td>
    </tr>
    <tr>
      <th>2017-02-15</th>
      <td>12.59</td>
      <td>12.9800</td>
      <td>12.5900</td>
      <td>12.895</td>
      <td>7114972.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.298001</td>
      <td>12.678956</td>
      <td>12.298001</td>
      <td>12.595928</td>
      <td>7114972.0</td>
      <td>0.102565</td>
    </tr>
    <tr>
      <th>2017-02-14</th>
      <td>12.50</td>
      <td>12.7500</td>
      <td>12.3250</td>
      <td>12.600</td>
      <td>6473359.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.210089</td>
      <td>12.454291</td>
      <td>12.039148</td>
      <td>12.307769</td>
      <td>6473359.0</td>
      <td>-0.288158</td>
    </tr>
    <tr>
      <th>2017-02-13</th>
      <td>12.50</td>
      <td>12.6300</td>
      <td>12.4150</td>
      <td>12.520</td>
      <td>4481494.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.210089</td>
      <td>12.337074</td>
      <td>12.127060</td>
      <td>12.229625</td>
      <td>4481494.0</td>
      <td>-0.078145</td>
    </tr>
    <tr>
      <th>2017-02-10</th>
      <td>12.46</td>
      <td>12.4700</td>
      <td>12.2350</td>
      <td>12.340</td>
      <td>4379473.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.171016</td>
      <td>12.180785</td>
      <td>11.951235</td>
      <td>12.053800</td>
      <td>4379473.0</td>
      <td>-0.175825</td>
    </tr>
    <tr>
      <th>2017-02-09</th>
      <td>12.65</td>
      <td>12.6900</td>
      <td>12.4100</td>
      <td>12.420</td>
      <td>4827880.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.356610</td>
      <td>12.395682</td>
      <td>12.122176</td>
      <td>12.131944</td>
      <td>4827880.0</td>
      <td>0.078145</td>
    </tr>
    <tr>
      <th>2017-02-08</th>
      <td>12.71</td>
      <td>12.7850</td>
      <td>12.5400</td>
      <td>12.650</td>
      <td>6658258.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.415218</td>
      <td>12.488479</td>
      <td>12.249161</td>
      <td>12.356610</td>
      <td>6658258.0</td>
      <td>0.224666</td>
    </tr>
    <tr>
      <th>2017-02-07</th>
      <td>12.83</td>
      <td>12.9400</td>
      <td>12.6650</td>
      <td>12.710</td>
      <td>4382695.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.532435</td>
      <td>12.639884</td>
      <td>12.371262</td>
      <td>12.415218</td>
      <td>4382695.0</td>
      <td>0.058608</td>
    </tr>
    <tr>
      <th>2017-02-06</th>
      <td>12.86</td>
      <td>12.9200</td>
      <td>12.7372</td>
      <td>12.850</td>
      <td>6699892.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.561739</td>
      <td>12.620348</td>
      <td>12.441787</td>
      <td>12.551971</td>
      <td>6699892.0</td>
      <td>0.136753</td>
    </tr>
    <tr>
      <th>2017-02-03</th>
      <td>12.28</td>
      <td>12.9700</td>
      <td>12.2800</td>
      <td>12.910</td>
      <td>23135862.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.995191</td>
      <td>12.669188</td>
      <td>11.995191</td>
      <td>12.610580</td>
      <td>23135862.0</td>
      <td>0.058608</td>
    </tr>
    <tr>
      <th>2017-02-02</th>
      <td>11.93</td>
      <td>12.0600</td>
      <td>11.7700</td>
      <td>11.850</td>
      <td>8424446.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.653309</td>
      <td>11.780294</td>
      <td>11.497020</td>
      <td>11.575164</td>
      <td>8424446.0</td>
      <td>-1.035416</td>
    </tr>
    <tr>
      <th>2017-02-01</th>
      <td>11.90</td>
      <td>12.0450</td>
      <td>11.7100</td>
      <td>12.040</td>
      <td>5419707.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.624004</td>
      <td>11.765642</td>
      <td>11.438411</td>
      <td>11.760757</td>
      <td>5419707.0</td>
      <td>0.185593</td>
    </tr>
    <tr>
      <th>2017-01-31</th>
      <td>11.85</td>
      <td>11.9000</td>
      <td>11.6300</td>
      <td>11.800</td>
      <td>4592335.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.575164</td>
      <td>11.624004</td>
      <td>11.360267</td>
      <td>11.526324</td>
      <td>4592335.0</td>
      <td>-0.234434</td>
    </tr>
    <tr>
      <th>2017-01-30</th>
      <td>12.04</td>
      <td>12.0400</td>
      <td>11.7100</td>
      <td>11.905</td>
      <td>6874063.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.760757</td>
      <td>11.760757</td>
      <td>11.438411</td>
      <td>11.628889</td>
      <td>6874063.0</td>
      <td>0.102565</td>
    </tr>
    <tr>
      <th>2017-01-27</th>
      <td>12.46</td>
      <td>12.5950</td>
      <td>12.0600</td>
      <td>12.080</td>
      <td>10323787.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>12.171016</td>
      <td>12.302885</td>
      <td>11.780294</td>
      <td>11.799830</td>
      <td>10323787.0</td>
      <td>0.170941</td>
    </tr>
    <tr>
      <th>2017-01-26</th>
      <td>12.26</td>
      <td>12.4700</td>
      <td>12.1800</td>
      <td>12.410</td>
      <td>6245115.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.975655</td>
      <td>12.180785</td>
      <td>11.897510</td>
      <td>12.122176</td>
      <td>6245115.0</td>
      <td>0.322346</td>
    </tr>
    <tr>
      <th>2017-01-25</th>
      <td>12.10</td>
      <td>12.4000</td>
      <td>12.0700</td>
      <td>12.220</td>
      <td>5867077.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.819366</td>
      <td>12.112408</td>
      <td>11.790062</td>
      <td>11.936583</td>
      <td>5867077.0</td>
      <td>-0.185593</td>
    </tr>
    <tr>
      <th>2017-01-24</th>
      <td>11.40</td>
      <td>12.0900</td>
      <td>11.3700</td>
      <td>12.040</td>
      <td>13199955.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.135601</td>
      <td>11.809598</td>
      <td>11.106297</td>
      <td>11.760757</td>
      <td>13199955.0</td>
      <td>-0.175825</td>
    </tr>
    <tr>
      <th>2017-01-23</th>
      <td>11.22</td>
      <td>11.3600</td>
      <td>10.9900</td>
      <td>11.360</td>
      <td>7072880.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>10.959776</td>
      <td>11.096529</td>
      <td>10.735110</td>
      <td>11.096529</td>
      <td>7072880.0</td>
      <td>-0.664229</td>
    </tr>
    <tr>
      <th>2017-01-20</th>
      <td>11.21</td>
      <td>11.4127</td>
      <td>11.1900</td>
      <td>11.260</td>
      <td>4999499.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>10.950008</td>
      <td>11.148006</td>
      <td>10.930471</td>
      <td>10.998848</td>
      <td>4999499.0</td>
      <td>-0.097681</td>
    </tr>
    <tr>
      <th>2017-01-19</th>
      <td>11.36</td>
      <td>11.4700</td>
      <td>11.1500</td>
      <td>11.180</td>
      <td>3884593.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.096529</td>
      <td>11.203977</td>
      <td>10.891399</td>
      <td>10.920703</td>
      <td>3884593.0</td>
      <td>-0.078145</td>
    </tr>
    <tr>
      <th>2017-01-18</th>
      <td>11.46</td>
      <td>11.5200</td>
      <td>11.3400</td>
      <td>11.380</td>
      <td>3700418.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.194209</td>
      <td>11.252818</td>
      <td>11.076993</td>
      <td>11.116065</td>
      <td>3700418.0</td>
      <td>0.195361</td>
    </tr>
    <tr>
      <th>2017-01-17</th>
      <td>11.60</td>
      <td>11.6000</td>
      <td>11.3300</td>
      <td>11.430</td>
      <td>3485887.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.330962</td>
      <td>11.330962</td>
      <td>11.067224</td>
      <td>11.164905</td>
      <td>3485887.0</td>
      <td>0.048840</td>
    </tr>
    <tr>
      <th>2017-01-13</th>
      <td>11.57</td>
      <td>11.7200</td>
      <td>11.5100</td>
      <td>11.610</td>
      <td>4737522.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.301658</td>
      <td>11.448179</td>
      <td>11.243050</td>
      <td>11.340730</td>
      <td>4737522.0</td>
      <td>0.175825</td>
    </tr>
    <tr>
      <th>2017-01-12</th>
      <td>11.52</td>
      <td>11.5200</td>
      <td>11.1816</td>
      <td>11.470</td>
      <td>3933456.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.252818</td>
      <td>11.252818</td>
      <td>10.922266</td>
      <td>11.203977</td>
      <td>3933456.0</td>
      <td>-0.136753</td>
    </tr>
    <tr>
      <th>2017-01-11</th>
      <td>11.55</td>
      <td>11.6250</td>
      <td>11.4700</td>
      <td>11.560</td>
      <td>3363666.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.282122</td>
      <td>11.355383</td>
      <td>11.203977</td>
      <td>11.291890</td>
      <td>3363666.0</td>
      <td>0.087913</td>
    </tr>
    <tr>
      <th>2017-01-10</th>
      <td>11.41</td>
      <td>11.5400</td>
      <td>11.3800</td>
      <td>11.530</td>
      <td>3203592.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.145369</td>
      <td>11.272354</td>
      <td>11.116065</td>
      <td>11.262586</td>
      <td>3203592.0</td>
      <td>-0.029304</td>
    </tr>
    <tr>
      <th>2017-01-09</th>
      <td>11.20</td>
      <td>11.4600</td>
      <td>11.1700</td>
      <td>11.450</td>
      <td>4221216.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>10.940240</td>
      <td>11.194209</td>
      <td>10.910935</td>
      <td>11.184441</td>
      <td>4221216.0</td>
      <td>-0.078145</td>
    </tr>
    <tr>
      <th>2017-01-06</th>
      <td>11.38</td>
      <td>11.4200</td>
      <td>11.1200</td>
      <td>11.150</td>
      <td>5195078.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.116065</td>
      <td>11.155137</td>
      <td>10.862095</td>
      <td>10.891399</td>
      <td>5195078.0</td>
      <td>-0.293042</td>
    </tr>
    <tr>
      <th>2017-01-05</th>
      <td>11.48</td>
      <td>11.5200</td>
      <td>11.2500</td>
      <td>11.360</td>
      <td>4343572.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.213746</td>
      <td>11.252818</td>
      <td>10.989080</td>
      <td>11.096529</td>
      <td>4343572.0</td>
      <td>0.205129</td>
    </tr>
    <tr>
      <th>2017-01-04</th>
      <td>11.38</td>
      <td>11.5700</td>
      <td>11.3700</td>
      <td>11.470</td>
      <td>4070898.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.116065</td>
      <td>11.301658</td>
      <td>11.106297</td>
      <td>11.203977</td>
      <td>4070898.0</td>
      <td>0.107449</td>
    </tr>
    <tr>
      <th>2017-01-03</th>
      <td>11.54</td>
      <td>11.6300</td>
      <td>11.3150</td>
      <td>11.370</td>
      <td>5746304.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>11.272354</td>
      <td>11.360267</td>
      <td>11.052572</td>
      <td>11.106297</td>
      <td>5746304.0</td>
      <td>-0.097681</td>
    </tr>
  </tbody>
</table>
</div>




```python
n_7_m = df_CY_07['Diff'].max()
n_7_i = df_CY_07['Diff'].idxmax()
n_8_m = df_CY_08['Diff'].max()
n_8_i = df_CY_08['Diff'].idxmax()
n_9_m = df_CY_09['Diff'].max()
n_9_i = df_CY_09['Diff'].idxmax()
n_10_m = df_CY_10['Diff'].max()
n_10_i = df_CY_10['Diff'].idxmax()
n_11_m = df_CY_11['Diff'].max()
n_11_i = df_CY_11['Diff'].idxmax()
n_12_m = df_CY_12['Diff'].max()
n_12_i = df_CY_12['Diff'].idxmax()
n_13_m = df_CY_13['Diff'].max()
n_13_i = df_CY_13['Diff'].idxmax()
n_14_m = df_CY_14['Diff'].max()
n_14_i = df_CY_14['Diff'].idxmax()
n_15_m = df_CY_15['Diff'].max()
n_15_i = df_CY_15['Diff'].idxmax()
n_16_m = df_CY_16['Diff'].max()
n_16_i = df_CY_16['Diff'].idxmax()
n_17_m = df_CY_17['Diff'].max()
n_17_i = df_CY_17['Diff'].idxmax()
CY_max_index_data = {n_7_m:n_7_i, n_8_m:n_8_i, n_9_m:n_9_i, n_10_m:n_10_i, n_11_m:n_11_i, n_12_m:n_12_i, n_13_m:n_13_i, n_14_m:n_14_i, n_15_m:n_15_i,n_16_m:n_16_i, n_17_m:n_17_i}
for i in CY_max_index_data:
    print (i,CY_max_index_data[i])
y = CY_max_index_data.keys()
x = CY_max_index_data.values()
plt.plot(x,y)
```

    0.9637239953116001 2007-11-09 00:00:00
    1.1100883890768993 2008-09-26 00:00:00
    0.46478811809889997 2009-04-16 00:00:00
    0.6065878829424989 2010-02-03 00:00:00
    1.171153146919 2011-08-17 00:00:00
    1.5609316394370012 2012-01-25 00:00:00
    1.4268978817391016 2013-09-23 00:00:00
    0.7547571305551015 2014-10-09 00:00:00
    0.8067966291899982 2015-03-24 00:00:00
    0.8053743777477003 2016-06-24 00:00:00
    1.1800000000000015 2017-11-28 00:00:00





    [<matplotlib.lines.Line2D at 0x1a14401fd0>]




![png](output_85_2.png)



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





    [<matplotlib.lines.Line2D at 0x1a144e98d0>]




![png](output_86_2.png)



```python
df_CY_07.corrwith(df_AAPL_07['AdjClose'])
```




    Open          0.964040
    High          0.965032
    Low           0.970374
    Close         0.969956
    Volume        0.027459
    ExDividend         NaN
    SplitRatio         NaN
    AdjOpen       0.964040
    AdjHigh       0.965032
    AdjLow        0.970374
    AdjClose      0.969956
    AdjVolume     0.027459
    Diff         -0.037416
    dtype: float64




```python
df_CY_08.corrwith(df_AAPL_08['AdjClose'])
```




    Open          0.900245
    High          0.899891
    Low           0.906946
    Close         0.905435
    Volume        0.393850
    ExDividend   -0.052990
    SplitRatio         NaN
    AdjOpen       0.883629
    AdjHigh       0.882896
    AdjLow        0.900045
    AdjClose      0.897186
    AdjVolume     0.393850
    Diff          0.033927
    dtype: float64




```python
df_CY_09.corrwith(df_AAPL_09['AdjClose'])
```




    Open          0.885299
    High          0.880892
    Low           0.888590
    Close         0.879430
    Volume        0.304379
    ExDividend         NaN
    SplitRatio         NaN
    AdjOpen       0.885299
    AdjHigh       0.880892
    AdjLow        0.888590
    AdjClose      0.879430
    AdjVolume     0.304379
    Diff          0.081868
    dtype: float64




```python
df_CY_10.corrwith(df_AAPL_10['AdjClose'])
```




    Open          0.739471
    High          0.746043
    Low           0.744991
    Close         0.746397
    Volume       -0.054642
    ExDividend         NaN
    SplitRatio         NaN
    AdjOpen       0.739471
    AdjHigh       0.746043
    AdjLow        0.744991
    AdjClose      0.746397
    AdjVolume    -0.054642
    Diff         -0.059993
    dtype: float64




```python
df_CY_11.corrwith(df_AAPL_11['AdjClose'])
```




    Open         -0.531626
    High         -0.521214
    Low          -0.544613
    Close        -0.529379
    Volume        0.067075
    ExDividend   -0.056867
    SplitRatio         NaN
    AdjOpen      -0.512909
    AdjHigh      -0.501991
    AdjLow       -0.526737
    AdjClose     -0.510543
    AdjVolume     0.067075
    Diff          0.115559
    dtype: float64




```python
df_CY_12.corrwith(df_AAPL_12['AdjClose'])
```




    Open         -0.564554
    High         -0.567548
    Low          -0.568304
    Close        -0.569890
    Volume        0.069354
    ExDividend   -0.025491
    SplitRatio         NaN
    AdjOpen      -0.564197
    AdjHigh      -0.567259
    AdjLow       -0.568188
    AdjClose     -0.569768
    AdjVolume     0.069354
    Diff          0.078186
    dtype: float64




```python
df_CY_13.corrwith(df_AAPL_13['AdjClose'])
```




    Open         -0.401055
    High         -0.411580
    Low          -0.377615
    Close        -0.393818
    Volume       -0.196961
    ExDividend    0.025310
    SplitRatio         NaN
    AdjOpen      -0.332955
    AdjHigh      -0.343539
    AdjLow       -0.308786
    AdjClose     -0.325258
    AdjVolume    -0.196961
    Diff          0.047371
    dtype: float64




```python
df_CY_14.corrwith(df_AAPL_14['AdjClose'])
```




    Open          0.440996
    High          0.444792
    Low           0.442170
    Close         0.448214
    Volume        0.223838
    ExDividend    0.034262
    SplitRatio         NaN
    AdjOpen       0.516877
    AdjHigh       0.520187
    AdjLow        0.518015
    AdjClose      0.523202
    AdjVolume     0.223838
    Diff         -0.125354
    dtype: float64




```python
df_CY_15.corrwith(df_AAPL_15['AdjClose'])
```




    Open          0.530250
    High          0.516298
    Low           0.538856
    Close         0.526287
    Volume        0.050312
    ExDividend   -0.015532
    SplitRatio         NaN
    AdjOpen       0.537029
    AdjHigh       0.522546
    AdjLow        0.545907
    AdjClose      0.532860
    AdjVolume     0.050312
    Diff          0.089424
    dtype: float64




```python
df_CY_16.corrwith(df_AAPL_16['AdjClose'])
```




    Open          0.574317
    High          0.559945
    Low           0.583500
    Close         0.565949
    Volume       -0.353781
    ExDividend    0.055053
    SplitRatio         NaN
    AdjOpen       0.597092
    AdjHigh       0.584001
    AdjLow        0.605118
    AdjClose      0.589211
    AdjVolume    -0.353781
    Diff          0.072197
    dtype: float64




```python
df_CY_17.corrwith(df_AAPL_17['AdjClose'])
```




    Open          0.832011
    High          0.834659
    Low           0.833041
    Close         0.831670
    Volume       -0.083872
    ExDividend   -0.023069
    SplitRatio         NaN
    AdjOpen       0.844703
    AdjHigh       0.847513
    AdjLow        0.845360
    AdjClose      0.844669
    AdjVolume    -0.083872
    Diff          0.074759
    dtype: float64




```python
df_CY_07_AdjClose = df_CY_07['AdjClose']
df_CY_07_AdjClose.head()
```




    Date
    2007-12-31    6.848713
    2007-12-28    6.995078
    2007-12-27    7.101524
    2007-12-26    7.363840
    2007-12-24    7.206070
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
df_CY_07_AdjClose.rename(index='Date')
df_CY_07_AdjClose.to_frame()
df_CY_07_AdjClose.head()
```




    Date
    2007-12-31    6.848713
    2007-12-28    6.995078
    2007-12-27    7.101524
    2007-12-26    7.363840
    2007-12-24    7.206070
    Name: AdjClose, dtype: float64




```python
df_AAPL_07_AdjClose.rename(index='Date')
df_CY_07_AdjClose.head()
```




    Date
    2007-12-31    6.848713
    2007-12-28    6.995078
    2007-12-27    7.101524
    2007-12-26    7.363840
    2007-12-24    7.206070
    Name: AdjClose, dtype: float64




```python
merged_07 = pd.concat([df_CY_07_AdjClose, df_AAPL_07_AdjClose], axis=1, join_axes=[df_CY_07_AdjClose.index])
merged_07.columns = ['CY_07', 'AAPL_07']
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
      <th>CY_07</th>
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
      <td>6.848713</td>
      <td>25.456041</td>
    </tr>
    <tr>
      <th>2007-12-28</th>
      <td>6.995078</td>
      <td>25.680940</td>
    </tr>
    <tr>
      <th>2007-12-27</th>
      <td>7.101524</td>
      <td>25.519013</td>
    </tr>
    <tr>
      <th>2007-12-26</th>
      <td>7.363840</td>
      <td>25.567848</td>
    </tr>
    <tr>
      <th>2007-12-24</th>
      <td>7.206070</td>
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
      <th>CY_07</th>
      <th>AAPL_07</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>CY_07</th>
      <td>1.000000</td>
      <td>0.969956</td>
    </tr>
    <tr>
      <th>AAPL_07</th>
      <td>0.969956</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
plt.scatter(df_CY_07['Diff'], df_AAPL_07['Diff'], marker = 'x', c='g')
plt.xlabel = ('Cypress price change per day')
plt.ylabel = ('Apple price change per day')
```


![png](output_104_0.png)



```python
seb.regplot(df_CY_07['Diff'], df_AAPL_07['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c728400>




![png](output_105_1.png)



```python
seb.regplot(df_CY_08['Diff'], df_AAPL_08['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c4362b0>




![png](output_106_1.png)



```python
seb.regplot(df_CY_09['Diff'], df_AAPL_09['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c077dd8>




![png](output_107_1.png)



```python
seb.regplot(df_CY_10['Diff'], df_AAPL_10['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c30a320>




![png](output_108_1.png)



```python
seb.regplot(df_CY_11['Diff'], df_AAPL_11['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c307080>




![png](output_109_1.png)



```python
seb.regplot(df_CY_12['Diff'], df_AAPL_12['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c667438>




![png](output_110_1.png)



```python
seb.regplot(df_CY_13['Diff'], df_AAPL_13['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1019bec18>




![png](output_111_1.png)



```python
seb.regplot(df_CY_14['Diff'], df_AAPL_14['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c59eb70>




![png](output_112_1.png)



```python
seb.regplot(df_CY_15['Diff'], df_AAPL_15['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c5a8c88>




![png](output_113_1.png)



```python
seb.regplot(df_CY_16['Diff'], df_AAPL_16['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c0849b0>




![png](output_114_1.png)



```python
seb.regplot(df_CY_17['Diff'], df_CY_17['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x103093278>




![png](output_115_1.png)



```python
stats.ttest_ind(df_CY_17['Diff'], df_AAPL_17['Diff'], equal_var=False)
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
df_CY_07.loc[:,"Diff"].std()
```




    0.141767715010873




```python
df_CY_08.loc[:,"Diff"].std()
```




    0.20109926616341067




```python
df_CY_09.loc[:,"Diff"].std()
```




    0.1698902341227937




```python
df_CY_10.loc[:,"Diff"].std()
```




    0.22627900698915646




```python
df_CY_11.loc[:,"Diff"].std()
```




    0.44956767227978134




```python
df_CY_12.loc[:,"Diff"].std()
```




    0.2943393516665419




```python
df_CY_13.loc[:,"Diff"].std()
```




    0.2029390009670052




```python
df_CY_14.loc[:,"Diff"].std()
```




    0.1927799921459957




```python
df_CY_15.loc[:,"Diff"].std()
```




    0.24473159092607266




```python
df_CY_16.loc[:,"Diff"].std()
```




    0.21674413706690018




```python
df_CY_17.loc[:,"Diff"].std()
```




    0.2748529047532917




```python
df_AAPL_07.loc[:,"Diff"].cov(df_CY_07.loc[:,"Diff"])
```




    0.025883743253753328




```python
df_AAPL_08.loc[:,"Diff"].cov(df_CY_08.loc[:,"Diff"])
```




    0.06513901074712933




```python
df_AAPL_09.loc[:,"Diff"].cov(df_CY_09.loc[:,"Diff"])
```




    0.028068314422787153




```python
df_AAPL_10.loc[:,"Diff"].cov(df_CY_10.loc[:,"Diff"])
```




    0.05735797095782032




```python
df_AAPL_11.loc[:,"Diff"].cov(df_CY_11.loc[:,"Diff"])
```




    0.1812752834343301




```python
df_AAPL_12.loc[:,"Diff"].cov(df_CY_12.loc[:,"Diff"])
```




    0.11471900380439318




```python
df_AAPL_13.loc[:,"Diff"].cov(df_CY_13.loc[:,"Diff"])
```




    0.04048169668172469




```python
df_AAPL_14.loc[:,"Diff"].cov(df_CY_14.loc[:,"Diff"])
```




    0.04426113529382242




```python
df_AAPL_15.loc[:,"Diff"].cov(df_CY_15.loc[:,"Diff"])
```




    0.16494666599913996




```python
df_AAPL_16.loc[:,"Diff"].cov(df_CY_16.loc[:,"Diff"])
```




    0.09156507465250803




```python
df_AAPL_17.loc[:,"Diff"].cov(df_CY_17.loc[:,"Diff"])
```




    0.17552700234664223




```python
df_CY_07['Diff'].mean()
```




    -0.014621232686265995




```python
df_AAPL_07['Diff'].mean()
```




    -0.05874629117882




```python
CY_07_mean=df_CY_07['Diff'].mean()
CY_07_mean
```




    -0.014621232686265995




```python
CY_08_mean = df_CY_08['Diff'].mean()
CY_08_mean
```




    0.012479650858558334




```python
CY_09_mean = df_CY_09['Diff'].mean()
CY_09_mean
```




    -0.018486069387550593




```python
CY_10_mean = df_CY_10['Diff'].mean()
CY_10_mean
```




    -0.025108413429611155




```python
CY_11_mean = df_CY_11['Diff'].mean()
CY_11_mean
```




    0.003337647833713152




```python
CY_12_mean = df_CY_12['Diff'].mean()
CY_12_mean
```




    0.018305103500734138




```python
CY_13_mean = df_CY_13['Diff'].mean()
CY_13_mean
```




    0.0012716251552211154




```python
CY_14_mean = df_CY_14['Diff'].mean()
CY_14_mean
```




    -0.015750506970117133




```python
CY_15_mean = df_CY_15['Diff'].mean()
CY_15_mean
```




    0.01528691772587888




```python
CY_16_mean = df_CY_16['Diff'].mean()
CY_16_mean
```




    -0.00929782990935259




```python
CY_17_mean = df_CY_17['Diff'].mean()
CY_17_mean
```




    -0.017348456335358867




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
population_n_07, population_a_07 = gendata_07(loc1=CY_07_mean, loc2=AAPL_07_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_07)), population_n_07, label="CY 07")
plt.scatter(range(len(population_a_07)), population_a_07, label="AAPL 07")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_07, 10, density=True, alpha=0.5, label="CY 07")
plt.hist(population_a_07, 10, density=True, alpha=0.5, label="AAPL 07")
plt.axvline(population_n_07.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_07.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a0c7c6e80>




![png](output_174_1.png)



```python
stats.ttest_ind(population_n_07, population_a_07, equal_var=False)
```




    Ttest_indResult(statistic=0.4824349706528323, pvalue=0.6297089610436643)




```python
def gendata_08(loc1=0, loc2=0):
    population_n_08 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_08 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_08, population_a_08
population_n_08, population_a_08 = gendata_08(loc1=CY_08_mean, loc2=AAPL_08_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_08)), population_n_08, label="CY 08")
plt.scatter(range(len(population_a_08)), population_a_08, label="AAPL 08")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_08, 10, density=True, alpha=0.5, label="CY 08")
plt.hist(population_a_08, 10, density=True, alpha=0.5, label="AAPL 08")
plt.axvline(population_n_08.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_08.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a0c8b95c0>




![png](output_176_1.png)



```python
stats.ttest_ind(population_n_08, population_a_08, equal_var=False)
```




    Ttest_indResult(statistic=-0.4740442393854202, pvalue=0.6356761273932535)




```python
def gendata_09(loc1=0, loc2=0):
    population_n_09 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_09 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_09, population_a_09
population_n_09, population_a_09 = gendata_09(loc1=CY_09_mean, loc2=AAPL_09_mean)
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




    <matplotlib.legend.Legend at 0x1a14f96a58>




![png](output_178_1.png)



```python
stats.ttest_ind(population_n_09, population_a_09, equal_var=False)
```




    Ttest_indResult(statistic=0.4695399776512597, pvalue=0.6388892316218685)




```python
def gendata_10(loc1=0, loc2=0):
    population_n_10 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_10 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_10, population_a_10
population_n_10, population_a_10 = gendata_10(loc1=CY_10_mean, loc2=AAPL_10_mean)
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




    <matplotlib.legend.Legend at 0x1a15113f98>




![png](output_180_1.png)



```python
stats.ttest_ind(population_n_10, population_a_10, equal_var=False)
```




    Ttest_indResult(statistic=0.33313962405949843, pvalue=0.7391690959532746)




```python
def gendata_11(loc1=0, loc2=0):
    population_n_11 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_11 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_11, population_a_11
population_n_11, population_a_11 = gendata_11(loc1=CY_11_mean, loc2=AAPL_11_mean)
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




    <matplotlib.legend.Legend at 0x1a1529c518>




![png](output_182_1.png)



```python
stats.ttest_ind(population_n_11, population_a_11, equal_var=False)
```




    Ttest_indResult(statistic=0.45874601425402434, pvalue=0.6466167096191889)




```python
def gendata_12(loc1=0, loc2=0):
    population_n_12 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_12 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_12, population_a_12
population_n_12, population_a_12 = gendata_12(loc1=CY_12_mean, loc2=AAPL_12_mean)
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




    <matplotlib.legend.Legend at 0x1a1541aa58>




![png](output_184_1.png)



```python
stats.ttest_ind(population_n_12, population_a_12, equal_var=False)
```




    Ttest_indResult(statistic=0.9097508874021379, pvalue=0.36339398986703153)




```python
def gendata_13(loc1=0, loc2=0):
    population_n_13 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_13 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_13, population_a_13
population_n_13, population_a_13 = gendata_13(loc1=CY_13_mean, loc2=AAPL_13_mean)
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




    <matplotlib.legend.Legend at 0x1a15595f98>




![png](output_186_1.png)



```python
stats.ttest_ind(population_n_13, population_a_13, equal_var=False)
```




    Ttest_indResult(statistic=0.1609778510441976, pvalue=0.872176126799213)




```python
def gendata_14(loc1=0, loc2=0):
    population_n_14 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_14 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_14, population_a_14
population_n_14, population_a_14 = gendata_14(loc1=CY_14_mean, loc2=AAPL_14_mean)
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




    <matplotlib.legend.Legend at 0x1a1571e518>




![png](output_188_1.png)



```python
stats.ttest_ind(population_n_14, population_a_14, equal_var=False)
```




    Ttest_indResult(statistic=1.192853574817147, pvalue=0.23349473883880525)




```python
def gendata_15(loc1=0, loc2=0):
    population_n_15 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_15 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_15, population_a_15
population_n_15, population_a_15 = gendata_15(loc1=CY_15_mean, loc2=AAPL_15_mean)
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




    <matplotlib.legend.Legend at 0x1a15787a58>




![png](output_190_1.png)



```python
stats.ttest_ind(population_n_15, population_a_15, equal_var=False)
```




    Ttest_indResult(statistic=0.07273814066485942, pvalue=0.9420437013106098)




```python
def gendata_16(loc1=0, loc2=0):
    population_n_16 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_16 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_16, population_a_16
population_n_16, population_a_16 = gendata_16(loc1=CY_16_mean, loc2=AAPL_16_mean)
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




    <matplotlib.legend.Legend at 0x1a15a1bf98>




![png](output_192_1.png)



```python
stats.ttest_ind(population_n_16, population_a_16, equal_var=False)
```




    Ttest_indResult(statistic=0.44743714222261743, pvalue=0.6547540146306996)




```python
def gendata_17(loc1=0, loc2=0):
    population_n_17 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_17 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_17, population_a_17
population_n_17, population_a_17 = gendata_17(loc1=CY_17_mean, loc2=AAPL_17_mean)
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




    <matplotlib.legend.Legend at 0x1a15ba1518>




![png](output_194_1.png)



```python
stats.ttest_ind(population_n_17, population_a_17, equal_var=False)
```




    Ttest_indResult(statistic=2.2136609290925517, pvalue=0.02730450259367364)




```python
critical_value = stats.chi2.ppf(q = 0.95, df = 249)
critical_value
```




    286.807794444232




```python
stats.chisquare(df_CY_07['Diff'],)
```




    Power_divergenceResult(statistic=nan, pvalue=nan)




```python
data1 = pd.DataFrame(df_CY_07['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_CY_08['Diff']).assign(Location=2)
data3 = pd.DataFrame(df_CY_09['Diff']).assign(Location=3)



cdf = pd.concat([data1, data2, data3])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.146364
    2         1   Diff  0.106447
    3         1   Diff  0.262315
    4         1   Diff -0.157769



![png](output_198_1.png)



```python
data4 = pd.DataFrame(df_CY_10['Diff']).assign(Location=4)
data5 = pd.DataFrame(df_CY_11['Diff']).assign(Location=5)
data6 = pd.DataFrame(df_CY_12['Diff']).assign(Location=6)

cdf = pd.concat([data4, data5, data6])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         4   Diff       NaN
    1         4   Diff -0.157555
    2         4   Diff -0.015756
    3         4   Diff -0.181189
    4         4   Diff  0.023633



![png](output_199_1.png)



```python
data7 = pd.DataFrame(df_CY_13['Diff']).assign(Location=7)
data8 = pd.DataFrame(df_CY_14['Diff']).assign(Location=8)
data9 = pd.DataFrame(df_CY_15['Diff']).assign(Location=9)

cdf = pd.concat([data7, data8, data9])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         7   Diff       NaN
    1         7   Diff -0.060599
    2         7   Diff -0.121197
    3         7   Diff -0.051942
    4         7   Diff  0.095226



![png](output_200_1.png)



```python
data10 = pd.DataFrame(df_CY_16['Diff']).assign(Location=10)
data11 = pd.DataFrame(df_CY_17['Diff']).assign(Location=11)


cdf = pd.concat([data10, data11])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0        10   Diff       NaN
    1        10   Diff  0.087913
    2        10   Diff  0.019536
    3        10   Diff  0.126985
    4        10   Diff -0.091931



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
data1 = pd.DataFrame(df_CY_07['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_07['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.146364
    2         1   Diff  0.106447
    3         1   Diff  0.262315
    4         1   Diff -0.157769



![png](output_207_1.png)



```python
data1 = pd.DataFrame(df_CY_08['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_08['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff -0.322988
    2         1   Diff -0.149678
    3         1   Diff  0.102411
    4         1   Diff  0.007878



![png](output_208_1.png)



```python
data1 = pd.DataFrame(df_CY_09['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_09['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.173311
    2         1   Diff -0.220577
    3         1   Diff  0.047267
    4         1   Diff  0.133922



![png](output_209_1.png)



```python
data1 = pd.DataFrame(df_CY_10['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_10['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff -0.157555
    2         1   Diff -0.015756
    3         1   Diff -0.181189
    4         1   Diff  0.023633



![png](output_210_1.png)



```python
data1 = pd.DataFrame(df_CY_11['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_11['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff -0.039812
    2         1   Diff -0.191099
    3         1   Diff  0.262761
    4         1   Diff -0.019906



![png](output_211_1.png)



```python
data1 = pd.DataFrame(df_CY_12['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_12['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff -0.282103
    2         1   Diff  0.165943
    3         1   Diff  0.157646
    4         1   Diff  0.049783



![png](output_212_1.png)



```python
data1 = pd.DataFrame(df_CY_12['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_12['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff -0.282103
    2         1   Diff  0.165943
    3         1   Diff  0.157646
    4         1   Diff  0.049783



![png](output_213_1.png)



```python
data1 = pd.DataFrame(df_CY_13['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_13['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff -0.060599
    2         1   Diff -0.121197
    3         1   Diff -0.051942
    4         1   Diff  0.095226



![png](output_214_1.png)



```python
data1 = pd.DataFrame(df_CY_14['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_14['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.198011
    2         1   Diff  0.018001
    3         1   Diff  0.072004
    4         1   Diff  0.009001



![png](output_215_1.png)



```python
data1 = pd.DataFrame(df_CY_15['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_15['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.084199
    2         1   Diff  0.140332
    3         1   Diff -0.490471
    4         1   Diff  0.092542



![png](output_216_1.png)



```python
data1 = pd.DataFrame(df_CY_16['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_16['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.087913
    2         1   Diff  0.019536
    3         1   Diff  0.126985
    4         1   Diff -0.091931



![png](output_217_1.png)



```python
data1 = pd.DataFrame(df_CY_17['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_AAPL_17['Diff']).assign(Location=2)

cdf = pd.concat([data1, data2])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter  value
    0         1   Diff    NaN
    1         1   Diff   0.05
    2         1   Diff  -0.07
    3         1   Diff   0.11
    4         1   Diff  -0.02



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
