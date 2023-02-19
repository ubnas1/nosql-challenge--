# nosql-challenge--

## Setup
I created a new database and collection using command line.

I used the data provided in json format and imported that using command line.

The code to create the database and importing the data is below.

 ## Code
 mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json
 
 After doing the above mentioned steps, next process was to enter a new document of a restaurant. And then check if it has been inserted.
 
 Next, I deleted all the establishments in Dover area.
 
 Then I changed the data types of coordinates from string to double.
 
 ## Exploratory Analysis
 
 For Analysis, first step is finding establishments that have a hygiene score equal to 20
 
 Then I used regex and collections.find() to locate establishments in London that have a RatingValue greater than or equal to 4
 
 As next step,  wrote a query to find and sort establishments which are closer to Penang Flavours restaurants and Rating of 5 and sorted by hygiene score.
 
 ## Data Pipeline
 
 The most complex part was to group restaurants by Local Authority Name, then finding establishments with hygiene score of 0 and then sorting by establishment count in each local authority. For this part, I made a data pipeline and used aggregate method.
 
 Finally, I made a Pandas Dataframe from the above mentioned results.
