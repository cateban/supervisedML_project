# Solar Radiation Prediction

This was a Kaggle competition. You can find it here https://www.kaggle.com/c/solar-energy-prediction-datamex0320/overview

The dataset contains columns such as wind speed and direction, humidity or temperature. The competition is to predict solar radiation based on those data. There are 4 months of data.

The error metric is the MSE, therefore, the lower the better the result.

#### The units of each column are:

- Radiation: Solar radiation in watts per meter ^ 2
- Temperature: Temperature in degrees Fahrenheit
- Humidity: Humidity in %
- Pressure: Atmospheric pressure in mm Hg
- WindDirection (degrees): Wind direction in degrees
- Speed: Wind speed in miles per hour
- Sunrise / sunset: Sunrise-Sunset (Hawaii time)
- UNIXTime: TimeStamp (seconds from 01-01-1970)
- Data: Date
- Time: Time



For this project, I cleaned the data, standarized it and used the following libraries and ML Models:

```python
from sklearn.preprocessing import StandardScaler, MinMaxScaler, RobustScaler
from sklearn.model_selection import train_test_split as tts
from sklearn.metrics import mean_squared_error as mse
from sklearn.linear_model import LinearRegression as LinReg
from sklearn.metrics import r2_score
from sklearn.linear_model import SGDRegressor as SGDR
from sklearn.linear_model import Lasso
from sklearn.linear_model import Ridge
from sklearn.linear_model import ElasticNet
from sklearn.svm import SVR
from sklearn.ensemble import RandomForestRegressor as RFR
from sklearn.tree import ExtraTreeRegressor as ETR
from sklearn.neighbors import KNeighborsRegressor as KNNR
from sklearn.ensemble import GradientBoostingRegressor as GBR
from mlxtend.regressor import StackingRegressor
```

##### Got third place with a MSE of 6173.56542. 
