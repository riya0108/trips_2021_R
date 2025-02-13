# trips_2021_R
Built-in R Studio

You are a junior data analyst on the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into yearly members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations.

I first analyzed the data separately (each month) in Excel, then used R to analyze the data as a whole (one year). Finally, I created a dashboard in Tableau.
I initially wanted to gather and analyze my data in Excel because it was the tool I was most familiar with and I could get a general understanding of the data quicker. I did not combine all of the spreadsheets into one because that would've taken more processing power than my computer had.  Then I went in to work with Google BigQuery but couldn't figure out how to utilize the Google Cloud Platform.

I began downloading the 12-month data for the year 2021.

Load all of the libraries I used: tidyverse, lubridate, hms, data.table 
Uploaded all of the original data from the data source divytrip into R using read_csv function to upload all individual csv files and save them in separate data frames.

Merged the 12 months of data using rbind to create a one year view.

Created a new data frame called trips that would contain all of my new columns 

### Created new columns for:

- Ride Length - did this by subtracting end_at time from start_at time
- Day of the Week 
- Month 
- Day 

- Time - convert the time to HH: MM: SS format
- Hour 

- Season - Spring, Summer, Winter or Fall

- Time of Day - Night, Morning, Afternoon or Evening

### Cleaned the data by:

Removing duplicate rows
Remove rows with NA values (blank rows)
Remove where ride_length is 0 or negative (ride_length should be a positive number)
Remove unnecessary columns: ride_id, start_station_id, end_station_id, start_lat, start_long, end_lat, end_lng

### Calculated Total Rides for:

Total number of rides which was just the row count = 4,152,139 <br>
Member type - casual riders vs. annual members <br>
Type of Bike - classic vs docked vs electric; separated by member type and total rides for each bike type <br>
Hour - separated by member type and total rides for each hour in a day <br>
Time of Day - separated by member type and total rides for each time of day (morning, afternoon, evening, night) <br>
Day of the Week - separated by member type and total rides for each day of the week <br>
Day of the Month - separated by member type and total rides for each day of the month <br>
Month - separated by member type and total rides for each month <br>
Season - separated by member type and total rides for each season (spring,  summer, fall, winter) <br>

### Calculated Average Ride Length for:

Total average ride length <br>
Member type - casual riders vs. annual members  <br>
Type of Bike - separated by member type and average ride length for each bike type <br>
Hour - separated by member type and average ride length for each hour in a day <br>
Time of Day - separated by member type and average ride length for each time of day (morning, afternoon, evening, night) <br>
Day of the Week - separated by member type and average ride length for each day of the week <br>
Day of the Month - separated by member type and average ride length for each day of the month <br>
Month - separated by member type and average ride length for each month <br>
Season - separated by member type and average ride lengths for each season (spring,  summer, fall, winter) <br>

### Created Dashboard in Tableau

Merging all the individual sheets created by using the exported CSV file from R studio. <br>

![trips_data_2021-ezgif com-speed](https://github.com/user-attachments/assets/4e2ea5ab-4a38-4b5f-bcf3-c76fdbfabc3e)


### Final Summary
- The most popular bike among riders was the classic. <br>
- The busiest time was the afternoon for both casual riders and members.  <br>
- The busiest weekday was Saturday, and casual riders used the service the most on the weekends.  <br>
- The busiest season was Summer for both types of riders.  <br>
- The average ride length was 13.18 minutes for members and 32.51 minutes for casual riders.  <br>

### BUSINESS SUGGESTIONS
This was the hardest part for me for the whole project. I have never provided suggestions for a business nor worked in marketing. <br>
- Have more kinds of passes to avail, like weekly, monthly, or weekends.
- Personalize discounts and show perks in the membership program based on their preferences and riding habits.
- Emphasize the benefits of memberships, including discounts during busy times of the year like during Summer, or on the weekends. 
- Have existing members share their stories about how using Cyclistic's system has changed their lives, to create a sense of community,and  offer a discount if they do so this will help encourage new riders to join the program. 
