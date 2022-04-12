# How can we recommend a better train schedule based on the traffic at the stations?

## Motivation
By calculating an optimal train schedule based on the usage data, the MTA can distribute their trains more efficiently throughout times and days of the week. Trains should come more or less frequently depending on the day and time at a particular station. Stations with higher traffic should have trains coming more often whereas stations with less traffic should  have trains come less frequently. Distributing trains more effectively across the lines aims to optimize use of the trains to save energy and fuel while still keeping wait times short. Trains from low traffic stations can be rerouted to stations with higher traffic or serve as backup trains in the event of maintenance or when trains are out of service.

## Data set
A Turnstile data set of 3 months long will be obtained from the [MTA website](http://web.mta.info/developers/turnstile.html) and pdf files of 
the train [schedules](https://new.mta.info/schedules).

## Tools
* I will be using SQL to download and store the data in the database. 
* Data will be analyzed with Pandas and visualized with Seaborn and Matplotlib.




