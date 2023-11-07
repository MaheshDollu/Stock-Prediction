Strategy_1: If the next trading day's close price is greater than today's close price then the signal is ‘buy’, otherwise ‘sell’ 
Strategy_2: Utilize the 50-day moving average vs the 200-day moving average. A golden cross (or golden crossover) is a chart pattern that involves a short-term moving average crossing above a long-term moving average. Typically, the 50-day MA is used as the short-term average, and the 200-day MA is used as the long-term average. This is an indicator of bullish (buying) signal. 

A death cross is basically the opposite of a golden cross. It’s a chart pattern where a short-term MA crosses below a long-term MA. For example, the 50-day MA crosses below the 200-day MA. As such, a death cross is typically considered to be a bearish (selling) signal.

NumPy library provides a plethora of building methods to handle current (today’s) price, yesterday’s price, Moving Averages (MAs), Roll, etc.

For instance, to calculate the values of the target variable for Strategy-1, use this NumPy call:

y = np.where(df[‘Stock_Price’].shift(-1) > df[‘Stock_Price’], 1, -1)

For Moving Averages (strategy_2) you should come up with a similar formula. 
The following steps, generating the ML classifiers, should be performed:

1. Pre-process and clean the data
2. Define the Feature Variable ‘X’, and the Label/Target variable ‘y’
3. Spilt the data into training and test datasets (use the 80/20 percent ratio)
4. Choose a Classifier and fit it on the training dataset (take its default parameters)
5. Evaluate the Classifier on the test dataset

Utilized the following ML Classifier Models:
1) K-Nearest Neighbors (KNN) from sklearn.neighbors import KNeighborsClassifier
2) Random Forest Classifier (RF) from sklearn.ensemble import RandomForestClassifier
3) Gradient Boosting Classifier (GB) from sklearn.ensemble import GradientBoostingClassifier
4) Support Vector Machines (SVMs) from sklearn.svm import SVC
5) XGBoost Classifier
(Note: You don't import it from scikit-learn module!)
(You need to install it, it not available: pip install xgboost)
from xgboost import XGBClassifier
