## linear regression in python 
see more at https://realpython.com/linear-regression-in-python/#simple-linear-regression
```
import numpy as np
from sklearn.linear_model import LinearRegression
```
need to reshape x before regression:
```
model = LinearRegression().fit(x.reshape(-1, 1), y)
```
get parameters by:
```
r_square = model.score(x.reshape(-1, 1), y)
intercept = model.intercept_
slope = model.coef_
```
predict simply by:
```
y_pred = model.predict(x.reshape(-1, 1))
```
or use a new x range
```
x_new = np.arange(...).reshape((-1, 1))
y_new = model.predict(x_new)
```
