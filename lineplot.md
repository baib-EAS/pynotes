## An example of plotting line chart in python
```
%matplotlib inline
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
```
```
df = pd.DataFrame({'x':x, 'y':y, 'z':z})
fig = plt.figure(num=3, figsize=(10, 5))
sz = 4
wd = 2
plt.plot( 'x', 'y', data=df, marker='o', markerfacecolor='green', markersize=sz, color='green', linestyle='--', linewidth=wd, label="y:x")
font = {'family': 'times-new-roman','weight': 'normal','size': 18,}
plt.xlabel('x',font)
plt.ylabel('y',font)
plt.xlim((-5, 5))
plt.ylim((-2, 2))
plt.legend(prop=font)
my_x_ticks = np.arange(a, b, sep_x)
my_y_ticks = np.arange(c, d, sep_y)
plt.xticks(my_x_ticks,size = size)
plt.yticks(my_y_ticks,size = size)
plt.show()
```
