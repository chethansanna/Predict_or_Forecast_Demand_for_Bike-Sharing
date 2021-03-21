# Predicts or forecasts demand for bike-sharing

A Neural network built from the scratch (without using any of the deep learning frameworks) has been used to predict the demand for bike-sharing based on the 17379 hours of data.

## Data

The bike-sharing rental process is highly correlated to environmental and seasonal settings. For instance, weather conditions,
precipitation, day of the week, season, hour of the day, etc. can affect the rental behaviours. The core data set is related to the two-year historical log corresponding to the years 2011 and 2012 from Capital Bikeshare system, Washington D.C., the USA which is publicly available in [capitalbikeshare](http://capitalbikeshare.com/system-data). Then aggregated the data on two hourly and daily basis and then extracted and added the corresponding weather and seasonal information. Weather information are extracted from [freemeteo](http://www.freemeteo.com).

There are two files of the dataset:

  - hour.csv: bike-sharing counts aggregated on an hourly basis. Records: 17379 hours
  - day.csv: bike-sharing counts aggregated on daily basis. Records: 731 days

More information about the dataset and the actual dataset can be found in the [Bike-Sharing-Dataset](/Bike-Sharing-Dataset).

**Test data:** Approximately the last 21 days of data has been used as a test set. This data was used to make predictions based on the trained model and compare them with the actual number of riders.

**Validation data:** Among the remaining data, approximately the data of the last 60 days was held out as validation data.

## Network architecture

In order to build a very simple neural network (since this project did not use any deep learning frameworks), only one hidden layer was used. 

## Results

After 2700 iterations of network training, the losses obtained are **training loss:** 0.077 **Validation loss:** 0.175. The graph below shows the behaviour of the training and validation loss over 2700 epochs.

![image](https://user-images.githubusercontent.com/47500198/111923193-4ad6f780-8a9e-11eb-81f8-3b1eb5bf3d58.png)

Testing on approximately the last 21 days of the testing data resulted in the following prediction. The predictions are pretty good for a very simple model with one hidden layer, except on and after Dec 22 because of the holiday season.

![image](https://user-images.githubusercontent.com/47500198/111923250-8376d100-8a9e-11eb-982e-f124c267939a.png)
