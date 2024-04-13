# momentum_prediction
MODEL ACCURACY:70%

I have currently split the model in train-test split but if you want to include your own validation set remove the (train_test_split line and add:
Also modify the plotting code to new dataframe and Y_pred_new instead of y_pred
```python
import pandas as pd

# Load the new dataset
new_data = pd.read_csv("new_data.csv")



# Assuming X_new contains the features of the new dataset
X_new = new_data[['open','close','high','low','volume','reserve','funding_rates','mvrv' , 'nrpl', 'nupl','stock_to_flow_reversion','sth_sopr','RSI','9_ema','21_ema','50_ema','200_ema','Fear_and_Greed_Index']]

# Assuming label_encoder is the same encoder used for the training data
# Encode the target variable if needed
# For example, if the 'Label' column contains categorical values
# y_new_encoded = label_encoder.transform(new_data['Label'])

# Use the trained model to make predictions on the new dataset
y_pred_new = knn.predict(X_new)
print(y_pred_new)
