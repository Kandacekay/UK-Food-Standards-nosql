# UK Food Standards Analysis Overview

The analysis of food hygiene ratings from the UK Food Standards Agency was conducted to support the editorial decisions of the "Eat Safe, Love" food magazine. MongoDB and Jupyter Notebook were employed for this purpose.

## Part 1: Database and Jupyter Notebook Set Up
### Importing Data:
The establishments.json file was imported into MongoDB using the mongoimport terminal command, establishing the "uk_food" database and the "establishments" collection.

### Setting Up MongoDB and Jupyter Notebook:
The Jupyter Notebook setup involved creating a MongoDB client, accessing the uk_food database, and initializing the establishments collection for subsequent analysis.

## Part 2: Updating the Database
### Add New Restaurant:
The database was updated with a new restaurant, "Penang Flavours," using Python code to insert relevant details into the establishments collection.

### Find and Update BusinessTypeID:
The BusinessTypeID for "Restaurant/Cafe/Canteen" was identified and associated with the new restaurant entry by updating its BusinessTypeID field.

### Remove Establishments in Dover:
Establishments in Dover were identified, removed from the database, and the count of documents before and after removal was verified.

### Convert Data Types:
Data types for latitude, longitude, and RatingValue were adjusted. Latitude and longitude were converted to decimal numbers, and RatingValue was converted to integers using the 'update_many' method.

These steps collectively contribute to a well-organized and updated database, facilitating meaningful analysis for "Eat Safe, Love" magazine articles.

## Part 3: Exploratory Analysis
1. Establishments with Hygiene Score of 20
- <b>Query:</b> Find establishments with a hygiene score of 20.
- <b>Results:</b>
   - Number of establishments with a hygiene score of 20: 41
   - Example Establishment:
      - <b>Name:</b> The Chase Rest Home
      -  <b>Address:</b> 5-6 Southfields Road, Eastbourne, East Sussex, BN21 1BU
      -  <b>Hygiene Score:</b> 20
- <b>Analysis:</b>
   - There are 41 establishments with a hygiene score of 20.
   - The example establishment, "The Chase Rest Home," is located in Eastbourne, East Sussex.
2. Establishments in London with RatingValue >= 4
- <b>Query:</b> Find establishments in London with a RatingValue greater than or equal to 4.
- <b>Results:</b>
   - Number of establishments in London with RatingValue >= 4: 34
   - Example Establishment:
        - <b>Name:</b> Charlie's
        - <b>Address:</b> Oak Apple Farm Building 103 Sheerness Docks, Sheppy Kent, ME12
        -  <b>RatingValue:</b> 4
- <b>Analysis:</b>
   - There are 34 establishments in London with a RatingValue greater than or equal to 4.
   - Example establishment, "Charlie's," is located in Sheerness Docks, Sheppy Kent.
3. Top 5 Establishments with RatingValue of 5, Sorted by Hygiene Score, Near "Penang Flavours"
- <b>Query:</b> Find the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to "Penang Flavours."
- <b>Results:</b>
   - <b>Establishment 1:</b>
      - <b>Name:</b> Volunteer
      - <b>Address:</b> 130-132 Plumstead High Street, Plumstead, Greenwich, SE18 1JQ
      - <b>Hygiene Score:</b> 0
  - <b>Establishment 2:</b>
     - <b>Name:</b> Plumstead Manor Nursery
     - <b>Address:</b> Plumstead Manor School Old Mill Road, Plumstead, Greenwich, SE18 1QG
     - <b>Hygiene Score:</b> 0
   - <b>Establishment 3:
     - <b>Name:</b> Atlantic Fish Bar
     - <b>Address:</b> 35 Lakedale Road, Plumstead, Greenwich, SE18 1PR
     - <b>Hygiene Score: 0</b>
   - <b>Establishment 4:
     - <b>Name:</b> Iceland
     - <b>Address:</b> 144-146 Plumstead High Street, Plumstead, Greenwich, SE18 1JQ
     - <b>Hygiene Score:</b> 0
   - Establishment 5:
     - <b>Name:</b> Howe and Co Fish and Chips - Van 17
     - <b>Address:</b> Restaurant And Premises 107A Plumstead High Street, Plumstead, Greenwich, SE18 1SE
     - <b>Hygiene Score:</b> 0
- <b>Analysis:</b>
   - The top 5 establishments with a RatingValue of 5, sorted by the lowest hygiene score, are all located in Plumstead, Greenwich, near "Penang Flavours."
   - These establishments have a hygiene score of 0.

## Summary:
- There are 41 establishments with a hygiene score of 20.
- In London, there are 34 establishments with a RatingValue greater than or equal to 4.
- The top 5 establishments with a RatingValue of 5, sorted by the lowest hygiene score, are all located in Plumstead, Greenwich, near "Penang Flavours," with a hygiene score of 0.
