

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
df_MSFT_07 = web.DataReader('MSFT','quandl', start_07,end_07)
```


```python
df_MSFT_07 = web.DataReader('MSFT','quandl', start_07,end_07)
```


```python
df_MSFT_08 = web.DataReader('MSFT','quandl', start_08,end_08)
```


```python
df_MSFT_09 = web.DataReader('MSFT','quandl', start_09,end_09)
```


```python
df_MSFT_10 = web.DataReader('MSFT','quandl', start_10,end_10)
```


```python
df_MSFT_11 = web.DataReader('MSFT','quandl', start_11,end_11)
```


```python
df_MSFT_12 = web.DataReader('MSFT','quandl', start_12,end_12)
```


```python
df_MSFT_13 = web.DataReader('MSFT','quandl', start_13,end_13)
```


```python
df_MSFT_14 = web.DataReader('MSFT','quandl', start_14,end_14)
```


```python
df_MSFT_15 = web.DataReader('MSFT','quandl', start_15,end_15)
```


```python
df_MSFT_16 = web.DataReader('MSFT','quandl', start_16,end_16)
```


```python
df_MSFT_17 = web.DataReader('MSFT','quandl', start_17,end_17)
```


```python
plt.plot(df_CY_07.index,df_CY_07['AdjClose'], c='r')
plt.plot(df_MSFT_07.index,df_MSFT_07['AdjClose'], c='g')
plt.show()
```


![png](output_68_0.png)



```python
plt.plot(df_CY_08.index,df_CY_08['AdjClose'], c='r')
plt.plot(df_MSFT_08.index,df_MSFT_08['AdjClose'], c='g')
plt.show()
```


![png](output_69_0.png)



```python
plt.plot(df_CY_09.index,df_CY_09['AdjClose'], c='r')
plt.plot(df_MSFT_09.index,df_MSFT_09['AdjClose'], c='g')
plt.show()
```


![png](output_70_0.png)



```python
plt.plot(df_CY_10.index,df_CY_10['AdjClose'], c='r')
plt.plot(df_MSFT_10.index,df_MSFT_10['AdjClose'], c='g')
plt.show()
```


![png](output_71_0.png)



```python
plt.plot(df_CY_11.index,df_CY_11['AdjClose'], c='r')
plt.plot(df_MSFT_11.index,df_MSFT_11['AdjClose'], c='g')
plt.show()
```


![png](output_72_0.png)



```python
plt.plot(df_CY_12.index,df_CY_12['AdjClose'], c='r')
plt.plot(df_MSFT_12.index,df_MSFT_12['AdjClose'], c='g')
plt.show()
```


![png](output_73_0.png)



```python
plt.plot(df_CY_13.index,df_CY_13['AdjClose'], c='r')
plt.plot(df_MSFT_13.index,df_MSFT_13['AdjClose'], c='g')
plt.show()
```


![png](output_74_0.png)



```python
plt.plot(df_CY_14.index,df_CY_14['AdjClose'], c='r')
plt.plot(df_MSFT_14.index,df_MSFT_14['AdjClose'], c='g')
plt.show()
```


![png](output_75_0.png)



```python
plt.plot(df_CY_15.index,df_CY_15['AdjClose'], c='r')
plt.plot(df_MSFT_15.index,df_MSFT_15['AdjClose'], c='g')
plt.show()
```


![png](output_76_0.png)



```python
plt.plot(df_CY_16.index,df_CY_16['AdjClose'], c='r')
plt.plot(df_MSFT_16.index,df_MSFT_16['AdjClose'], c='g')
plt.show()
```


![png](output_77_0.png)



```python
plt.plot(df_CY_17.index,df_CY_17['AdjClose'], c='r')
plt.plot(df_MSFT_17.index,df_MSFT_17['AdjClose'], c='g')
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
df_MSFT_07.head()
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
      <td>35.90</td>
      <td>35.9900</td>
      <td>35.52</td>
      <td>35.60</td>
      <td>35229700.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>27.988417</td>
      <td>28.058583</td>
      <td>27.692161</td>
      <td>27.754531</td>
      <td>35229700.0</td>
    </tr>
    <tr>
      <th>2007-12-28</th>
      <td>36.10</td>
      <td>36.2300</td>
      <td>35.67</td>
      <td>36.12</td>
      <td>33447200.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>28.144342</td>
      <td>28.245692</td>
      <td>27.809104</td>
      <td>28.159934</td>
      <td>33447200.0</td>
    </tr>
    <tr>
      <th>2007-12-27</th>
      <td>36.35</td>
      <td>36.5501</td>
      <td>35.94</td>
      <td>35.97</td>
      <td>33311100.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>28.339247</td>
      <td>28.495249</td>
      <td>28.019602</td>
      <td>28.042991</td>
      <td>33311100.0</td>
    </tr>
    <tr>
      <th>2007-12-26</th>
      <td>36.41</td>
      <td>36.6400</td>
      <td>36.26</td>
      <td>36.61</td>
      <td>30252400.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>28.386024</td>
      <td>28.565337</td>
      <td>28.269081</td>
      <td>28.541949</td>
      <td>30252400.0</td>
    </tr>
    <tr>
      <th>2007-12-24</th>
      <td>36.13</td>
      <td>36.7200</td>
      <td>36.05</td>
      <td>36.58</td>
      <td>29622600.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>28.167730</td>
      <td>28.627707</td>
      <td>28.105360</td>
      <td>28.518560</td>
      <td>29622600.0</td>
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
df_MSFT_07['Diff'] = df_MSFT_07['AdjClose'] - df_MSFT_07['AdjClose'].shift(1)
df_MSFT_08['Diff'] = df_MSFT_08['AdjClose'] - df_MSFT_08['AdjClose'].shift(1)
df_MSFT_09['Diff'] = df_MSFT_09['AdjClose'] - df_MSFT_09['AdjClose'].shift(1)
df_MSFT_10['Diff'] = df_MSFT_10['AdjClose'] - df_MSFT_10['AdjClose'].shift(1)
df_MSFT_11['Diff'] = df_MSFT_11['AdjClose'] - df_MSFT_11['AdjClose'].shift(1)
df_MSFT_12['Diff'] = df_MSFT_12['AdjClose'] - df_MSFT_12['AdjClose'].shift(1)
df_MSFT_13['Diff'] = df_MSFT_13['AdjClose'] - df_MSFT_13['AdjClose'].shift(1)
df_MSFT_14['Diff'] = df_MSFT_14['AdjClose'] - df_MSFT_14['AdjClose'].shift(1)
df_MSFT_15['Diff'] = df_MSFT_15['AdjClose'] - df_MSFT_15['AdjClose'].shift(1)
df_MSFT_16['Diff'] = df_MSFT_16['AdjClose'] - df_MSFT_16['AdjClose'].shift(1)
df_MSFT_17['Diff'] = df_MSFT_17['AdjClose'] - df_MSFT_17['AdjClose'].shift(1)
df_MSFT_07.head()
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
      <td>35.90</td>
      <td>35.9900</td>
      <td>35.52</td>
      <td>35.60</td>
      <td>35229700.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>27.988417</td>
      <td>28.058583</td>
      <td>27.692161</td>
      <td>27.754531</td>
      <td>35229700.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2007-12-28</th>
      <td>36.10</td>
      <td>36.2300</td>
      <td>35.67</td>
      <td>36.12</td>
      <td>33447200.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>28.144342</td>
      <td>28.245692</td>
      <td>27.809104</td>
      <td>28.159934</td>
      <td>33447200.0</td>
      <td>0.405403</td>
    </tr>
    <tr>
      <th>2007-12-27</th>
      <td>36.35</td>
      <td>36.5501</td>
      <td>35.94</td>
      <td>35.97</td>
      <td>33311100.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>28.339247</td>
      <td>28.495249</td>
      <td>28.019602</td>
      <td>28.042991</td>
      <td>33311100.0</td>
      <td>-0.116943</td>
    </tr>
    <tr>
      <th>2007-12-26</th>
      <td>36.41</td>
      <td>36.6400</td>
      <td>36.26</td>
      <td>36.61</td>
      <td>30252400.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>28.386024</td>
      <td>28.565337</td>
      <td>28.269081</td>
      <td>28.541949</td>
      <td>30252400.0</td>
      <td>0.498958</td>
    </tr>
    <tr>
      <th>2007-12-24</th>
      <td>36.13</td>
      <td>36.7200</td>
      <td>36.05</td>
      <td>36.58</td>
      <td>29622600.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>28.167730</td>
      <td>28.627707</td>
      <td>28.105360</td>
      <td>28.518560</td>
      <td>29622600.0</td>
      <td>-0.023389</td>
    </tr>
  </tbody>
</table>
</div>




```python
df_MSFT_17
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
      <td>85.630</td>
      <td>86.0500</td>
      <td>85.5000</td>
      <td>85.540</td>
      <td>18162779.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>85.630000</td>
      <td>86.050000</td>
      <td>85.500000</td>
      <td>85.540000</td>
      <td>18162779.0</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2017-12-28</th>
      <td>85.900</td>
      <td>85.9300</td>
      <td>85.5500</td>
      <td>85.720</td>
      <td>9872795.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>85.900000</td>
      <td>85.930000</td>
      <td>85.550000</td>
      <td>85.720000</td>
      <td>9872795.0</td>
      <td>0.180000</td>
    </tr>
    <tr>
      <th>2017-12-27</th>
      <td>85.650</td>
      <td>85.9800</td>
      <td>85.2150</td>
      <td>85.710</td>
      <td>13000828.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>85.650000</td>
      <td>85.980000</td>
      <td>85.215000</td>
      <td>85.710000</td>
      <td>13000828.0</td>
      <td>-0.010000</td>
    </tr>
    <tr>
      <th>2017-12-26</th>
      <td>85.310</td>
      <td>85.5346</td>
      <td>85.0300</td>
      <td>85.400</td>
      <td>9737412.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>85.310000</td>
      <td>85.534600</td>
      <td>85.030000</td>
      <td>85.400000</td>
      <td>9737412.0</td>
      <td>-0.310000</td>
    </tr>
    <tr>
      <th>2017-12-22</th>
      <td>85.400</td>
      <td>85.6300</td>
      <td>84.9200</td>
      <td>85.510</td>
      <td>14033977.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>85.400000</td>
      <td>85.630000</td>
      <td>84.920000</td>
      <td>85.510000</td>
      <td>14033977.0</td>
      <td>0.110000</td>
    </tr>
    <tr>
      <th>2017-12-21</th>
      <td>86.050</td>
      <td>86.1000</td>
      <td>85.4000</td>
      <td>85.500</td>
      <td>16638402.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>86.050000</td>
      <td>86.100000</td>
      <td>85.400000</td>
      <td>85.500000</td>
      <td>16638402.0</td>
      <td>-0.010000</td>
    </tr>
    <tr>
      <th>2017-12-20</th>
      <td>86.200</td>
      <td>86.3000</td>
      <td>84.7100</td>
      <td>85.520</td>
      <td>23425009.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>86.200000</td>
      <td>86.300000</td>
      <td>84.710000</td>
      <td>85.520000</td>
      <td>23425009.0</td>
      <td>0.020000</td>
    </tr>
    <tr>
      <th>2017-12-19</th>
      <td>86.350</td>
      <td>86.3500</td>
      <td>85.2700</td>
      <td>85.830</td>
      <td>23241979.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>86.350000</td>
      <td>86.350000</td>
      <td>85.270000</td>
      <td>85.830000</td>
      <td>23241979.0</td>
      <td>0.310000</td>
    </tr>
    <tr>
      <th>2017-12-18</th>
      <td>87.120</td>
      <td>87.4999</td>
      <td>86.2300</td>
      <td>86.380</td>
      <td>21551076.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>87.120000</td>
      <td>87.499900</td>
      <td>86.230000</td>
      <td>86.380000</td>
      <td>21551076.0</td>
      <td>0.550000</td>
    </tr>
    <tr>
      <th>2017-12-15</th>
      <td>85.260</td>
      <td>87.0900</td>
      <td>84.8800</td>
      <td>86.850</td>
      <td>52430167.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>85.260000</td>
      <td>87.090000</td>
      <td>84.880000</td>
      <td>86.850000</td>
      <td>52430167.0</td>
      <td>0.470000</td>
    </tr>
    <tr>
      <th>2017-12-14</th>
      <td>85.430</td>
      <td>85.8739</td>
      <td>84.5300</td>
      <td>84.690</td>
      <td>19080106.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>85.430000</td>
      <td>85.873900</td>
      <td>84.530000</td>
      <td>84.690000</td>
      <td>19080106.0</td>
      <td>-2.160000</td>
    </tr>
    <tr>
      <th>2017-12-13</th>
      <td>85.740</td>
      <td>86.0000</td>
      <td>85.1700</td>
      <td>85.350</td>
      <td>21307911.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>85.740000</td>
      <td>86.000000</td>
      <td>85.170000</td>
      <td>85.350000</td>
      <td>21307911.0</td>
      <td>0.660000</td>
    </tr>
    <tr>
      <th>2017-12-12</th>
      <td>85.310</td>
      <td>86.0500</td>
      <td>85.0800</td>
      <td>85.580</td>
      <td>23534946.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>85.310000</td>
      <td>86.050000</td>
      <td>85.080000</td>
      <td>85.580000</td>
      <td>23534946.0</td>
      <td>0.230000</td>
    </tr>
    <tr>
      <th>2017-12-11</th>
      <td>84.290</td>
      <td>85.3700</td>
      <td>84.1200</td>
      <td>85.230</td>
      <td>19909119.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>84.290000</td>
      <td>85.370000</td>
      <td>84.120000</td>
      <td>85.230000</td>
      <td>19909119.0</td>
      <td>-0.350000</td>
    </tr>
    <tr>
      <th>2017-12-08</th>
      <td>83.630</td>
      <td>84.5800</td>
      <td>83.3300</td>
      <td>84.160</td>
      <td>23825056.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.630000</td>
      <td>84.580000</td>
      <td>83.330000</td>
      <td>84.160000</td>
      <td>23825056.0</td>
      <td>-1.070000</td>
    </tr>
    <tr>
      <th>2017-12-07</th>
      <td>82.540</td>
      <td>82.8000</td>
      <td>82.0000</td>
      <td>82.490</td>
      <td>20378114.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>82.540000</td>
      <td>82.800000</td>
      <td>82.000000</td>
      <td>82.490000</td>
      <td>20378114.0</td>
      <td>-1.670000</td>
    </tr>
    <tr>
      <th>2017-12-06</th>
      <td>81.550</td>
      <td>83.1400</td>
      <td>81.4300</td>
      <td>82.780</td>
      <td>24821403.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>81.550000</td>
      <td>83.140000</td>
      <td>81.430000</td>
      <td>82.780000</td>
      <td>24821403.0</td>
      <td>0.290000</td>
    </tr>
    <tr>
      <th>2017-12-05</th>
      <td>81.340</td>
      <td>82.6800</td>
      <td>80.9801</td>
      <td>81.590</td>
      <td>25512120.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>81.340000</td>
      <td>82.680000</td>
      <td>80.980100</td>
      <td>81.590000</td>
      <td>25512120.0</td>
      <td>-1.190000</td>
    </tr>
    <tr>
      <th>2017-12-04</th>
      <td>84.420</td>
      <td>84.4299</td>
      <td>80.7000</td>
      <td>81.080</td>
      <td>37977732.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>84.420000</td>
      <td>84.429900</td>
      <td>80.700000</td>
      <td>81.080000</td>
      <td>37977732.0</td>
      <td>-0.510000</td>
    </tr>
    <tr>
      <th>2017-12-01</th>
      <td>83.600</td>
      <td>84.8100</td>
      <td>83.2200</td>
      <td>84.260</td>
      <td>29113662.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.600000</td>
      <td>84.810000</td>
      <td>83.220000</td>
      <td>84.260000</td>
      <td>29113662.0</td>
      <td>3.180000</td>
    </tr>
    <tr>
      <th>2017-11-30</th>
      <td>83.510</td>
      <td>84.5200</td>
      <td>83.3400</td>
      <td>84.170</td>
      <td>32074914.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.510000</td>
      <td>84.520000</td>
      <td>83.340000</td>
      <td>84.170000</td>
      <td>32074914.0</td>
      <td>-0.090000</td>
    </tr>
    <tr>
      <th>2017-11-29</th>
      <td>84.710</td>
      <td>84.9172</td>
      <td>83.1750</td>
      <td>83.340</td>
      <td>26401761.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>84.710000</td>
      <td>84.917200</td>
      <td>83.175000</td>
      <td>83.340000</td>
      <td>26401761.0</td>
      <td>-0.830000</td>
    </tr>
    <tr>
      <th>2017-11-28</th>
      <td>84.070</td>
      <td>85.0600</td>
      <td>84.0200</td>
      <td>84.880</td>
      <td>21162639.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>84.070000</td>
      <td>85.060000</td>
      <td>84.020000</td>
      <td>84.880000</td>
      <td>21162639.0</td>
      <td>1.540000</td>
    </tr>
    <tr>
      <th>2017-11-27</th>
      <td>83.310</td>
      <td>83.9800</td>
      <td>83.3000</td>
      <td>83.870</td>
      <td>17603760.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.310000</td>
      <td>83.980000</td>
      <td>83.300000</td>
      <td>83.870000</td>
      <td>17603760.0</td>
      <td>-1.010000</td>
    </tr>
    <tr>
      <th>2017-11-24</th>
      <td>83.010</td>
      <td>83.4300</td>
      <td>82.7800</td>
      <td>83.260</td>
      <td>7425503.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.010000</td>
      <td>83.430000</td>
      <td>82.780000</td>
      <td>83.260000</td>
      <td>7425503.0</td>
      <td>-0.610000</td>
    </tr>
    <tr>
      <th>2017-11-22</th>
      <td>83.830</td>
      <td>83.9000</td>
      <td>83.0400</td>
      <td>83.110</td>
      <td>20213704.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.830000</td>
      <td>83.900000</td>
      <td>83.040000</td>
      <td>83.110000</td>
      <td>20213704.0</td>
      <td>-0.150000</td>
    </tr>
    <tr>
      <th>2017-11-21</th>
      <td>82.740</td>
      <td>83.8400</td>
      <td>82.7400</td>
      <td>83.720</td>
      <td>21033981.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>82.740000</td>
      <td>83.840000</td>
      <td>82.740000</td>
      <td>83.720000</td>
      <td>21033981.0</td>
      <td>0.610000</td>
    </tr>
    <tr>
      <th>2017-11-20</th>
      <td>82.400</td>
      <td>82.5900</td>
      <td>82.2500</td>
      <td>82.530</td>
      <td>16072495.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>82.400000</td>
      <td>82.590000</td>
      <td>82.250000</td>
      <td>82.530000</td>
      <td>16072495.0</td>
      <td>-1.190000</td>
    </tr>
    <tr>
      <th>2017-11-17</th>
      <td>83.120</td>
      <td>83.1200</td>
      <td>82.2400</td>
      <td>82.400</td>
      <td>21715498.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.120000</td>
      <td>83.120000</td>
      <td>82.240000</td>
      <td>82.400000</td>
      <td>21715498.0</td>
      <td>-0.130000</td>
    </tr>
    <tr>
      <th>2017-11-16</th>
      <td>83.100</td>
      <td>83.4200</td>
      <td>82.9400</td>
      <td>83.200</td>
      <td>20659209.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.100000</td>
      <td>83.420000</td>
      <td>82.940000</td>
      <td>83.200000</td>
      <td>20659209.0</td>
      <td>0.800000</td>
    </tr>
    <tr>
      <th>2017-11-15</th>
      <td>83.470</td>
      <td>83.6900</td>
      <td>82.6900</td>
      <td>82.980</td>
      <td>19097333.0</td>
      <td>0.42</td>
      <td>1.0</td>
      <td>83.470000</td>
      <td>83.690000</td>
      <td>82.690000</td>
      <td>82.980000</td>
      <td>19097333.0</td>
      <td>-0.220000</td>
    </tr>
    <tr>
      <th>2017-11-14</th>
      <td>83.500</td>
      <td>84.1000</td>
      <td>82.9800</td>
      <td>84.050</td>
      <td>18604034.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.079496</td>
      <td>83.676475</td>
      <td>82.562115</td>
      <td>83.626727</td>
      <td>18604034.0</td>
      <td>0.646727</td>
    </tr>
    <tr>
      <th>2017-11-13</th>
      <td>83.660</td>
      <td>83.9400</td>
      <td>83.4600</td>
      <td>83.930</td>
      <td>14080820.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.238691</td>
      <td>83.517281</td>
      <td>83.039698</td>
      <td>83.507331</td>
      <td>14080820.0</td>
      <td>-0.119396</td>
    </tr>
    <tr>
      <th>2017-11-10</th>
      <td>83.790</td>
      <td>84.0950</td>
      <td>83.2300</td>
      <td>83.870</td>
      <td>19340435.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.368036</td>
      <td>83.671500</td>
      <td>82.810856</td>
      <td>83.447633</td>
      <td>19340435.0</td>
      <td>-0.059698</td>
    </tr>
    <tr>
      <th>2017-11-09</th>
      <td>84.110</td>
      <td>84.2700</td>
      <td>82.9000</td>
      <td>84.090</td>
      <td>20924172.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.686424</td>
      <td>83.845619</td>
      <td>82.482518</td>
      <td>83.666525</td>
      <td>20924172.0</td>
      <td>0.218892</td>
    </tr>
    <tr>
      <th>2017-11-07</th>
      <td>84.770</td>
      <td>84.9000</td>
      <td>83.9300</td>
      <td>84.270</td>
      <td>17152583.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>84.343101</td>
      <td>84.472446</td>
      <td>83.507331</td>
      <td>83.845619</td>
      <td>17152583.0</td>
      <td>0.179094</td>
    </tr>
    <tr>
      <th>2017-11-06</th>
      <td>84.200</td>
      <td>84.7000</td>
      <td>84.0825</td>
      <td>84.470</td>
      <td>19039847.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.775971</td>
      <td>84.273453</td>
      <td>83.659063</td>
      <td>84.044612</td>
      <td>19039847.0</td>
      <td>0.198993</td>
    </tr>
    <tr>
      <th>2017-11-03</th>
      <td>84.080</td>
      <td>84.5400</td>
      <td>83.4000</td>
      <td>84.140</td>
      <td>17569120.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.656576</td>
      <td>84.114259</td>
      <td>82.980000</td>
      <td>83.716273</td>
      <td>17569120.0</td>
      <td>-0.328338</td>
    </tr>
    <tr>
      <th>2017-11-02</th>
      <td>83.350</td>
      <td>84.4600</td>
      <td>83.1200</td>
      <td>84.050</td>
      <td>23822964.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>82.930252</td>
      <td>84.034662</td>
      <td>82.701410</td>
      <td>83.626727</td>
      <td>23822964.0</td>
      <td>-0.089547</td>
    </tr>
    <tr>
      <th>2017-11-01</th>
      <td>83.680</td>
      <td>83.7600</td>
      <td>82.8800</td>
      <td>83.180</td>
      <td>22039635.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.258590</td>
      <td>83.338187</td>
      <td>82.462619</td>
      <td>82.761108</td>
      <td>22039635.0</td>
      <td>-0.865619</td>
    </tr>
    <tr>
      <th>2017-10-31</th>
      <td>84.360</td>
      <td>84.3600</td>
      <td>83.1100</td>
      <td>83.180</td>
      <td>26728947.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.935165</td>
      <td>83.935165</td>
      <td>82.691460</td>
      <td>82.761108</td>
      <td>26728947.0</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2017-10-30</th>
      <td>83.700</td>
      <td>84.3250</td>
      <td>83.1050</td>
      <td>83.890</td>
      <td>31291801.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.278489</td>
      <td>83.900342</td>
      <td>82.686486</td>
      <td>83.467532</td>
      <td>31291801.0</td>
      <td>0.706424</td>
    </tr>
    <tr>
      <th>2017-10-27</th>
      <td>84.370</td>
      <td>86.2000</td>
      <td>83.6100</td>
      <td>83.810</td>
      <td>70877350.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>83.945115</td>
      <td>85.765899</td>
      <td>83.188942</td>
      <td>83.387935</td>
      <td>70877350.0</td>
      <td>-0.079597</td>
    </tr>
    <tr>
      <th>2017-10-26</th>
      <td>79.200</td>
      <td>79.4200</td>
      <td>78.7500</td>
      <td>78.760</td>
      <td>29181652.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>78.801151</td>
      <td>79.020043</td>
      <td>78.353417</td>
      <td>78.363367</td>
      <td>29181652.0</td>
      <td>-5.024568</td>
    </tr>
    <tr>
      <th>2017-10-25</th>
      <td>78.580</td>
      <td>79.1000</td>
      <td>78.0100</td>
      <td>78.630</td>
      <td>19714512.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>78.184273</td>
      <td>78.701655</td>
      <td>77.617144</td>
      <td>78.234022</td>
      <td>19714512.0</td>
      <td>-0.129345</td>
    </tr>
    <tr>
      <th>2017-10-24</th>
      <td>78.900</td>
      <td>79.2000</td>
      <td>78.4600</td>
      <td>78.860</td>
      <td>16613928.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>78.502662</td>
      <td>78.801151</td>
      <td>78.064878</td>
      <td>78.462863</td>
      <td>16613928.0</td>
      <td>0.228842</td>
    </tr>
    <tr>
      <th>2017-10-23</th>
      <td>78.990</td>
      <td>79.3400</td>
      <td>78.7600</td>
      <td>78.830</td>
      <td>20479731.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>78.592209</td>
      <td>78.940446</td>
      <td>78.363367</td>
      <td>78.433014</td>
      <td>20479731.0</td>
      <td>-0.029849</td>
    </tr>
    <tr>
      <th>2017-10-20</th>
      <td>78.320</td>
      <td>78.9700</td>
      <td>78.2200</td>
      <td>78.810</td>
      <td>22517092.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>77.925583</td>
      <td>78.572309</td>
      <td>77.826086</td>
      <td>78.413115</td>
      <td>22517092.0</td>
      <td>-0.019899</td>
    </tr>
    <tr>
      <th>2017-10-19</th>
      <td>77.570</td>
      <td>77.9300</td>
      <td>77.3500</td>
      <td>77.910</td>
      <td>14982129.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>77.179360</td>
      <td>77.537547</td>
      <td>76.960468</td>
      <td>77.517647</td>
      <td>14982129.0</td>
      <td>-0.895468</td>
    </tr>
    <tr>
      <th>2017-10-18</th>
      <td>77.670</td>
      <td>77.8500</td>
      <td>77.3700</td>
      <td>77.610</td>
      <td>13147124.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>77.278856</td>
      <td>77.457950</td>
      <td>76.980367</td>
      <td>77.219158</td>
      <td>13147124.0</td>
      <td>-0.298489</td>
    </tr>
    <tr>
      <th>2017-10-17</th>
      <td>77.470</td>
      <td>77.6200</td>
      <td>77.2500</td>
      <td>77.590</td>
      <td>15953665.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>77.079863</td>
      <td>77.229108</td>
      <td>76.860971</td>
      <td>77.199259</td>
      <td>15953665.0</td>
      <td>-0.019899</td>
    </tr>
    <tr>
      <th>2017-10-16</th>
      <td>77.420</td>
      <td>77.8100</td>
      <td>77.3500</td>
      <td>77.650</td>
      <td>12331147.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>77.030115</td>
      <td>77.418151</td>
      <td>76.960468</td>
      <td>77.258957</td>
      <td>12331147.0</td>
      <td>0.059698</td>
    </tr>
    <tr>
      <th>2017-10-13</th>
      <td>77.590</td>
      <td>77.8700</td>
      <td>77.2900</td>
      <td>77.490</td>
      <td>15250772.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>77.199259</td>
      <td>77.477849</td>
      <td>76.900770</td>
      <td>77.099763</td>
      <td>15250772.0</td>
      <td>-0.159194</td>
    </tr>
    <tr>
      <th>2017-10-12</th>
      <td>76.490</td>
      <td>77.2900</td>
      <td>76.3700</td>
      <td>77.120</td>
      <td>16778148.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>76.104799</td>
      <td>76.900770</td>
      <td>75.985403</td>
      <td>76.731626</td>
      <td>16778148.0</td>
      <td>-0.368137</td>
    </tr>
    <tr>
      <th>2017-10-11</th>
      <td>76.360</td>
      <td>76.4600</td>
      <td>75.9500</td>
      <td>76.420</td>
      <td>14780652.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>75.975453</td>
      <td>76.074950</td>
      <td>75.567518</td>
      <td>76.035151</td>
      <td>14780652.0</td>
      <td>-0.696475</td>
    </tr>
    <tr>
      <th>2017-10-10</th>
      <td>76.330</td>
      <td>76.6300</td>
      <td>76.1400</td>
      <td>76.290</td>
      <td>13734627.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>75.945604</td>
      <td>76.244094</td>
      <td>75.756561</td>
      <td>75.905806</td>
      <td>13734627.0</td>
      <td>-0.129345</td>
    </tr>
    <tr>
      <th>2017-10-09</th>
      <td>75.970</td>
      <td>76.5500</td>
      <td>75.8600</td>
      <td>76.290</td>
      <td>11364275.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>75.587417</td>
      <td>76.164496</td>
      <td>75.477971</td>
      <td>75.905806</td>
      <td>11364275.0</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2017-10-06</th>
      <td>75.670</td>
      <td>76.0300</td>
      <td>75.5400</td>
      <td>76.000</td>
      <td>13692791.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>75.288928</td>
      <td>75.647115</td>
      <td>75.159583</td>
      <td>75.617266</td>
      <td>13692791.0</td>
      <td>-0.288540</td>
    </tr>
    <tr>
      <th>2017-10-05</th>
      <td>75.220</td>
      <td>76.1200</td>
      <td>74.9600</td>
      <td>75.970</td>
      <td>20656238.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>74.841194</td>
      <td>75.736662</td>
      <td>74.582504</td>
      <td>75.587417</td>
      <td>20656238.0</td>
      <td>-0.029849</td>
    </tr>
    <tr>
      <th>2017-10-04</th>
      <td>74.000</td>
      <td>74.7200</td>
      <td>73.7100</td>
      <td>74.690</td>
      <td>13287346.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.627338</td>
      <td>74.343712</td>
      <td>73.338799</td>
      <td>74.313863</td>
      <td>13287346.0</td>
      <td>-1.273554</td>
    </tr>
    <tr>
      <th>2017-10-03</th>
      <td>74.670</td>
      <td>74.8800</td>
      <td>74.1950</td>
      <td>74.260</td>
      <td>11935853.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>74.293964</td>
      <td>74.502906</td>
      <td>73.821356</td>
      <td>73.886029</td>
      <td>11935853.0</td>
      <td>-0.427835</td>
    </tr>
    <tr>
      <th>2017-10-02</th>
      <td>74.710</td>
      <td>75.0100</td>
      <td>74.2950</td>
      <td>74.610</td>
      <td>15210338.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>74.333763</td>
      <td>74.632252</td>
      <td>73.920853</td>
      <td>74.234266</td>
      <td>15210338.0</td>
      <td>0.348237</td>
    </tr>
    <tr>
      <th>2017-09-29</th>
      <td>73.940</td>
      <td>74.5350</td>
      <td>73.8800</td>
      <td>74.490</td>
      <td>16700435.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.567640</td>
      <td>74.159644</td>
      <td>73.507942</td>
      <td>74.114871</td>
      <td>16700435.0</td>
      <td>-0.119396</td>
    </tr>
    <tr>
      <th>2017-09-28</th>
      <td>73.540</td>
      <td>73.9700</td>
      <td>73.3100</td>
      <td>73.870</td>
      <td>10814063.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.169655</td>
      <td>73.597489</td>
      <td>72.940813</td>
      <td>73.497993</td>
      <td>10814063.0</td>
      <td>-0.616878</td>
    </tr>
    <tr>
      <th>2017-09-27</th>
      <td>73.550</td>
      <td>74.1700</td>
      <td>73.1700</td>
      <td>73.850</td>
      <td>18934048.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.179604</td>
      <td>73.796482</td>
      <td>72.801518</td>
      <td>73.478094</td>
      <td>18934048.0</td>
      <td>-0.019899</td>
    </tr>
    <tr>
      <th>2017-09-26</th>
      <td>73.670</td>
      <td>73.8100</td>
      <td>72.9900</td>
      <td>73.260</td>
      <td>17105469.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.299000</td>
      <td>73.438295</td>
      <td>72.622424</td>
      <td>72.891065</td>
      <td>17105469.0</td>
      <td>-0.587029</td>
    </tr>
    <tr>
      <th>2017-09-25</th>
      <td>74.090</td>
      <td>74.2500</td>
      <td>72.9200</td>
      <td>73.260</td>
      <td>23502422.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.716885</td>
      <td>73.876079</td>
      <td>72.552777</td>
      <td>72.891065</td>
      <td>23502422.0</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2017-09-22</th>
      <td>73.990</td>
      <td>74.5100</td>
      <td>73.8500</td>
      <td>74.410</td>
      <td>13969937.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.617388</td>
      <td>74.134770</td>
      <td>73.478094</td>
      <td>74.035273</td>
      <td>13969937.0</td>
      <td>1.144209</td>
    </tr>
    <tr>
      <th>2017-09-21</th>
      <td>75.110</td>
      <td>75.2400</td>
      <td>74.1100</td>
      <td>74.210</td>
      <td>19038998.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>74.731748</td>
      <td>74.861094</td>
      <td>73.736784</td>
      <td>73.836281</td>
      <td>19038998.0</td>
      <td>-0.198993</td>
    </tr>
    <tr>
      <th>2017-09-20</th>
      <td>75.350</td>
      <td>75.5500</td>
      <td>74.3100</td>
      <td>74.940</td>
      <td>20415084.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>74.970540</td>
      <td>75.169532</td>
      <td>73.935777</td>
      <td>74.562604</td>
      <td>20415084.0</td>
      <td>0.726324</td>
    </tr>
    <tr>
      <th>2017-09-19</th>
      <td>75.210</td>
      <td>75.7100</td>
      <td>75.0100</td>
      <td>75.440</td>
      <td>15606870.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>74.831245</td>
      <td>75.328727</td>
      <td>74.632252</td>
      <td>75.060086</td>
      <td>15606870.0</td>
      <td>0.497482</td>
    </tr>
    <tr>
      <th>2017-09-18</th>
      <td>75.230</td>
      <td>75.9700</td>
      <td>75.0400</td>
      <td>75.160</td>
      <td>22730355.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>74.851144</td>
      <td>75.587417</td>
      <td>74.662101</td>
      <td>74.781496</td>
      <td>22730355.0</td>
      <td>-0.278590</td>
    </tr>
    <tr>
      <th>2017-09-15</th>
      <td>74.830</td>
      <td>75.3900</td>
      <td>74.0700</td>
      <td>75.310</td>
      <td>37901927.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>74.453158</td>
      <td>75.010338</td>
      <td>73.696986</td>
      <td>74.930741</td>
      <td>37901927.0</td>
      <td>0.149245</td>
    </tr>
    <tr>
      <th>2017-09-14</th>
      <td>75.000</td>
      <td>75.4900</td>
      <td>74.5200</td>
      <td>74.770</td>
      <td>15373384.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>74.622302</td>
      <td>75.109835</td>
      <td>74.144719</td>
      <td>74.393460</td>
      <td>15373384.0</td>
      <td>-0.537281</td>
    </tr>
    <tr>
      <th>2017-09-13</th>
      <td>74.930</td>
      <td>75.2300</td>
      <td>74.5500</td>
      <td>75.210</td>
      <td>12998629.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>74.552655</td>
      <td>74.851144</td>
      <td>74.174568</td>
      <td>74.831245</td>
      <td>12998629.0</td>
      <td>0.437784</td>
    </tr>
    <tr>
      <th>2017-09-12</th>
      <td>74.760</td>
      <td>75.2400</td>
      <td>74.3700</td>
      <td>74.680</td>
      <td>14003880.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>74.383511</td>
      <td>74.861094</td>
      <td>73.995475</td>
      <td>74.303914</td>
      <td>14003880.0</td>
      <td>-0.527331</td>
    </tr>
    <tr>
      <th>2017-09-11</th>
      <td>74.310</td>
      <td>74.9450</td>
      <td>74.3100</td>
      <td>74.760</td>
      <td>17428067.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.935777</td>
      <td>74.567579</td>
      <td>73.935777</td>
      <td>74.383511</td>
      <td>17428067.0</td>
      <td>0.079597</td>
    </tr>
    <tr>
      <th>2017-09-08</th>
      <td>74.330</td>
      <td>74.4400</td>
      <td>73.8400</td>
      <td>73.980</td>
      <td>14474383.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.955676</td>
      <td>74.065122</td>
      <td>73.468144</td>
      <td>73.607439</td>
      <td>14474383.0</td>
      <td>-0.776072</td>
    </tr>
    <tr>
      <th>2017-09-07</th>
      <td>73.680</td>
      <td>74.6000</td>
      <td>73.6000</td>
      <td>74.340</td>
      <td>17165518.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.308950</td>
      <td>74.224317</td>
      <td>73.229353</td>
      <td>73.965626</td>
      <td>17165518.0</td>
      <td>0.358187</td>
    </tr>
    <tr>
      <th>2017-09-06</th>
      <td>73.740</td>
      <td>74.0400</td>
      <td>73.3500</td>
      <td>73.400</td>
      <td>15945136.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.368647</td>
      <td>73.667137</td>
      <td>72.980612</td>
      <td>73.030360</td>
      <td>15945136.0</td>
      <td>-0.935266</td>
    </tr>
    <tr>
      <th>2017-09-05</th>
      <td>73.340</td>
      <td>73.8900</td>
      <td>72.9800</td>
      <td>73.610</td>
      <td>21432599.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.970662</td>
      <td>73.517892</td>
      <td>72.612475</td>
      <td>73.239302</td>
      <td>21432599.0</td>
      <td>0.208942</td>
    </tr>
    <tr>
      <th>2017-09-01</th>
      <td>74.710</td>
      <td>74.7400</td>
      <td>73.6400</td>
      <td>73.940</td>
      <td>21593192.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>74.333763</td>
      <td>74.363612</td>
      <td>73.269151</td>
      <td>73.567640</td>
      <td>21593192.0</td>
      <td>0.328338</td>
    </tr>
    <tr>
      <th>2017-08-31</th>
      <td>74.030</td>
      <td>74.9600</td>
      <td>73.8000</td>
      <td>74.770</td>
      <td>26688077.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.657187</td>
      <td>74.582504</td>
      <td>73.428345</td>
      <td>74.393460</td>
      <td>26688077.0</td>
      <td>0.825820</td>
    </tr>
    <tr>
      <th>2017-08-30</th>
      <td>73.010</td>
      <td>74.2099</td>
      <td>72.8293</td>
      <td>74.010</td>
      <td>16826094.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.642324</td>
      <td>73.836181</td>
      <td>72.462534</td>
      <td>73.637288</td>
      <td>16826094.0</td>
      <td>-0.756173</td>
    </tr>
    <tr>
      <th>2017-08-29</th>
      <td>72.250</td>
      <td>73.1600</td>
      <td>72.0500</td>
      <td>73.050</td>
      <td>11325418.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.886151</td>
      <td>72.791568</td>
      <td>71.687158</td>
      <td>72.682122</td>
      <td>11325418.0</td>
      <td>-0.955165</td>
    </tr>
    <tr>
      <th>2017-08-28</th>
      <td>73.060</td>
      <td>73.0900</td>
      <td>72.5500</td>
      <td>72.830</td>
      <td>14112777.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.692072</td>
      <td>72.721921</td>
      <td>72.184640</td>
      <td>72.463230</td>
      <td>14112777.0</td>
      <td>-0.218892</td>
    </tr>
    <tr>
      <th>2017-08-25</th>
      <td>72.860</td>
      <td>73.3500</td>
      <td>72.4800</td>
      <td>72.820</td>
      <td>12574503.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.493079</td>
      <td>72.980612</td>
      <td>72.114993</td>
      <td>72.453281</td>
      <td>12574503.0</td>
      <td>-0.009950</td>
    </tr>
    <tr>
      <th>2017-08-24</th>
      <td>72.740</td>
      <td>72.8600</td>
      <td>72.0700</td>
      <td>72.690</td>
      <td>15980144.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.373683</td>
      <td>72.493079</td>
      <td>71.707058</td>
      <td>72.323935</td>
      <td>15980144.0</td>
      <td>-0.129345</td>
    </tr>
    <tr>
      <th>2017-08-23</th>
      <td>72.960</td>
      <td>73.1500</td>
      <td>72.5300</td>
      <td>72.720</td>
      <td>13586784.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.592576</td>
      <td>72.781619</td>
      <td>72.164741</td>
      <td>72.353784</td>
      <td>13586784.0</td>
      <td>0.029849</td>
    </tr>
    <tr>
      <th>2017-08-22</th>
      <td>72.350</td>
      <td>73.2400</td>
      <td>72.3500</td>
      <td>73.160</td>
      <td>14183146.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.985647</td>
      <td>72.871165</td>
      <td>71.985647</td>
      <td>72.791568</td>
      <td>14183146.0</td>
      <td>0.437784</td>
    </tr>
    <tr>
      <th>2017-08-21</th>
      <td>72.470</td>
      <td>72.4800</td>
      <td>71.7000</td>
      <td>72.150</td>
      <td>17656716.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.105043</td>
      <td>72.114993</td>
      <td>71.338921</td>
      <td>71.786655</td>
      <td>17656716.0</td>
      <td>-1.004914</td>
    </tr>
    <tr>
      <th>2017-08-18</th>
      <td>72.270</td>
      <td>72.8400</td>
      <td>71.9300</td>
      <td>72.490</td>
      <td>18215276.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.906050</td>
      <td>72.473180</td>
      <td>71.567763</td>
      <td>72.124942</td>
      <td>18215276.0</td>
      <td>0.338288</td>
    </tr>
    <tr>
      <th>2017-08-17</th>
      <td>73.580</td>
      <td>73.8700</td>
      <td>72.4000</td>
      <td>72.400</td>
      <td>21834250.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.209453</td>
      <td>73.497993</td>
      <td>72.035396</td>
      <td>72.035396</td>
      <td>21834250.0</td>
      <td>-0.089547</td>
    </tr>
    <tr>
      <th>2017-08-16</th>
      <td>73.340</td>
      <td>74.1000</td>
      <td>73.1700</td>
      <td>73.650</td>
      <td>17814317.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.970662</td>
      <td>73.726835</td>
      <td>72.801518</td>
      <td>73.279101</td>
      <td>17814317.0</td>
      <td>1.243705</td>
    </tr>
    <tr>
      <th>2017-08-15</th>
      <td>73.590</td>
      <td>73.5900</td>
      <td>73.0400</td>
      <td>73.220</td>
      <td>17791179.0</td>
      <td>0.39</td>
      <td>1.0</td>
      <td>73.219403</td>
      <td>73.219403</td>
      <td>72.672173</td>
      <td>72.851266</td>
      <td>17791179.0</td>
      <td>-0.427835</td>
    </tr>
    <tr>
      <th>2017-08-14</th>
      <td>73.060</td>
      <td>73.7200</td>
      <td>72.9500</td>
      <td>73.590</td>
      <td>19756773.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.306935</td>
      <td>72.960132</td>
      <td>72.198069</td>
      <td>72.831472</td>
      <td>19756773.0</td>
      <td>-0.019794</td>
    </tr>
    <tr>
      <th>2017-08-11</th>
      <td>71.610</td>
      <td>72.7000</td>
      <td>71.2800</td>
      <td>72.500</td>
      <td>21121250.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>70.871881</td>
      <td>71.950646</td>
      <td>70.545283</td>
      <td>71.752707</td>
      <td>21121250.0</td>
      <td>-1.078765</td>
    </tr>
    <tr>
      <th>2017-08-10</th>
      <td>71.900</td>
      <td>72.1900</td>
      <td>71.3500</td>
      <td>71.410</td>
      <td>23153711.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.158892</td>
      <td>71.445903</td>
      <td>70.614561</td>
      <td>70.673943</td>
      <td>23153711.0</td>
      <td>-1.078765</td>
    </tr>
    <tr>
      <th>2017-08-09</th>
      <td>72.250</td>
      <td>72.5100</td>
      <td>72.0500</td>
      <td>72.470</td>
      <td>20401071.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.505284</td>
      <td>71.762604</td>
      <td>71.307346</td>
      <td>71.723017</td>
      <td>20401071.0</td>
      <td>1.049074</td>
    </tr>
    <tr>
      <th>2017-08-08</th>
      <td>72.090</td>
      <td>73.1300</td>
      <td>71.7500</td>
      <td>72.790</td>
      <td>21446993.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.346934</td>
      <td>72.376214</td>
      <td>71.010438</td>
      <td>72.039718</td>
      <td>21446993.0</td>
      <td>0.316702</td>
    </tr>
    <tr>
      <th>2017-08-07</th>
      <td>72.800</td>
      <td>72.9000</td>
      <td>72.2600</td>
      <td>72.400</td>
      <td>18582345.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.049615</td>
      <td>72.148584</td>
      <td>71.515181</td>
      <td>71.653738</td>
      <td>18582345.0</td>
      <td>-0.385980</td>
    </tr>
    <tr>
      <th>2017-08-04</th>
      <td>72.400</td>
      <td>73.0400</td>
      <td>72.2400</td>
      <td>72.680</td>
      <td>22412719.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.653738</td>
      <td>72.287141</td>
      <td>71.495387</td>
      <td>71.930852</td>
      <td>22412719.0</td>
      <td>0.277114</td>
    </tr>
    <tr>
      <th>2017-08-03</th>
      <td>72.190</td>
      <td>72.4400</td>
      <td>71.8450</td>
      <td>72.150</td>
      <td>17937522.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.445903</td>
      <td>71.693326</td>
      <td>71.104459</td>
      <td>71.406315</td>
      <td>17937522.0</td>
      <td>-0.524537</td>
    </tr>
    <tr>
      <th>2017-08-02</th>
      <td>72.550</td>
      <td>72.5600</td>
      <td>71.4450</td>
      <td>72.260</td>
      <td>26405096.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.802192</td>
      <td>71.812089</td>
      <td>70.708582</td>
      <td>71.515181</td>
      <td>26405096.0</td>
      <td>0.108866</td>
    </tr>
    <tr>
      <th>2017-08-01</th>
      <td>73.100</td>
      <td>73.4200</td>
      <td>72.4900</td>
      <td>72.580</td>
      <td>19060885.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.346523</td>
      <td>72.663225</td>
      <td>71.742811</td>
      <td>71.831883</td>
      <td>19060885.0</td>
      <td>0.316702</td>
    </tr>
    <tr>
      <th>2017-07-31</th>
      <td>73.300</td>
      <td>73.4400</td>
      <td>72.4100</td>
      <td>72.720</td>
      <td>23151962.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.544462</td>
      <td>72.683018</td>
      <td>71.663635</td>
      <td>71.970440</td>
      <td>23151962.0</td>
      <td>0.138557</td>
    </tr>
    <tr>
      <th>2017-07-28</th>
      <td>72.670</td>
      <td>73.3100</td>
      <td>72.5400</td>
      <td>73.040</td>
      <td>17472880.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.920955</td>
      <td>72.554358</td>
      <td>71.792295</td>
      <td>72.287141</td>
      <td>17472880.0</td>
      <td>0.316702</td>
    </tr>
    <tr>
      <th>2017-07-27</th>
      <td>73.760</td>
      <td>74.4200</td>
      <td>72.3200</td>
      <td>73.160</td>
      <td>35518251.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.999720</td>
      <td>73.652917</td>
      <td>71.574563</td>
      <td>72.405905</td>
      <td>35518251.0</td>
      <td>0.118763</td>
    </tr>
    <tr>
      <th>2017-07-26</th>
      <td>74.340</td>
      <td>74.3800</td>
      <td>73.8100</td>
      <td>74.050</td>
      <td>15850344.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.573742</td>
      <td>73.613329</td>
      <td>73.049205</td>
      <td>73.286731</td>
      <td>15850344.0</td>
      <td>0.880826</td>
    </tr>
    <tr>
      <th>2017-07-25</th>
      <td>73.800</td>
      <td>74.3100</td>
      <td>73.5000</td>
      <td>74.190</td>
      <td>21522189.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.039308</td>
      <td>73.544051</td>
      <td>72.742400</td>
      <td>73.425288</td>
      <td>21522189.0</td>
      <td>0.138557</td>
    </tr>
    <tr>
      <th>2017-07-24</th>
      <td>73.530</td>
      <td>73.7500</td>
      <td>73.1300</td>
      <td>73.600</td>
      <td>20836422.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.772091</td>
      <td>72.989823</td>
      <td>72.376214</td>
      <td>72.841369</td>
      <td>20836422.0</td>
      <td>-0.583919</td>
    </tr>
    <tr>
      <th>2017-07-21</th>
      <td>73.450</td>
      <td>74.2900</td>
      <td>73.1700</td>
      <td>73.790</td>
      <td>45302930.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.692915</td>
      <td>73.524257</td>
      <td>72.415801</td>
      <td>73.029411</td>
      <td>45302930.0</td>
      <td>0.188042</td>
    </tr>
    <tr>
      <th>2017-07-20</th>
      <td>74.180</td>
      <td>74.3000</td>
      <td>73.2800</td>
      <td>74.240</td>
      <td>34174677.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>73.415391</td>
      <td>73.534154</td>
      <td>72.524668</td>
      <td>73.474772</td>
      <td>34174677.0</td>
      <td>0.445362</td>
    </tr>
    <tr>
      <th>2017-07-19</th>
      <td>73.500</td>
      <td>74.0400</td>
      <td>73.4500</td>
      <td>73.860</td>
      <td>21769229.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.742400</td>
      <td>73.276834</td>
      <td>72.692915</td>
      <td>73.098689</td>
      <td>21769229.0</td>
      <td>-0.376083</td>
    </tr>
    <tr>
      <th>2017-07-18</th>
      <td>73.090</td>
      <td>73.3900</td>
      <td>72.6600</td>
      <td>73.300</td>
      <td>26150272.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.336626</td>
      <td>72.633534</td>
      <td>71.911058</td>
      <td>72.544462</td>
      <td>26150272.0</td>
      <td>-0.554228</td>
    </tr>
    <tr>
      <th>2017-07-17</th>
      <td>72.800</td>
      <td>73.4500</td>
      <td>72.7200</td>
      <td>73.350</td>
      <td>21481069.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>72.049615</td>
      <td>72.692915</td>
      <td>71.970440</td>
      <td>72.593946</td>
      <td>21481069.0</td>
      <td>0.049485</td>
    </tr>
    <tr>
      <th>2017-07-14</th>
      <td>72.240</td>
      <td>73.2700</td>
      <td>71.9600</td>
      <td>72.780</td>
      <td>25689303.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.495387</td>
      <td>72.514771</td>
      <td>71.218274</td>
      <td>72.029821</td>
      <td>25689303.0</td>
      <td>-0.564125</td>
    </tr>
    <tr>
      <th>2017-07-13</th>
      <td>71.500</td>
      <td>72.0399</td>
      <td>71.3100</td>
      <td>71.770</td>
      <td>20149208.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>70.763015</td>
      <td>71.297350</td>
      <td>70.574973</td>
      <td>71.030232</td>
      <td>20149208.0</td>
      <td>-0.999589</td>
    </tr>
    <tr>
      <th>2017-07-12</th>
      <td>70.690</td>
      <td>71.2800</td>
      <td>70.5500</td>
      <td>71.150</td>
      <td>17382861.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>69.961364</td>
      <td>70.545283</td>
      <td>69.822807</td>
      <td>70.416623</td>
      <td>17382861.0</td>
      <td>-0.613609</td>
    </tr>
    <tr>
      <th>2017-07-11</th>
      <td>70.000</td>
      <td>70.6800</td>
      <td>69.7500</td>
      <td>69.990</td>
      <td>16880205.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>69.278476</td>
      <td>69.951467</td>
      <td>69.031053</td>
      <td>69.268579</td>
      <td>16880205.0</td>
      <td>-1.148043</td>
    </tr>
    <tr>
      <th>2017-07-10</th>
      <td>69.460</td>
      <td>70.2500</td>
      <td>69.2000</td>
      <td>69.980</td>
      <td>14903400.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>68.744042</td>
      <td>69.525899</td>
      <td>68.486722</td>
      <td>69.258682</td>
      <td>14903400.0</td>
      <td>-0.009897</td>
    </tr>
    <tr>
      <th>2017-07-07</th>
      <td>68.700</td>
      <td>69.8400</td>
      <td>68.7000</td>
      <td>69.460</td>
      <td>15897154.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.991876</td>
      <td>69.120125</td>
      <td>67.991876</td>
      <td>68.744042</td>
      <td>15897154.0</td>
      <td>-0.514640</td>
    </tr>
    <tr>
      <th>2017-07-06</th>
      <td>68.270</td>
      <td>68.7800</td>
      <td>68.1200</td>
      <td>68.570</td>
      <td>20776555.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.566308</td>
      <td>68.071051</td>
      <td>67.417854</td>
      <td>67.863216</td>
      <td>20776555.0</td>
      <td>-0.880826</td>
    </tr>
    <tr>
      <th>2017-07-05</th>
      <td>68.255</td>
      <td>69.4400</td>
      <td>68.2200</td>
      <td>69.080</td>
      <td>20174523.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.551463</td>
      <td>68.724248</td>
      <td>67.516824</td>
      <td>68.367959</td>
      <td>20174523.0</td>
      <td>0.504743</td>
    </tr>
    <tr>
      <th>2017-07-03</th>
      <td>69.330</td>
      <td>69.6000</td>
      <td>68.0200</td>
      <td>68.170</td>
      <td>16164331.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>68.615382</td>
      <td>68.882599</td>
      <td>67.318885</td>
      <td>67.467339</td>
      <td>16164331.0</td>
      <td>-0.900620</td>
    </tr>
    <tr>
      <th>2017-06-30</th>
      <td>68.780</td>
      <td>69.3800</td>
      <td>68.7400</td>
      <td>68.930</td>
      <td>23039328.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>68.071051</td>
      <td>68.664867</td>
      <td>68.031464</td>
      <td>68.219505</td>
      <td>23039328.0</td>
      <td>0.752166</td>
    </tr>
    <tr>
      <th>2017-06-29</th>
      <td>69.380</td>
      <td>69.4900</td>
      <td>68.0900</td>
      <td>68.490</td>
      <td>28231562.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>68.664867</td>
      <td>68.773733</td>
      <td>67.388163</td>
      <td>67.784040</td>
      <td>28231562.0</td>
      <td>-0.435465</td>
    </tr>
    <tr>
      <th>2017-06-28</th>
      <td>69.210</td>
      <td>69.8410</td>
      <td>68.7900</td>
      <td>69.800</td>
      <td>25226070.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>68.496619</td>
      <td>69.121115</td>
      <td>68.080948</td>
      <td>69.080538</td>
      <td>25226070.0</td>
      <td>1.296497</td>
    </tr>
    <tr>
      <th>2017-06-27</th>
      <td>70.110</td>
      <td>70.1800</td>
      <td>69.1800</td>
      <td>69.210</td>
      <td>24862560.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>69.387342</td>
      <td>69.456621</td>
      <td>68.466928</td>
      <td>68.496619</td>
      <td>24862560.0</td>
      <td>-0.583919</td>
    </tr>
    <tr>
      <th>2017-06-26</th>
      <td>71.400</td>
      <td>71.7100</td>
      <td>70.4450</td>
      <td>70.530</td>
      <td>19308122.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>70.664046</td>
      <td>70.970850</td>
      <td>69.718889</td>
      <td>69.803013</td>
      <td>19308122.0</td>
      <td>1.306394</td>
    </tr>
    <tr>
      <th>2017-06-23</th>
      <td>70.090</td>
      <td>71.2500</td>
      <td>69.9200</td>
      <td>71.210</td>
      <td>23176418.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>69.367549</td>
      <td>70.515592</td>
      <td>69.199301</td>
      <td>70.476004</td>
      <td>23176418.0</td>
      <td>0.672991</td>
    </tr>
    <tr>
      <th>2017-06-22</th>
      <td>70.540</td>
      <td>70.5900</td>
      <td>69.7100</td>
      <td>70.260</td>
      <td>22222851.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>69.812910</td>
      <td>69.862395</td>
      <td>68.991465</td>
      <td>69.535796</td>
      <td>22222851.0</td>
      <td>-0.940208</td>
    </tr>
    <tr>
      <th>2017-06-21</th>
      <td>70.210</td>
      <td>70.6200</td>
      <td>69.9400</td>
      <td>70.270</td>
      <td>19190623.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>69.486312</td>
      <td>69.892086</td>
      <td>69.219095</td>
      <td>69.545693</td>
      <td>19190623.0</td>
      <td>0.009897</td>
    </tr>
    <tr>
      <th>2017-06-20</th>
      <td>70.820</td>
      <td>70.8700</td>
      <td>69.8700</td>
      <td>69.910</td>
      <td>20775590.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>70.090024</td>
      <td>70.139509</td>
      <td>69.149816</td>
      <td>69.189404</td>
      <td>20775590.0</td>
      <td>-0.356289</td>
    </tr>
    <tr>
      <th>2017-06-19</th>
      <td>70.500</td>
      <td>70.9450</td>
      <td>70.3500</td>
      <td>70.870</td>
      <td>23146852.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>69.773322</td>
      <td>70.213736</td>
      <td>69.624869</td>
      <td>70.139509</td>
      <td>23146852.0</td>
      <td>0.950105</td>
    </tr>
    <tr>
      <th>2017-06-16</th>
      <td>69.730</td>
      <td>70.0252</td>
      <td>69.2200</td>
      <td>70.000</td>
      <td>46911637.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>69.011259</td>
      <td>69.303416</td>
      <td>68.506516</td>
      <td>69.278476</td>
      <td>46911637.0</td>
      <td>-0.861032</td>
    </tr>
    <tr>
      <th>2017-06-15</th>
      <td>69.270</td>
      <td>70.2100</td>
      <td>68.8000</td>
      <td>69.900</td>
      <td>25701569.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>68.556001</td>
      <td>69.486312</td>
      <td>68.090845</td>
      <td>69.179507</td>
      <td>25701569.0</td>
      <td>-0.098969</td>
    </tr>
    <tr>
      <th>2017-06-14</th>
      <td>70.910</td>
      <td>71.1000</td>
      <td>69.4300</td>
      <td>70.270</td>
      <td>25271276.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>70.179096</td>
      <td>70.367138</td>
      <td>68.714351</td>
      <td>69.545693</td>
      <td>25271276.0</td>
      <td>0.366186</td>
    </tr>
    <tr>
      <th>2017-06-13</th>
      <td>70.020</td>
      <td>70.8200</td>
      <td>69.9600</td>
      <td>70.650</td>
      <td>24815455.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>69.298270</td>
      <td>70.090024</td>
      <td>69.238888</td>
      <td>69.921776</td>
      <td>24815455.0</td>
      <td>0.376083</td>
    </tr>
    <tr>
      <th>2017-06-12</th>
      <td>69.250</td>
      <td>69.9400</td>
      <td>68.1300</td>
      <td>69.780</td>
      <td>47363986.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>68.536207</td>
      <td>69.219095</td>
      <td>67.427751</td>
      <td>69.060744</td>
      <td>47363986.0</td>
      <td>-0.861032</td>
    </tr>
    <tr>
      <th>2017-06-09</th>
      <td>72.035</td>
      <td>72.0800</td>
      <td>68.5900</td>
      <td>70.320</td>
      <td>48619420.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.292500</td>
      <td>71.337037</td>
      <td>67.883010</td>
      <td>69.595178</td>
      <td>48619420.0</td>
      <td>0.534434</td>
    </tr>
    <tr>
      <th>2017-06-08</th>
      <td>72.510</td>
      <td>72.5200</td>
      <td>71.5000</td>
      <td>71.945</td>
      <td>23982410.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.762604</td>
      <td>71.772501</td>
      <td>70.763015</td>
      <td>71.203428</td>
      <td>23982410.0</td>
      <td>1.608250</td>
    </tr>
    <tr>
      <th>2017-06-07</th>
      <td>72.635</td>
      <td>72.7700</td>
      <td>71.9500</td>
      <td>72.390</td>
      <td>21895156.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.886316</td>
      <td>72.019924</td>
      <td>71.208377</td>
      <td>71.643841</td>
      <td>21895156.0</td>
      <td>0.440413</td>
    </tr>
    <tr>
      <th>2017-06-06</th>
      <td>72.300</td>
      <td>72.6200</td>
      <td>72.2700</td>
      <td>72.520</td>
      <td>31220057.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.554769</td>
      <td>71.871471</td>
      <td>71.525078</td>
      <td>71.772501</td>
      <td>31220057.0</td>
      <td>0.128660</td>
    </tr>
    <tr>
      <th>2017-06-05</th>
      <td>71.970</td>
      <td>72.8900</td>
      <td>71.8100</td>
      <td>72.280</td>
      <td>29507429.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>71.228170</td>
      <td>72.138688</td>
      <td>71.069820</td>
      <td>71.534975</td>
      <td>29507429.0</td>
      <td>-0.237526</td>
    </tr>
    <tr>
      <th>2017-06-02</th>
      <td>70.440</td>
      <td>71.8600</td>
      <td>70.2400</td>
      <td>71.760</td>
      <td>34586054.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>69.713941</td>
      <td>71.119304</td>
      <td>69.516002</td>
      <td>71.020335</td>
      <td>34586054.0</td>
      <td>-0.514640</td>
    </tr>
    <tr>
      <th>2017-06-01</th>
      <td>70.240</td>
      <td>70.6100</td>
      <td>69.4510</td>
      <td>70.100</td>
      <td>21066468.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>69.516002</td>
      <td>69.882189</td>
      <td>68.735135</td>
      <td>69.377445</td>
      <td>21066468.0</td>
      <td>-1.642890</td>
    </tr>
    <tr>
      <th>2017-05-31</th>
      <td>70.530</td>
      <td>70.7400</td>
      <td>69.8100</td>
      <td>69.840</td>
      <td>29538356.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>69.803013</td>
      <td>70.010849</td>
      <td>69.090435</td>
      <td>69.120125</td>
      <td>29538356.0</td>
      <td>-0.257320</td>
    </tr>
    <tr>
      <th>2017-05-30</th>
      <td>69.790</td>
      <td>70.4100</td>
      <td>69.7700</td>
      <td>70.410</td>
      <td>16901792.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>69.070641</td>
      <td>69.684250</td>
      <td>69.050847</td>
      <td>69.684250</td>
      <td>16901792.0</td>
      <td>0.564125</td>
    </tr>
    <tr>
      <th>2017-05-26</th>
      <td>69.800</td>
      <td>70.2200</td>
      <td>69.5200</td>
      <td>69.970</td>
      <td>19644260.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>69.080538</td>
      <td>69.496209</td>
      <td>68.803424</td>
      <td>69.248785</td>
      <td>19644260.0</td>
      <td>-0.435465</td>
    </tr>
    <tr>
      <th>2017-05-25</th>
      <td>68.970</td>
      <td>69.8800</td>
      <td>68.9100</td>
      <td>69.620</td>
      <td>21702912.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>68.259093</td>
      <td>69.159713</td>
      <td>68.199711</td>
      <td>68.902393</td>
      <td>21702912.0</td>
      <td>-0.346392</td>
    </tr>
    <tr>
      <th>2017-05-24</th>
      <td>68.870</td>
      <td>68.8800</td>
      <td>68.4500</td>
      <td>68.770</td>
      <td>14422965.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>68.160124</td>
      <td>68.170021</td>
      <td>67.744453</td>
      <td>68.061154</td>
      <td>14422965.0</td>
      <td>-0.841239</td>
    </tr>
    <tr>
      <th>2017-05-23</th>
      <td>68.720</td>
      <td>68.7500</td>
      <td>68.3800</td>
      <td>68.680</td>
      <td>15347877.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>68.011670</td>
      <td>68.041361</td>
      <td>67.675174</td>
      <td>67.972082</td>
      <td>15347877.0</td>
      <td>-0.089072</td>
    </tr>
    <tr>
      <th>2017-05-22</th>
      <td>67.890</td>
      <td>68.5000</td>
      <td>67.5000</td>
      <td>68.450</td>
      <td>15484530.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.190225</td>
      <td>67.793937</td>
      <td>66.804245</td>
      <td>67.744453</td>
      <td>15484530.0</td>
      <td>-0.227629</td>
    </tr>
    <tr>
      <th>2017-05-19</th>
      <td>67.500</td>
      <td>68.0950</td>
      <td>67.4300</td>
      <td>67.690</td>
      <td>26496478.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>66.804245</td>
      <td>67.393112</td>
      <td>66.734966</td>
      <td>66.992286</td>
      <td>26496478.0</td>
      <td>-0.752166</td>
    </tr>
    <tr>
      <th>2017-05-18</th>
      <td>67.400</td>
      <td>68.1300</td>
      <td>67.1400</td>
      <td>67.710</td>
      <td>24789790.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>66.705276</td>
      <td>67.427751</td>
      <td>66.447956</td>
      <td>67.012080</td>
      <td>24789790.0</td>
      <td>0.019794</td>
    </tr>
    <tr>
      <th>2017-05-17</th>
      <td>68.890</td>
      <td>69.1000</td>
      <td>67.4300</td>
      <td>67.480</td>
      <td>29964198.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>68.179918</td>
      <td>68.387753</td>
      <td>66.734966</td>
      <td>66.784451</td>
      <td>29964198.0</td>
      <td>-0.227629</td>
    </tr>
    <tr>
      <th>2017-05-16</th>
      <td>68.230</td>
      <td>69.4400</td>
      <td>68.1600</td>
      <td>69.410</td>
      <td>33250702.0</td>
      <td>0.39</td>
      <td>1.0</td>
      <td>67.526720</td>
      <td>68.724248</td>
      <td>67.457442</td>
      <td>68.694558</td>
      <td>33250702.0</td>
      <td>1.910107</td>
    </tr>
    <tr>
      <th>2017-05-15</th>
      <td>68.140</td>
      <td>68.4800</td>
      <td>67.5700</td>
      <td>68.430</td>
      <td>30705323.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.060848</td>
      <td>67.395463</td>
      <td>66.499875</td>
      <td>67.346255</td>
      <td>30705323.0</td>
      <td>-1.348303</td>
    </tr>
    <tr>
      <th>2017-05-12</th>
      <td>68.610</td>
      <td>68.6100</td>
      <td>68.0400</td>
      <td>68.380</td>
      <td>17073013.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.523404</td>
      <td>67.523404</td>
      <td>66.962431</td>
      <td>67.297047</td>
      <td>17073013.0</td>
      <td>-0.049208</td>
    </tr>
    <tr>
      <th>2017-05-11</th>
      <td>68.360</td>
      <td>68.7300</td>
      <td>68.1200</td>
      <td>68.460</td>
      <td>27985424.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.277363</td>
      <td>67.641504</td>
      <td>67.041164</td>
      <td>67.375780</td>
      <td>27985424.0</td>
      <td>0.078733</td>
    </tr>
    <tr>
      <th>2017-05-10</th>
      <td>68.990</td>
      <td>69.5600</td>
      <td>68.9200</td>
      <td>69.310</td>
      <td>17842038.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.897386</td>
      <td>68.458359</td>
      <td>67.828494</td>
      <td>68.212318</td>
      <td>17842038.0</td>
      <td>0.836538</td>
    </tr>
    <tr>
      <th>2017-05-09</th>
      <td>68.860</td>
      <td>69.2800</td>
      <td>68.6800</td>
      <td>69.040</td>
      <td>22318181.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.769445</td>
      <td>68.182793</td>
      <td>67.592295</td>
      <td>67.946594</td>
      <td>22318181.0</td>
      <td>-0.265724</td>
    </tr>
    <tr>
      <th>2017-05-08</th>
      <td>68.970</td>
      <td>69.0500</td>
      <td>68.4200</td>
      <td>68.940</td>
      <td>18446053.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.877703</td>
      <td>67.956436</td>
      <td>67.336413</td>
      <td>67.848178</td>
      <td>18446053.0</td>
      <td>-0.098416</td>
    </tr>
    <tr>
      <th>2017-05-05</th>
      <td>68.900</td>
      <td>69.0300</td>
      <td>68.4850</td>
      <td>69.000</td>
      <td>18882845.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.808811</td>
      <td>67.936752</td>
      <td>67.400384</td>
      <td>67.907227</td>
      <td>18882845.0</td>
      <td>0.059050</td>
    </tr>
    <tr>
      <th>2017-05-04</th>
      <td>69.030</td>
      <td>69.0800</td>
      <td>68.6400</td>
      <td>68.810</td>
      <td>21421413.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.936752</td>
      <td>67.985960</td>
      <td>67.552929</td>
      <td>67.720237</td>
      <td>21421413.0</td>
      <td>-0.186991</td>
    </tr>
    <tr>
      <th>2017-05-03</th>
      <td>69.380</td>
      <td>69.3800</td>
      <td>68.7100</td>
      <td>69.080</td>
      <td>28725646.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>68.281209</td>
      <td>68.281209</td>
      <td>67.621820</td>
      <td>67.985960</td>
      <td>28725646.0</td>
      <td>0.265724</td>
    </tr>
    <tr>
      <th>2017-05-02</th>
      <td>69.710</td>
      <td>69.7100</td>
      <td>69.1300</td>
      <td>69.300</td>
      <td>23000828.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>68.605983</td>
      <td>68.605983</td>
      <td>68.035169</td>
      <td>68.202476</td>
      <td>23000828.0</td>
      <td>0.216516</td>
    </tr>
    <tr>
      <th>2017-05-01</th>
      <td>68.680</td>
      <td>69.5500</td>
      <td>68.5000</td>
      <td>69.410</td>
      <td>31304672.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.592295</td>
      <td>68.448517</td>
      <td>67.415146</td>
      <td>68.310734</td>
      <td>31304672.0</td>
      <td>0.108258</td>
    </tr>
    <tr>
      <th>2017-04-28</th>
      <td>68.910</td>
      <td>69.1400</td>
      <td>67.6900</td>
      <td>68.460</td>
      <td>38940853.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.818653</td>
      <td>68.045010</td>
      <td>66.617974</td>
      <td>67.375780</td>
      <td>38940853.0</td>
      <td>-0.934955</td>
    </tr>
    <tr>
      <th>2017-04-27</th>
      <td>68.150</td>
      <td>68.3800</td>
      <td>67.5800</td>
      <td>68.270</td>
      <td>32219234.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.070689</td>
      <td>67.297047</td>
      <td>66.509716</td>
      <td>67.188789</td>
      <td>32219234.0</td>
      <td>-0.186991</td>
    </tr>
    <tr>
      <th>2017-04-26</th>
      <td>68.080</td>
      <td>68.3100</td>
      <td>67.6200</td>
      <td>67.830</td>
      <td>25544417.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>67.001798</td>
      <td>67.228155</td>
      <td>66.549083</td>
      <td>66.755757</td>
      <td>25544417.0</td>
      <td>-0.433032</td>
    </tr>
    <tr>
      <th>2017-04-25</th>
      <td>67.900</td>
      <td>68.0400</td>
      <td>67.6000</td>
      <td>67.920</td>
      <td>29983174.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>66.824648</td>
      <td>66.962431</td>
      <td>66.529400</td>
      <td>66.844332</td>
      <td>29983174.0</td>
      <td>0.088575</td>
    </tr>
    <tr>
      <th>2017-04-24</th>
      <td>67.480</td>
      <td>67.6600</td>
      <td>67.1000</td>
      <td>67.530</td>
      <td>29721254.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>66.411300</td>
      <td>66.588449</td>
      <td>66.037318</td>
      <td>66.460508</td>
      <td>29721254.0</td>
      <td>-0.383823</td>
    </tr>
    <tr>
      <th>2017-04-21</th>
      <td>65.670</td>
      <td>66.7000</td>
      <td>65.4500</td>
      <td>66.400</td>
      <td>32522645.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.629966</td>
      <td>65.643653</td>
      <td>64.413450</td>
      <td>65.348404</td>
      <td>32522645.0</td>
      <td>-1.112104</td>
    </tr>
    <tr>
      <th>2017-04-20</th>
      <td>65.460</td>
      <td>65.7500</td>
      <td>65.1400</td>
      <td>65.500</td>
      <td>22299477.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.423291</td>
      <td>64.708699</td>
      <td>64.108359</td>
      <td>64.462658</td>
      <td>22299477.0</td>
      <td>-0.885746</td>
    </tr>
    <tr>
      <th>2017-04-19</th>
      <td>65.650</td>
      <td>65.7500</td>
      <td>64.8900</td>
      <td>65.040</td>
      <td>26992771.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.610282</td>
      <td>64.708699</td>
      <td>63.862319</td>
      <td>64.009943</td>
      <td>26992771.0</td>
      <td>-0.452715</td>
    </tr>
    <tr>
      <th>2017-04-18</th>
      <td>65.330</td>
      <td>65.7100</td>
      <td>65.1600</td>
      <td>65.390</td>
      <td>15155611.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.295350</td>
      <td>64.669332</td>
      <td>64.128043</td>
      <td>64.354400</td>
      <td>15155611.0</td>
      <td>0.344457</td>
    </tr>
    <tr>
      <th>2017-04-17</th>
      <td>65.040</td>
      <td>65.4900</td>
      <td>65.0100</td>
      <td>65.480</td>
      <td>16689265.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.009943</td>
      <td>64.452816</td>
      <td>63.980418</td>
      <td>64.442975</td>
      <td>16689265.0</td>
      <td>0.088575</td>
    </tr>
    <tr>
      <th>2017-04-13</th>
      <td>65.290</td>
      <td>65.8600</td>
      <td>64.9500</td>
      <td>64.950</td>
      <td>17896483.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.255984</td>
      <td>64.816957</td>
      <td>63.921368</td>
      <td>63.921368</td>
      <td>17896483.0</td>
      <td>-0.521606</td>
    </tr>
    <tr>
      <th>2017-04-12</th>
      <td>65.420</td>
      <td>65.5100</td>
      <td>65.1100</td>
      <td>65.230</td>
      <td>17108513.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.383925</td>
      <td>64.472500</td>
      <td>64.078834</td>
      <td>64.196934</td>
      <td>17108513.0</td>
      <td>0.275566</td>
    </tr>
    <tr>
      <th>2017-04-11</th>
      <td>65.600</td>
      <td>65.6100</td>
      <td>64.8500</td>
      <td>65.480</td>
      <td>18791533.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.561074</td>
      <td>64.570916</td>
      <td>63.822952</td>
      <td>64.442975</td>
      <td>18791533.0</td>
      <td>0.246041</td>
    </tr>
    <tr>
      <th>2017-04-10</th>
      <td>65.610</td>
      <td>65.8200</td>
      <td>65.3600</td>
      <td>65.530</td>
      <td>17952742.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.570916</td>
      <td>64.777590</td>
      <td>64.324875</td>
      <td>64.492183</td>
      <td>17952742.0</td>
      <td>0.049208</td>
    </tr>
    <tr>
      <th>2017-04-07</th>
      <td>65.850</td>
      <td>65.9600</td>
      <td>65.4400</td>
      <td>65.680</td>
      <td>14089274.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.807115</td>
      <td>64.915373</td>
      <td>64.403608</td>
      <td>64.639807</td>
      <td>14089274.0</td>
      <td>0.147624</td>
    </tr>
    <tr>
      <th>2017-04-06</th>
      <td>65.600</td>
      <td>66.0550</td>
      <td>65.4800</td>
      <td>65.730</td>
      <td>18103453.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.561074</td>
      <td>65.008868</td>
      <td>64.442975</td>
      <td>64.689015</td>
      <td>18103453.0</td>
      <td>0.049208</td>
    </tr>
    <tr>
      <th>2017-04-05</th>
      <td>66.300</td>
      <td>66.3500</td>
      <td>65.4443</td>
      <td>65.560</td>
      <td>21448594.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>65.249988</td>
      <td>65.299196</td>
      <td>64.407840</td>
      <td>64.521708</td>
      <td>21448594.0</td>
      <td>-0.167308</td>
    </tr>
    <tr>
      <th>2017-04-04</th>
      <td>65.390</td>
      <td>65.8100</td>
      <td>65.2800</td>
      <td>65.730</td>
      <td>12997449.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.354400</td>
      <td>64.767748</td>
      <td>64.246142</td>
      <td>64.689015</td>
      <td>12997449.0</td>
      <td>0.167308</td>
    </tr>
    <tr>
      <th>2017-04-03</th>
      <td>65.810</td>
      <td>65.9400</td>
      <td>65.1900</td>
      <td>65.550</td>
      <td>20400871.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.767748</td>
      <td>64.895690</td>
      <td>64.157567</td>
      <td>64.511866</td>
      <td>20400871.0</td>
      <td>-0.177149</td>
    </tr>
    <tr>
      <th>2017-03-31</th>
      <td>65.650</td>
      <td>66.1900</td>
      <td>65.4500</td>
      <td>65.860</td>
      <td>21040331.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.610282</td>
      <td>65.141730</td>
      <td>64.413450</td>
      <td>64.816957</td>
      <td>21040331.0</td>
      <td>0.305090</td>
    </tr>
    <tr>
      <th>2017-03-30</th>
      <td>65.420</td>
      <td>65.9800</td>
      <td>65.3600</td>
      <td>65.710</td>
      <td>15122823.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.383925</td>
      <td>64.935056</td>
      <td>64.324875</td>
      <td>64.669332</td>
      <td>15122823.0</td>
      <td>-0.147624</td>
    </tr>
    <tr>
      <th>2017-03-29</th>
      <td>65.120</td>
      <td>65.5000</td>
      <td>64.9475</td>
      <td>65.470</td>
      <td>13618424.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.088676</td>
      <td>64.462658</td>
      <td>63.918908</td>
      <td>64.433133</td>
      <td>13618424.0</td>
      <td>-0.236199</td>
    </tr>
    <tr>
      <th>2017-03-28</th>
      <td>64.960</td>
      <td>65.4700</td>
      <td>64.6500</td>
      <td>65.290</td>
      <td>20080358.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.931210</td>
      <td>64.433133</td>
      <td>63.626120</td>
      <td>64.255984</td>
      <td>20080358.0</td>
      <td>-0.177149</td>
    </tr>
    <tr>
      <th>2017-03-27</th>
      <td>64.630</td>
      <td>65.2200</td>
      <td>64.3500</td>
      <td>65.100</td>
      <td>18614662.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.606436</td>
      <td>64.187092</td>
      <td>63.330871</td>
      <td>64.068993</td>
      <td>18614662.0</td>
      <td>-0.186991</td>
    </tr>
    <tr>
      <th>2017-03-24</th>
      <td>65.360</td>
      <td>65.4500</td>
      <td>64.7600</td>
      <td>64.980</td>
      <td>22617105.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.324875</td>
      <td>64.413450</td>
      <td>63.734378</td>
      <td>63.950893</td>
      <td>22617105.0</td>
      <td>-0.118100</td>
    </tr>
    <tr>
      <th>2017-03-23</th>
      <td>64.940</td>
      <td>65.2350</td>
      <td>64.7650</td>
      <td>64.870</td>
      <td>19269203.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.911527</td>
      <td>64.201855</td>
      <td>63.739298</td>
      <td>63.842635</td>
      <td>19269203.0</td>
      <td>-0.108258</td>
    </tr>
    <tr>
      <th>2017-03-22</th>
      <td>64.120</td>
      <td>65.1400</td>
      <td>64.1200</td>
      <td>65.030</td>
      <td>20680015.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.104513</td>
      <td>64.108359</td>
      <td>63.104513</td>
      <td>64.000101</td>
      <td>20680015.0</td>
      <td>0.157466</td>
    </tr>
    <tr>
      <th>2017-03-21</th>
      <td>65.190</td>
      <td>65.5000</td>
      <td>64.1300</td>
      <td>64.210</td>
      <td>26640480.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.157567</td>
      <td>64.462658</td>
      <td>63.114355</td>
      <td>63.193088</td>
      <td>26640480.0</td>
      <td>-0.807013</td>
    </tr>
    <tr>
      <th>2017-03-20</th>
      <td>64.910</td>
      <td>65.1750</td>
      <td>64.7200</td>
      <td>64.930</td>
      <td>14598083.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.882002</td>
      <td>64.142805</td>
      <td>63.695011</td>
      <td>63.901685</td>
      <td>14598083.0</td>
      <td>0.708597</td>
    </tr>
    <tr>
      <th>2017-03-17</th>
      <td>64.910</td>
      <td>65.2400</td>
      <td>64.6800</td>
      <td>64.870</td>
      <td>49219686.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.882002</td>
      <td>64.206776</td>
      <td>63.655645</td>
      <td>63.842635</td>
      <td>49219686.0</td>
      <td>-0.059050</td>
    </tr>
    <tr>
      <th>2017-03-16</th>
      <td>64.750</td>
      <td>64.7600</td>
      <td>64.3000</td>
      <td>64.640</td>
      <td>20674296.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.724536</td>
      <td>63.734378</td>
      <td>63.281663</td>
      <td>63.616278</td>
      <td>20674296.0</td>
      <td>-0.226357</td>
    </tr>
    <tr>
      <th>2017-03-15</th>
      <td>64.550</td>
      <td>64.9200</td>
      <td>64.2500</td>
      <td>64.750</td>
      <td>24833810.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.527703</td>
      <td>63.891844</td>
      <td>63.232455</td>
      <td>63.724536</td>
      <td>24833810.0</td>
      <td>0.108258</td>
    </tr>
    <tr>
      <th>2017-03-14</th>
      <td>64.530</td>
      <td>64.5500</td>
      <td>64.1500</td>
      <td>64.410</td>
      <td>14280202.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.508020</td>
      <td>63.527703</td>
      <td>63.134038</td>
      <td>63.389921</td>
      <td>14280202.0</td>
      <td>-0.334615</td>
    </tr>
    <tr>
      <th>2017-03-13</th>
      <td>65.010</td>
      <td>65.1950</td>
      <td>64.5700</td>
      <td>64.710</td>
      <td>20100035.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.980418</td>
      <td>64.162488</td>
      <td>63.547387</td>
      <td>63.685169</td>
      <td>20100035.0</td>
      <td>0.295249</td>
    </tr>
    <tr>
      <th>2017-03-10</th>
      <td>65.110</td>
      <td>65.2600</td>
      <td>64.7500</td>
      <td>64.930</td>
      <td>19538245.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.078834</td>
      <td>64.226459</td>
      <td>63.724536</td>
      <td>63.901685</td>
      <td>19538245.0</td>
      <td>0.216516</td>
    </tr>
    <tr>
      <th>2017-03-09</th>
      <td>65.190</td>
      <td>65.2000</td>
      <td>64.4800</td>
      <td>64.730</td>
      <td>19846832.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.157567</td>
      <td>64.167409</td>
      <td>63.458812</td>
      <td>63.704853</td>
      <td>19846832.0</td>
      <td>-0.196833</td>
    </tr>
    <tr>
      <th>2017-03-08</th>
      <td>64.260</td>
      <td>65.0850</td>
      <td>64.2500</td>
      <td>64.990</td>
      <td>21510907.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.242296</td>
      <td>64.054230</td>
      <td>63.232455</td>
      <td>63.960735</td>
      <td>21510907.0</td>
      <td>0.255882</td>
    </tr>
    <tr>
      <th>2017-03-07</th>
      <td>64.190</td>
      <td>64.7750</td>
      <td>64.1900</td>
      <td>64.400</td>
      <td>18520987.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.173405</td>
      <td>63.749140</td>
      <td>63.173405</td>
      <td>63.380079</td>
      <td>18520987.0</td>
      <td>-0.580656</td>
    </tr>
    <tr>
      <th>2017-03-06</th>
      <td>63.970</td>
      <td>64.5600</td>
      <td>63.8100</td>
      <td>64.270</td>
      <td>18750255.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>62.956889</td>
      <td>63.537545</td>
      <td>62.799423</td>
      <td>63.252138</td>
      <td>18750255.0</td>
      <td>-0.127941</td>
    </tr>
    <tr>
      <th>2017-03-03</th>
      <td>63.990</td>
      <td>64.2800</td>
      <td>63.6200</td>
      <td>64.250</td>
      <td>18139405.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>62.976572</td>
      <td>63.261979</td>
      <td>62.612432</td>
      <td>63.232455</td>
      <td>18139405.0</td>
      <td>-0.019683</td>
    </tr>
    <tr>
      <th>2017-03-02</th>
      <td>64.690</td>
      <td>64.7500</td>
      <td>63.8800</td>
      <td>64.010</td>
      <td>24539597.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.665486</td>
      <td>63.724536</td>
      <td>62.868314</td>
      <td>62.996255</td>
      <td>24539597.0</td>
      <td>-0.236199</td>
    </tr>
    <tr>
      <th>2017-03-01</th>
      <td>64.130</td>
      <td>64.9900</td>
      <td>64.0218</td>
      <td>64.940</td>
      <td>26937459.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.114355</td>
      <td>63.960735</td>
      <td>63.007869</td>
      <td>63.911527</td>
      <td>26937459.0</td>
      <td>0.915271</td>
    </tr>
    <tr>
      <th>2017-02-28</th>
      <td>64.080</td>
      <td>64.2000</td>
      <td>63.7600</td>
      <td>63.980</td>
      <td>23239825.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.065147</td>
      <td>63.183246</td>
      <td>62.750215</td>
      <td>62.966731</td>
      <td>23239825.0</td>
      <td>-0.944796</td>
    </tr>
    <tr>
      <th>2017-02-27</th>
      <td>64.540</td>
      <td>64.5400</td>
      <td>64.0450</td>
      <td>64.230</td>
      <td>15871507.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.517862</td>
      <td>63.517862</td>
      <td>63.030701</td>
      <td>63.212771</td>
      <td>15871507.0</td>
      <td>0.246041</td>
    </tr>
    <tr>
      <th>2017-02-24</th>
      <td>64.530</td>
      <td>64.8000</td>
      <td>64.1350</td>
      <td>64.620</td>
      <td>21796800.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.508020</td>
      <td>63.773744</td>
      <td>63.119276</td>
      <td>63.596595</td>
      <td>21796800.0</td>
      <td>0.383823</td>
    </tr>
    <tr>
      <th>2017-02-23</th>
      <td>64.420</td>
      <td>64.7285</td>
      <td>64.1950</td>
      <td>64.620</td>
      <td>20273128.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.399762</td>
      <td>63.703376</td>
      <td>63.178326</td>
      <td>63.596595</td>
      <td>20273128.0</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2017-02-22</th>
      <td>64.330</td>
      <td>64.3900</td>
      <td>64.0500</td>
      <td>64.360</td>
      <td>19292651.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.311188</td>
      <td>63.370237</td>
      <td>63.035622</td>
      <td>63.340712</td>
      <td>19292651.0</td>
      <td>-0.255882</td>
    </tr>
    <tr>
      <th>2017-02-21</th>
      <td>64.610</td>
      <td>64.9500</td>
      <td>64.4500</td>
      <td>64.490</td>
      <td>20655869.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.586753</td>
      <td>63.921368</td>
      <td>63.429287</td>
      <td>63.468654</td>
      <td>20655869.0</td>
      <td>0.127941</td>
    </tr>
    <tr>
      <th>2017-02-17</th>
      <td>64.470</td>
      <td>64.6900</td>
      <td>64.3000</td>
      <td>64.620</td>
      <td>21248818.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.448970</td>
      <td>63.665486</td>
      <td>63.281663</td>
      <td>63.596595</td>
      <td>21248818.0</td>
      <td>0.127941</td>
    </tr>
    <tr>
      <th>2017-02-16</th>
      <td>64.740</td>
      <td>65.2400</td>
      <td>64.4400</td>
      <td>64.520</td>
      <td>20546345.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.714694</td>
      <td>64.206776</td>
      <td>63.419445</td>
      <td>63.498178</td>
      <td>20546345.0</td>
      <td>-0.098416</td>
    </tr>
    <tr>
      <th>2017-02-15</th>
      <td>64.500</td>
      <td>64.5700</td>
      <td>64.1550</td>
      <td>64.530</td>
      <td>17005157.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.478495</td>
      <td>63.547387</td>
      <td>63.138959</td>
      <td>63.508020</td>
      <td>17005157.0</td>
      <td>0.009842</td>
    </tr>
    <tr>
      <th>2017-02-14</th>
      <td>64.410</td>
      <td>64.7200</td>
      <td>64.0200</td>
      <td>64.570</td>
      <td>23108426.0</td>
      <td>0.39</td>
      <td>1.0</td>
      <td>63.389921</td>
      <td>63.695011</td>
      <td>63.006097</td>
      <td>63.547387</td>
      <td>23108426.0</td>
      <td>0.039367</td>
    </tr>
    <tr>
      <th>2017-02-13</th>
      <td>64.240</td>
      <td>64.8600</td>
      <td>64.1300</td>
      <td>64.720</td>
      <td>22920101.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>62.843044</td>
      <td>63.449561</td>
      <td>62.735436</td>
      <td>63.312606</td>
      <td>22920101.0</td>
      <td>-0.234781</td>
    </tr>
    <tr>
      <th>2017-02-10</th>
      <td>64.250</td>
      <td>64.3000</td>
      <td>63.9750</td>
      <td>64.000</td>
      <td>18170729.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>62.852826</td>
      <td>62.901739</td>
      <td>62.583806</td>
      <td>62.608263</td>
      <td>18170729.0</td>
      <td>-0.704343</td>
    </tr>
    <tr>
      <th>2017-02-09</th>
      <td>63.520</td>
      <td>64.4350</td>
      <td>63.3200</td>
      <td>64.060</td>
      <td>22644443.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>62.138701</td>
      <td>63.033803</td>
      <td>61.943050</td>
      <td>62.666958</td>
      <td>22644443.0</td>
      <td>0.058695</td>
    </tr>
    <tr>
      <th>2017-02-08</th>
      <td>63.570</td>
      <td>63.8100</td>
      <td>63.2200</td>
      <td>63.340</td>
      <td>18096358.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>62.187613</td>
      <td>62.422394</td>
      <td>61.845224</td>
      <td>61.962615</td>
      <td>18096358.0</td>
      <td>-0.704343</td>
    </tr>
    <tr>
      <th>2017-02-07</th>
      <td>63.740</td>
      <td>63.7800</td>
      <td>63.2300</td>
      <td>63.430</td>
      <td>20277226.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>62.353917</td>
      <td>62.393047</td>
      <td>61.855007</td>
      <td>62.050658</td>
      <td>20277226.0</td>
      <td>0.088043</td>
    </tr>
    <tr>
      <th>2017-02-06</th>
      <td>63.500</td>
      <td>63.6500</td>
      <td>63.1400</td>
      <td>63.640</td>
      <td>19796360.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>62.119136</td>
      <td>62.265874</td>
      <td>61.766964</td>
      <td>62.256091</td>
      <td>19796360.0</td>
      <td>0.205433</td>
    </tr>
    <tr>
      <th>2017-02-03</th>
      <td>63.500</td>
      <td>63.7000</td>
      <td>63.0700</td>
      <td>63.680</td>
      <td>30301759.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>62.119136</td>
      <td>62.314786</td>
      <td>61.698486</td>
      <td>62.295221</td>
      <td>30301759.0</td>
      <td>0.039130</td>
    </tr>
    <tr>
      <th>2017-02-02</th>
      <td>63.250</td>
      <td>63.4100</td>
      <td>62.7500</td>
      <td>63.170</td>
      <td>45827013.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>61.874572</td>
      <td>62.031093</td>
      <td>61.385445</td>
      <td>61.796312</td>
      <td>45827013.0</td>
      <td>-0.498910</td>
    </tr>
    <tr>
      <th>2017-02-01</th>
      <td>64.355</td>
      <td>64.6200</td>
      <td>63.4700</td>
      <td>63.580</td>
      <td>39671528.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>62.955543</td>
      <td>63.214780</td>
      <td>62.089788</td>
      <td>62.197396</td>
      <td>39671528.0</td>
      <td>0.401084</td>
    </tr>
    <tr>
      <th>2017-01-31</th>
      <td>64.860</td>
      <td>65.1500</td>
      <td>64.2600</td>
      <td>64.650</td>
      <td>25270549.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.449561</td>
      <td>63.733255</td>
      <td>62.862609</td>
      <td>63.244128</td>
      <td>25270549.0</td>
      <td>1.046732</td>
    </tr>
    <tr>
      <th>2017-01-30</th>
      <td>65.690</td>
      <td>65.7900</td>
      <td>64.8000</td>
      <td>65.130</td>
      <td>31651445.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>64.261512</td>
      <td>64.359338</td>
      <td>63.390866</td>
      <td>63.713690</td>
      <td>31651445.0</td>
      <td>0.469562</td>
    </tr>
    <tr>
      <th>2017-01-27</th>
      <td>65.390</td>
      <td>65.9100</td>
      <td>64.8900</td>
      <td>65.780</td>
      <td>44817972.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>63.968036</td>
      <td>64.476728</td>
      <td>63.478909</td>
      <td>64.349555</td>
      <td>44817972.0</td>
      <td>0.635865</td>
    </tr>
    <tr>
      <th>2017-01-26</th>
      <td>64.120</td>
      <td>64.5350</td>
      <td>63.5500</td>
      <td>64.270</td>
      <td>43554645.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>62.725653</td>
      <td>63.131629</td>
      <td>62.168048</td>
      <td>62.872391</td>
      <td>43554645.0</td>
      <td>-1.477164</td>
    </tr>
    <tr>
      <th>2017-01-25</th>
      <td>63.950</td>
      <td>64.1000</td>
      <td>63.4500</td>
      <td>63.680</td>
      <td>24654933.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>62.559350</td>
      <td>62.706088</td>
      <td>62.070223</td>
      <td>62.295221</td>
      <td>24654933.0</td>
      <td>-0.577170</td>
    </tr>
    <tr>
      <th>2017-01-24</th>
      <td>63.200</td>
      <td>63.7350</td>
      <td>62.9400</td>
      <td>63.520</td>
      <td>24672940.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>61.825659</td>
      <td>62.349025</td>
      <td>61.571313</td>
      <td>62.138701</td>
      <td>24672940.0</td>
      <td>-0.156521</td>
    </tr>
    <tr>
      <th>2017-01-23</th>
      <td>62.700</td>
      <td>63.1159</td>
      <td>62.5700</td>
      <td>62.960</td>
      <td>23097581.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>61.336532</td>
      <td>61.743388</td>
      <td>61.209359</td>
      <td>61.590878</td>
      <td>23097581.0</td>
      <td>-0.547822</td>
    </tr>
    <tr>
      <th>2017-01-20</th>
      <td>62.670</td>
      <td>62.8200</td>
      <td>62.3700</td>
      <td>62.740</td>
      <td>30213462.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>61.307185</td>
      <td>61.453923</td>
      <td>61.013708</td>
      <td>61.375662</td>
      <td>30213462.0</td>
      <td>-0.215216</td>
    </tr>
    <tr>
      <th>2017-01-19</th>
      <td>62.240</td>
      <td>62.9800</td>
      <td>62.1950</td>
      <td>62.300</td>
      <td>18451655.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>60.886535</td>
      <td>61.610443</td>
      <td>60.842514</td>
      <td>60.945231</td>
      <td>18451655.0</td>
      <td>-0.430432</td>
    </tr>
    <tr>
      <th>2017-01-18</th>
      <td>62.670</td>
      <td>62.7000</td>
      <td>62.1200</td>
      <td>62.500</td>
      <td>19670102.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>61.307185</td>
      <td>61.336532</td>
      <td>60.769145</td>
      <td>61.140882</td>
      <td>19670102.0</td>
      <td>0.195651</td>
    </tr>
    <tr>
      <th>2017-01-17</th>
      <td>62.680</td>
      <td>62.7000</td>
      <td>62.0300</td>
      <td>62.530</td>
      <td>20663983.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>61.316967</td>
      <td>61.336532</td>
      <td>60.681102</td>
      <td>61.170229</td>
      <td>20663983.0</td>
      <td>0.029348</td>
    </tr>
    <tr>
      <th>2017-01-13</th>
      <td>62.620</td>
      <td>62.8650</td>
      <td>62.3500</td>
      <td>62.700</td>
      <td>19422310.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>61.258272</td>
      <td>61.497944</td>
      <td>60.994143</td>
      <td>61.336532</td>
      <td>19422310.0</td>
      <td>0.166303</td>
    </tr>
    <tr>
      <th>2017-01-12</th>
      <td>63.060</td>
      <td>63.4000</td>
      <td>61.9500</td>
      <td>62.610</td>
      <td>20968223.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>61.688704</td>
      <td>62.021310</td>
      <td>60.602842</td>
      <td>61.248489</td>
      <td>20968223.0</td>
      <td>-0.088043</td>
    </tr>
    <tr>
      <th>2017-01-11</th>
      <td>62.610</td>
      <td>63.2300</td>
      <td>62.4300</td>
      <td>63.190</td>
      <td>21517335.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>61.248489</td>
      <td>61.855007</td>
      <td>61.072404</td>
      <td>61.815877</td>
      <td>21517335.0</td>
      <td>0.567387</td>
    </tr>
    <tr>
      <th>2017-01-10</th>
      <td>62.730</td>
      <td>63.0700</td>
      <td>62.2800</td>
      <td>62.620</td>
      <td>18593004.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>61.365880</td>
      <td>61.698486</td>
      <td>60.925666</td>
      <td>61.258272</td>
      <td>18593004.0</td>
      <td>-0.557605</td>
    </tr>
    <tr>
      <th>2017-01-09</th>
      <td>62.760</td>
      <td>63.0800</td>
      <td>62.5400</td>
      <td>62.640</td>
      <td>20382730.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>61.395228</td>
      <td>61.708269</td>
      <td>61.180012</td>
      <td>61.277837</td>
      <td>20382730.0</td>
      <td>0.019565</td>
    </tr>
    <tr>
      <th>2017-01-06</th>
      <td>62.300</td>
      <td>63.1500</td>
      <td>62.0400</td>
      <td>62.840</td>
      <td>19922919.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>60.945231</td>
      <td>61.776747</td>
      <td>60.690885</td>
      <td>61.473488</td>
      <td>19922919.0</td>
      <td>0.195651</td>
    </tr>
    <tr>
      <th>2017-01-05</th>
      <td>62.190</td>
      <td>62.6600</td>
      <td>62.0300</td>
      <td>62.300</td>
      <td>24875968.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>60.837623</td>
      <td>61.297402</td>
      <td>60.681102</td>
      <td>60.945231</td>
      <td>24875968.0</td>
      <td>-0.528257</td>
    </tr>
    <tr>
      <th>2017-01-04</th>
      <td>62.480</td>
      <td>62.7500</td>
      <td>62.1200</td>
      <td>62.300</td>
      <td>21339969.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>61.121316</td>
      <td>61.385445</td>
      <td>60.769145</td>
      <td>60.945231</td>
      <td>21339969.0</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2017-01-03</th>
      <td>62.790</td>
      <td>62.8400</td>
      <td>62.1250</td>
      <td>62.580</td>
      <td>20694101.0</td>
      <td>0.00</td>
      <td>1.0</td>
      <td>61.424575</td>
      <td>61.473488</td>
      <td>60.774036</td>
      <td>61.219142</td>
      <td>20694101.0</td>
      <td>0.273911</td>
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





    [<matplotlib.lines.Line2D at 0x1a100e5cf8>]




![png](output_85_2.png)



```python
a_7_m = df_MSFT_07['Diff'].max()
a_7_i = df_MSFT_07['Diff'].idxmax()
a_8_m = df_MSFT_08['Diff'].max()
a_8_i = df_MSFT_08['Diff'].idxmax()
a_9_m = df_MSFT_09['Diff'].max()
a_9_i = df_MSFT_09['Diff'].idxmax()
a_10_m = df_MSFT_10['Diff'].max()
a_10_i = df_MSFT_10['Diff'].idxmax()
a_11_m = df_MSFT_11['Diff'].max()
a_11_i = df_MSFT_11['Diff'].idxmax()
a_12_m = df_MSFT_12['Diff'].max()
a_12_i = df_MSFT_12['Diff'].idxmax()
a_13_m = df_MSFT_13['Diff'].max()
a_13_i = df_MSFT_13['Diff'].idxmax()
a_14_m = df_MSFT_14['Diff'].max()
a_14_i = df_MSFT_14['Diff'].idxmax()
a_15_m = df_MSFT_15['Diff'].max()
a_15_i = df_MSFT_15['Diff'].idxmax()
a_16_m = df_MSFT_16['Diff'].max()
a_16_i = df_MSFT_16['Diff'].idxmax()
a_17_m = df_MSFT_17['Diff'].max()
a_17_i = df_MSFT_17['Diff'].idxmax()
MSFT_max_index_data = {a_7_m:a_7_i, a_8_m:a_8_i, a_9_m:a_9_i, a_10_m:a_10_i, a_11_m:a_11_i, a_12_m:a_12_i, a_13_m:a_13_i, a_14_m:a_14_i, a_15_m:a_15_i, a_16_m:a_16_i, a_17_m:a_17_i}
for i in MSFT_max_index_data:
    print (i,MSFT_max_index_data[i])
y = MSFT_max_index_data.keys()
x = MSFT_max_index_data.values()
plt.plot(x,y)
```

    0.926284269252001 2007-02-26 00:00:00
    1.8850404939919976 2008-09-26 00:00:00
    1.802257067267 2009-01-21 00:00:00
    0.9267709536399984 2010-05-19 00:00:00
    1.1591251656560004 2011-08-09 00:00:00
    0.7821760980000008 2012-11-12 00:00:00
    3.592443939916997 2013-07-18 00:00:00
    1.6763917514790023 2014-10-09 00:00:00
    4.0322446197329995 2015-01-26 00:00:00
    3.835714570905999 2016-04-21 00:00:00
    3.180000000000007 2017-12-01 00:00:00





    [<matplotlib.lines.Line2D at 0x1a17c0def0>]




![png](output_86_2.png)



```python
df_CY_07.corrwith(df_MSFT_07['AdjClose'])
```




    Open          0.766066
    High          0.765969
    Low           0.761964
    Close         0.762478
    Volume        0.113771
    ExDividend         NaN
    SplitRatio         NaN
    AdjOpen       0.766066
    AdjHigh       0.765969
    AdjLow        0.761964
    AdjClose      0.762478
    AdjVolume     0.113771
    Diff          0.027863
    dtype: float64




```python
df_CY_08.corrwith(df_MSFT_08['AdjClose'])
```




    Open          0.814615
    High          0.816708
    Low           0.809525
    Close         0.812624
    Volume        0.543386
    ExDividend    0.002629
    SplitRatio         NaN
    AdjOpen       0.732445
    AdjHigh       0.731266
    AdjLow        0.726302
    AdjClose      0.727433
    AdjVolume     0.543386
    Diff          0.107738
    dtype: float64




```python
df_CY_09.corrwith(df_MSFT_09['AdjClose'])
```




    Open          0.805971
    High          0.801337
    Low           0.812744
    Close         0.803599
    Volume        0.178883
    ExDividend         NaN
    SplitRatio         NaN
    AdjOpen       0.805971
    AdjHigh       0.801337
    AdjLow        0.812744
    AdjClose      0.803599
    AdjVolume     0.178883
    Diff          0.065047
    dtype: float64




```python
df_CY_10.corrwith(df_MSFT_10['AdjClose'])
```




    Open          0.180730
    High          0.174627
    Low           0.168876
    Close         0.173180
    Volume        0.157625
    ExDividend         NaN
    SplitRatio         NaN
    AdjOpen       0.180730
    AdjHigh       0.174627
    AdjLow        0.168876
    AdjClose      0.173180
    AdjVolume     0.157625
    Diff          0.081063
    dtype: float64




```python
df_CY_11.corrwith(df_MSFT_11['AdjClose'])
```




    Open          0.037941
    High          0.063605
    Low           0.048204
    Close         0.073510
    Volume        0.132737
    ExDividend   -0.078726
    SplitRatio         NaN
    AdjOpen       0.045161
    AdjHigh       0.071406
    AdjLow        0.055456
    AdjClose      0.081443
    AdjVolume     0.132737
    Diff          0.009169
    dtype: float64




```python
df_CY_12.corrwith(df_MSFT_12['AdjClose'])
```




    Open          0.395520
    High          0.389934
    Low           0.390912
    Close         0.386007
    Volume        0.092949
    ExDividend   -0.034055
    SplitRatio         NaN
    AdjOpen       0.394041
    AdjHigh       0.388280
    AdjLow        0.389197
    AdjClose      0.384134
    AdjVolume     0.092949
    Diff          0.184856
    dtype: float64




```python
df_CY_13.corrwith(df_MSFT_13['AdjClose'])
```




    Open         -0.244973
    High         -0.251219
    Low          -0.227828
    Close        -0.231966
    Volume       -0.183743
    ExDividend    0.011963
    SplitRatio         NaN
    AdjOpen      -0.145623
    AdjHigh      -0.150807
    AdjLow       -0.127831
    AdjClose     -0.131577
    AdjVolume    -0.183743
    Diff         -0.069612
    dtype: float64




```python
df_CY_14.corrwith(df_MSFT_14['AdjClose'])
```




    Open          0.399728
    High          0.402745
    Low           0.397647
    Close         0.401501
    Volume        0.207134
    ExDividend    0.059092
    SplitRatio         NaN
    AdjOpen       0.478192
    AdjHigh       0.480751
    AdjLow        0.476208
    AdjClose      0.479303
    AdjVolume     0.207134
    Diff         -0.083332
    dtype: float64




```python
df_CY_15.corrwith(df_MSFT_15['AdjClose'])
```




    Open         -0.546094
    High         -0.550605
    Low          -0.537179
    Close        -0.538299
    Volume       -0.137651
    ExDividend    0.021248
    SplitRatio         NaN
    AdjOpen      -0.532405
    AdjHigh      -0.537338
    AdjLow       -0.522759
    AdjClose     -0.524228
    AdjVolume    -0.137651
    Diff         -0.010876
    dtype: float64




```python
df_CY_16.corrwith(df_MSFT_16['AdjClose'])
```




    Open          0.662601
    High          0.654571
    Low           0.670483
    Close         0.657769
    Volume       -0.259842
    ExDividend    0.038389
    SplitRatio         NaN
    AdjOpen       0.686834
    AdjHigh       0.679728
    AdjLow        0.693638
    AdjClose      0.682345
    AdjVolume    -0.259842
    Diff          0.030357
    dtype: float64




```python
df_CY_17.corrwith(df_MSFT_17['AdjClose'])
```




    Open          0.848061
    High          0.848232
    Low           0.851382
    Close         0.847400
    Volume       -0.110622
    ExDividend   -0.037306
    SplitRatio         NaN
    AdjOpen       0.866817
    AdjHigh       0.867406
    AdjLow        0.869560
    AdjClose      0.866525
    AdjVolume    -0.110622
    Diff          0.067530
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
df_MSFT_07_AdjClose = df_MSFT_07['AdjClose']
df_MSFT_07_AdjClose.head()
```




    Date
    2007-12-31    27.754531
    2007-12-28    28.159934
    2007-12-27    28.042991
    2007-12-26    28.541949
    2007-12-24    28.518560
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
df_MSFT_07_AdjClose.rename(index='Date')
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
merged_07 = pd.concat([df_CY_07_AdjClose, df_MSFT_07_AdjClose], axis=1, join_axes=[df_CY_07_AdjClose.index])
merged_07.columns = ['CY_07', 'MSFT_07']
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
      <th>MSFT_07</th>
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
      <td>27.754531</td>
    </tr>
    <tr>
      <th>2007-12-28</th>
      <td>6.995078</td>
      <td>28.159934</td>
    </tr>
    <tr>
      <th>2007-12-27</th>
      <td>7.101524</td>
      <td>28.042991</td>
    </tr>
    <tr>
      <th>2007-12-26</th>
      <td>7.363840</td>
      <td>28.541949</td>
    </tr>
    <tr>
      <th>2007-12-24</th>
      <td>7.206070</td>
      <td>28.518560</td>
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
      <th>MSFT_07</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>CY_07</th>
      <td>1.000000</td>
      <td>0.762478</td>
    </tr>
    <tr>
      <th>MSFT_07</th>
      <td>0.762478</td>
      <td>1.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
plt.scatter(df_CY_07['Diff'], df_MSFT_07['Diff'], marker = 'x', c='g')
plt.xlabel = ('Cypress price change per day')
plt.ylabel = ('Microsoft price change per day')
```


![png](output_104_0.png)



```python
seb.regplot(df_CY_07['Diff'], df_MSFT_07['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0fef0eb8>




![png](output_105_1.png)



```python
seb.regplot(df_CY_08['Diff'], df_MSFT_08['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0fcc04e0>




![png](output_106_1.png)



```python
seb.regplot(df_CY_09['Diff'], df_MSFT_09['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0fad1208>




![png](output_107_1.png)



```python
seb.regplot(df_CY_10['Diff'], df_MSFT_10['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0f8ac128>




![png](output_108_1.png)



```python
seb.regplot(df_CY_11['Diff'], df_MSFT_11['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x10678cf28>




![png](output_109_1.png)



```python
seb.regplot(df_CY_12['Diff'], df_MSFT_12['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0f8dc710>




![png](output_110_1.png)



```python
seb.regplot(df_CY_13['Diff'], df_MSFT_13['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0fd5d2e8>




![png](output_111_1.png)



```python
seb.regplot(df_CY_14['Diff'], df_MSFT_14['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0fb91588>




![png](output_112_1.png)



```python
seb.regplot(df_CY_15['Diff'], df_MSFT_15['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0efc89b0>




![png](output_113_1.png)



```python
seb.regplot(df_CY_16['Diff'], df_MSFT_16['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0f97d828>




![png](output_114_1.png)



```python
seb.regplot(df_CY_17['Diff'], df_CY_17['Diff'], marker = 'x')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1a0eedcf98>




![png](output_115_1.png)



```python
stats.ttest_ind(df_CY_17['Diff'], df_MSFT_17['Diff'], equal_var=False)
```




    Ttest_indResult(statistic=nan, pvalue=nan)




```python
df_MSFT_07.loc[:,"Diff"].std()
```




    0.35077240043179797




```python
df_MSFT_08.loc[:,"Diff"].std()
```




    0.5845877464416749




```python
df_MSFT_09.loc[:,"Diff"].std()
```




    0.38296700519260185




```python
df_MSFT_10.loc[:,"Diff"].std()
```




    0.3024108524697126




```python
df_MSFT_11.loc[:,"Diff"].std()
```




    0.3226440714612046




```python
df_MSFT_12.loc[:,"Diff"].std()
```




    0.33083451904892114




```python
df_MSFT_13.loc[:,"Diff"].std()
```




    0.4652181694387321




```python
df_MSFT_14.loc[:,"Diff"].std()
```




    0.4623605878515603




```python
df_MSFT_15.loc[:,"Diff"].std()
```




    0.7679312707845981




```python
df_MSFT_16.loc[:,"Diff"].std()
```




    0.7429402494673895




```python
df_MSFT_17.loc[:,"Diff"].std()
```




    0.690696303224638




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
df_MSFT_07.loc[:,"Diff"].cov(df_CY_07.loc[:,"Diff"])
```




    0.015790963458765586




```python
df_MSFT_08.loc[:,"Diff"].cov(df_CY_08.loc[:,"Diff"])
```




    0.051796583717296646




```python
df_MSFT_09.loc[:,"Diff"].cov(df_CY_09.loc[:,"Diff"])
```




    0.02340080626663888




```python
df_MSFT_10.loc[:,"Diff"].cov(df_CY_10.loc[:,"Diff"])
```




    0.03631702158001247




```python
df_MSFT_11.loc[:,"Diff"].cov(df_CY_11.loc[:,"Diff"])
```




    0.08214651530562196




```python
df_MSFT_12.loc[:,"Diff"].cov(df_CY_12.loc[:,"Diff"])
```




    0.042393794681665195




```python
df_MSFT_13.loc[:,"Diff"].cov(df_CY_13.loc[:,"Diff"])
```




    0.018486348420632803




```python
df_MSFT_14.loc[:,"Diff"].cov(df_CY_14.loc[:,"Diff"])
```




    0.023230158670972254




```python
df_MSFT_15.loc[:,"Diff"].cov(df_CY_15.loc[:,"Diff"])
```




    0.07236236063057977




```python
df_MSFT_16.loc[:,"Diff"].cov(df_CY_16.loc[:,"Diff"])
```




    0.05018303941566921




```python
df_MSFT_17.loc[:,"Diff"].cov(df_CY_17.loc[:,"Diff"])
```




    0.0727378858676513




```python
df_CY_07['Diff'].mean()
```




    -0.014621232686265995




```python
df_MSFT_07['Diff'].mean()
```




    -0.019138678441384




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
MSFT_07_mean=df_MSFT_07['Diff'].mean()
MSFT_07_mean
```




    -0.019138678441384




```python
MSFT_08_mean=df_MSFT_08['Diff'].mean()
MSFT_08_mean
```




    0.04771415588460318




```python
MSFT_09_mean=df_MSFT_09['Diff'].mean()
MSFT_09_mean
```




    -0.03438477143411155




```python
MSFT_10_mean=df_MSFT_10['Diff'].mean()
MSFT_10_mean
```




    0.007968026377111552




```python
MSFT_11_mean=df_MSFT_11['Diff'].mean()
MSFT_11_mean
```




    0.004401720543235059




```python
MSFT_12_mean=df_MSFT_12['Diff'].mean()
MSFT_12_mean
```




    -0.0024290254723011995




```python
MSFT_13_mean=df_MSFT_13['Diff'].mean()
MSFT_13_mean
```




    -0.038103262979334654




```python
MSFT_14_mean=df_MSFT_14['Diff'].mean()
MSFT_14_mean
```




    -0.037944850225175276




```python
MSFT_15_mean=df_MSFT_15['Diff'].mean()
MSFT_15_mean
```




    -0.037788025484533895




```python
MSFT_16_mean=df_MSFT_16['Diff'].mean()
MSFT_16_mean
```




    -0.03429128380367728




```python
MSFT_17_mean=df_MSFT_17['Diff'].mean()
MSFT_17_mean
```




    -0.09767412915843779




```python
def gendata_07(loc1=0, loc2=0):
    population_n_07 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_07 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_07, population_a_07
population_n_07, population_a_07 = gendata_07(loc1=CY_07_mean, loc2=MSFT_07_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_07)), population_n_07, label="CY 07")
plt.scatter(range(len(population_a_07)), population_a_07, label="MSFT 07")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_07, 10, density=True, alpha=0.5, label="CY 07")
plt.hist(population_a_07, 10, density=True, alpha=0.5, label="MSFT 07")
plt.axvline(population_n_07.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_07.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a0ff4bc50>




![png](output_174_1.png)



```python
stats.ttest_ind(population_n_07, population_a_07, equal_var=False)
```




    Ttest_indResult(statistic=0.049390842409055974, pvalue=0.960627628277517)




```python
def gendata_08(loc1=0, loc2=0):
    population_n_08 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_08 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_08, population_a_08
population_n_08, population_a_08 = gendata_08(loc1=CY_08_mean, loc2=MSFT_08_mean)
plt.subplot(2, 1, 1)
plt.scatter(range(len(population_n_08)), population_n_08, label="CY 08")
plt.scatter(range(len(population_a_08)), population_a_08, label="MSFT 08")
plt.legend()

    # Histogram Plot of Data
plt.subplot(2, 1, 2)
plt.hist(population_n_08, 10, density=True, alpha=0.5, label="CY 08")
plt.hist(population_a_08, 10, density=True, alpha=0.5, label="MSFT 08")
plt.axvline(population_n_08.mean(), color='r', linestyle='dashed', linewidth=1)
plt.axvline(population_a_08.mean(), color='r', linestyle='dashed', linewidth=1)
plt.legend() 
```




    <matplotlib.legend.Legend at 0x1a0f8573c8>




![png](output_176_1.png)



```python
stats.ttest_ind(population_n_08, population_a_08, equal_var=False)
```




    Ttest_indResult(statistic=-0.385231385043387, pvalue=0.7002304743671055)




```python
def gendata_09(loc1=0, loc2=0):
    population_n_09 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_09 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_09, population_a_09
population_n_09, population_a_09 = gendata_09(loc1=CY_09_mean, loc2=MSFT_09_mean)
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




    <matplotlib.legend.Legend at 0x1a18337860>




![png](output_178_1.png)



```python
stats.ttest_ind(population_n_09, population_a_09, equal_var=False)
```




    Ttest_indResult(statistic=0.173826168560095, pvalue=0.8620727131180247)




```python
def gendata_10(loc1=0, loc2=0):
    population_n_10 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_10 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_10, population_a_10
population_n_10, population_a_10 = gendata_10(loc1=CY_10_mean, loc2=MSFT_10_mean)
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




    <matplotlib.legend.Legend at 0x1a184b4da0>




![png](output_180_1.png)



```python
stats.ttest_ind(population_n_10, population_a_10, equal_var=False)
```




    Ttest_indResult(statistic=-0.36163648984508895, pvalue=0.7177770771971019)




```python
def gendata_11(loc1=0, loc2=0):
    population_n_11 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_11 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_11, population_a_11
population_n_11, population_a_11 = gendata_11(loc1=CY_11_mean, loc2=MSFT_11_mean)
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




    <matplotlib.legend.Legend at 0x1a1863c320>




![png](output_182_1.png)



```python
stats.ttest_ind(population_n_11, population_a_11, equal_var=False)
```




    Ttest_indResult(statistic=-0.011633885686005607, pvalue=0.9907223706492247)




```python
def gendata_12(loc1=0, loc2=0):
    population_n_12 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_12 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_12, population_a_12
population_n_12, population_a_12 = gendata_12(loc1=CY_12_mean, loc2=MSFT_12_mean)
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




    <matplotlib.legend.Legend at 0x1a186a5860>




![png](output_184_1.png)



```python
stats.ttest_ind(population_n_12, population_a_12, equal_var=False)
```




    Ttest_indResult(statistic=0.2266936122998297, pvalue=0.8207550155095757)




```python
def gendata_13(loc1=0, loc2=0):
    population_n_13 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_13 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_13, population_a_13
population_n_13, population_a_13 = gendata_13(loc1=CY_13_mean, loc2=MSFT_13_mean)
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




    <matplotlib.legend.Legend at 0x1a18937da0>




![png](output_186_1.png)



```python
stats.ttest_ind(population_n_13, population_a_13, equal_var=False)
```




    Ttest_indResult(statistic=0.43049966732301365, pvalue=0.6670184566018142)




```python
def gendata_14(loc1=0, loc2=0):
    population_n_14 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_14 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_14, population_a_14
population_n_14, population_a_14 = gendata_14(loc1=CY_14_mean, loc2=MSFT_14_mean)
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




    <matplotlib.legend.Legend at 0x1a18ac1320>




![png](output_188_1.png)



```python
stats.ttest_ind(population_n_14, population_a_14, equal_var=False)
```




    Ttest_indResult(statistic=0.24265865480313614, pvalue=0.8083697454881813)




```python
def gendata_15(loc1=0, loc2=0):
    population_n_15 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_15 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_15, population_a_15
population_n_15, population_a_15 = gendata_15(loc1=CY_15_mean, loc2=MSFT_15_mean)
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




    <matplotlib.legend.Legend at 0x1a18c3d860>




![png](output_190_1.png)



```python
stats.ttest_ind(population_n_15, population_a_15, equal_var=False)
```




    Ttest_indResult(statistic=0.5802872459520274, pvalue=0.5619833920327753)




```python
def gendata_16(loc1=0, loc2=0):
    population_n_16 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_16 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_16, population_a_16
population_n_16, population_a_16 = gendata_16(loc1=CY_16_mean, loc2=MSFT_16_mean)
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




    <matplotlib.legend.Legend at 0x1a18dbdda0>




![png](output_192_1.png)



```python
stats.ttest_ind(population_n_16, population_a_16, equal_var=False)
```




    Ttest_indResult(statistic=0.2732623277554674, pvalue=0.7847648576736541)




```python
def gendata_17(loc1=0, loc2=0):
    population_n_17 = stats.norm.rvs(loc=loc1, size = 250, random_state=250)
    population_a_17 = stats.norm.rvs(loc=loc2, size = 250, random_state=250)
    return population_n_17, population_a_17
population_n_17, population_a_17 = gendata_17(loc1=CY_17_mean, loc2=MSFT_17_mean)
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




    <matplotlib.legend.Legend at 0x1a18f43320>




![png](output_194_1.png)



```python
stats.ttest_ind(population_n_17, population_a_17, equal_var=False)
```




    Ttest_indResult(statistic=0.8782291726051847, pvalue=0.38024287650001654)




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
data1 = pd.DataFrame(df_MSFT_07['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_MSFT_08['Diff']).assign(Location=2)
data3 = pd.DataFrame(df_MSFT_09['Diff']).assign(Location=3)



cdf = pd.concat([data1, data2, data3])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         1   Diff       NaN
    1         1   Diff  0.405403
    2         1   Diff -0.116943
    3         1   Diff  0.498958
    4         1   Diff -0.023389



![png](output_202_1.png)



```python
data4 = pd.DataFrame(df_MSFT_10['Diff']).assign(Location=4)
data5 = pd.DataFrame(df_MSFT_11['Diff']).assign(Location=5)
data6 = pd.DataFrame(df_MSFT_12['Diff']).assign(Location=6)

cdf = pd.concat([data4, data5, data6])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         4   Diff       NaN
    1         4   Diff -0.049775
    2         4   Diff  0.099549
    3         4   Diff  0.033183
    4         4   Diff  0.049775



![png](output_203_1.png)



```python
data7 = pd.DataFrame(df_MSFT_13['Diff']).assign(Location=7)
data8 = pd.DataFrame(df_MSFT_14['Diff']).assign(Location=8)
data9 = pd.DataFrame(df_MSFT_15['Diff']).assign(Location=9)

cdf = pd.concat([data7, data8, data9])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0         7   Diff       NaN
    1         7   Diff -0.108287
    2         7   Diff  0.000000
    3         7   Diff  0.135358
    4         7   Diff -0.324860



![png](output_204_1.png)



```python
data10 = pd.DataFrame(df_MSFT_16['Diff']).assign(Location=10)
data11 = pd.DataFrame(df_MSFT_17['Diff']).assign(Location=11)


cdf = pd.concat([data10, data11])    
mdf = pd.melt(cdf, id_vars=['Location'], var_name=['Letter'])
print(mdf.head())
ax = seb.boxplot(x="Location", y="value", hue="Letter", data=mdf)    
plt.show()
```

       Location Letter     value
    0        10   Diff       NaN
    1        10   Diff  0.743473
    2        10   Diff  0.088043
    3        10   Diff  0.283694
    4        10   Diff -0.039130



![png](output_205_1.png)



```python
#==================================================================================
```


```python
data1 = pd.DataFrame(df_CY_07['Diff']).assign(Location=1)
data2 = pd.DataFrame(df_MSFT_07['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_MSFT_08['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_MSFT_09['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_MSFT_10['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_MSFT_11['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_MSFT_12['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_MSFT_12['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_MSFT_13['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_MSFT_14['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_MSFT_15['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_MSFT_16['Diff']).assign(Location=2)

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
data2 = pd.DataFrame(df_MSFT_17['Diff']).assign(Location=2)

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
