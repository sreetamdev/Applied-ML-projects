##### Table Of Contents:

* 1.Introduction
* 2.Dataset Source
* 3.Exploring The Data
* 4.Modelling The Data
* 5.Outcome For The Business Metric of the "Bike Sharing System" to find the  count of riders on daily basis:
* 6.Technologies Used
* 7.Setup Environment
* 8.Attributes within dataset
* 9.References


###### Note: 
* Refer the Setup Environment as there are two files namely created under Jupyter notebook: 
    * 1.BIKE_final_file.ipynb
    * 2.Script_bike_final.ipynb

* Refer the Azure_Bike_Share.pdf file version to look out for the similar data analysis and modelling process undertaken within Azure ML studio environment.

##### 1.Introduction

* General info: 

    * This dataset is about the bike-sharing system, which discloses instances of riders on various facets influenced by different environmental-based conditions.

    * No of instances sharing information within this system is 731 days

    * No of features found within the data file is 17.

* Project Aim: The target is to design a regression algorithm to find "count of rental bike riders on daily basis" which is under the "cnt" feature of the dataset.

##### 2.Dataset Source:

* Bike Sharing Dataset Data Set. Retrieved from https://archive.ics.uci.edu/ml/datasets/Bike+Sharing+Dataset

##### 3.Exploring The Data

* The objective is to perform exploratory data analysis by understanding features, descriptive figures (Plots/Boxplots, Cross-Correlation Plot), using statistics such as IQR to discover potential outliers and skewness associated with the features.

* Transforming and normalizing features to prepare the data for the application of machine learning regression algorithms.

##### 4.Modelling The Data

* The objective is to split the data after EDA is completed. Train and test splits are performed on the data set in the ratio of 80:20 respectively.

* Performing the similar modelling process with other ML algorithms.

* Validating the results of the model using statistical tools 

##### 5.Outcome For The Business Metric Of The "Bike Sharing System" To Find The  Count Of Riders On Daily Basis:

* As per the model, the factor temperature influences the most for bike count.

* Month, weather situation of the year closely follow after temperature and influence the bike count.

* The statistical tool Rsquare for both feature selected linear model and Random Forest Regressor model perform similarly in this case. So, 88.6% variance of  "cnt"(target features)can be explained by the explanatory features: temp, year, month, weather situation, weekday, working day and holiday

##### 6.Technologies Used

* Jupyter Notebook for writing scripts in python3.

* Python ML, visualisation and model metrics libraries : pandas, numpy, matplotlib, seaborn, statsmodels, sklearn (LinearRegression, DecisionTreeRegressor, RandomForestRegressor, GridSearchCV, StratifiedKFold, cross_val_score,MinMaxScaler,r2_score,mean_squared_error,mean_absolute_error).


##### 7.Setup Environment.

* Anaconda for Python 3.8 environment for initiating Jupyterlab.

* Uploading data files from the source into Jupyter.

* Operating the python script to perform the analysis.

* There are two script files : 

    * 1.BIKE_final_file.ipynb - the complete end to end data analysis including EDA, data modelling, validation of results, recommendations.
    * 2.Script_bike_final.ipynb - the complete end to end function script that can be applied by the user on the data set without coding.


##### 8. Attributes Within A Dataset:

* instant: record index
* dteday : date
* season : season (1:springer, 2:summer, 3:fall, 4:winter)
* yr : year (0: 2011, 1:2012)
* mnth : month ( 1 to 12)
* holiday : weather day is holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
* weekday : day of the week
* workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
* weathersit : 
	* 1: Clear, Few clouds, Partly cloudy, Partly cloudy
	* 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
	* 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
	* 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
* temp : Normalized temperature in Celsius. The values are divided to 41 (max)
* atemp: Normalized feeling temperature in Celsius. The values are divided to 50 (max)
* hum: Normalized humidity. The values are divided to 100 (max)
* windspeed: Normalized wind speed. The values are divided to 67 (max)
* casual: count of casual users
* registered: count of registered users
* cnt: count of total rental bikes including both casual and registered


##### 9.References:

* [1] Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg, doi:10.1007/s13748-013-0040-3.

* "DSDJ", Kyle Mckiou's team for conceptual understanding of models and code methodology adopted.
