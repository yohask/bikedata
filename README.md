
# Google Data Analytics Capstone Project
Data retrieved from https://divvy-tripdata.s3.amazonaws.com/index.html 

## About the company
In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that
are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and
returned to any other station in the system anytime.

Our company has been tasked to: Design marketing strategies aimed at converting casual riders into annual members. In order to
do that, however, the marketing analyst team needs to better understand how annual members and casual riders differ, why
casual riders would buy a membership, and how digital media could affect their marketing tactics. To do this our comapny is
analyzing the Cyclistic historical bike trip data to identify trends.


## Goal of the project is to answer this question:
How do annual members and casual riders use Cyclistic bikes
differently?

You will produce a report with the following deliverables:
1. A clear statement of the business task
2. A description of all data sources used
3. Documentation of any cleaning or manipulation of data
4. A summary of your analysis
5. Supporting visualizations and key findings
6. Your top three recommendations based on your analysis <br/>


  

# Process
By using and applying the steps taught within the course we can produce these deliverables

## 1. Ask - Identify the business task based on the question we were given.

   * Find data and trends from historic data to create a marketing strategy to convert casual riders to annual members.


## 2. Prepare - Retrieve relavent data and organize accordingly
 
   Downloaded the data for the previous year from https://divvy-tripdata.s3.amazonaws.com/index.html
   April 2022 - April 2023.
   Sorted and organized into folders for ease of viewing and access.
   Created a backup for the originals.

## 3. Process - Process and prepare the data for analysis

  For this section I wanted to do use both Excel and R.
  Excel would demonstrate cleaning as well as utilization of visualization tools and pivot tables.
  R would show programming skills as well as getting it ready for visulization tools such as Tableau.

### Excel
#### 1. I began by adding 2 additional columns to all the months: <br/>
    - ride_length
    - day_of_week
  
  a. ride_length was calculated by subtracting the ended_at column by the started_at columnm. <br/>
      - This was then formatted as a time value <br/>
    
  b. day_of_week was calculated using the WEEKDAY function with the started_at column. <br/>
      - This function was then nested in a TEXT function to format it to show the weekday instead of an integer <br/>
      
#### 2. Came up with metrics to answer the business task at hand.<br/>
    - total number of rides per weekday
    - Average length of rides per weekday by the member types
    - Rides per hour
    - Rides per day
    - Rides by bike type
    
#### 3. For every month I created pivot tables and charts according to the metrics above.
  [Refer to Excel Release for the files mentioned](https://github.com/yohask/bikedata/releases/tag/v1)

### R
#### Refer to the 2 code files for actual code </br>
[Data cleaning/analysis in R](https://github.com/yohask/bikedata/blob/main/Code%20to%20transform%20data%20in%20R.txt) <br/>
[Data cleaning and prep for Tableau](https://github.com/yohask/bikedata/blob/main/Prep%20Data%20for%20Tableau.txt) <br/>

  1. Loaded libraries that will be used. <br/>

    - tidyverse
    - lubridate
    - hms
    - data. table

  2. Uploaded the data from the Prepare step and saved them as seperate data frames.
  3. Merged all the files into one to create a year view.<br/>
  
  4. Created a new data frame from the year view called last_annum.
  5. Created new columns for: <br/>

    - ride_length
    - day_of_week
    - month
    - year
    - time - converted into HH:MM:SS
    - Hour
    - Season (Fall, Winter, Summer, Spring)
    - time_of_day (Morning, Afternoon, Evening, Night)

  6. Cleaned the data: <br/>

    - Omitted any NA value data
    - Removed duplicate rows
    - Removed negative ride times or 0's

  7. Calculated total rides for: <br/>

    - Last cycle year
    - Last cycle year by member type
    - By every hour
    - By times of day per member type
    - By season per member type

  8. Calculated average rides for: <br/>

    - Ride time by member type
    - Ride time per hour by member type
    - Ride time per time of day by member type
    - Ride time per weekday by member type
    - Ride time per day of month by member type
    - Ride time per month by member type
    - Ride time per season by member type
    
  9. Created another R code for analyzing the data to put into Tableau for visualizations and dashboards.

    - Transformations were kept the same
    - Exported the data into a .csv file to upload


## 4. Share - Creating visulizations
For this section I had already done the visualizations in the workbooks for Excel so this will focus on the R code that was uploaded to Tableau.

### R
For the R code it was kept the same for the transformation of the data, but this time I kept the starting and ending latitudes and longitudes. I then converted the data frame into a CSV file to be used in Tableau. <br />

### Tableau
[Link to Tableau Dashboard](https://public.tableau.com/app/profile/hunter.su5538/viz/GoogleDataAnalyticsCapstone_16852832168870/Dashboard1)

## 5. Act - Final Conclusions
Back to answering the business task that we determined at the beginning: <br/>

  - Find data and trends from historic data to create a marketing strategy to convert casual riders to annual members. <br/>
  
  Through my analysis I found that these would be the best steps for this:
-  Launch marketing campaigns around the busiest times of the year - July and August.
- Increase the amount of bike stations to more neighbourhoods to introduce Cyclistic as a form of transportation.
- Introduce lower prices for popular bike stations.

# Conclusion
This was a very rewarding experience to go through as I got to learn about all parts of data analytics and got hands on experience with coding and creating visualizations.
### Next steps: 
I still beleive that I have a great deal to learn:
- Data visualizations need to be improved.
  - Experiment with colour palletes
  - Create better looking dashboards
  - More exposure needed
- Code needs to be more optimized.

