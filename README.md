# NoSQL Challenge: UK Food Hygiene Ratings

## Before You Begin
This project involves evaluating food hygiene ratings across various establishments in the UK for the magazine *Eat Safe, Love*. The analysis is based on data provided by the UK Food Standards Agency.

### Repository Setup
1. **Create a new repository** named `nosql-challenge`. Do not add this homework to an existing repository.
2. **Clone the repository** to your computer.
3. **Add your Jupyter notebook starter files** and your `Resources` folder containing `establishments.json` to this folder.
4. **Push the changes to GitHub**.

## Instructions
The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, *Eat Safe, Love*, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

### Part 1: Database and Jupyter Notebook Set Up
Use `NoSQL_setup_starter.ipynb` for this section of the challenge.

1. Import the data provided in the `establishments.json` file from your Terminal. Name the database `uk_food` and the collection `establishments`.
2. Copy the text you used to import your data from your Terminal to a markdown cell in your notebook.
3. Within your notebook, import the libraries you need: `PyMongo` and `Pretty Print (pprint)`.
4. Create an instance of the Mongo Client.
5. Confirm that you created the database and loaded the data properly:
   - List the databases you have in MongoDB. Confirm that `uk_food` is listed.
   - List the collection(s) in the database to ensure that `establishments` is there.
   - Find and display one document in the `establishments` collection using `find_one` and display with `pprint`.
   - Assign the `establishments` collection to a variable to prepare the collection for use.

### Part 2: Update the Database
Use `NoSQL_setup_starter.ipynb` for this section of the challenge.

1. Add a new halal restaurant, **Penang Flavours**, in Greenwich to the database.
2. Find the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and update the new restaurant with this ID.
3. Remove any establishments within the Dover Local Authority from the database.
4. Convert latitude and longitude to decimal numbers, and convert `RatingValue` to integer numbers.

### Part 3: Exploratory Analysis
Use `NoSQL_analysis_starter.ipynb` for this section of the challenge.

1. Explore the dataset to answer the following questions:
   - Which establishments have a hygiene score equal to 20?
   - Which establishments in London have a `RatingValue` greater than or equal to 4?
   - What are the top 5 establishments with a `RatingValue` of 5, sorted by lowest hygiene score, nearest to **Penang Flavours**?
   - How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest.

### Expected Output
The first 5 rows of your resulting DataFrame should look something like this:

| _id      | count |
|----------|-------|
| Thanet   | 1130  |
| Greenwich| 882   |
| Maidstone| 713   |
| Newham   | 711   |
| Swale    | 686   |

## Conclusion
This analysis will help the magazine editors identify establishments with varying hygiene ratings, guiding their future articles and reviews.
