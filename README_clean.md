
 UK Food Hygiene Ratings  Challenge

This repository contains the solution for Challenge analysing UK Food Standards Agency foodhygiene data with MongoDB and PyMongo

 Contents

 File  Purpose 

 establishmentsjson  Raw data set from the FSA used to seed MongoDB 
 NoSQLsetupstarteripynb  Notebook for importing the data cleaning it and applying required database updates 
 NoSQLanalysisstarteripynb  Notebook for answering the four exploratoryanalysis questions 
 READMEmd  Youre reading it  project overview and run instructions 

 Prerequisites

 MongoDB running locally on the default port 
 Python
 Packages pymongo pandas jupyter or VSCode with the Jupyter extension

Install Python dependencies

bash
pip install pymongo pandas jupyter


 Database setup

In a terminal from the project folder run

bash
mongoimport drop   db ukfood   collection establishments   file establishmentsjson   jsonArray


This creates the ukfood database and the establishments collection k docs

 Notebooks

 NoSQLsetupstarteripynb

 Connect imports PyMongo creates MongoClient
 Verification lists DBs  collections prints a sample document
 Updates
    Inserts the new restaurant PenangFlavours
    Retrieves the correct BusinessTypeID and updates the doc
    Removes all Dover records
    Converts geocodelongitude geocodelatitude to double and RatingValue to int

 NoSQLanalysisstarteripynb

Answers the editors questions

   Query  Expected count 

   Hygiene score   
   London establishments with RatingValue   
    nearest establishments rating to PenangFlavours sorted by hygiene   
   Authorities with hygiene score ranked  dynamic 

Each section prints

 countdocuments result  
 first documents with pprint  
 DataFrame size and head

 Running everything

 Launch Jupyter or VSCode
 Open NoSQLsetupstarteripynb  KernelRestart  RunAll No errors should appear
 Open NoSQLanalysisstarteripynb  KernelRestart  RunAll Validate the counts above

 Author

Prepared for the editors of EatSafe Love

