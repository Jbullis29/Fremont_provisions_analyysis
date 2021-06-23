# Fremont Provision Review ETL. Extract, Transform and Load
## Extract
#### A new restaurant named Fremont Provisions just opened up in Canon City Colorado and upon opening they have asked customer to fill out reviews on their experience. The reviews are written by the customer on a review card and manually input into an excel spreadsheet with the format you see below:
![original_review_format](https://user-images.githubusercontent.com/72579469/123179592-f9e0f180-d446-11eb-9198-b570393e75de.JPG)

#### I then take the original format and extract the dat using a for loop to itterate through the rows and many if statements compare the ratings column to the 1 in the review columns and appends that to a list dictonary. this completes the extract phase. 
![Extractin reviews dat](https://user-images.githubusercontent.com/72579469/123180190-07e34200-d448-11eb-9c07-b287aecf8d2a.JPG)

## Transform
#### From here I take the data ansd the comments from two seperate csv file and merge them together to create a transformed data the includes all the ratings and their comments in the same row and save that to a csv in the cleaned foleder save as fp_<date>: 
![Cleaned review post python](https://user-images.githubusercontent.com/72579469/123180454-893ad480-d448-11eb-8506-4ea0ad64fe42.JPG)
#### Before Uploading I run some analysis to store the daily averages and all reviews in a mongoDB:
![Analysis Pre DB](https://user-images.githubusercontent.com/72579469/123180571-c56e3500-d448-11eb-9a35-68aaa1bf570d.JPG)

## Load 
#### I then load my daily averages into a mongoDB called fp_daily_averages:
![Mongo averages DB](https://user-images.githubusercontent.com/72579469/123180671-f3537980-d448-11eb-912a-ab2039d84624.JPG)
#### I also upload all my reviews to a DB called fp_reviews
![Mongo Review DB](https://user-images.githubusercontent.com/72579469/123180816-4d543f00-d449-11eb-8fe1-bfee33479c5f.JPG)

## Query and Visualize
#### This is still a work in progress but from here I will query the DBs into python where I want to create graphs and dataframes to present to restaurant owners:
![Pythonn Mongo DB Query](https://user-images.githubusercontent.com/72579469/123180990-a45a1400-d449-11eb-9bbc-bb46698bb601.JPG)

## All of this will be done to boost customer satifaction and overall restaurant performance
