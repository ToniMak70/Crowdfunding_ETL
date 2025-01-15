# Project 2 
# Crowdfunding_ETL
    ___________________________________________
    Overview
    The Crowdfunding_ETL project is an ETL (Extract, Transform, Load) pipeline focused on processing crowdfunding data. The goal is to extract data from the provided crowdfunding.xlsx and contacts.xlsx Excel files, transform it into appropriate formats using Python and Pandas, and then load it into a PostgreSQL database. The project also includes designing an ERD (Entity Relationship Diagram), creating a table schema, and verifying the correctness of the imported data.
    This project aims to provide hands-on experience in data extraction, transformation, database design, and Postgres database management.
        Key Files:
        1.	category.csv - Contains category data.
        2.	subcategory.csv - Contains subcategory data.
        3.	campaign.csv - Contains campaign details.
        4.	contacts.csv - Contains contact information.
        5.	crowdfunding_db_schema.sql - SQL script for creating tables in the PostgreSQL database.
        6.	crowdfunding.xlsx - Input data for crowdfunding campaigns.
        7.	contacts.xlsx - Input data for contacts associated with campaigns.
        8.	ERD_Diagram.png - Visual representation of the database schema
        ________________________________________
        Objectives
        •	Extract data from the crowdfunding.xlsx and contacts.xlsx files.
        •	Transform the data into four DataFrames: Category, Subcategory, Campaign, and  Contacts.
        •	Export the DataFrames as CSV files.
        •	Design an ERD and implement a database schema for the CSV data.
        •	Create and populate a PostgreSQL database with the CSV data.
        ________________________________________
        Let's get started
            • Ensure you have the following installed on your system:
                •	Python 3.x
                •	Pandas library (pip install pandas)
                •	PostgreSQL database server
            • Clone the repository to your local machine: [GitHub Link] (https://github.com/ToniMak70/Crowdfunding_ETL.git)
            • Start up jupyter notebook and begin to execute the following commands:
                1. import the dependancies
                2. Read the data into a Pandas DataFrame
                    ![output2] (Crowdfunding_ETL/Images/crowdfunding_info_df.png at main · ToniMak70/Crowdfunding_ETL)
                3. Get a brief summary of the crowdfunding_info DataFrame
                4. Get the crowdfunding_info_df columns
                5. Assign the category and subcategory values to category and subcategory columns
                6. Get the unique categories and subcategories in separate lists
                7. Get the number of distinct values in the categories and subcategories lists
                8. Create numpy arrays from 1-9 for the categories and 1-24 for the subcategories
                9. Use a list comprehension to add "cat" to each category_id and Use a list comprehension to add "subcat" to each subcategory_id
                10. Create a category DataFrame with the category_id array as the category_id and categories list as the category name and Create a category DataFrame with the subcategory_id array as the subcategory_id and subcategories list as the subcategory name
                11. Dislay the category_df
                    ![output11] (Crowdfunding_ETL/Images/category_df.png at main · ToniMak70/Crowdfunding_ETL)
                12. Display the subcategory_df
                    ![output12] (Crowdfunding_ETL/Images/subcategory_df.png at main · ToniMak70/Crowdfunding_ETL)
                13. Export categories_df and subcategories_df as CSV files
                14. Create a copy of the crowdfunding_info_df DataFrame name campaign_df
                    ![output14] (Crowdfunding_ETL/Images/campain_df.png at main · ToniMak70/Crowdfunding_ETL)
                15. Rename the blurb, launched_at, and deadline columns
                16. Convert the goal and pledged columns to a `float` data type
                17. Check the datatypes
                18. Format the launched_date and end_date columns to datetime format
                19. Merge the campaign_df with the category_df on the "category" column and the subcategory_df on the "subcategory" column
                20. Drop unwanted columns
                21. Export the DataFrame as a CSV file
                22. Read the data into a Pandas DataFrame. Use the `header=2` parameter when reading in the data
                23. create the contacts DataFrame ensure to import json then Iterate through the contact_info_df and convert each row to a dictionary, append the converted data, then print out the list of values for each row
                24. Create a contact_info DataFrame and add each list of values, i.e., each row to the 'contact_id', 'name', 'email' columns
                25. Create a contact_info DataFrame and add each list of values, i.e., each row to the 'contact_id', 'name', 'email' columns
                26. Check the datatypes
                27. Create a "first"name" and "last_name" column with the first and last names from the "name" column then drop the contact_name column
                28. Reorder the columns
                    ![output28] (Crowdfunding_ETL/Images/contacts_df_clean.png at main · ToniMak70/Crowdfunding_ETL)
                29. Check the datatypes one more time before exporting as CSV file
                30. Export the DataFrame as a CSV file
             • Open up PostgreSQL database server
                1. create a crowdfunding_db and load in the crowdfunding_db_schema.sql from the repo on your local machine
                2. Import these csv files from the resource folder in the repo on your local machine into the appropriate tables:
                        campaign, category, contacts, and subcategory
                3. Verify the data for each table has has the correct data by using a new query tool and running the following select statements individually:
                    SELECT * FROM campaign;
                    SELECT * FROM category;
                    SELECT * FROM contacts;
                    SELECT * FROM subcategory;
                   
    __________________________________________
    Conclusion
    This project walks through the process of building an ETL pipeline, transforming data, and integrating it into a PostgreSQL database. By following the steps, you will practice working with Python, Pandas, SQL, and database management, while handling real-world crowdfunding data.


# File Submission:
    This assignment includes the following attchments:
      A ipynb file that contains jupyter notebook starter file named ETL_Mini_Project_AMakakoa
      A Resources folder containing csv, xlsx and sql files
      A Database Results folder containing csv files of the database outputs and a png file of an ERD sketch
      A License
      A readme file  


# Acknowledgements
    **Classmates: I recieved coding and debuging help from multiple classmates during breakout sessions.
    **Internet Search: I utilized Google Search and slack overflow to research coding concepts, algorithms, and best practices.
    **Gemini AI: I leveraged Gemini AI to generate code suggestions, debug errors, and provide explanations for complex code segments.
    **Support Staff: I recieved help from my instructor and class TA during office hours for help with debugging errors and further explanation for complex code segments.
    **Please note: While these tools were invaluable in my development process, the final code is the result of my analysis, testing, and refinement.

