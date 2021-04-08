# game-app-optimization
How to optimize the game app
Introduction
Greetings from the Kaggle bot! This is an automatically-generated kernel with starter code demonstrating how to read in the data and begin exploring. If you're inspired to dig deeper, click the blue "Fork Notebook" button at the top of this kernel to begin editing.

Exploratory Analysis
To begin this exploratory analysis, first import libraries and define functions for plotting the data using matplotlib. Depending on the data, not all plots will be made. (Hey, I'm just a simple kerneling bot, not a Kaggle Competitions Grandmaster!)

from mpl_toolkits.mplot3d import Axes3D
from sklearn.preprocessing import StandardScaler
import matplotlib.pyplot as plt # plotting
import numpy as np # linear algebra
import os # accessing directory structure
import pandas as pd # data processing, CSV file I/O (e.g. pd.read_csv)
There are 3 csv files in the current version of the dataset:

for dirname, _, filenames in os.walk('/kaggle/input'):
    for filename in filenames:
        print(os.path.join(dirname, filename))
/kaggle/input/channel_event.csv
/kaggle/input/d1.csv
/kaggle/input/pivot_ce_d1.csv
The next hidden code cells define functions for plotting data. Click on the "Code" button in the published kernel to reveal the hidden code.

Now you're ready to read in the data and use the plotting functions to visualize the data.

Let's check 1st file: /kaggle/input/channel_event.csv
nRowsRead = 1000 # specify 'None' if want to read whole file
# channel_event.csv may have more rows in reality, but we are only loading/previewing the first 1000 rows
df1 = pd.read_csv('/kaggle/input/channel_event.csv', delimiter=',', nrows = nRowsRead)
df1.dataframeName = 'channel_event.csv'
nRow, nCol = df1.shape
print(f'There are {nRow} rows and {nCol} columns')
There are 85 rows and 6 columns
Let's take a quick look at what the data looks like:

df1.head(5)
event	channel	country	language	os	device
0	install	A	KR	ko-KR	ios	phone
1	install	A	KR	ko-KR	ios	phone
2	install	A	KR	ko-KR	ios	phone
3	install	A	KR	ko-KR	ios	phone
4	install	A	KR	ko-KR	ios	phone
Distribution graphs (histogram/bar graph) of sampled columns:

plotPerColumnDistribution(df1, 10, 5)
/opt/conda/lib/python3.7/site-packages/ipykernel_launcher.py:10: MatplotlibDeprecationWarning: Passing non-integers as three-element position specification is deprecated since 3.3 and will be removed two minor releases later.
  # Remove the CWD from sys.path while we load stuff.
/opt/conda/lib/python3.7/site-packages/ipykernel_launcher.py:10: MatplotlibDeprecationWarning: Passing non-integers as three-element position specification is deprecated since 3.3 and will be removed two minor releases later.
  # Remove the CWD from sys.path while we load stuff.

Let's check 2nd file: /kaggle/input/d1.csv
nRowsRead = 1000 # specify 'None' if want to read whole file
# d1.csv may have more rows in reality, but we are only loading/previewing the first 1000 rows
df2 = pd.read_csv('/kaggle/input/d1.csv', delimiter=',', nrows = nRowsRead)
df2.dataframeName = 'd1.csv'
nRow, nCol = df2.shape
print(f'There are {nRow} rows and {nCol} columns')
There are 7 rows and 3 columns
Let's take a quick look at what the data looks like:

df2.head(5)
channel	install	day1
0	A	10	4
1	B	2	0
2	C	1	1
3	D	5	1
4	E	5	1
Distribution graphs (histogram/bar graph) of sampled columns:

plotPerColumnDistribution(df2, 10, 5)
/opt/conda/lib/python3.7/site-packages/ipykernel_launcher.py:10: MatplotlibDeprecationWarning: Passing non-integers as three-element position specification is deprecated since 3.3 and will be removed two minor releases later.
  # Remove the CWD from sys.path while we load stuff.
/opt/conda/lib/python3.7/site-packages/ipykernel_launcher.py:10: MatplotlibDeprecationWarning: Passing non-integers as three-element position specification is deprecated since 3.3 and will be removed two minor releases later.
  # Remove the CWD from sys.path while we load stuff.

Correlation matrix:

plotCorrelationMatrix(df2, 8)

Scatter and density plots:

plotScatterMatrix(df2, 6, 15)

Let's check 3rd file: /kaggle/input/pivot_ce_d1.csv
nRowsRead = 1000 # specify 'None' if want to read whole file
# pivot_ce_d1.csv may have more rows in reality, but we are only loading/previewing the first 1000 rows
df3 = pd.read_csv('/kaggle/input/pivot_ce_d1.csv', delimiter=',', nrows = nRowsRead)
df3.dataframeName = 'pivot_ce_d1.csv'
nRow, nCol = df3.shape
print(f'There are {nRow} rows and {nCol} columns')
There are 7 rows and 11 columns
Let's take a quick look at what the data looks like:

df3.head(5)
channel	install	af_complete_registration	af_level5_achieved	af_level8_achieved	af_purchase	day1	nru	Lv5	purchase_rate	day1_retention
0	G	11	0	0	0	0	1	0.00%	0.00%	0.00%	9.09%
1	D	5	0	0	0	0	1	0.00%	0.00%	0.00%	20.00%
2	E	5	0	0	0	0	1	0.00%	0.00%	0.00%	20.00%
3	F	9	0	0	0	0	3	0.00%	0.00%	0.00%	33.33%
4	A	10	10	5	4	0	4	100.00%	50.00%	0.00%	40.00%
Distribution graphs (histogram/bar graph) of sampled columns:

plotPerColumnDistribution(df3, 10, 5)
/opt/conda/lib/python3.7/site-packages/ipykernel_launcher.py:10: MatplotlibDeprecationWarning: Passing non-integers as three-element position specification is deprecated since 3.3 and will be removed two minor releases later.
  # Remove the CWD from sys.path while we load stuff.
/opt/conda/lib/python3.7/site-packages/ipykernel_launcher.py:10: MatplotlibDeprecationWarning: Passing non-integers as three-element position specification is deprecated since 3.3 and will be removed two minor releases later.
  # Remove the CWD from sys.path while we load stuff.
/opt/conda/lib/python3.7/site-packages/ipykernel_launcher.py:10: MatplotlibDeprecationWarning: Passing non-integers as three-element position specification is deprecated since 3.3 and will be removed two minor releases later.
  # Remove the CWD from sys.path while we load stuff.
/opt/conda/lib/python3.7/site-packages/ipykernel_launcher.py:10: MatplotlibDeprecationWarning: Passing non-integers as three-element position specification is deprecated since 3.3 and will be removed two minor releases later.
  # Remove the CWD from sys.path while we load stuff.

Correlation matrix:

plotCorrelationMatrix(df3, 8)

Scatter and density plots:

plotScatterMatrix(df3, 18, 10)

Conclusion
This concludes your starter analysis! To go forward from here, click the blue "Fork Notebook" button at the top of this kernel. This will create a copy of the code and environment for you to edit. Delete, modify, and add code as you please. Happy Kaggling!
