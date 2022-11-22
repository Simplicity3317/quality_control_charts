## Introduction

The Quality control Charts are very useful in industries to determine if a process is under **Statistical control**.
Quality control Charts are divided into two:
1. Control Charts for Variables.
2. Control Charts for Attributes.
- Control Charts for <code>variables</code> are used if the observations are **Continuous**.
- Control Charts for <code>Attributes</code> are used if the observerations are **Discrete**.
**Examples of Control Charts for Variables are:**
- x-bar Charts
- Range Charts
- s chart
- x chart
**Examples of Control Charts for attributes are:**
-c chart
- u chart
- p chart
- np chart

-----------------------------------------------------------------------------------------------------------------------------------
## Code Usage

1. Copy and Paste the code to your pythhon environment.
2. Make sure your dataframe is a Pandas DataFrame.
3. Create an instance by passing <code>qc_charts</code> to the dataframe  
Available Charts.
1. R Chart  
2. X bar Chart
3. s chart
 __Code Example.__
 
 import pandas as pd
 data = pd.read_csv('mydata.csv')
 df = qc_charts(data)
 #### To plot x_bar charts
 df.mean_charts(n = 5)
 #### n is the number of observations in the sample.
 ---------------------------------------------------------------------------------------------------------------------------------
#### Other methods
df.r_charts(5) #to plot R chart.
df.s_chart(5) #to plot S charts.
#### Additional methods
df.describe_table #To show the summary of the table. 

#### You can also set Title,x_label,y_label for your plot.

df.range_chart(n = 3,title = 'Range chart for the production of Oil ',y_label = 'Range of Sample',
               x_label = 'Sample')

