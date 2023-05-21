
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


Goal of the project is to answer this question:
How do annual members and casual riders use Cyclistic bikes
differently?

You will produce a report with the following deliverables:
1. A clear statement of the business task
2. A description of all data sources used
3. Documentation of any cleaning or manipulation of data
4. A summary of your analysis
5. Supporting visualizations and key findings
6. Your top three recommendations based on your analysis


  

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
1. I began by adding 2 additional columns to all the months: <br/>
    - ride_length <br/>
    - day_of_week <br/>
  
  a. ride_length was calculated by subtracting the ended_at column by the started_at columnm. <br/>
    - This was then formatted as a time value <br/>
    
  b. day_of_week was calculated using the WEEKDAY function with the started_at column. <br/>
    - This function was then nested in a TEXT function to format it to show the weekday instead of an integer
