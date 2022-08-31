# How can we recommend a better train schedule based on the traffic at the stations?

## Links
[Code](https://github.com/lee-jin81/metis_project_1_EDA/blob/main/eda_train_FINAL.ipynb)<br>
[Slides](https://github.com/lee-jin81/metis_project_1_EDA/blob/main/slides_eda.pdf)<br>
[Write-up](https://github.com/lee-jin81/metis_project_1_EDA/blob/main/writeup_eda.pdf)<br>
[MVP](https://github.com/lee-jin81/metis_project_1_EDA/blob/main/mvp_eda.pdf)<br>
[Proposal](https://github.com/lee-jin81/metis_project_1_EDA/blob/main/proposal_eda.pdf)

## Abstract
In this project, I am analyzing subway station entry data to recommend a train schedule that will optimize passenger experience by sending the most trains at the times of the most entries. By calculating an optimal train schedule based on the usage data, trains can be more efficiently used throughout the day. As a proof of concept, I focused on portions of the train 1 mta turnstile data only and compared it to the train 1 schedule. Based on my analysis, the peak usage of train 1 subways is slightly shifted from the peak hours of ridership. Instead, trains are arriving more frequently after peak ridership. For a train schedule that will more efficiently use trains, train arrivals should be shifted by 1 hour earlier allowing riders to get on them during peak hours. The same analysis can be applied to other trains to identify any need for an updated train schedule.

## Introduction
By calculating an optimal train schedule based on the usage data, the MTA can distribute their trains more efficiently throughout times and days of the week. Trains should come more or less frequently depending on the day and time at a particular station. Stations with higher traffic should have trains coming more often whereas stations with less traffic should  have trains come less frequently. Distributing trains more effectively across the lines aims to optimize use of the trains to save energy and fuel while still keeping wait times short. Trains from low traffic stations can be rerouted to stations with higher traffic or serve as backup trains in the event of maintenance or when trains are out of service.

## Data 
A Turnstile data set of 3 months long will be obtained from the [MTA website](http://web.mta.info/developers/turnstile.html) and pdf files of 
the train [schedules](https://new.mta.info/schedules).

## Algorithms
Exploratory data analysis was performed on the data sets:
* Removing duplicates entries since each unique station’s turnstile should have 1 entry only per datetime.
* Creating a datetime object from the date and time columns for date and hourly analysis.
* Calculating the actual entries and exits data by looking at the difference between daily counter values.
* Recalculating the daily entries and exits since impossibly high values were observed. Some of these are likely due to the counter being reset.
* For the train schedule, entries in the timetable (.pdf) file were uploaded into excel, then time was converted to 24-hour format and then uploaded to pandas.

## Tools
* SQLite: to download and store the data in the database. 
* SQLAlchemy: to access the SQLite database and import the data into Jupyter notebook
* Pandas and Matplotlib: Data visualization
* Python: to use Pandas and Matplotlib libraries




