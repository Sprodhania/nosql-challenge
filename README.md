Part 1: Database and Jupyter Notebook Set Up

Include the mongoimport command text you used to import establishments.json in a markdown cell at the beginning of your Jupyter notebook file

The mongoimport command text correctly drops any existing establishments collection before importing establishments.json into MongoDB

The database is named uk_food and the collection is named establishments

Correctly imports PyMongo and Pretty Print

An instance of the Mongo Client is created

Lists the databases you have in Mongo, which includes uk_food

Lists the collection(s) in the uk_food database, which includes establishments in the output

Uses find_one() and pprint to display one document in the establishments collection

The establishments collection is assigned to a variable

Part 2: Update the Database

The supplied data for the "Penang Flavours" restaurant is correctly inserted into the establishments collection

A query is performed to find the BusinessTypeID for "Restaurant/Cafe/Canteen" and returns only the BusinessTypeID and BusinessType fields

The "Penang Flavours" document is updated with the correct value for BusinessTypeID

A query is correctly performed to delete all the documents in the collection where "Dover Local Authority" is the value for LocalAuthorityName

A count_documents() check is performed before and after the removal of the Dover documents to ensure the documents were removed

An update_many() query is performed to convert the latitude and longitude fields from strings to decimal numbers and RatingValue to integers

Part 3: Exploratory Analysis

Use NoSQL_analysis_starter.ipynb for this section of the challenge.

Some notes to be aware of while you are exploring the dataset:

RatingValue refers to the overall rating decided by the Food Authority and ranges from 1-5. The higher the value, the better the rating.

Note: This field also includes non-numeric values such as 'Pass', where 'Pass' means that the establishment passed their inspection but isn't given a number rating. We will coerce non-numeric values to nulls during the database setup before converting ratings to integers.

The scores for Hygiene, Structural, and ConfidenceInManagement work in reverse. This means, the higher the value, the worse the establishment is in these areas.

Use the following questions to explore the database, and find the answers, so you can provide them to the magazine editors.

Unless otherwise stated, for each question:

Use count_documents to display the number of documents contained in the result.

Display the first document in the results using pprint.

Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.

Which establishments have a hygiene score equal to 20?

Which establishments in London have a RatingValue greater than or equal to 4?

Hint: The London Local Authority has a longer name than "London" so you will need to use $regex as part of your search.

What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

Hint: You will need to compare the geocode to find the nearest locations. Search within 0.01 degree on either side of the latitude and longitude.

How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

Hint: You will need to use the aggregation method to answer this.

(instructions source : courses.bootcampspot.com) Link : courses
