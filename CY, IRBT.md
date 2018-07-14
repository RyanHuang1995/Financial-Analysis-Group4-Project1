

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
df_IRBT_07 = web.DataReader('IRBT','quandl', start_07,end_07)
```


```python
df_IRBT_07 = web.DataReader('IRBT','quandl', start_07,end_07)
```


```python
df_IRBT_08 = web.DataReader('IRBT','quandl', start_08,end_08)
```


```python
df_IRBT_09 = web.DataReader('IRBT','quandl', start_09,end_09)
```


```python
df_IRBT_10 = web.DataReader('IRBT','quandl', start_10,end_10)
```


```python
df_IRBT_11 = web.DataReader('IRBT','quandl', start_11,end_11)
```


```python
df_IRBT_12 = web.DataReader('IRBT','quandl', start_12,end_12)
```


```python
df_IRBT_13 = web.DataReader('IRBT','quandl', start_13,end_13)
```


```python
df_IRBT_14 = web.DataReader('IRBT','quandl', start_14,end_14)
```


```python
df_IRBT_15 = web.DataReader('IRBT','quandl', start_15,end_15)
```


```python
df_IRBT_16 = web.DataReader('IRBT','quandl', start_16,end_16)
```


```python
df_IRBT_17 = web.DataReader('IRBT','quandl', start_17,end_17)
```


```python
plt.plot(df_CY_07.index,df_CY_07['AdjClose'], c='r')
plt.plot(df_IRBT_07.index,df_IRBT_07['AdjClose'], c='g')
plt.show()
```


![png](output_68_0.png)



```python
plt.plot(df_CY_08.index,df_CY_08['AdjClose'], c='r')
plt.plot(df_IRBT_08.index,df_IRBT_08['AdjClose'], c='g')
plt.show()
```


![png](output_69_0.png)



```python
plt.plot(df_CY_09.index,df_CY_09['AdjClose'], c='r')
plt.plot(df_IRBT_09.index,df_IRBT_09['AdjClose'], c='g')
plt.show()
```


![png](output_70_0.png)



```python
plt.plot(df_CY_10.index,df_CY_10['AdjClose'], c='r')
plt.plot(df_IRBT_10.index,df_IRBT_10['AdjClose'], c='g')
plt.show()
```


![png](output_71_0.png)



```python
plt.plot(df_CY_11.index,df_CY_11['AdjClose'], c='r')
plt.plot(df_IRBT_11.index,df_IRBT_11['AdjClose'], c='g')
plt.show()
```


![png](output_72_0.png)



```python
plt.plot(df_CY_12.index,df_CY_12['AdjClose'], c='r')
plt.plot(df_IRBT_12.index,df_IRBT_12['AdjClose'], c='g')
plt.show()
```


![png](output_73_0.png)



```python
plt.plot(df_CY_13.index,df_CY_13['AdjClose'], c='r')
plt.plot(df_IRBT_13.index,df_IRBT_13['AdjClose'], c='g')
plt.show()
```


![png](output_74_0.png)



```python
plt.plot(df_CY_14.index,df_CY_14['AdjClose'], c='r')
plt.plot(df_IRBT_14.index,df_IRBT_14['AdjClose'], c='g')
plt.show()
```


![png](output_75_0.png)



```python
plt.plot(df_CY_15.index,df_CY_15['AdjClose'], c='r')
plt.plot(df_IRBT_15.index,df_IRBT_15['AdjClose'], c='g')
plt.show()
```


![png](output_76_0.png)



```python
plt.plot(df_CY_16.index,df_CY_16['AdjClose'], c='r')
plt.plot(df_IRBT_16.index,df_IRBT_16['AdjClose'], c='g')
plt.show()
```


![png](output_77_0.png)



```python
plt.plot(df_CY_17.index,df_CY_17['AdjClose'], c='r')
plt.plot(df_IRBT_17.index,df_IRBT_17['AdjClose'], c='g')
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
df_IRBT_07.head()
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
      <td>18.03</td>
      <td>18.1600</td>
      <td>17.8500</td>
      <td>18.08</td>
      <td>307900.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>18.03</td>
      <td>18.1600</td>
      <td>17.8500</td>
      <td>18.08</td>
      <td>307900.0</td>
    </tr>
    <tr>
      <th>2007-12-28</th>
      <td>18.02</td>
      <td>18.3799</td>
      <td>17.9500</td>
      <td>18.04</td>
      <td>213300.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>18.02</td>
      <td>18.3799</td>
      <td>17.9500</td>
      <td>18.04</td>
      <td>213300.0</td>
    </tr>
    <tr>
      <th>2007-12-27</th>
      <td>18.25</td>
      <td>18.3700</td>
      <td>17.9201</td>
      <td>17.97</td>
      <td>232000.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>18.25</td>
      <td>18.3700</td>
      <td>17.9201</td>
      <td>17.97</td>
      <td>232000.0</td>
    </tr>
    <tr>
      <th>2007-12-26</th>
      <td>18.00</td>
      <td>18.4700</td>
      <td>18.0000</td>
      <td>18.34</td>
      <td>177500.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>18.00</td>
      <td>18.4700</td>
      <td>18.0000</td>
      <td>18.34</td>
      <td>177500.0</td>
    </tr>
    <tr>
      <th>2007-12-24</th>
      <td>18.07</td>
      <td>18.1900</td>
      <td>18.0000</td>
      <td>18.19</td>
      <td>78300.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>18.07</td>
      <td>18.1900</td>
      <td>18.0000</td>
      <td>18.19</td>
      <td>78300.0</td>
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
df_IRBT_07['Diff'] = df_IRBT_07['AdjClose'] - df_IRBT_07['AdjClose'].shift(1)
df_IRBT_08['Diff'] = df_IRBT_08['AdjClose'] - df_IRBT_08['AdjClose'].shift(1)
df_IRBT_09['Diff'] = df_IRBT_09['AdjClose'] - df_IRBT_09['AdjClose'].shift(1)
df_IRBT_10['Diff'] = df_IRBT_10['AdjClose'] - df_IRBT_10['AdjClose'].shift(1)
df_IRBT_11['Diff'] = df_IRBT_11['AdjClose'] - df_IRBT_11['AdjClose'].shift(1)
df_IRBT_12['Diff'] = df_IRBT_12['AdjClose'] - df_IRBT_12['AdjClose'].shift(1)
df_IRBT_13['Diff'] = df_IRBT_13['AdjClose'] - df_IRBT_13['AdjClose'].shift(1)
df_IRBT_14['Diff'] = df_IRBT_14['AdjClose'] - df_IRBT_14['AdjClose'].shift(1)
df_IRBT_15['Diff'] = df_IRBT_15['AdjClose'] - df_IRBT_15['AdjClose'].shift(1)
df_IRBT_16['Diff'] = df_IRBT_16['AdjClose'] - df_IRBT_16['AdjClose'].shift(1)
df_IRBT_17['Diff'] = df_IRBT_17['AdjClose'] - df_IRBT_17['AdjClose'].shift(1)
df_IRBT_07.head()
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
      <td>18.03</td>
      <td>18.1600</td>
      <td>17.8500</td>
      <td>18.08</td>
      <td>307900.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>18.03</td>
      <td>18.1600</td>
      <td>17.8500</td>
      <td>18.08</td>
      <td>307900.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2007-12-28</th>
      <td>18.02</td>
      <td>18.3799</td>
      <td>17.9500</td>
      <td>18.04</td>
      <td>213300.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>18.02</td>
      <td>18.3799</td>
      <td>17.9500</td>
      <td>18.04</td>
      <td>213300.0</td>
      <td>-0.04</td>
    </tr>
    <tr>
      <th>2007-12-27</th>
      <td>18.25</td>
      <td>18.3700</td>
      <td>17.9201</td>
      <td>17.97</td>
      <td>232000.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>18.25</td>
      <td>18.3700</td>
      <td>17.9201</td>
      <td>17.97</td>
      <td>232000.0</td>
      <td>-0.07</td>
    </tr>
    <tr>
      <th>2007-12-26</th>
      <td>18.00</td>
      <td>18.4700</td>
      <td>18.0000</td>
      <td>18.34</td>
      <td>177500.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>18.00</td>
      <td>18.4700</td>
      <td>18.0000</td>
      <td>18.34</td>
      <td>177500.0</td>
      <td>0.37</td>
    </tr>
    <tr>
      <th>2007-12-24</th>
      <td>18.07</td>
      <td>18.1900</td>
      <td>18.0000</td>
      <td>18.19</td>
      <td>78300.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>18.07</td>
      <td>18.1900</td>
      <td>18.0000</td>
      <td>18.19</td>
      <td>78300.0</td>
      <td>-0.15</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_IRBT_17
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
      <td>79.160</td>
      <td>79.1600</td>
      <td>76.7000</td>
      <td>76.700</td>
      <td>529077.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>79.160</td>
      <td>79.1600</td>
      <td>76.7000</td>
      <td>76.700</td>
      <td>529077.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2017-12-28</th>
      <td>80.390</td>
      <td>80.3900</td>
      <td>78.1900</td>
      <td>78.970</td>
      <td>514815.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>80.390</td>
      <td>80.3900</td>
      <td>78.1900</td>
      <td>78.970</td>
      <td>514815.0</td>
      <td>2.270</td>
    </tr>
    <tr>
      <th>2017-12-27</th>
      <td>80.110</td>
      <td>81.1590</td>
      <td>79.9500</td>
      <td>80.040</td>
      <td>486344.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>80.110</td>
      <td>81.1590</td>
      <td>79.9500</td>
      <td>80.040</td>
      <td>486344.0</td>
      <td>1.070</td>
    </tr>
    <tr>
      <th>2017-12-26</th>
      <td>79.240</td>
      <td>80.2400</td>
      <td>78.8400</td>
      <td>80.110</td>
      <td>617933.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>79.240</td>
      <td>80.2400</td>
      <td>78.8400</td>
      <td>80.110</td>
      <td>617933.0</td>
      <td>0.070</td>
    </tr>
    <tr>
      <th>2017-12-22</th>
      <td>79.000</td>
      <td>80.0000</td>
      <td>77.5010</td>
      <td>79.520</td>
      <td>606920.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>79.000</td>
      <td>80.0000</td>
      <td>77.5010</td>
      <td>79.520</td>
      <td>606920.0</td>
      <td>-0.590</td>
    </tr>
    <tr>
      <th>2017-12-21</th>
      <td>77.650</td>
      <td>79.4700</td>
      <td>77.2900</td>
      <td>79.240</td>
      <td>720397.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>77.650</td>
      <td>79.4700</td>
      <td>77.2900</td>
      <td>79.240</td>
      <td>720397.0</td>
      <td>-0.280</td>
    </tr>
    <tr>
      <th>2017-12-20</th>
      <td>77.140</td>
      <td>77.5700</td>
      <td>76.1700</td>
      <td>77.560</td>
      <td>650481.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>77.140</td>
      <td>77.5700</td>
      <td>76.1700</td>
      <td>77.560</td>
      <td>650481.0</td>
      <td>-1.680</td>
    </tr>
    <tr>
      <th>2017-12-19</th>
      <td>75.000</td>
      <td>77.4500</td>
      <td>74.8780</td>
      <td>77.140</td>
      <td>959659.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>75.000</td>
      <td>77.4500</td>
      <td>74.8780</td>
      <td>77.140</td>
      <td>959659.0</td>
      <td>-0.420</td>
    </tr>
    <tr>
      <th>2017-12-18</th>
      <td>75.070</td>
      <td>76.7900</td>
      <td>73.4600</td>
      <td>74.730</td>
      <td>1345462.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>75.070</td>
      <td>76.7900</td>
      <td>73.4600</td>
      <td>74.730</td>
      <td>1345462.0</td>
      <td>-2.410</td>
    </tr>
    <tr>
      <th>2017-12-15</th>
      <td>73.250</td>
      <td>74.4300</td>
      <td>73.2000</td>
      <td>74.430</td>
      <td>1949507.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>73.250</td>
      <td>74.4300</td>
      <td>73.2000</td>
      <td>74.430</td>
      <td>1949507.0</td>
      <td>-0.300</td>
    </tr>
    <tr>
      <th>2017-12-14</th>
      <td>74.000</td>
      <td>74.6900</td>
      <td>72.0000</td>
      <td>73.220</td>
      <td>1333400.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>74.000</td>
      <td>74.6900</td>
      <td>72.0000</td>
      <td>73.220</td>
      <td>1333400.0</td>
      <td>-1.210</td>
    </tr>
    <tr>
      <th>2017-12-13</th>
      <td>70.480</td>
      <td>74.2500</td>
      <td>70.2400</td>
      <td>74.030</td>
      <td>1971182.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>70.480</td>
      <td>74.2500</td>
      <td>70.2400</td>
      <td>74.030</td>
      <td>1971182.0</td>
      <td>0.810</td>
    </tr>
    <tr>
      <th>2017-12-12</th>
      <td>66.220</td>
      <td>70.9700</td>
      <td>65.9700</td>
      <td>70.400</td>
      <td>1503111.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>66.220</td>
      <td>70.9700</td>
      <td>65.9700</td>
      <td>70.400</td>
      <td>1503111.0</td>
      <td>-3.630</td>
    </tr>
    <tr>
      <th>2017-12-11</th>
      <td>66.630</td>
      <td>66.6350</td>
      <td>64.4500</td>
      <td>66.340</td>
      <td>1087420.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>66.630</td>
      <td>66.6350</td>
      <td>64.4500</td>
      <td>66.340</td>
      <td>1087420.0</td>
      <td>-4.060</td>
    </tr>
    <tr>
      <th>2017-12-08</th>
      <td>67.590</td>
      <td>68.7500</td>
      <td>65.9950</td>
      <td>66.770</td>
      <td>1036447.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>67.590</td>
      <td>68.7500</td>
      <td>65.9950</td>
      <td>66.770</td>
      <td>1036447.0</td>
      <td>0.430</td>
    </tr>
    <tr>
      <th>2017-12-07</th>
      <td>64.920</td>
      <td>67.1600</td>
      <td>64.6500</td>
      <td>66.850</td>
      <td>1140285.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>64.920</td>
      <td>67.1600</td>
      <td>64.6500</td>
      <td>66.850</td>
      <td>1140285.0</td>
      <td>0.080</td>
    </tr>
    <tr>
      <th>2017-12-06</th>
      <td>65.000</td>
      <td>66.4500</td>
      <td>64.7700</td>
      <td>65.030</td>
      <td>818651.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>65.000</td>
      <td>66.4500</td>
      <td>64.7700</td>
      <td>65.030</td>
      <td>818651.0</td>
      <td>-1.820</td>
    </tr>
    <tr>
      <th>2017-12-05</th>
      <td>64.440</td>
      <td>65.8770</td>
      <td>63.0000</td>
      <td>65.230</td>
      <td>1097056.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>64.440</td>
      <td>65.8770</td>
      <td>63.0000</td>
      <td>65.230</td>
      <td>1097056.0</td>
      <td>0.200</td>
    </tr>
    <tr>
      <th>2017-12-04</th>
      <td>66.900</td>
      <td>66.9000</td>
      <td>63.6600</td>
      <td>64.580</td>
      <td>968494.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>66.900</td>
      <td>66.9000</td>
      <td>63.6600</td>
      <td>64.580</td>
      <td>968494.0</td>
      <td>-0.650</td>
    </tr>
    <tr>
      <th>2017-12-01</th>
      <td>68.640</td>
      <td>68.6700</td>
      <td>64.2700</td>
      <td>65.990</td>
      <td>1222877.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>68.640</td>
      <td>68.6700</td>
      <td>64.2700</td>
      <td>65.990</td>
      <td>1222877.0</td>
      <td>1.410</td>
    </tr>
    <tr>
      <th>2017-11-30</th>
      <td>67.800</td>
      <td>68.9590</td>
      <td>65.8700</td>
      <td>68.620</td>
      <td>693595.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>67.800</td>
      <td>68.9590</td>
      <td>65.8700</td>
      <td>68.620</td>
      <td>693595.0</td>
      <td>2.630</td>
    </tr>
    <tr>
      <th>2017-11-29</th>
      <td>67.940</td>
      <td>68.6000</td>
      <td>65.2100</td>
      <td>67.650</td>
      <td>899331.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>67.940</td>
      <td>68.6000</td>
      <td>65.2100</td>
      <td>67.650</td>
      <td>899331.0</td>
      <td>-0.970</td>
    </tr>
    <tr>
      <th>2017-11-28</th>
      <td>69.490</td>
      <td>69.8900</td>
      <td>67.7690</td>
      <td>68.140</td>
      <td>612159.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>69.490</td>
      <td>69.8900</td>
      <td>67.7690</td>
      <td>68.140</td>
      <td>612159.0</td>
      <td>0.490</td>
    </tr>
    <tr>
      <th>2017-11-27</th>
      <td>68.500</td>
      <td>70.4900</td>
      <td>68.5000</td>
      <td>69.600</td>
      <td>775341.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>68.500</td>
      <td>70.4900</td>
      <td>68.5000</td>
      <td>69.600</td>
      <td>775341.0</td>
      <td>1.460</td>
    </tr>
    <tr>
      <th>2017-11-24</th>
      <td>68.800</td>
      <td>69.3565</td>
      <td>67.3400</td>
      <td>68.370</td>
      <td>367516.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>68.800</td>
      <td>69.3565</td>
      <td>67.3400</td>
      <td>68.370</td>
      <td>367516.0</td>
      <td>-1.230</td>
    </tr>
    <tr>
      <th>2017-11-22</th>
      <td>73.240</td>
      <td>73.2800</td>
      <td>66.0000</td>
      <td>68.500</td>
      <td>2117874.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>73.240</td>
      <td>73.2800</td>
      <td>66.0000</td>
      <td>68.500</td>
      <td>2117874.0</td>
      <td>0.130</td>
    </tr>
    <tr>
      <th>2017-11-21</th>
      <td>72.320</td>
      <td>73.2000</td>
      <td>72.1800</td>
      <td>73.070</td>
      <td>421733.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>72.320</td>
      <td>73.2000</td>
      <td>72.1800</td>
      <td>73.070</td>
      <td>421733.0</td>
      <td>4.570</td>
    </tr>
    <tr>
      <th>2017-11-20</th>
      <td>71.610</td>
      <td>72.2200</td>
      <td>70.6100</td>
      <td>72.120</td>
      <td>474959.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>71.610</td>
      <td>72.2200</td>
      <td>70.6100</td>
      <td>72.120</td>
      <td>474959.0</td>
      <td>-0.950</td>
    </tr>
    <tr>
      <th>2017-11-17</th>
      <td>70.640</td>
      <td>72.1700</td>
      <td>70.5100</td>
      <td>71.450</td>
      <td>824481.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>70.640</td>
      <td>72.1700</td>
      <td>70.5100</td>
      <td>71.450</td>
      <td>824481.0</td>
      <td>-0.670</td>
    </tr>
    <tr>
      <th>2017-11-16</th>
      <td>69.110</td>
      <td>71.1000</td>
      <td>69.0000</td>
      <td>70.710</td>
      <td>757236.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>69.110</td>
      <td>71.1000</td>
      <td>69.0000</td>
      <td>70.710</td>
      <td>757236.0</td>
      <td>-0.740</td>
    </tr>
    <tr>
      <th>2017-11-15</th>
      <td>68.200</td>
      <td>68.7900</td>
      <td>66.6600</td>
      <td>68.260</td>
      <td>584924.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>68.200</td>
      <td>68.7900</td>
      <td>66.6600</td>
      <td>68.260</td>
      <td>584924.0</td>
      <td>-2.450</td>
    </tr>
    <tr>
      <th>2017-11-14</th>
      <td>69.780</td>
      <td>72.7500</td>
      <td>68.7600</td>
      <td>68.790</td>
      <td>1309238.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>69.780</td>
      <td>72.7500</td>
      <td>68.7600</td>
      <td>68.790</td>
      <td>1309238.0</td>
      <td>0.530</td>
    </tr>
    <tr>
      <th>2017-11-13</th>
      <td>68.500</td>
      <td>70.2100</td>
      <td>67.7600</td>
      <td>70.090</td>
      <td>579251.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>68.500</td>
      <td>70.2100</td>
      <td>67.7600</td>
      <td>70.090</td>
      <td>579251.0</td>
      <td>1.300</td>
    </tr>
    <tr>
      <th>2017-11-10</th>
      <td>67.790</td>
      <td>69.2600</td>
      <td>67.7404</td>
      <td>68.800</td>
      <td>489914.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>67.790</td>
      <td>69.2600</td>
      <td>67.7404</td>
      <td>68.800</td>
      <td>489914.0</td>
      <td>-1.290</td>
    </tr>
    <tr>
      <th>2017-11-09</th>
      <td>67.640</td>
      <td>68.6500</td>
      <td>67.0500</td>
      <td>67.790</td>
      <td>539449.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>67.640</td>
      <td>68.6500</td>
      <td>67.0500</td>
      <td>67.790</td>
      <td>539449.0</td>
      <td>-1.010</td>
    </tr>
    <tr>
      <th>2017-11-07</th>
      <td>68.600</td>
      <td>69.0000</td>
      <td>66.9700</td>
      <td>67.000</td>
      <td>1039854.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>68.600</td>
      <td>69.0000</td>
      <td>66.9700</td>
      <td>67.000</td>
      <td>1039854.0</td>
      <td>-0.790</td>
    </tr>
    <tr>
      <th>2017-11-06</th>
      <td>67.550</td>
      <td>68.9100</td>
      <td>67.4400</td>
      <td>68.550</td>
      <td>712638.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>67.550</td>
      <td>68.9100</td>
      <td>67.4400</td>
      <td>68.550</td>
      <td>712638.0</td>
      <td>1.550</td>
    </tr>
    <tr>
      <th>2017-11-03</th>
      <td>67.100</td>
      <td>68.4200</td>
      <td>66.4000</td>
      <td>67.400</td>
      <td>1053277.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>67.100</td>
      <td>68.4200</td>
      <td>66.4000</td>
      <td>67.400</td>
      <td>1053277.0</td>
      <td>-1.150</td>
    </tr>
    <tr>
      <th>2017-11-02</th>
      <td>66.310</td>
      <td>67.6800</td>
      <td>66.2100</td>
      <td>66.850</td>
      <td>1029113.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>66.310</td>
      <td>67.6800</td>
      <td>66.2100</td>
      <td>66.850</td>
      <td>1029113.0</td>
      <td>-0.550</td>
    </tr>
    <tr>
      <th>2017-11-01</th>
      <td>67.060</td>
      <td>67.8080</td>
      <td>66.2000</td>
      <td>66.670</td>
      <td>789521.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>67.060</td>
      <td>67.8080</td>
      <td>66.2000</td>
      <td>66.670</td>
      <td>789521.0</td>
      <td>-0.180</td>
    </tr>
    <tr>
      <th>2017-10-31</th>
      <td>64.650</td>
      <td>68.0000</td>
      <td>64.5000</td>
      <td>67.190</td>
      <td>1398954.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>64.650</td>
      <td>68.0000</td>
      <td>64.5000</td>
      <td>67.190</td>
      <td>1398954.0</td>
      <td>0.520</td>
    </tr>
    <tr>
      <th>2017-10-30</th>
      <td>66.190</td>
      <td>66.9800</td>
      <td>62.9600</td>
      <td>64.650</td>
      <td>1389113.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>66.190</td>
      <td>66.9800</td>
      <td>62.9600</td>
      <td>64.650</td>
      <td>1389113.0</td>
      <td>-2.540</td>
    </tr>
    <tr>
      <th>2017-10-27</th>
      <td>65.000</td>
      <td>67.6600</td>
      <td>64.5200</td>
      <td>66.670</td>
      <td>1892922.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>65.000</td>
      <td>67.6600</td>
      <td>64.5200</td>
      <td>66.670</td>
      <td>1892922.0</td>
      <td>2.020</td>
    </tr>
    <tr>
      <th>2017-10-26</th>
      <td>65.720</td>
      <td>65.8400</td>
      <td>63.0000</td>
      <td>63.375</td>
      <td>2487182.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>65.720</td>
      <td>65.8400</td>
      <td>63.0000</td>
      <td>63.375</td>
      <td>2487182.0</td>
      <td>-3.295</td>
    </tr>
    <tr>
      <th>2017-10-25</th>
      <td>80.220</td>
      <td>81.9317</td>
      <td>64.7900</td>
      <td>65.110</td>
      <td>8161206.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>80.220</td>
      <td>81.9317</td>
      <td>64.7900</td>
      <td>65.110</td>
      <td>8161206.0</td>
      <td>1.735</td>
    </tr>
    <tr>
      <th>2017-10-24</th>
      <td>75.010</td>
      <td>76.3500</td>
      <td>73.6300</td>
      <td>75.260</td>
      <td>1984244.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>75.010</td>
      <td>76.3500</td>
      <td>73.6300</td>
      <td>75.260</td>
      <td>1984244.0</td>
      <td>10.150</td>
    </tr>
    <tr>
      <th>2017-10-23</th>
      <td>77.000</td>
      <td>77.0000</td>
      <td>74.0500</td>
      <td>74.830</td>
      <td>1161598.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>77.000</td>
      <td>77.0000</td>
      <td>74.0500</td>
      <td>74.830</td>
      <td>1161598.0</td>
      <td>-0.430</td>
    </tr>
    <tr>
      <th>2017-10-20</th>
      <td>76.530</td>
      <td>77.2900</td>
      <td>75.4100</td>
      <td>76.250</td>
      <td>789073.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>76.530</td>
      <td>77.2900</td>
      <td>75.4100</td>
      <td>76.250</td>
      <td>789073.0</td>
      <td>1.420</td>
    </tr>
    <tr>
      <th>2017-10-19</th>
      <td>76.170</td>
      <td>76.5500</td>
      <td>74.5400</td>
      <td>75.900</td>
      <td>603903.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>76.170</td>
      <td>76.5500</td>
      <td>74.5400</td>
      <td>75.900</td>
      <td>603903.0</td>
      <td>-0.350</td>
    </tr>
    <tr>
      <th>2017-10-18</th>
      <td>77.020</td>
      <td>78.4100</td>
      <td>76.1600</td>
      <td>76.830</td>
      <td>790427.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>77.020</td>
      <td>78.4100</td>
      <td>76.1600</td>
      <td>76.830</td>
      <td>790427.0</td>
      <td>0.930</td>
    </tr>
    <tr>
      <th>2017-10-17</th>
      <td>75.290</td>
      <td>76.6090</td>
      <td>74.2600</td>
      <td>76.430</td>
      <td>1330307.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>75.290</td>
      <td>76.6090</td>
      <td>74.2600</td>
      <td>76.430</td>
      <td>1330307.0</td>
      <td>-0.400</td>
    </tr>
    <tr>
      <th>2017-10-16</th>
      <td>77.000</td>
      <td>77.9500</td>
      <td>75.4200</td>
      <td>75.510</td>
      <td>636799.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>77.000</td>
      <td>77.9500</td>
      <td>75.4200</td>
      <td>75.510</td>
      <td>636799.0</td>
      <td>-0.920</td>
    </tr>
    <tr>
      <th>2017-10-13</th>
      <td>78.620</td>
      <td>78.7300</td>
      <td>76.1400</td>
      <td>76.620</td>
      <td>773837.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>78.620</td>
      <td>78.7300</td>
      <td>76.1400</td>
      <td>76.620</td>
      <td>773837.0</td>
      <td>1.110</td>
    </tr>
    <tr>
      <th>2017-10-12</th>
      <td>77.160</td>
      <td>79.6000</td>
      <td>76.8000</td>
      <td>78.970</td>
      <td>802932.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>77.160</td>
      <td>79.6000</td>
      <td>76.8000</td>
      <td>78.970</td>
      <td>802932.0</td>
      <td>2.350</td>
    </tr>
    <tr>
      <th>2017-10-11</th>
      <td>77.790</td>
      <td>78.0160</td>
      <td>75.4500</td>
      <td>77.070</td>
      <td>655295.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>77.790</td>
      <td>78.0160</td>
      <td>75.4500</td>
      <td>77.070</td>
      <td>655295.0</td>
      <td>-1.900</td>
    </tr>
    <tr>
      <th>2017-10-10</th>
      <td>77.000</td>
      <td>77.8800</td>
      <td>76.4100</td>
      <td>77.520</td>
      <td>524913.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>77.000</td>
      <td>77.8800</td>
      <td>76.4100</td>
      <td>77.520</td>
      <td>524913.0</td>
      <td>0.450</td>
    </tr>
    <tr>
      <th>2017-10-09</th>
      <td>75.620</td>
      <td>77.6800</td>
      <td>75.6200</td>
      <td>77.220</td>
      <td>651155.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>75.620</td>
      <td>77.6800</td>
      <td>75.6200</td>
      <td>77.220</td>
      <td>651155.0</td>
      <td>-0.300</td>
    </tr>
    <tr>
      <th>2017-10-06</th>
      <td>75.000</td>
      <td>76.3300</td>
      <td>75.0000</td>
      <td>75.620</td>
      <td>891637.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>75.000</td>
      <td>76.3300</td>
      <td>75.0000</td>
      <td>75.620</td>
      <td>891637.0</td>
      <td>-1.600</td>
    </tr>
    <tr>
      <th>2017-10-05</th>
      <td>78.440</td>
      <td>78.8200</td>
      <td>75.1600</td>
      <td>75.340</td>
      <td>743003.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>78.440</td>
      <td>78.8200</td>
      <td>75.1600</td>
      <td>75.340</td>
      <td>743003.0</td>
      <td>-0.280</td>
    </tr>
    <tr>
      <th>2017-10-04</th>
      <td>79.840</td>
      <td>80.1000</td>
      <td>77.8400</td>
      <td>78.290</td>
      <td>491745.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>79.840</td>
      <td>80.1000</td>
      <td>77.8400</td>
      <td>78.290</td>
      <td>491745.0</td>
      <td>2.950</td>
    </tr>
    <tr>
      <th>2017-10-03</th>
      <td>79.500</td>
      <td>80.2800</td>
      <td>78.5200</td>
      <td>79.610</td>
      <td>515513.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>79.500</td>
      <td>80.2800</td>
      <td>78.5200</td>
      <td>79.610</td>
      <td>515513.0</td>
      <td>1.320</td>
    </tr>
    <tr>
      <th>2017-10-02</th>
      <td>77.000</td>
      <td>79.3990</td>
      <td>77.0000</td>
      <td>79.200</td>
      <td>670046.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>77.000</td>
      <td>79.3990</td>
      <td>77.0000</td>
      <td>79.200</td>
      <td>670046.0</td>
      <td>-0.410</td>
    </tr>
    <tr>
      <th>2017-09-29</th>
      <td>77.000</td>
      <td>78.0000</td>
      <td>76.4800</td>
      <td>77.060</td>
      <td>733407.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>77.000</td>
      <td>78.0000</td>
      <td>76.4800</td>
      <td>77.060</td>
      <td>733407.0</td>
      <td>-2.140</td>
    </tr>
    <tr>
      <th>2017-09-28</th>
      <td>79.400</td>
      <td>81.4000</td>
      <td>76.5000</td>
      <td>76.670</td>
      <td>1237577.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>79.400</td>
      <td>81.4000</td>
      <td>76.5000</td>
      <td>76.670</td>
      <td>1237577.0</td>
      <td>-0.390</td>
    </tr>
    <tr>
      <th>2017-09-27</th>
      <td>77.280</td>
      <td>80.0899</td>
      <td>77.2800</td>
      <td>79.460</td>
      <td>835527.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>77.280</td>
      <td>80.0899</td>
      <td>77.2800</td>
      <td>79.460</td>
      <td>835527.0</td>
      <td>2.790</td>
    </tr>
    <tr>
      <th>2017-09-26</th>
      <td>73.860</td>
      <td>78.0700</td>
      <td>73.5900</td>
      <td>77.100</td>
      <td>1111354.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>73.860</td>
      <td>78.0700</td>
      <td>73.5900</td>
      <td>77.100</td>
      <td>1111354.0</td>
      <td>-2.360</td>
    </tr>
    <tr>
      <th>2017-09-25</th>
      <td>74.580</td>
      <td>75.2900</td>
      <td>72.6300</td>
      <td>73.760</td>
      <td>1215027.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>74.580</td>
      <td>75.2900</td>
      <td>72.6300</td>
      <td>73.760</td>
      <td>1215027.0</td>
      <td>-3.340</td>
    </tr>
    <tr>
      <th>2017-09-22</th>
      <td>79.980</td>
      <td>80.4931</td>
      <td>74.8600</td>
      <td>76.140</td>
      <td>1677063.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>79.980</td>
      <td>80.4931</td>
      <td>74.8600</td>
      <td>76.140</td>
      <td>1677063.0</td>
      <td>2.380</td>
    </tr>
    <tr>
      <th>2017-09-21</th>
      <td>80.020</td>
      <td>81.2000</td>
      <td>79.1516</td>
      <td>79.940</td>
      <td>673355.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>80.020</td>
      <td>81.2000</td>
      <td>79.1516</td>
      <td>79.940</td>
      <td>673355.0</td>
      <td>3.800</td>
    </tr>
    <tr>
      <th>2017-09-20</th>
      <td>82.450</td>
      <td>83.2089</td>
      <td>79.1274</td>
      <td>79.990</td>
      <td>1073755.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>82.450</td>
      <td>83.2089</td>
      <td>79.1274</td>
      <td>79.990</td>
      <td>1073755.0</td>
      <td>0.050</td>
    </tr>
    <tr>
      <th>2017-09-19</th>
      <td>82.000</td>
      <td>83.4800</td>
      <td>81.8271</td>
      <td>82.690</td>
      <td>903917.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>82.000</td>
      <td>83.4800</td>
      <td>81.8271</td>
      <td>82.690</td>
      <td>903917.0</td>
      <td>2.700</td>
    </tr>
    <tr>
      <th>2017-09-18</th>
      <td>80.120</td>
      <td>82.2100</td>
      <td>79.0000</td>
      <td>81.200</td>
      <td>1343590.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>80.120</td>
      <td>82.2100</td>
      <td>79.0000</td>
      <td>81.200</td>
      <td>1343590.0</td>
      <td>-1.490</td>
    </tr>
    <tr>
      <th>2017-09-15</th>
      <td>82.930</td>
      <td>83.5900</td>
      <td>79.1900</td>
      <td>79.810</td>
      <td>2617326.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>82.930</td>
      <td>83.5900</td>
      <td>79.1900</td>
      <td>79.810</td>
      <td>2617326.0</td>
      <td>-1.390</td>
    </tr>
    <tr>
      <th>2017-09-14</th>
      <td>86.480</td>
      <td>87.4900</td>
      <td>80.1200</td>
      <td>81.850</td>
      <td>3550508.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>86.480</td>
      <td>87.4900</td>
      <td>80.1200</td>
      <td>81.850</td>
      <td>3550508.0</td>
      <td>2.040</td>
    </tr>
    <tr>
      <th>2017-09-13</th>
      <td>100.250</td>
      <td>100.5000</td>
      <td>84.7000</td>
      <td>85.080</td>
      <td>6514616.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>100.250</td>
      <td>100.5000</td>
      <td>84.7000</td>
      <td>85.080</td>
      <td>6514616.0</td>
      <td>3.230</td>
    </tr>
    <tr>
      <th>2017-09-12</th>
      <td>95.890</td>
      <td>100.9600</td>
      <td>95.8900</td>
      <td>100.870</td>
      <td>734405.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>95.890</td>
      <td>100.9600</td>
      <td>95.8900</td>
      <td>100.870</td>
      <td>734405.0</td>
      <td>15.790</td>
    </tr>
    <tr>
      <th>2017-09-11</th>
      <td>95.880</td>
      <td>97.9900</td>
      <td>95.8800</td>
      <td>96.780</td>
      <td>424756.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>95.880</td>
      <td>97.9900</td>
      <td>95.8800</td>
      <td>96.780</td>
      <td>424756.0</td>
      <td>-4.090</td>
    </tr>
    <tr>
      <th>2017-09-08</th>
      <td>96.000</td>
      <td>97.0750</td>
      <td>95.0600</td>
      <td>95.170</td>
      <td>458203.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>96.000</td>
      <td>97.0750</td>
      <td>95.0600</td>
      <td>95.170</td>
      <td>458203.0</td>
      <td>-1.610</td>
    </tr>
    <tr>
      <th>2017-09-07</th>
      <td>94.700</td>
      <td>96.5800</td>
      <td>94.1100</td>
      <td>96.550</td>
      <td>508457.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>94.700</td>
      <td>96.5800</td>
      <td>94.1100</td>
      <td>96.550</td>
      <td>508457.0</td>
      <td>1.380</td>
    </tr>
    <tr>
      <th>2017-09-06</th>
      <td>95.410</td>
      <td>96.8306</td>
      <td>93.3800</td>
      <td>94.880</td>
      <td>555109.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>95.410</td>
      <td>96.8306</td>
      <td>93.3800</td>
      <td>94.880</td>
      <td>555109.0</td>
      <td>-1.670</td>
    </tr>
    <tr>
      <th>2017-09-05</th>
      <td>96.780</td>
      <td>97.0100</td>
      <td>94.8910</td>
      <td>96.040</td>
      <td>484772.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>96.780</td>
      <td>97.0100</td>
      <td>94.8910</td>
      <td>96.040</td>
      <td>484772.0</td>
      <td>1.160</td>
    </tr>
    <tr>
      <th>2017-09-01</th>
      <td>95.750</td>
      <td>96.9900</td>
      <td>95.4000</td>
      <td>96.700</td>
      <td>471978.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>95.750</td>
      <td>96.9900</td>
      <td>95.4000</td>
      <td>96.700</td>
      <td>471978.0</td>
      <td>0.660</td>
    </tr>
    <tr>
      <th>2017-08-31</th>
      <td>94.590</td>
      <td>95.5000</td>
      <td>93.0500</td>
      <td>95.420</td>
      <td>527366.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>94.590</td>
      <td>95.5000</td>
      <td>93.0500</td>
      <td>95.420</td>
      <td>527366.0</td>
      <td>-1.280</td>
    </tr>
    <tr>
      <th>2017-08-30</th>
      <td>93.080</td>
      <td>94.3200</td>
      <td>92.9110</td>
      <td>93.920</td>
      <td>332901.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>93.080</td>
      <td>94.3200</td>
      <td>92.9110</td>
      <td>93.920</td>
      <td>332901.0</td>
      <td>-1.500</td>
    </tr>
    <tr>
      <th>2017-08-29</th>
      <td>90.990</td>
      <td>93.4800</td>
      <td>90.9800</td>
      <td>92.630</td>
      <td>520386.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>90.990</td>
      <td>93.4800</td>
      <td>90.9800</td>
      <td>92.630</td>
      <td>520386.0</td>
      <td>-1.290</td>
    </tr>
    <tr>
      <th>2017-08-28</th>
      <td>91.000</td>
      <td>92.5000</td>
      <td>90.4600</td>
      <td>91.860</td>
      <td>568598.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>91.000</td>
      <td>92.5000</td>
      <td>90.4600</td>
      <td>91.860</td>
      <td>568598.0</td>
      <td>-0.770</td>
    </tr>
    <tr>
      <th>2017-08-25</th>
      <td>91.000</td>
      <td>91.8699</td>
      <td>90.1100</td>
      <td>90.700</td>
      <td>527002.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>91.000</td>
      <td>91.8699</td>
      <td>90.1100</td>
      <td>90.700</td>
      <td>527002.0</td>
      <td>-1.160</td>
    </tr>
    <tr>
      <th>2017-08-24</th>
      <td>92.890</td>
      <td>93.4250</td>
      <td>90.1600</td>
      <td>90.690</td>
      <td>658541.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>92.890</td>
      <td>93.4250</td>
      <td>90.1600</td>
      <td>90.690</td>
      <td>658541.0</td>
      <td>-0.010</td>
    </tr>
    <tr>
      <th>2017-08-23</th>
      <td>92.360</td>
      <td>93.2500</td>
      <td>91.2700</td>
      <td>92.525</td>
      <td>634322.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>92.360</td>
      <td>93.2500</td>
      <td>91.2700</td>
      <td>92.525</td>
      <td>634322.0</td>
      <td>1.835</td>
    </tr>
    <tr>
      <th>2017-08-22</th>
      <td>94.160</td>
      <td>94.9100</td>
      <td>92.4900</td>
      <td>92.730</td>
      <td>721262.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>94.160</td>
      <td>94.9100</td>
      <td>92.4900</td>
      <td>92.730</td>
      <td>721262.0</td>
      <td>0.205</td>
    </tr>
    <tr>
      <th>2017-08-21</th>
      <td>97.140</td>
      <td>97.6700</td>
      <td>93.9500</td>
      <td>94.100</td>
      <td>720432.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>97.140</td>
      <td>97.6700</td>
      <td>93.9500</td>
      <td>94.100</td>
      <td>720432.0</td>
      <td>1.370</td>
    </tr>
    <tr>
      <th>2017-08-18</th>
      <td>98.620</td>
      <td>99.0500</td>
      <td>96.1900</td>
      <td>97.280</td>
      <td>1059698.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>98.620</td>
      <td>99.0500</td>
      <td>96.1900</td>
      <td>97.280</td>
      <td>1059698.0</td>
      <td>3.180</td>
    </tr>
    <tr>
      <th>2017-08-17</th>
      <td>101.790</td>
      <td>102.6400</td>
      <td>98.7200</td>
      <td>98.820</td>
      <td>503846.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>101.790</td>
      <td>102.6400</td>
      <td>98.7200</td>
      <td>98.820</td>
      <td>503846.0</td>
      <td>1.540</td>
    </tr>
    <tr>
      <th>2017-08-16</th>
      <td>104.080</td>
      <td>104.0800</td>
      <td>101.2300</td>
      <td>102.370</td>
      <td>389433.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>104.080</td>
      <td>104.0800</td>
      <td>101.2300</td>
      <td>102.370</td>
      <td>389433.0</td>
      <td>3.550</td>
    </tr>
    <tr>
      <th>2017-08-15</th>
      <td>105.400</td>
      <td>105.4000</td>
      <td>102.5100</td>
      <td>103.280</td>
      <td>385906.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>105.400</td>
      <td>105.4000</td>
      <td>102.5100</td>
      <td>103.280</td>
      <td>385906.0</td>
      <td>0.910</td>
    </tr>
    <tr>
      <th>2017-08-14</th>
      <td>103.570</td>
      <td>105.3600</td>
      <td>102.2015</td>
      <td>104.850</td>
      <td>626631.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>103.570</td>
      <td>105.3600</td>
      <td>102.2015</td>
      <td>104.850</td>
      <td>626631.0</td>
      <td>1.570</td>
    </tr>
    <tr>
      <th>2017-08-11</th>
      <td>101.080</td>
      <td>103.2700</td>
      <td>101.0100</td>
      <td>102.230</td>
      <td>469456.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>101.080</td>
      <td>103.2700</td>
      <td>101.0100</td>
      <td>102.230</td>
      <td>469456.0</td>
      <td>-2.620</td>
    </tr>
    <tr>
      <th>2017-08-10</th>
      <td>103.850</td>
      <td>104.5900</td>
      <td>100.6100</td>
      <td>100.880</td>
      <td>553873.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>103.850</td>
      <td>104.5900</td>
      <td>100.6100</td>
      <td>100.880</td>
      <td>553873.0</td>
      <td>-1.350</td>
    </tr>
    <tr>
      <th>2017-08-09</th>
      <td>104.840</td>
      <td>105.3400</td>
      <td>103.3300</td>
      <td>104.610</td>
      <td>455440.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>104.840</td>
      <td>105.3400</td>
      <td>103.3300</td>
      <td>104.610</td>
      <td>455440.0</td>
      <td>3.730</td>
    </tr>
    <tr>
      <th>2017-08-08</th>
      <td>106.380</td>
      <td>106.8400</td>
      <td>104.5000</td>
      <td>105.290</td>
      <td>665365.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>106.380</td>
      <td>106.8400</td>
      <td>104.5000</td>
      <td>105.290</td>
      <td>665365.0</td>
      <td>0.680</td>
    </tr>
    <tr>
      <th>2017-08-07</th>
      <td>103.890</td>
      <td>107.0814</td>
      <td>103.0000</td>
      <td>105.170</td>
      <td>901335.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>103.890</td>
      <td>107.0814</td>
      <td>103.0000</td>
      <td>105.170</td>
      <td>901335.0</td>
      <td>-0.120</td>
    </tr>
    <tr>
      <th>2017-08-04</th>
      <td>102.370</td>
      <td>103.2839</td>
      <td>101.2800</td>
      <td>102.810</td>
      <td>546814.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>102.370</td>
      <td>103.2839</td>
      <td>101.2800</td>
      <td>102.810</td>
      <td>546814.0</td>
      <td>-2.360</td>
    </tr>
    <tr>
      <th>2017-08-03</th>
      <td>103.880</td>
      <td>105.4600</td>
      <td>101.9800</td>
      <td>102.260</td>
      <td>530463.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>103.880</td>
      <td>105.4600</td>
      <td>101.9800</td>
      <td>102.260</td>
      <td>530463.0</td>
      <td>-0.550</td>
    </tr>
    <tr>
      <th>2017-08-02</th>
      <td>107.820</td>
      <td>107.8200</td>
      <td>102.2711</td>
      <td>103.860</td>
      <td>911215.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>107.820</td>
      <td>107.8200</td>
      <td>102.2711</td>
      <td>103.860</td>
      <td>911215.0</td>
      <td>1.600</td>
    </tr>
    <tr>
      <th>2017-08-01</th>
      <td>106.050</td>
      <td>107.2500</td>
      <td>104.5810</td>
      <td>106.580</td>
      <td>715043.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>106.050</td>
      <td>107.2500</td>
      <td>104.5810</td>
      <td>106.580</td>
      <td>715043.0</td>
      <td>2.720</td>
    </tr>
    <tr>
      <th>2017-07-31</th>
      <td>107.530</td>
      <td>109.7800</td>
      <td>104.2200</td>
      <td>105.510</td>
      <td>1009018.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>107.530</td>
      <td>109.7800</td>
      <td>104.2200</td>
      <td>105.510</td>
      <td>1009018.0</td>
      <td>-1.070</td>
    </tr>
    <tr>
      <th>2017-07-28</th>
      <td>104.000</td>
      <td>107.8544</td>
      <td>103.5200</td>
      <td>107.250</td>
      <td>1129577.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>104.000</td>
      <td>107.8544</td>
      <td>103.5200</td>
      <td>107.250</td>
      <td>1129577.0</td>
      <td>1.740</td>
    </tr>
    <tr>
      <th>2017-07-27</th>
      <td>106.710</td>
      <td>108.9200</td>
      <td>102.1240</td>
      <td>105.240</td>
      <td>2320485.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>106.710</td>
      <td>108.9200</td>
      <td>102.1240</td>
      <td>105.240</td>
      <td>2320485.0</td>
      <td>-2.010</td>
    </tr>
    <tr>
      <th>2017-07-26</th>
      <td>101.245</td>
      <td>109.4000</td>
      <td>95.7500</td>
      <td>106.490</td>
      <td>7452422.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>101.245</td>
      <td>109.4000</td>
      <td>95.7500</td>
      <td>106.490</td>
      <td>7452422.0</td>
      <td>1.250</td>
    </tr>
    <tr>
      <th>2017-07-25</th>
      <td>90.700</td>
      <td>90.7000</td>
      <td>87.1010</td>
      <td>87.900</td>
      <td>1909387.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>90.700</td>
      <td>90.7000</td>
      <td>87.1010</td>
      <td>87.900</td>
      <td>1909387.0</td>
      <td>-18.590</td>
    </tr>
    <tr>
      <th>2017-07-24</th>
      <td>89.490</td>
      <td>92.3100</td>
      <td>88.5200</td>
      <td>90.380</td>
      <td>1730702.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>89.490</td>
      <td>92.3100</td>
      <td>88.5200</td>
      <td>90.380</td>
      <td>1730702.0</td>
      <td>2.480</td>
    </tr>
    <tr>
      <th>2017-07-21</th>
      <td>85.020</td>
      <td>88.9200</td>
      <td>85.0200</td>
      <td>88.470</td>
      <td>913952.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>85.020</td>
      <td>88.9200</td>
      <td>85.0200</td>
      <td>88.470</td>
      <td>913952.0</td>
      <td>-1.910</td>
    </tr>
    <tr>
      <th>2017-07-20</th>
      <td>87.290</td>
      <td>87.6880</td>
      <td>84.6400</td>
      <td>85.000</td>
      <td>516948.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>87.290</td>
      <td>87.6880</td>
      <td>84.6400</td>
      <td>85.000</td>
      <td>516948.0</td>
      <td>-3.470</td>
    </tr>
    <tr>
      <th>2017-07-19</th>
      <td>85.010</td>
      <td>87.4699</td>
      <td>85.0100</td>
      <td>86.770</td>
      <td>558040.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>85.010</td>
      <td>87.4699</td>
      <td>85.0100</td>
      <td>86.770</td>
      <td>558040.0</td>
      <td>1.770</td>
    </tr>
    <tr>
      <th>2017-07-18</th>
      <td>84.920</td>
      <td>85.1200</td>
      <td>83.9200</td>
      <td>84.750</td>
      <td>472737.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>84.920</td>
      <td>85.1200</td>
      <td>83.9200</td>
      <td>84.750</td>
      <td>472737.0</td>
      <td>-2.020</td>
    </tr>
    <tr>
      <th>2017-07-17</th>
      <td>84.030</td>
      <td>85.6600</td>
      <td>83.5800</td>
      <td>84.900</td>
      <td>554840.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>84.030</td>
      <td>85.6600</td>
      <td>83.5800</td>
      <td>84.900</td>
      <td>554840.0</td>
      <td>0.150</td>
    </tr>
    <tr>
      <th>2017-07-14</th>
      <td>84.750</td>
      <td>84.9600</td>
      <td>83.5900</td>
      <td>83.990</td>
      <td>410374.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>84.750</td>
      <td>84.9600</td>
      <td>83.5900</td>
      <td>83.990</td>
      <td>410374.0</td>
      <td>-0.910</td>
    </tr>
    <tr>
      <th>2017-07-13</th>
      <td>85.650</td>
      <td>85.6500</td>
      <td>83.0500</td>
      <td>84.620</td>
      <td>524322.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>85.650</td>
      <td>85.6500</td>
      <td>83.0500</td>
      <td>84.620</td>
      <td>524322.0</td>
      <td>0.630</td>
    </tr>
    <tr>
      <th>2017-07-12</th>
      <td>84.120</td>
      <td>85.2500</td>
      <td>83.3700</td>
      <td>85.020</td>
      <td>811856.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>84.120</td>
      <td>85.2500</td>
      <td>83.3700</td>
      <td>85.020</td>
      <td>811856.0</td>
      <td>0.400</td>
    </tr>
    <tr>
      <th>2017-07-11</th>
      <td>84.300</td>
      <td>85.3800</td>
      <td>82.2859</td>
      <td>83.240</td>
      <td>809283.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>84.300</td>
      <td>85.3800</td>
      <td>82.2859</td>
      <td>83.240</td>
      <td>809283.0</td>
      <td>-1.780</td>
    </tr>
    <tr>
      <th>2017-07-10</th>
      <td>83.960</td>
      <td>85.0000</td>
      <td>82.6760</td>
      <td>84.470</td>
      <td>771819.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>83.960</td>
      <td>85.0000</td>
      <td>82.6760</td>
      <td>84.470</td>
      <td>771819.0</td>
      <td>1.230</td>
    </tr>
    <tr>
      <th>2017-07-07</th>
      <td>80.300</td>
      <td>84.5000</td>
      <td>80.2300</td>
      <td>83.650</td>
      <td>988983.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>80.300</td>
      <td>84.5000</td>
      <td>80.2300</td>
      <td>83.650</td>
      <td>988983.0</td>
      <td>-0.820</td>
    </tr>
    <tr>
      <th>2017-07-06</th>
      <td>80.780</td>
      <td>81.4200</td>
      <td>79.4000</td>
      <td>80.540</td>
      <td>1398242.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>80.780</td>
      <td>81.4200</td>
      <td>79.4000</td>
      <td>80.540</td>
      <td>1398242.0</td>
      <td>-3.110</td>
    </tr>
    <tr>
      <th>2017-07-05</th>
      <td>83.040</td>
      <td>84.3000</td>
      <td>81.5400</td>
      <td>82.180</td>
      <td>1138538.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>83.040</td>
      <td>84.3000</td>
      <td>81.5400</td>
      <td>82.180</td>
      <td>1138538.0</td>
      <td>1.640</td>
    </tr>
    <tr>
      <th>2017-07-03</th>
      <td>83.300</td>
      <td>84.7600</td>
      <td>81.0600</td>
      <td>83.540</td>
      <td>886425.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>83.300</td>
      <td>84.7600</td>
      <td>81.0600</td>
      <td>83.540</td>
      <td>886425.0</td>
      <td>1.360</td>
    </tr>
    <tr>
      <th>2017-06-30</th>
      <td>86.220</td>
      <td>86.8500</td>
      <td>84.0900</td>
      <td>84.140</td>
      <td>1091539.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>86.220</td>
      <td>86.8500</td>
      <td>84.0900</td>
      <td>84.140</td>
      <td>1091539.0</td>
      <td>0.600</td>
    </tr>
    <tr>
      <th>2017-06-29</th>
      <td>92.740</td>
      <td>92.7800</td>
      <td>86.3401</td>
      <td>86.780</td>
      <td>1266048.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>92.740</td>
      <td>92.7800</td>
      <td>86.3401</td>
      <td>86.780</td>
      <td>1266048.0</td>
      <td>2.640</td>
    </tr>
    <tr>
      <th>2017-06-28</th>
      <td>91.030</td>
      <td>93.6300</td>
      <td>88.4300</td>
      <td>92.470</td>
      <td>1350789.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>91.030</td>
      <td>93.6300</td>
      <td>88.4300</td>
      <td>92.470</td>
      <td>1350789.0</td>
      <td>5.690</td>
    </tr>
    <tr>
      <th>2017-06-27</th>
      <td>100.360</td>
      <td>100.4600</td>
      <td>90.0800</td>
      <td>90.650</td>
      <td>1904499.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>100.360</td>
      <td>100.4600</td>
      <td>90.0800</td>
      <td>90.650</td>
      <td>1904499.0</td>
      <td>-1.820</td>
    </tr>
    <tr>
      <th>2017-06-26</th>
      <td>101.950</td>
      <td>102.8700</td>
      <td>99.4300</td>
      <td>100.980</td>
      <td>389160.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>101.950</td>
      <td>102.8700</td>
      <td>99.4300</td>
      <td>100.980</td>
      <td>389160.0</td>
      <td>10.330</td>
    </tr>
    <tr>
      <th>2017-06-23</th>
      <td>100.390</td>
      <td>102.7000</td>
      <td>100.2700</td>
      <td>101.200</td>
      <td>680765.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>100.390</td>
      <td>102.7000</td>
      <td>100.2700</td>
      <td>101.200</td>
      <td>680765.0</td>
      <td>0.220</td>
    </tr>
    <tr>
      <th>2017-06-22</th>
      <td>100.990</td>
      <td>101.6500</td>
      <td>99.0000</td>
      <td>100.430</td>
      <td>537581.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>100.990</td>
      <td>101.6500</td>
      <td>99.0000</td>
      <td>100.430</td>
      <td>537581.0</td>
      <td>-0.770</td>
    </tr>
    <tr>
      <th>2017-06-21</th>
      <td>98.400</td>
      <td>102.3200</td>
      <td>97.7744</td>
      <td>101.080</td>
      <td>756849.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>98.400</td>
      <td>102.3200</td>
      <td>97.7744</td>
      <td>101.080</td>
      <td>756849.0</td>
      <td>0.650</td>
    </tr>
    <tr>
      <th>2017-06-20</th>
      <td>99.000</td>
      <td>99.9800</td>
      <td>97.3223</td>
      <td>97.730</td>
      <td>581543.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>99.000</td>
      <td>99.9800</td>
      <td>97.3223</td>
      <td>97.730</td>
      <td>581543.0</td>
      <td>-3.350</td>
    </tr>
    <tr>
      <th>2017-06-19</th>
      <td>96.960</td>
      <td>99.2700</td>
      <td>96.6100</td>
      <td>98.780</td>
      <td>855417.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>96.960</td>
      <td>99.2700</td>
      <td>96.6100</td>
      <td>98.780</td>
      <td>855417.0</td>
      <td>1.050</td>
    </tr>
    <tr>
      <th>2017-06-16</th>
      <td>98.680</td>
      <td>98.8600</td>
      <td>95.7700</td>
      <td>96.270</td>
      <td>1318596.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>98.680</td>
      <td>98.8600</td>
      <td>95.7700</td>
      <td>96.270</td>
      <td>1318596.0</td>
      <td>-2.510</td>
    </tr>
    <tr>
      <th>2017-06-15</th>
      <td>100.200</td>
      <td>101.0500</td>
      <td>97.1800</td>
      <td>97.970</td>
      <td>1634053.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>100.200</td>
      <td>101.0500</td>
      <td>97.1800</td>
      <td>97.970</td>
      <td>1634053.0</td>
      <td>1.700</td>
    </tr>
    <tr>
      <th>2017-06-14</th>
      <td>100.340</td>
      <td>104.6100</td>
      <td>100.1300</td>
      <td>101.990</td>
      <td>1276940.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>100.340</td>
      <td>104.6100</td>
      <td>100.1300</td>
      <td>101.990</td>
      <td>1276940.0</td>
      <td>4.020</td>
    </tr>
    <tr>
      <th>2017-06-13</th>
      <td>99.430</td>
      <td>101.5368</td>
      <td>98.5000</td>
      <td>100.280</td>
      <td>800361.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>99.430</td>
      <td>101.5368</td>
      <td>98.5000</td>
      <td>100.280</td>
      <td>800361.0</td>
      <td>-1.710</td>
    </tr>
    <tr>
      <th>2017-06-12</th>
      <td>95.990</td>
      <td>98.7600</td>
      <td>91.5100</td>
      <td>98.650</td>
      <td>1045008.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>95.990</td>
      <td>98.7600</td>
      <td>91.5100</td>
      <td>98.650</td>
      <td>1045008.0</td>
      <td>-1.630</td>
    </tr>
    <tr>
      <th>2017-06-09</th>
      <td>100.420</td>
      <td>100.9499</td>
      <td>93.1300</td>
      <td>95.990</td>
      <td>1112576.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>100.420</td>
      <td>100.9499</td>
      <td>93.1300</td>
      <td>95.990</td>
      <td>1112576.0</td>
      <td>-2.660</td>
    </tr>
    <tr>
      <th>2017-06-08</th>
      <td>98.980</td>
      <td>100.4800</td>
      <td>97.8201</td>
      <td>99.930</td>
      <td>615704.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>98.980</td>
      <td>100.4800</td>
      <td>97.8201</td>
      <td>99.930</td>
      <td>615704.0</td>
      <td>3.940</td>
    </tr>
    <tr>
      <th>2017-06-07</th>
      <td>96.860</td>
      <td>99.3100</td>
      <td>96.0800</td>
      <td>99.300</td>
      <td>658388.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>96.860</td>
      <td>99.3100</td>
      <td>96.0800</td>
      <td>99.300</td>
      <td>658388.0</td>
      <td>-0.630</td>
    </tr>
    <tr>
      <th>2017-06-06</th>
      <td>96.750</td>
      <td>98.8700</td>
      <td>96.3100</td>
      <td>96.860</td>
      <td>553069.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>96.750</td>
      <td>98.8700</td>
      <td>96.3100</td>
      <td>96.860</td>
      <td>553069.0</td>
      <td>-2.440</td>
    </tr>
    <tr>
      <th>2017-06-05</th>
      <td>97.550</td>
      <td>98.0600</td>
      <td>96.2700</td>
      <td>97.200</td>
      <td>655715.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>97.550</td>
      <td>98.0600</td>
      <td>96.2700</td>
      <td>97.200</td>
      <td>655715.0</td>
      <td>0.340</td>
    </tr>
    <tr>
      <th>2017-06-02</th>
      <td>95.290</td>
      <td>97.5800</td>
      <td>94.4300</td>
      <td>97.460</td>
      <td>691979.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>95.290</td>
      <td>97.5800</td>
      <td>94.4300</td>
      <td>97.460</td>
      <td>691979.0</td>
      <td>0.260</td>
    </tr>
    <tr>
      <th>2017-06-01</th>
      <td>92.580</td>
      <td>95.2200</td>
      <td>92.4000</td>
      <td>95.160</td>
      <td>937128.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>92.580</td>
      <td>95.2200</td>
      <td>92.4000</td>
      <td>95.160</td>
      <td>937128.0</td>
      <td>-2.300</td>
    </tr>
    <tr>
      <th>2017-05-31</th>
      <td>98.280</td>
      <td>98.9100</td>
      <td>92.2700</td>
      <td>92.720</td>
      <td>1452220.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>98.280</td>
      <td>98.9100</td>
      <td>92.2700</td>
      <td>92.720</td>
      <td>1452220.0</td>
      <td>-2.440</td>
    </tr>
    <tr>
      <th>2017-05-30</th>
      <td>96.860</td>
      <td>99.9800</td>
      <td>96.0700</td>
      <td>99.820</td>
      <td>844954.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>96.860</td>
      <td>99.9800</td>
      <td>96.0700</td>
      <td>99.820</td>
      <td>844954.0</td>
      <td>7.100</td>
    </tr>
    <tr>
      <th>2017-05-26</th>
      <td>94.690</td>
      <td>97.6800</td>
      <td>94.0900</td>
      <td>97.140</td>
      <td>597667.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>94.690</td>
      <td>97.6800</td>
      <td>94.0900</td>
      <td>97.140</td>
      <td>597667.0</td>
      <td>-2.680</td>
    </tr>
    <tr>
      <th>2017-05-25</th>
      <td>94.980</td>
      <td>95.4936</td>
      <td>93.3000</td>
      <td>94.770</td>
      <td>742504.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>94.980</td>
      <td>95.4936</td>
      <td>93.3000</td>
      <td>94.770</td>
      <td>742504.0</td>
      <td>-2.370</td>
    </tr>
    <tr>
      <th>2017-05-24</th>
      <td>97.260</td>
      <td>97.8000</td>
      <td>94.1200</td>
      <td>94.350</td>
      <td>786282.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>97.260</td>
      <td>97.8000</td>
      <td>94.1200</td>
      <td>94.350</td>
      <td>786282.0</td>
      <td>-0.420</td>
    </tr>
    <tr>
      <th>2017-05-23</th>
      <td>96.560</td>
      <td>97.6800</td>
      <td>95.2300</td>
      <td>97.000</td>
      <td>592279.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>96.560</td>
      <td>97.6800</td>
      <td>95.2300</td>
      <td>97.000</td>
      <td>592279.0</td>
      <td>2.650</td>
    </tr>
    <tr>
      <th>2017-05-22</th>
      <td>94.470</td>
      <td>96.2300</td>
      <td>94.0100</td>
      <td>96.020</td>
      <td>562732.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>94.470</td>
      <td>96.2300</td>
      <td>94.0100</td>
      <td>96.020</td>
      <td>562732.0</td>
      <td>-0.980</td>
    </tr>
    <tr>
      <th>2017-05-19</th>
      <td>92.260</td>
      <td>94.2400</td>
      <td>92.2600</td>
      <td>93.220</td>
      <td>610565.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>92.260</td>
      <td>94.2400</td>
      <td>92.2600</td>
      <td>93.220</td>
      <td>610565.0</td>
      <td>-2.800</td>
    </tr>
    <tr>
      <th>2017-05-18</th>
      <td>89.030</td>
      <td>92.9200</td>
      <td>87.1400</td>
      <td>91.700</td>
      <td>765607.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>89.030</td>
      <td>92.9200</td>
      <td>87.1400</td>
      <td>91.700</td>
      <td>765607.0</td>
      <td>-1.520</td>
    </tr>
    <tr>
      <th>2017-05-17</th>
      <td>92.250</td>
      <td>92.8600</td>
      <td>90.0800</td>
      <td>90.140</td>
      <td>738670.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>92.250</td>
      <td>92.8600</td>
      <td>90.0800</td>
      <td>90.140</td>
      <td>738670.0</td>
      <td>-1.560</td>
    </tr>
    <tr>
      <th>2017-05-16</th>
      <td>93.050</td>
      <td>93.8300</td>
      <td>90.3500</td>
      <td>93.510</td>
      <td>952646.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>93.050</td>
      <td>93.8300</td>
      <td>90.3500</td>
      <td>93.510</td>
      <td>952646.0</td>
      <td>3.370</td>
    </tr>
    <tr>
      <th>2017-05-15</th>
      <td>90.500</td>
      <td>92.9400</td>
      <td>90.4000</td>
      <td>92.370</td>
      <td>583464.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>90.500</td>
      <td>92.9400</td>
      <td>90.4000</td>
      <td>92.370</td>
      <td>583464.0</td>
      <td>-1.140</td>
    </tr>
    <tr>
      <th>2017-05-12</th>
      <td>89.400</td>
      <td>90.4899</td>
      <td>88.9600</td>
      <td>89.990</td>
      <td>518714.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>89.400</td>
      <td>90.4899</td>
      <td>88.9600</td>
      <td>89.990</td>
      <td>518714.0</td>
      <td>-2.380</td>
    </tr>
    <tr>
      <th>2017-05-11</th>
      <td>88.770</td>
      <td>89.5411</td>
      <td>87.0200</td>
      <td>89.490</td>
      <td>432052.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>88.770</td>
      <td>89.5411</td>
      <td>87.0200</td>
      <td>89.490</td>
      <td>432052.0</td>
      <td>-0.500</td>
    </tr>
    <tr>
      <th>2017-05-10</th>
      <td>86.580</td>
      <td>88.7700</td>
      <td>86.4500</td>
      <td>88.700</td>
      <td>544648.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>86.580</td>
      <td>88.7700</td>
      <td>86.4500</td>
      <td>88.700</td>
      <td>544648.0</td>
      <td>-0.790</td>
    </tr>
    <tr>
      <th>2017-05-09</th>
      <td>85.420</td>
      <td>86.7100</td>
      <td>85.1500</td>
      <td>86.580</td>
      <td>420836.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>85.420</td>
      <td>86.7100</td>
      <td>85.1500</td>
      <td>86.580</td>
      <td>420836.0</td>
      <td>-2.120</td>
    </tr>
    <tr>
      <th>2017-05-08</th>
      <td>87.990</td>
      <td>87.9900</td>
      <td>85.1000</td>
      <td>85.345</td>
      <td>561436.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>87.990</td>
      <td>87.9900</td>
      <td>85.1000</td>
      <td>85.345</td>
      <td>561436.0</td>
      <td>-1.235</td>
    </tr>
    <tr>
      <th>2017-05-05</th>
      <td>85.260</td>
      <td>86.4500</td>
      <td>84.9700</td>
      <td>85.900</td>
      <td>586622.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>85.260</td>
      <td>86.4500</td>
      <td>84.9700</td>
      <td>85.900</td>
      <td>586622.0</td>
      <td>0.555</td>
    </tr>
    <tr>
      <th>2017-05-04</th>
      <td>85.660</td>
      <td>85.9500</td>
      <td>84.3200</td>
      <td>84.720</td>
      <td>425707.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>85.660</td>
      <td>85.9500</td>
      <td>84.3200</td>
      <td>84.720</td>
      <td>425707.0</td>
      <td>-1.180</td>
    </tr>
    <tr>
      <th>2017-05-03</th>
      <td>83.750</td>
      <td>85.1200</td>
      <td>83.3300</td>
      <td>85.090</td>
      <td>498916.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>83.750</td>
      <td>85.1200</td>
      <td>83.3300</td>
      <td>85.090</td>
      <td>498916.0</td>
      <td>0.370</td>
    </tr>
    <tr>
      <th>2017-05-02</th>
      <td>84.180</td>
      <td>84.7700</td>
      <td>82.9500</td>
      <td>83.660</td>
      <td>769496.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>84.180</td>
      <td>84.7700</td>
      <td>82.9500</td>
      <td>83.660</td>
      <td>769496.0</td>
      <td>-1.430</td>
    </tr>
    <tr>
      <th>2017-05-01</th>
      <td>79.890</td>
      <td>83.4800</td>
      <td>79.6100</td>
      <td>83.260</td>
      <td>1155000.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>79.890</td>
      <td>83.4800</td>
      <td>79.6100</td>
      <td>83.260</td>
      <td>1155000.0</td>
      <td>-0.400</td>
    </tr>
    <tr>
      <th>2017-04-28</th>
      <td>79.950</td>
      <td>79.9900</td>
      <td>78.9800</td>
      <td>79.740</td>
      <td>982514.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>79.950</td>
      <td>79.9900</td>
      <td>78.9800</td>
      <td>79.740</td>
      <td>982514.0</td>
      <td>-3.520</td>
    </tr>
    <tr>
      <th>2017-04-27</th>
      <td>80.080</td>
      <td>81.3800</td>
      <td>78.1100</td>
      <td>79.890</td>
      <td>1193440.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>80.080</td>
      <td>81.3800</td>
      <td>78.1100</td>
      <td>79.890</td>
      <td>1193440.0</td>
      <td>0.150</td>
    </tr>
    <tr>
      <th>2017-04-26</th>
      <td>74.880</td>
      <td>82.4400</td>
      <td>74.0000</td>
      <td>80.020</td>
      <td>3672208.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>74.880</td>
      <td>82.4400</td>
      <td>74.0000</td>
      <td>80.020</td>
      <td>3672208.0</td>
      <td>0.130</td>
    </tr>
    <tr>
      <th>2017-04-25</th>
      <td>69.520</td>
      <td>70.3400</td>
      <td>68.6450</td>
      <td>69.140</td>
      <td>924937.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>69.520</td>
      <td>70.3400</td>
      <td>68.6450</td>
      <td>69.140</td>
      <td>924937.0</td>
      <td>-10.880</td>
    </tr>
    <tr>
      <th>2017-04-24</th>
      <td>68.680</td>
      <td>69.2799</td>
      <td>68.0000</td>
      <td>69.260</td>
      <td>590191.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>68.680</td>
      <td>69.2799</td>
      <td>68.0000</td>
      <td>69.260</td>
      <td>590191.0</td>
      <td>0.120</td>
    </tr>
    <tr>
      <th>2017-04-21</th>
      <td>67.310</td>
      <td>68.3900</td>
      <td>66.9000</td>
      <td>67.610</td>
      <td>481348.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>67.310</td>
      <td>68.3900</td>
      <td>66.9000</td>
      <td>67.610</td>
      <td>481348.0</td>
      <td>-1.650</td>
    </tr>
    <tr>
      <th>2017-04-20</th>
      <td>67.320</td>
      <td>68.3000</td>
      <td>66.9800</td>
      <td>67.440</td>
      <td>528590.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>67.320</td>
      <td>68.3000</td>
      <td>66.9800</td>
      <td>67.440</td>
      <td>528590.0</td>
      <td>-0.170</td>
    </tr>
    <tr>
      <th>2017-04-19</th>
      <td>65.960</td>
      <td>67.8500</td>
      <td>65.9100</td>
      <td>67.240</td>
      <td>702866.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>65.960</td>
      <td>67.8500</td>
      <td>65.9100</td>
      <td>67.240</td>
      <td>702866.0</td>
      <td>-0.200</td>
    </tr>
    <tr>
      <th>2017-04-18</th>
      <td>66.160</td>
      <td>66.2800</td>
      <td>65.5000</td>
      <td>65.850</td>
      <td>393393.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>66.160</td>
      <td>66.2800</td>
      <td>65.5000</td>
      <td>65.850</td>
      <td>393393.0</td>
      <td>-1.390</td>
    </tr>
    <tr>
      <th>2017-04-17</th>
      <td>65.610</td>
      <td>66.2000</td>
      <td>65.1900</td>
      <td>66.180</td>
      <td>322915.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>65.610</td>
      <td>66.2000</td>
      <td>65.1900</td>
      <td>66.180</td>
      <td>322915.0</td>
      <td>0.330</td>
    </tr>
    <tr>
      <th>2017-04-13</th>
      <td>65.200</td>
      <td>65.8200</td>
      <td>65.0000</td>
      <td>65.130</td>
      <td>380269.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>65.200</td>
      <td>65.8200</td>
      <td>65.0000</td>
      <td>65.130</td>
      <td>380269.0</td>
      <td>-1.050</td>
    </tr>
    <tr>
      <th>2017-04-12</th>
      <td>67.240</td>
      <td>67.2500</td>
      <td>65.1800</td>
      <td>65.370</td>
      <td>369744.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>67.240</td>
      <td>67.2500</td>
      <td>65.1800</td>
      <td>65.370</td>
      <td>369744.0</td>
      <td>0.240</td>
    </tr>
    <tr>
      <th>2017-04-11</th>
      <td>65.930</td>
      <td>67.3000</td>
      <td>65.5000</td>
      <td>67.250</td>
      <td>412890.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>65.930</td>
      <td>67.3000</td>
      <td>65.5000</td>
      <td>67.250</td>
      <td>412890.0</td>
      <td>1.880</td>
    </tr>
    <tr>
      <th>2017-04-10</th>
      <td>66.490</td>
      <td>67.0950</td>
      <td>65.7500</td>
      <td>66.110</td>
      <td>293102.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>66.490</td>
      <td>67.0950</td>
      <td>65.7500</td>
      <td>66.110</td>
      <td>293102.0</td>
      <td>-1.140</td>
    </tr>
    <tr>
      <th>2017-04-07</th>
      <td>66.150</td>
      <td>66.9000</td>
      <td>66.0200</td>
      <td>66.450</td>
      <td>471664.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>66.150</td>
      <td>66.9000</td>
      <td>66.0200</td>
      <td>66.450</td>
      <td>471664.0</td>
      <td>0.340</td>
    </tr>
    <tr>
      <th>2017-04-06</th>
      <td>65.600</td>
      <td>66.7900</td>
      <td>65.3300</td>
      <td>66.480</td>
      <td>425083.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>65.600</td>
      <td>66.7900</td>
      <td>65.3300</td>
      <td>66.480</td>
      <td>425083.0</td>
      <td>0.030</td>
    </tr>
    <tr>
      <th>2017-04-05</th>
      <td>66.000</td>
      <td>66.8900</td>
      <td>65.5600</td>
      <td>65.690</td>
      <td>360646.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>66.000</td>
      <td>66.8900</td>
      <td>65.5600</td>
      <td>65.690</td>
      <td>360646.0</td>
      <td>-0.790</td>
    </tr>
    <tr>
      <th>2017-04-04</th>
      <td>65.280</td>
      <td>66.2900</td>
      <td>65.2800</td>
      <td>65.910</td>
      <td>431233.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>65.280</td>
      <td>66.2900</td>
      <td>65.2800</td>
      <td>65.910</td>
      <td>431233.0</td>
      <td>0.220</td>
    </tr>
    <tr>
      <th>2017-04-03</th>
      <td>66.110</td>
      <td>66.3900</td>
      <td>65.0600</td>
      <td>65.440</td>
      <td>398270.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>66.110</td>
      <td>66.3900</td>
      <td>65.0600</td>
      <td>65.440</td>
      <td>398270.0</td>
      <td>-0.470</td>
    </tr>
    <tr>
      <th>2017-03-31</th>
      <td>65.290</td>
      <td>66.2400</td>
      <td>65.0500</td>
      <td>66.140</td>
      <td>414979.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>65.290</td>
      <td>66.2400</td>
      <td>65.0500</td>
      <td>66.140</td>
      <td>414979.0</td>
      <td>0.700</td>
    </tr>
    <tr>
      <th>2017-03-30</th>
      <td>65.000</td>
      <td>65.8200</td>
      <td>65.0000</td>
      <td>65.630</td>
      <td>291178.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>65.000</td>
      <td>65.8200</td>
      <td>65.0000</td>
      <td>65.630</td>
      <td>291178.0</td>
      <td>-0.510</td>
    </tr>
    <tr>
      <th>2017-03-29</th>
      <td>64.250</td>
      <td>65.1200</td>
      <td>63.9550</td>
      <td>64.940</td>
      <td>442539.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>64.250</td>
      <td>65.1200</td>
      <td>63.9550</td>
      <td>64.940</td>
      <td>442539.0</td>
      <td>-0.690</td>
    </tr>
    <tr>
      <th>2017-03-28</th>
      <td>62.730</td>
      <td>64.6600</td>
      <td>62.6600</td>
      <td>64.430</td>
      <td>502058.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>62.730</td>
      <td>64.6600</td>
      <td>62.6600</td>
      <td>64.430</td>
      <td>502058.0</td>
      <td>-0.510</td>
    </tr>
    <tr>
      <th>2017-03-27</th>
      <td>61.990</td>
      <td>63.0700</td>
      <td>60.6700</td>
      <td>62.810</td>
      <td>470905.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>61.990</td>
      <td>63.0700</td>
      <td>60.6700</td>
      <td>62.810</td>
      <td>470905.0</td>
      <td>-1.620</td>
    </tr>
    <tr>
      <th>2017-03-24</th>
      <td>61.500</td>
      <td>62.5400</td>
      <td>61.5000</td>
      <td>62.490</td>
      <td>625420.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>61.500</td>
      <td>62.5400</td>
      <td>61.5000</td>
      <td>62.490</td>
      <td>625420.0</td>
      <td>-0.320</td>
    </tr>
    <tr>
      <th>2017-03-23</th>
      <td>60.170</td>
      <td>61.4000</td>
      <td>60.0000</td>
      <td>61.310</td>
      <td>357815.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>60.170</td>
      <td>61.4000</td>
      <td>60.0000</td>
      <td>61.310</td>
      <td>357815.0</td>
      <td>-1.180</td>
    </tr>
    <tr>
      <th>2017-03-22</th>
      <td>59.150</td>
      <td>60.2300</td>
      <td>58.7050</td>
      <td>60.230</td>
      <td>356158.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>59.150</td>
      <td>60.2300</td>
      <td>58.7050</td>
      <td>60.230</td>
      <td>356158.0</td>
      <td>-1.080</td>
    </tr>
    <tr>
      <th>2017-03-21</th>
      <td>60.270</td>
      <td>60.8100</td>
      <td>59.0200</td>
      <td>59.150</td>
      <td>661329.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>60.270</td>
      <td>60.8100</td>
      <td>59.0200</td>
      <td>59.150</td>
      <td>661329.0</td>
      <td>-1.080</td>
    </tr>
    <tr>
      <th>2017-03-20</th>
      <td>59.670</td>
      <td>60.3650</td>
      <td>59.1700</td>
      <td>60.230</td>
      <td>420862.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>59.670</td>
      <td>60.3650</td>
      <td>59.1700</td>
      <td>60.230</td>
      <td>420862.0</td>
      <td>1.080</td>
    </tr>
    <tr>
      <th>2017-03-17</th>
      <td>58.700</td>
      <td>59.5400</td>
      <td>58.5412</td>
      <td>59.460</td>
      <td>745194.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>58.700</td>
      <td>59.5400</td>
      <td>58.5412</td>
      <td>59.460</td>
      <td>745194.0</td>
      <td>-0.770</td>
    </tr>
    <tr>
      <th>2017-03-16</th>
      <td>58.320</td>
      <td>59.2400</td>
      <td>58.1400</td>
      <td>58.670</td>
      <td>641419.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>58.320</td>
      <td>59.2400</td>
      <td>58.1400</td>
      <td>58.670</td>
      <td>641419.0</td>
      <td>-0.790</td>
    </tr>
    <tr>
      <th>2017-03-15</th>
      <td>57.110</td>
      <td>58.4900</td>
      <td>56.8900</td>
      <td>58.290</td>
      <td>620492.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>57.110</td>
      <td>58.4900</td>
      <td>56.8900</td>
      <td>58.290</td>
      <td>620492.0</td>
      <td>-0.380</td>
    </tr>
    <tr>
      <th>2017-03-14</th>
      <td>56.220</td>
      <td>57.3600</td>
      <td>56.1405</td>
      <td>56.830</td>
      <td>260137.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>56.220</td>
      <td>57.3600</td>
      <td>56.1405</td>
      <td>56.830</td>
      <td>260137.0</td>
      <td>-1.460</td>
    </tr>
    <tr>
      <th>2017-03-13</th>
      <td>57.310</td>
      <td>57.4000</td>
      <td>56.5401</td>
      <td>56.610</td>
      <td>342990.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>57.310</td>
      <td>57.4000</td>
      <td>56.5401</td>
      <td>56.610</td>
      <td>342990.0</td>
      <td>-0.220</td>
    </tr>
    <tr>
      <th>2017-03-10</th>
      <td>56.480</td>
      <td>57.3950</td>
      <td>56.1200</td>
      <td>57.330</td>
      <td>244005.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>56.480</td>
      <td>57.3950</td>
      <td>56.1200</td>
      <td>57.330</td>
      <td>244005.0</td>
      <td>0.720</td>
    </tr>
    <tr>
      <th>2017-03-09</th>
      <td>56.830</td>
      <td>56.8300</td>
      <td>56.2200</td>
      <td>56.370</td>
      <td>188068.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>56.830</td>
      <td>56.8300</td>
      <td>56.2200</td>
      <td>56.370</td>
      <td>188068.0</td>
      <td>-0.960</td>
    </tr>
    <tr>
      <th>2017-03-08</th>
      <td>56.030</td>
      <td>56.9300</td>
      <td>55.9600</td>
      <td>56.620</td>
      <td>302195.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>56.030</td>
      <td>56.9300</td>
      <td>55.9600</td>
      <td>56.620</td>
      <td>302195.0</td>
      <td>0.250</td>
    </tr>
    <tr>
      <th>2017-03-07</th>
      <td>56.270</td>
      <td>56.5775</td>
      <td>55.8200</td>
      <td>55.920</td>
      <td>418562.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>56.270</td>
      <td>56.5775</td>
      <td>55.8200</td>
      <td>55.920</td>
      <td>418562.0</td>
      <td>-0.700</td>
    </tr>
    <tr>
      <th>2017-03-06</th>
      <td>56.790</td>
      <td>56.9500</td>
      <td>56.1600</td>
      <td>56.690</td>
      <td>328254.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>56.790</td>
      <td>56.9500</td>
      <td>56.1600</td>
      <td>56.690</td>
      <td>328254.0</td>
      <td>0.770</td>
    </tr>
    <tr>
      <th>2017-03-03</th>
      <td>57.200</td>
      <td>57.5400</td>
      <td>56.5900</td>
      <td>57.320</td>
      <td>431203.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>57.200</td>
      <td>57.5400</td>
      <td>56.5900</td>
      <td>57.320</td>
      <td>431203.0</td>
      <td>0.630</td>
    </tr>
    <tr>
      <th>2017-03-02</th>
      <td>57.700</td>
      <td>58.0700</td>
      <td>57.0500</td>
      <td>57.120</td>
      <td>389679.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>57.700</td>
      <td>58.0700</td>
      <td>57.0500</td>
      <td>57.120</td>
      <td>389679.0</td>
      <td>-0.200</td>
    </tr>
    <tr>
      <th>2017-03-01</th>
      <td>57.520</td>
      <td>58.7000</td>
      <td>57.3200</td>
      <td>58.080</td>
      <td>428337.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>57.520</td>
      <td>58.7000</td>
      <td>57.3200</td>
      <td>58.080</td>
      <td>428337.0</td>
      <td>0.960</td>
    </tr>
    <tr>
      <th>2017-02-28</th>
      <td>58.200</td>
      <td>58.2700</td>
      <td>56.9800</td>
      <td>57.080</td>
      <td>540147.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>58.200</td>
      <td>58.2700</td>
      <td>56.9800</td>
      <td>57.080</td>
      <td>540147.0</td>
      <td>-1.000</td>
    </tr>
    <tr>
      <th>2017-02-27</th>
      <td>57.270</td>
      <td>58.4100</td>
      <td>57.0000</td>
      <td>58.400</td>
      <td>396137.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>57.270</td>
      <td>58.4100</td>
      <td>57.0000</td>
      <td>58.400</td>
      <td>396137.0</td>
      <td>1.320</td>
    </tr>
    <tr>
      <th>2017-02-24</th>
      <td>56.510</td>
      <td>57.5700</td>
      <td>56.0000</td>
      <td>57.560</td>
      <td>390331.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>56.510</td>
      <td>57.5700</td>
      <td>56.0000</td>
      <td>57.560</td>
      <td>390331.0</td>
      <td>-0.840</td>
    </tr>
    <tr>
      <th>2017-02-23</th>
      <td>57.890</td>
      <td>57.8900</td>
      <td>56.6200</td>
      <td>57.130</td>
      <td>395481.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>57.890</td>
      <td>57.8900</td>
      <td>56.6200</td>
      <td>57.130</td>
      <td>395481.0</td>
      <td>-0.430</td>
    </tr>
    <tr>
      <th>2017-02-22</th>
      <td>57.080</td>
      <td>57.9100</td>
      <td>57.0600</td>
      <td>57.740</td>
      <td>446493.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>57.080</td>
      <td>57.9100</td>
      <td>57.0600</td>
      <td>57.740</td>
      <td>446493.0</td>
      <td>0.610</td>
    </tr>
    <tr>
      <th>2017-02-21</th>
      <td>55.750</td>
      <td>57.1900</td>
      <td>55.7500</td>
      <td>57.060</td>
      <td>465432.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>55.750</td>
      <td>57.1900</td>
      <td>55.7500</td>
      <td>57.060</td>
      <td>465432.0</td>
      <td>-0.680</td>
    </tr>
    <tr>
      <th>2017-02-17</th>
      <td>55.550</td>
      <td>55.8100</td>
      <td>55.1100</td>
      <td>55.580</td>
      <td>405143.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>55.550</td>
      <td>55.8100</td>
      <td>55.1100</td>
      <td>55.580</td>
      <td>405143.0</td>
      <td>-1.480</td>
    </tr>
    <tr>
      <th>2017-02-16</th>
      <td>56.040</td>
      <td>56.6400</td>
      <td>55.2900</td>
      <td>55.560</td>
      <td>381723.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>56.040</td>
      <td>56.6400</td>
      <td>55.2900</td>
      <td>55.560</td>
      <td>381723.0</td>
      <td>-0.020</td>
    </tr>
    <tr>
      <th>2017-02-15</th>
      <td>54.780</td>
      <td>56.2100</td>
      <td>54.7200</td>
      <td>55.820</td>
      <td>482610.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>54.780</td>
      <td>56.2100</td>
      <td>54.7200</td>
      <td>55.820</td>
      <td>482610.0</td>
      <td>0.260</td>
    </tr>
    <tr>
      <th>2017-02-14</th>
      <td>54.380</td>
      <td>55.3900</td>
      <td>54.3800</td>
      <td>54.870</td>
      <td>371400.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>54.380</td>
      <td>55.3900</td>
      <td>54.3800</td>
      <td>54.870</td>
      <td>371400.0</td>
      <td>-0.950</td>
    </tr>
    <tr>
      <th>2017-02-13</th>
      <td>54.770</td>
      <td>54.7900</td>
      <td>54.0570</td>
      <td>54.600</td>
      <td>684825.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>54.770</td>
      <td>54.7900</td>
      <td>54.0570</td>
      <td>54.600</td>
      <td>684825.0</td>
      <td>-0.270</td>
    </tr>
    <tr>
      <th>2017-02-10</th>
      <td>53.420</td>
      <td>56.7500</td>
      <td>53.4200</td>
      <td>54.310</td>
      <td>2089881.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>53.420</td>
      <td>56.7500</td>
      <td>53.4200</td>
      <td>54.310</td>
      <td>2089881.0</td>
      <td>-0.290</td>
    </tr>
    <tr>
      <th>2017-02-09</th>
      <td>54.500</td>
      <td>55.1200</td>
      <td>52.1200</td>
      <td>53.320</td>
      <td>5878903.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>54.500</td>
      <td>55.1200</td>
      <td>52.1200</td>
      <td>53.320</td>
      <td>5878903.0</td>
      <td>-0.990</td>
    </tr>
    <tr>
      <th>2017-02-08</th>
      <td>62.220</td>
      <td>62.5300</td>
      <td>60.4400</td>
      <td>61.240</td>
      <td>930291.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>62.220</td>
      <td>62.5300</td>
      <td>60.4400</td>
      <td>61.240</td>
      <td>930291.0</td>
      <td>7.920</td>
    </tr>
    <tr>
      <th>2017-02-07</th>
      <td>62.560</td>
      <td>63.9900</td>
      <td>61.8300</td>
      <td>61.890</td>
      <td>781184.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>62.560</td>
      <td>63.9900</td>
      <td>61.8300</td>
      <td>61.890</td>
      <td>781184.0</td>
      <td>0.650</td>
    </tr>
    <tr>
      <th>2017-02-06</th>
      <td>62.850</td>
      <td>62.9140</td>
      <td>61.8400</td>
      <td>62.150</td>
      <td>393648.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>62.850</td>
      <td>62.9140</td>
      <td>61.8400</td>
      <td>62.150</td>
      <td>393648.0</td>
      <td>0.260</td>
    </tr>
    <tr>
      <th>2017-02-03</th>
      <td>61.360</td>
      <td>62.9000</td>
      <td>61.0200</td>
      <td>62.740</td>
      <td>462071.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>61.360</td>
      <td>62.9000</td>
      <td>61.0200</td>
      <td>62.740</td>
      <td>462071.0</td>
      <td>0.590</td>
    </tr>
    <tr>
      <th>2017-02-02</th>
      <td>61.620</td>
      <td>62.1100</td>
      <td>61.0800</td>
      <td>61.240</td>
      <td>466005.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>61.620</td>
      <td>62.1100</td>
      <td>61.0800</td>
      <td>61.240</td>
      <td>466005.0</td>
      <td>-1.500</td>
    </tr>
    <tr>
      <th>2017-02-01</th>
      <td>60.800</td>
      <td>61.5350</td>
      <td>60.7700</td>
      <td>61.270</td>
      <td>289194.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>60.800</td>
      <td>61.5350</td>
      <td>60.7700</td>
      <td>61.270</td>
      <td>289194.0</td>
      <td>0.030</td>
    </tr>
    <tr>
      <th>2017-01-31</th>
      <td>60.460</td>
      <td>60.8200</td>
      <td>60.2500</td>
      <td>60.560</td>
      <td>351015.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>60.460</td>
      <td>60.8200</td>
      <td>60.2500</td>
      <td>60.560</td>
      <td>351015.0</td>
      <td>-0.710</td>
    </tr>
    <tr>
      <th>2017-01-30</th>
      <td>61.880</td>
      <td>61.8800</td>
      <td>60.4001</td>
      <td>60.950</td>
      <td>520090.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>61.880</td>
      <td>61.8800</td>
      <td>60.4001</td>
      <td>60.950</td>
      <td>520090.0</td>
      <td>0.390</td>
    </tr>
    <tr>
      <th>2017-01-27</th>
      <td>63.000</td>
      <td>63.1000</td>
      <td>61.1000</td>
      <td>62.180</td>
      <td>382551.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>63.000</td>
      <td>63.1000</td>
      <td>61.1000</td>
      <td>62.180</td>
      <td>382551.0</td>
      <td>1.230</td>
    </tr>
    <tr>
      <th>2017-01-26</th>
      <td>62.590</td>
      <td>63.1650</td>
      <td>62.2600</td>
      <td>63.080</td>
      <td>354206.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>62.590</td>
      <td>63.1650</td>
      <td>62.2600</td>
      <td>63.080</td>
      <td>354206.0</td>
      <td>0.900</td>
    </tr>
    <tr>
      <th>2017-01-25</th>
      <td>62.660</td>
      <td>62.9900</td>
      <td>61.2700</td>
      <td>62.220</td>
      <td>411456.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>62.660</td>
      <td>62.9900</td>
      <td>61.2700</td>
      <td>62.220</td>
      <td>411456.0</td>
      <td>-0.860</td>
    </tr>
    <tr>
      <th>2017-01-24</th>
      <td>59.970</td>
      <td>62.0600</td>
      <td>59.8700</td>
      <td>61.730</td>
      <td>488747.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>59.970</td>
      <td>62.0600</td>
      <td>59.8700</td>
      <td>61.730</td>
      <td>488747.0</td>
      <td>-0.490</td>
    </tr>
    <tr>
      <th>2017-01-23</th>
      <td>60.640</td>
      <td>60.6850</td>
      <td>59.6300</td>
      <td>59.800</td>
      <td>367967.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>60.640</td>
      <td>60.6850</td>
      <td>59.6300</td>
      <td>59.800</td>
      <td>367967.0</td>
      <td>-1.930</td>
    </tr>
    <tr>
      <th>2017-01-20</th>
      <td>59.650</td>
      <td>60.7800</td>
      <td>59.5945</td>
      <td>60.500</td>
      <td>382588.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>59.650</td>
      <td>60.7800</td>
      <td>59.5945</td>
      <td>60.500</td>
      <td>382588.0</td>
      <td>0.700</td>
    </tr>
    <tr>
      <th>2017-01-19</th>
      <td>59.710</td>
      <td>60.4500</td>
      <td>57.8910</td>
      <td>59.400</td>
      <td>543760.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>59.710</td>
      <td>60.4500</td>
      <td>57.8910</td>
      <td>59.400</td>
      <td>543760.0</td>
      <td>-1.100</td>
    </tr>
    <tr>
      <th>2017-01-18</th>
      <td>58.560</td>
      <td>61.0000</td>
      <td>58.4800</td>
      <td>59.570</td>
      <td>727734.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>58.560</td>
      <td>61.0000</td>
      <td>58.4800</td>
      <td>59.570</td>
      <td>727734.0</td>
      <td>0.170</td>
    </tr>
    <tr>
      <th>2017-01-17</th>
      <td>59.000</td>
      <td>59.6700</td>
      <td>58.3400</td>
      <td>58.460</td>
      <td>405982.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>59.000</td>
      <td>59.6700</td>
      <td>58.3400</td>
      <td>58.460</td>
      <td>405982.0</td>
      <td>-1.110</td>
    </tr>
    <tr>
      <th>2017-01-13</th>
      <td>58.370</td>
      <td>59.7700</td>
      <td>58.3700</td>
      <td>59.220</td>
      <td>202290.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>58.370</td>
      <td>59.7700</td>
      <td>58.3700</td>
      <td>59.220</td>
      <td>202290.0</td>
      <td>0.760</td>
    </tr>
    <tr>
      <th>2017-01-12</th>
      <td>58.360</td>
      <td>58.4300</td>
      <td>57.3600</td>
      <td>58.340</td>
      <td>321897.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>58.360</td>
      <td>58.4300</td>
      <td>57.3600</td>
      <td>58.340</td>
      <td>321897.0</td>
      <td>-0.880</td>
    </tr>
    <tr>
      <th>2017-01-11</th>
      <td>59.250</td>
      <td>59.3500</td>
      <td>57.9300</td>
      <td>58.330</td>
      <td>343193.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>59.250</td>
      <td>59.3500</td>
      <td>57.9300</td>
      <td>58.330</td>
      <td>343193.0</td>
      <td>-0.010</td>
    </tr>
    <tr>
      <th>2017-01-10</th>
      <td>57.990</td>
      <td>59.1300</td>
      <td>57.5000</td>
      <td>59.040</td>
      <td>865972.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>57.990</td>
      <td>59.1300</td>
      <td>57.5000</td>
      <td>59.040</td>
      <td>865972.0</td>
      <td>0.710</td>
    </tr>
    <tr>
      <th>2017-01-09</th>
      <td>58.630</td>
      <td>58.7800</td>
      <td>57.6500</td>
      <td>57.690</td>
      <td>270710.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>58.630</td>
      <td>58.7800</td>
      <td>57.6500</td>
      <td>57.690</td>
      <td>270710.0</td>
      <td>-1.350</td>
    </tr>
    <tr>
      <th>2017-01-06</th>
      <td>58.520</td>
      <td>59.4000</td>
      <td>58.2800</td>
      <td>58.730</td>
      <td>266215.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>58.520</td>
      <td>59.4000</td>
      <td>58.2800</td>
      <td>58.730</td>
      <td>266215.0</td>
      <td>1.040</td>
    </tr>
    <tr>
      <th>2017-01-05</th>
      <td>59.280</td>
      <td>59.5600</td>
      <td>57.8900</td>
      <td>58.300</td>
      <td>470367.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>59.280</td>
      <td>59.5600</td>
      <td>57.8900</td>
      <td>58.300</td>
      <td>470367.0</td>
      <td>-0.430</td>
    </tr>
    <tr>
      <th>2017-01-04</th>
      <td>57.580</td>
      <td>59.4700</td>
      <td>57.5800</td>
      <td>59.220</td>
      <td>385460.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>57.580</td>
      <td>59.4700</td>
      <td>57.5800</td>
      <td>59.220</td>
      <td>385460.0</td>
      <td>0.920</td>
    </tr>
    <tr>
      <th>2017-01-03</th>
      <td>59.220</td>
      <td>59.8500</td>
      <td>57.3400</td>
      <td>57.580</td>
      <td>484914.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>59.220</td>
      <td>59.8500</td>
      <td>57.3400</td>
      <td>57.580</td>
      <td>484914.0</td>
      <td>-1.640</td>
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





    [<matplotlib.lines.Line2D at 0x1a1449aa20>]




![png](output_85_2.png)



```python
a_7_m = df_IRBT_07['Diff'].max()
a_7_i = df_IRBT_07['Diff'].idxmax()
a_8_m = df_IRBT_08['Diff'].max()
a_8_i = df_IRBT_08['Diff'].idxmax()
a_9_m = df_IRBT_09['Diff'].max()
a_9_i = df_IRBT_09['Diff'].idxmax()
a_10_m = df_IRBT_10['Diff'].max()
a_10_i = df_IRBT_10['Diff'].idxmax()
a_11_m = df_IRBT_11['Diff'].max()
a_11_i = df_IRBT_11['Diff'].idxmax()
a_12_m = df_IRBT_12['Diff'].max()
a_12_i = df_IRBT_12['Diff'].idxmax()
a_13_m = df_IRBT_13['Diff'].max()
a_13_i = df_IRBT_13['Diff'].idxmax()
a_14_m = df_IRBT_14['Diff'].max()
a_14_i = df_IRBT_14['Diff'].idxmax()
a_15_m = df_IRBT_15['Diff'].max()
a_15_i = df_IRBT_15['Diff'].idxmax()
a_16_m = df_IRBT_16['Diff'].max()
a_16_i = df_IRBT_16['Diff'].idxmax()
a_17_m = df_IRBT_17['Diff'].max()
a_17_i = df_IRBT_17['Diff'].idxmax()
IRBT_max_index_data = {a_7_m:a_7_i, a_8_m:a_8_i, a_9_m:a_9_i, a_10_m:a_10_i, a_11_m:a_11_i, a_12_m:a_12_i, a_13_m:a_13_i, a_14_m:a_14_i, a_15_m:a_15_i, a_16_m:a_16_i, a_17_m:a_17_i}
for i in IRBT_max_index_data:
    print (i,IRBT_max_index_data[i])
y = IRBT_max_index_data.keys()
x = IRBT_max_index_data.values()
plt.plot(x,y)
```

    5.350000000000001 2007-09-14 00:00:00
    2.0999999999999996 2008-09-19 00:00:00
    1.8699999999999992 2009-07-22 00:00:00
    1.8500000000000014 2010-06-03 00:00:00
    3.25 2011-08-05 00:00:00
    13.129999999999995 2012-02-08 00:00:00
    5.170000000000002 2013-07-23 00:00:00
    4.1299999999999955 2014-04-22 00:00:00
    2.8100000000000023 2015-02-04 00:00:00
    4.700000000000003 2016-02-10 00:00:00
    15.790000000000006 2017-09-12 00:00:00





    [<matplotlib.lines.Line2D at 0x1a0c8ac438>]




![png](output_86_2.png)



```python
df_CY_07.corrwith(df_IRBT_07['AdjClose'])
```




    Open          0.274373
    High          0.274848
    Low           0.282799
    Close         0.281673
    Volume       -0.156614
    ExDividend         NaN
    SplitRatio         NaN
    AdjOpen       0.274373
    AdjHigh       0.274848
    AdjLow        0.282799
    AdjClose      0.281673
    AdjVolume    -0.156614
    Diff          0.011001
    dtype: float64




```python
df_CY_08.corrwith(df_IRBT_08['AdjClose'])
```




    Open          0.577037
    High          0.581744
    Low           0.569495
    Close         0.575937
    Volume        0.530550
    ExDividend    0.006104
    SplitRatio         NaN
    AdjOpen       0.378248
    AdjHigh       0.374375
    AdjLow        0.371967
    AdjClose      0.372605
    AdjVolume     0.530550
    Diff          0.059237
    dtype: float64




```python
df_CY_09.corrwith(df_IRBT_09['AdjClose'])
```




    Open          0.770366
    High          0.769543
    Low           0.777026
    Close         0.772474
    Volume        0.070392
    ExDividend         NaN
    SplitRatio         NaN
    AdjOpen       0.770366
    AdjHigh       0.769543
    AdjLow        0.777026
    AdjClose      0.772474
    AdjVolume     0.070392
    Diff          0.039739
    dtype: float64




```python
df_CY_10.corrwith(df_IRBT_10['AdjClose'])
```




    Open          0.581741
    High          0.581362
    Low           0.580158
    Close         0.577752
    Volume       -0.165157
    ExDividend         NaN
    SplitRatio         NaN
    AdjOpen       0.581741
    AdjHigh       0.581362
    AdjLow        0.580158
    AdjClose      0.577752
    AdjVolume    -0.165157
    Diff          0.077204
    dtype: float64




```python
df_CY_11.corrwith(df_IRBT_11['AdjClose'])
```




    Open          0.432049
    High          0.442118
    Low           0.451647
    Close         0.453158
    Volume       -0.313439
    ExDividend   -0.040825
    SplitRatio         NaN
    AdjOpen       0.442793
    AdjHigh       0.452989
    AdjLow        0.462576
    AdjClose      0.464139
    AdjVolume    -0.313439
    Diff          0.059015
    dtype: float64




```python
df_CY_12.corrwith(df_IRBT_12['AdjClose'])
```




    Open          0.774676
    High          0.778867
    Low           0.778083
    Close         0.781738
    Volume        0.007659
    ExDividend    0.010153
    SplitRatio         NaN
    AdjOpen       0.774595
    AdjHigh       0.778945
    AdjLow        0.778103
    AdjClose      0.781905
    AdjVolume     0.007659
    Diff         -0.007411
    dtype: float64




```python
df_CY_13.corrwith(df_IRBT_13['AdjClose'])
```




    Open          0.112234
    High          0.102289
    Low           0.116986
    Close         0.115514
    Volume       -0.059659
    ExDividend    0.059309
    SplitRatio         NaN
    AdjOpen       0.208975
    AdjHigh       0.200755
    AdjLow        0.213788
    AdjClose      0.213107
    AdjVolume    -0.059659
    Diff         -0.011644
    dtype: float64




```python
df_CY_14.corrwith(df_IRBT_14['AdjClose'])
```




    Open         -0.001500
    High          0.000532
    Low           0.012981
    Close         0.015517
    Volume       -0.081757
    ExDividend    0.018092
    SplitRatio         NaN
    AdjOpen      -0.059349
    AdjHigh      -0.057469
    AdjLow       -0.045484
    AdjClose     -0.042852
    AdjVolume    -0.081757
    Diff         -0.012212
    dtype: float64




```python
df_CY_15.corrwith(df_IRBT_15['AdjClose'])
```




    Open          0.371440
    High          0.362763
    Low           0.381091
    Close         0.373832
    Volume       -0.132097
    ExDividend    0.076378
    SplitRatio         NaN
    AdjOpen       0.382479
    AdjHigh       0.373410
    AdjLow        0.392668
    AdjClose      0.384977
    AdjVolume    -0.132097
    Diff          0.081730
    dtype: float64




```python
df_CY_16.corrwith(df_IRBT_16['AdjClose'])
```




    Open          0.615065
    High          0.609207
    Low           0.619801
    Close         0.610756
    Volume       -0.220427
    ExDividend    0.043555
    SplitRatio         NaN
    AdjOpen       0.642257
    AdjHigh       0.637211
    AdjLow        0.646066
    AdjClose      0.638270
    AdjVolume    -0.220427
    Diff          0.000990
    dtype: float64




```python
df_CY_17.corrwith(df_IRBT_17['AdjClose'])
```




    Open          0.090549
    High          0.093066
    Low           0.076399
    Close         0.081896
    Volume       -0.028692
    ExDividend    0.006924
    SplitRatio         NaN
    AdjOpen       0.106882
    AdjHigh       0.109487
    AdjLow        0.093658
    AdjClose      0.099110
    AdjVolume    -0.028692
    Diff          0.068446
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
df_IRBT_07_AdjClose = df_IRBT_07['AdjClose']
df_IRBT_07_AdjClose.head()
```




    Date
    2007-12-31    18.08
    2007-12-28    18.04
    2007-12-27    17.97
    2007-12-26    18.34
    2007-12-24    18.19
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
df_IRBT_07_AdjClose.rename(index='Date')
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
merged_07 = pd.concat([df_CY_07_AdjClose, df_IRBT_07_AdjClose], axis=1, join_axes=[df_CY_07_AdjClose.index])
merged_07.columns = ['CY_07', 'IRBT_07']
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
      <th>IRBT_07</th>
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
      <td>18.08</td>
    </tr>
    <tr>
      <th>2007-12-28</th>
      <td>6.995078</td>
      <td>18.04</td>
    </tr>
    <tr>
      <th>2007-12-27</th>
      <td>7.101524</td>
      <td>17.97</td>
    </tr>
    <tr>
      <th>2007-12-26</th>
      <td>7.363840</td>
      <td>18.34</td>
    </tr>
    <tr>
      <th>2007-12-24</th>
      <td>7.206070</td>
      <td>18.19</td>
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
      <th>IRBT_07</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>CY_07</th>
      <td>1.000000</td>
      <td>0.281673</td>
    </tr>
    <tr>
      <th>IRBT_07</th>
      <td>0.281673</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
plt.scatter(df_CY_07['Diff'], df_IRBT_07['Diff'], marker = 'x', c='g')
plt.xlabel = ('Cypress price change per day')
plt.ylabel = ('IRobot price change per day')
```


![png](output_104_0.png)



```python
seb.regplot(df_CY_07['Diff'], df_IRBT_07['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c41ec50>




![png](output_105_1.png)



```python
seb.regplot(df_CY_08['Diff'], df_IRBT_08['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c1306d8>




![png](output_106_1.png)



```python
seb.regplot(df_CY_09['Diff'], df_IRBT_09['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0b7c02e8>




![png](output_107_1.png)



```python
seb.regplot(df_CY_10['Diff'], df_IRBT_10['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x102f9beb8>




![png](output_108_1.png)



```python
seb.regplot(df_CY_11['Diff'], df_IRBT_11['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c6714e0>




![png](output_109_1.png)



```python
seb.regplot(df_CY_12['Diff'], df_IRBT_12['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c718c88>




![png](output_110_1.png)



```python
seb.regplot(df_CY_13['Diff'], df_IRBT_13['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0b6efb00>




![png](output_111_1.png)



```python
seb.regplot(df_CY_14['Diff'], df_IRBT_14['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c040dd8>




![png](output_112_1.png)



```python
seb.regplot(df_CY_15['Diff'], df_IRBT_15['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c365160>




![png](output_113_1.png)



```python
seb.regplot(df_CY_16['Diff'], df_IRBT_16['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c468080>




![png](output_114_1.png)



```python
seb.regplot(df_CY_17['Diff'], df_CY_17['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0c6cb588>




![png](output_115_1.png)



```python
stats.ttest_ind(df_CY_17['Diff'], df_IRBT_17['Diff'], equal_var=False)
```




    Ttest_indResult(statistic=nan, pvalue=nan)




```python
df_IRBT_07.loc[:,"Diff"].std()
```




    0.6792712538487261




```python
df_IRBT_08.loc[:,"Diff"].std()
```




    0.6022873134185115




```python
df_IRBT_09.loc[:,"Diff"].std()
```




    0.40918207015198577




```python
df_IRBT_10.loc[:,"Diff"].std()
```




    0.645881312718925




```python
df_IRBT_11.loc[:,"Diff"].std()
```




    1.063545533292512




```python
df_IRBT_12.loc[:,"Diff"].std()
```




    1.0376354645834829




```python
df_IRBT_13.loc[:,"Diff"].std()
```




    0.918250249965527




```python
df_IRBT_14.loc[:,"Diff"].std()
```




    1.0327093601309087




```python
df_IRBT_15.loc[:,"Diff"].std()
```




    0.5677967967419666




```python
df_IRBT_16.loc[:,"Diff"].std()
```




    0.7828616965062052




```python
df_IRBT_17.loc[:,"Diff"].std()
```




    2.613638376551463




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
df_IRBT_07.loc[:,"Diff"].cov(df_CY_07.loc[:,"Diff"])
```




    0.014675896768137303




```python
df_IRBT_08.loc[:,"Diff"].cov(df_CY_08.loc[:,"Diff"])
```




    0.029679270658269762




```python
df_IRBT_09.loc[:,"Diff"].cov(df_CY_09.loc[:,"Diff"])
```




    0.014892249445702796




```python
df_IRBT_10.loc[:,"Diff"].cov(df_CY_10.loc[:,"Diff"])
```




    0.05901862265351421




```python
df_IRBT_11.loc[:,"Diff"].cov(df_CY_11.loc[:,"Diff"])
```




    0.24750050367122062




```python
df_IRBT_12.loc[:,"Diff"].cov(df_CY_12.loc[:,"Diff"])
```




    0.06506987821126543




```python
df_IRBT_13.loc[:,"Diff"].cov(df_CY_13.loc[:,"Diff"])
```




    0.05072581673109567




```python
df_IRBT_14.loc[:,"Diff"].cov(df_CY_14.loc[:,"Diff"])
```




    0.04792575886148833




```python
df_IRBT_15.loc[:,"Diff"].cov(df_CY_15.loc[:,"Diff"])
```




    0.04803665450842905




```python
df_IRBT_16.loc[:,"Diff"].cov(df_CY_16.loc[:,"Diff"])
```




    0.04243725844331379




```python
df_IRBT_17.loc[:,"Diff"].cov(df_CY_17.loc[:,"Diff"])
```




    0.1512233882400111




```python
df_CY_07['Diff'].mean()
```




    -0.014621232686265995




```python
df_IRBT_07['Diff'].mean()
```




    -0.0003599999999999994




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
IRBT_07_mean=df_IRBT_07['Diff'].mean()
IRBT_07_mean
```




    -0.0003599999999999994




```python
IRBT_08_mean=df_IRBT_08['Diff'].mean()
IRBT_08_mean
```




    0.03543650793650794




```python
IRBT_09_mean=df_IRBT_09['Diff'].mean()
IRBT_09_mean
```




    -0.03282868525896415




```python
IRBT_10_mean=df_IRBT_10['Diff'].mean()
IRBT_10_mean
```




    -0.02756972111553784




```python
IRBT_11_mean=df_IRBT_11['Diff'].mean()
IRBT_11_mean
```




    -0.018286852589641432




```python
IRBT_12_mean=df_IRBT_12['Diff'].mean()
IRBT_12_mean
```




    0.03955823293172692




```python
IRBT_13_mean=df_IRBT_13['Diff'].mean()
IRBT_13_mean
```




    -0.05553784860557771




```python
IRBT_14_mean=df_IRBT_14['Diff'].mean()
IRBT_14_mean
```




    0.0001593625498007934




```python
IRBT_15_mean=df_IRBT_15['Diff'].mean()
IRBT_15_mean
```




    -0.002231075697211136




```python
IRBT_16_mean=df_IRBT_16['Diff'].mean()
IRBT_16_mean
```




    -0.09701195219123507




```python
IRBT_17_mean=df_IRBT_17['Diff'].mean()
IRBT_17_mean
```




    -0.07678714859437753




```python
def gendata_07(loc1=0, loc2=0):
    population_n_07 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_07 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_07, population_a_07
population_n_07, population_a_07 = gendata_07(loc1=CY_07_mean, loc2=IRBT_07_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_07)), population_n_07, label="CY 07")
plt.scatter(range(len(population_a_07)), population_a_07, label="IRBT 07")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_07, 10, density=True, alpha=0.5, label="CY 07")
plt.hist(population_a_07, 10, density=True, alpha=0.5, label="IRBT 07")
plt.axvline(population_n_07.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_07.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a0c584780>




![png](output_174_1.png)



```python
stats.ttest_ind(population_n_07, population_a_07, equal_var=False)
```




    Ttest_indResult(statistic=-0.1559231331927402, pvalue=0.8761567940872432)




```python
def gendata_08(loc1=0, loc2=0):
    population_n_08 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_08 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_08, population_a_08
population_n_08, population_a_08 = gendata_08(loc1=CY_08_mean, loc2=IRBT_08_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_08)), population_n_08, label="CY 08")
plt.scatter(range(len(population_a_08)), population_a_08, label="IRBT 08")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_08, 10, density=True, alpha=0.5, label="CY 08")
plt.hist(population_a_08, 10, density=True, alpha=0.5, label="IRBT 08")
plt.axvline(population_n_08.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_08.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a0c0f8f98>




![png](output_176_1.png)



```python
stats.ttest_ind(population_n_08, population_a_08, equal_var=False)
```




    Ttest_indResult(statistic=-0.2509954898428253, pvalue=0.8019211234818463)




```python
def gendata_09(loc1=0, loc2=0):
    population_n_09 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_09 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_09, population_a_09
population_n_09, population_a_09 = gendata_09(loc1=CY_09_mean, loc2=IRBT_09_mean)
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




    <matplotlib.legend.Legend at 0x1a14e35470>




![png](output_178_1.png)



```python
stats.ttest_ind(population_n_09, population_a_09, equal_var=False)
```




    Ttest_indResult(statistic=0.1568129245240064, pvalue=0.8754558389724436)




```python
def gendata_10(loc1=0, loc2=0):
    population_n_10 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_10 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_10, population_a_10
population_n_10, population_a_10 = gendata_10(loc1=CY_10_mean, loc2=IRBT_10_mean)
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




    <matplotlib.legend.Legend at 0x1a14fb09b0>




![png](output_180_1.png)



```python
stats.ttest_ind(population_n_10, population_a_10, equal_var=False)
```




    Ttest_indResult(statistic=0.02691035302373609, pvalue=0.9785420159688522)




```python
def gendata_11(loc1=0, loc2=0):
    population_n_11 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_11 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_11, population_a_11
population_n_11, population_a_11 = gendata_11(loc1=CY_11_mean, loc2=IRBT_11_mean)
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




    <matplotlib.legend.Legend at 0x1a15016ef0>




![png](output_182_1.png)



```python
stats.ttest_ind(population_n_11, population_a_11, equal_var=False)
```




    Ttest_indResult(statistic=0.2364283602906421, pvalue=0.8131975036744455)




```python
def gendata_12(loc1=0, loc2=0):
    population_n_12 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_12 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_12, population_a_12
population_n_12, population_a_12 = gendata_12(loc1=CY_12_mean, loc2=IRBT_12_mean)
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




    <matplotlib.legend.Legend at 0x1a152b9470>




![png](output_184_1.png)



```python
stats.ttest_ind(population_n_12, population_a_12, equal_var=False)
```




    Ttest_indResult(statistic=-0.2323680290430001, pvalue=0.8163476397363967)




```python
def gendata_13(loc1=0, loc2=0):
    population_n_13 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_13 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_13, population_a_13
population_n_13, population_a_13 = gendata_13(loc1=CY_13_mean, loc2=IRBT_13_mean)
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




    <matplotlib.legend.Legend at 0x1a154329b0>




![png](output_186_1.png)



```python
stats.ttest_ind(population_n_13, population_a_13, equal_var=False)
```




    Ttest_indResult(statistic=0.6211181977519357, pvalue=0.5348060387807902)




```python
def gendata_14(loc1=0, loc2=0):
    population_n_14 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_14 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_14, population_a_14
population_n_14, population_a_14 = gendata_14(loc1=CY_14_mean, loc2=IRBT_14_mean)
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




    <matplotlib.legend.Legend at 0x1a1549af28>




![png](output_188_1.png)



```python
stats.ttest_ind(population_n_14, population_a_14, equal_var=False)
```




    Ttest_indResult(statistic=-0.17394826652132941, pvalue=0.8619768058235839)




```python
def gendata_15(loc1=0, loc2=0):
    population_n_15 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_15 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_15, population_a_15
population_n_15, population_a_15 = gendata_15(loc1=CY_15_mean, loc2=IRBT_15_mean)
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




    <matplotlib.legend.Legend at 0x1a1573a470>




![png](output_190_1.png)



```python
stats.ttest_ind(population_n_15, population_a_15, equal_var=False)
```




    Ttest_indResult(statistic=0.1915304575605514, pvalue=0.8481880856309792)




```python
def gendata_16(loc1=0, loc2=0):
    population_n_16 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_16 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_16, population_a_16
population_n_16, population_a_16 = gendata_16(loc1=CY_16_mean, loc2=IRBT_16_mean)
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




    <matplotlib.legend.Legend at 0x1a158b79b0>




![png](output_192_1.png)



```python
stats.ttest_ind(population_n_16, population_a_16, equal_var=False)
```




    Ttest_indResult(statistic=0.9590097204299394, pvalue=0.3380192039043107)




```python
def gendata_17(loc1=0, loc2=0):
    population_n_17 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_17 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_17, population_a_17
population_n_17, population_a_17 = gendata_17(loc1=CY_17_mean, loc2=IRBT_17_mean)
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




    <matplotlib.legend.Legend at 0x1a15919d68>




![png](output_194_1.png)



```python
stats.ttest_ind(population_n_17, population_a_17, equal_var=False)
```




    Ttest_indResult(statistic=0.6498643794537132, pvalue=0.5160794748984388)




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
data1 = pd.DataFrame(df_IRBT_07['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_IRBT_08['Diff']).assign(Location=2)
data3 = pd.DataFrame(df_IRBT_09['Diff']).assign(Location=3)



cdf = pd.concat([data1, data2, data3])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter  value
    0         1   Diff    NaN
    1         1   Diff  -0.04
    2         1   Diff  -0.07
    3         1   Diff   0.37
    4         1   Diff  -0.15



![png](output_202_1.png)



```python
data4 = pd.DataFrame(df_IRBT_10['Diff']).assign(Location=4)
data5 = pd.DataFrame(df_IRBT_11['Diff']).assign(Location=5)
data6 = pd.DataFrame(df_IRBT_12['Diff']).assign(Location=6)

cdf = pd.concat([data4, data5, data6])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter  value
    0         4   Diff    NaN
    1         4   Diff  -0.35
    2         4   Diff   0.48
    3         4   Diff  -0.05
    4         4   Diff   0.01



![png](output_203_1.png)



```python
data7 = pd.DataFrame(df_IRBT_13['Diff']).assign(Location=7)
data8 = pd.DataFrame(df_IRBT_14['Diff']).assign(Location=8)
data9 = pd.DataFrame(df_IRBT_15['Diff']).assign(Location=9)

cdf = pd.concat([data7, data8, data9])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter  value
    0         7   Diff    NaN
    1         7   Diff   0.62
    2         7   Diff   0.02
    3         7   Diff   0.23
    4         7   Diff   0.00



![png](output_204_1.png)



```python
data10 = pd.DataFrame(df_IRBT_16['Diff']).assign(Location=10)
data11 = pd.DataFrame(df_IRBT_17['Diff']).assign(Location=11)


cdf = pd.concat([data10, data11])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter  value
    0        10   Diff    NaN
    1        10   Diff   0.03
    2        10   Diff  -0.12
    3        10   Diff   0.85
    4        10   Diff  -0.58



![png](output_205_1.png)



```python
#==================================================================================
```


```python
data1 = pd.DataFrame(df_CY_07['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_IRBT_07['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_IRBT_08['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_IRBT_09['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_IRBT_10['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_IRBT_11['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_IRBT_12['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_IRBT_12['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_IRBT_13['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_IRBT_14['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_IRBT_15['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_IRBT_16['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_IRBT_17['Diff']).assign(Location=2)

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
