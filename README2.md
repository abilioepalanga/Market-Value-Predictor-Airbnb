Orphan Branch Structure
This is an orphan branch used to keep the production model isolated from the development and training code. It contains only what is necessary for running the model in a production environment.
.

├── model/

│ └── final_model.joblib 
├── data/

│ └── new_data.csv

└── README.md

Rent Price Prediction with HashMoveis
This repository contains the production model for the project "Rent Price Prediction with HashMoveis".

The model has been successfully trained, selected, and exported, and is ready to be applied to new data for real-time predictions.
Production Model
The production model is a RandomForestRegressor, optimized and chosen after an extensive testing and validation phase.
It has been exported using the joblib library and can be loaded directly for predictions.

How to Use
To load the model and make predictions, in general you can use the following code:

python:

from joblib import load
import pandas as pd

#Load the model
model = load('path/Market-Value-Predictor-Airbnb/final_model.joblib')

#Load new data for prediction
new_data = pd.read_csv('path/new_data.csv')

#Make predictions
predictions = model.predict(new_data)

#Add predictions to the DataFrame
new_data['rent_prediction'] = predictions

#Save the predictions
new_data.to_csv('data/predictions.csv', index=False)

Contact
elvisprizley@yahoo.com.
