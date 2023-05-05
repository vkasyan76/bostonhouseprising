# bostonhouseprising

Create a new environment

```
conda create -p venv python==3.7 -y

1	Create Panndas dataset: 	dataset=pd.DataFrame(boston.data,columns=boston.feature_names)
2	Add Target to dataset:	dataset['Price']=boston.target
3	Analyze Dataset using seaborn
4	Train / Test Split:	from sklearn.model_selection import train_test_split	X_train,X_test,y_train,y_test=train_test_split(X,y,test_size=0.3,random_state=42)
5	Standardize the dataset:	X_train=scaler.fit_transform(X_train) /	X_test=scaler.transform(X_test)
6	Train Datamodel: from sklearn.linear_model import LinearRegression / regression=LinearRegression() / regression.fit(X_train,y_train)
7	Prediction With Test Data: reg_pred=regression.predict(X_test)
8   New Data Prediction: scaler.transform(boston.data[0].reshape(1,-1)) / regression.predict(scaler.transform(boston.data[0].reshape(1,-1)))
9   Pickling The Model file For Deployment: pickle.dump(regression,open('regmodel.pkl','wb')) / pickled_model=pickle.load(open('regmodel.pkl','rb'))
10  Prediction with pickle model: pickled_model.predict(scaler.transform(boston.data[0].reshape(1,-1)))
```
