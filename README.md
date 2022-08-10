# NYC_CitiBike
## Overview of Project
Now that we've gotten an honest idea of the way to create our story, there's still some more work to be done to convince investors that a bike-sharing program in Des Moines may be a solid business proposal. To solidify the proposal, one among the key stakeholders would really like to ascertain a motorcycle trip analysis. 
For this analysis, you’ll use Pandas to vary the "tripduration" column from an integer to a datetime datatype. 
Then, using the converted datatype, you’ll create a group of visualizations to: 
- Show the length of your time that bikes are verified for all riders and genders 
- Show the amount of motorcycle trips for all riders and genders for every hour of every day of the week 
- Show the amount of motorcycle trips for every sort of user and gender for every day of the week. 
Finally, you’ll add these new visualizations to the 2 you created during this module for your final presentation and analysis to pitch to investors.

1. ***Deliverable 1***: Change Trip Duration to a Datetime Format
2. ***Deliverable 2***: Create Visualizations for the Trip Analysis
3. ***Deliverable 3***: Create a Story and Report for the Final Presentation
4. **Extra**: A written report on Des Moines - Bike Sharing Project Analysis 

## Resources and Before Start Notes:

* Data Source: `NYC_CitiBike_Challenge_starter_code.ipynb`, `NYC_Citibike_Challenge.ipynb` and `201908-citibike-tripdata.csv`
* Data Tools: Jupyter Notebook, CSV, Tableau and IO (Web Server)
* Software: Jupyter Notebook and Visual Studio Code 

For more information, visit [`Tableau website`](https://public.tableau.com/en-us/s/). 


## Download Tableau Public
First, go to the [`Tableau website`](https://public.tableau.com/en-us/s/) and enter your email. You will also be required to enter some contact information, but you can always unsubscribe from communications.

## Install Tableau Public
Once you have downloaded Tableau Public, we can start the process of installing Tableau Public. The process of installing Tableau Public is very similar to installing most other programs.

After it's finished downloading, click to open the file and then follow the on-screen instructions. This is the first screen you will see as part of the installation. Go ahead and click "Continue."


Once you click "Continue," you should see the following screen. Click "Install."


This process may take a few minutes. 


When the installation is complete, you will see a window confirming that the software was installed successfully:


Now that Tableau is installed, let's get started with downloading the data we'll need.



> Let's move on!

# Deliverable 1:  
## Change Trip Duration to a Datetime Format
### Deliverable Requirements:
Using Python and Pandas functions, you’ll convert the "tripduration" column from an integer to a datetime datatype to get the time in hours, minutes, and seconds (00:00:00). After you convert the "tripduration" column to a datetime dataytpe, you’ll export the DataFrame as a CSV file to use for the trip analysis in Deliverable 2




1. The data in the "tripduration" column is converted to a datetime datatype and has the correct time format.
2. The DataFrame is exported as a new file without the index column.

 
### Results with detail analysis:

1. **The data in the "tripduration" column is converted to a datetime datatype and has the correct time format.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

**Code and Image**


````py
# CHALLENGE 14


import pandas as pd

# 1. Create a DataFrame for the 201908-citibike-tripdata data. 
citibike_data = "201908-citibike-tripdata.csv"
citibike_df = pd.read_csv(citibike_data)

# 2. Check the datatypes of your columns. 
citibike_df.info()

# 3. Convert the 'tripduration' column to datetime datatype.
citibike_df['tripdur_orig'] = citibike_df['tripduration']
citibike_df['tripduration'] = pd.to_datetime(citibike_df['tripduration'], unit='m')
citibike_df.head()

# 4. Check the datatypes of your columns. 
citibike_df.info()
````



2. **The DataFrame is exported as a new file without the index column.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

**Code and Image**


````py
# 5. Export the Dataframe as a new CSV file without the index.
citibike_df.to_csv('citibike_201908_updt.csv', index=False)

# Challenge 14
````


# Deliverable 2:  
## Create Visualizations for the Trip Analysis
### Deliverable Requirements:
Using Tableau, create visualizations that show:

  - How long bikes are checked out for all riders and genders.
  - How many trips are taken by the hour for each day of the week, for all riders and genders.
  - A breakdown of what days of the week a user might be more likely to check out a bike, by type of user and gender.

### Create the Checkout Times for Users Viz
In this visualization, you’ll graph the length of time that bikes are checked out for all riders.

Your final results should look similar to the following image:




### Create the Checkout Times by Gender Viz
In this visualization, you’ll graph the length of time that bikes are checked out for each gender.

Your final results should look similar to the following image:


### Create the Trips by Weekday for Each Hour Viz
In this visualization, you’ll graph the number of bike trips by weekday for each hour of the day as a heatmap.

Your final results should look similar to the following image:


### Create the Trips by Gender (Weekday per Hour) Viz
In this visualization, you’ll graph the number of bike trips by gender for each hour of each day of the week as a heatmap.



### Create the User Trips by Gender by Weekday Viz
In this visualization, you’ll graph the number of bike trips by gender for each hour for each day of the week as a heatmap.



### Deliverable 2 Requirements:
You will earn a perfect score for Deliverable 2 by completing all requirements below:

1. There is a line graph displaying the number of bikes checked out by duration for all users, and the graph can be filtered by the hour.
2. There is a line graph displaying the number of bikes that are checked out by duration for each gender by the hour, and the graph can be filtered by the hour and gender.
3. A heatmap is created showing the number of bike trips for each hour of each day of the week.
4. A heatmap is created showing the number of bike trips by gender for each hour of each day of the week, and the heatmap can be filtered by gender.
5. A heatmap is created showing the number of bike trips for each type of user and gender for each day of the week, and you can only filter by user and gender.

 
### Results with detail analysis:

1. **There is a line graph displaying the number of bikes checked out by duration for all users, and the graph can be filtered by the hour.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

**Code and Image**


````js

// Module 14

````




2. **There is a line graph displaying the number of bikes that are checked out by duration for each gender by the hour, and the graph can be filtered by the hour and gender.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

**Code and Image**


````js

// Module 14

````



3. **A heatmap is created showing the number of bike trips for each hour of each day of the week.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

**Code and Image**


````js

// Module 14

````


4. **A heatmap is created showing the number of bike trips by gender for each hour of each day of the week, and the heatmap can be filtered by gender.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

**Code and Image**


````js

// Module 14

````


5. **A heatmap is created showing the number of bike trips for each type of user and gender for each day of the week, and you can only filter by user and gender.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

**Code and Image**


````js

// Module 14

````


# Deliverable 3:  
## Create a Story and Report for the Final Presentation
### Deliverable Requirements:
For this part of the Challenge, you’ll create a story in Tableau and write a report that describes the key outcomes of the NYC Citibike analysis you did in the module and in Deliverable 2.

Follow the instructions below to complete Deliverable 2.

In Tableau, create a new Story using visualizations that will support the key findings you want to show.

1. You must use the five visualizations that you created in Deliverable 2.

> TABLEAU DASHBOARDS:



>TABLEAU PUBLIC URL:



2. You must use at least two visualizations that you created in this module.



3. In your README markdown file, include the following:
  **Overview of the analysis:**, **Results:** & **Summary:** 
  
  - CitiBike Analysis tells that more than 80% are Subscribers, with an ~19% or regular non-subscribers, that data creates a new need, such better user experiance interaction in the future.



  - Total of 65% General Male use, 25% General Female with an Unknown gender that relies on non-subscribers users. In addition, Peak by Gener spike on same time frame, and Top 10 Start and Ending locations are on same zone (that's really good!)


  - Inventory Use and Maintenance may be an issue in the future, locations are different time to time.


>TABLEAU PUBLIC URL:

 [`Final Data Analysis - Aug 2019`](https://public.tableau.com/views/Des-Moines-Bike-Sharing/FINALSTORYREPORT?:language=en&:display_count=y&publish=yes&:origin=viz_share_link). 

>DES MOINES BIKE SHARING PROJECT - Readme:
