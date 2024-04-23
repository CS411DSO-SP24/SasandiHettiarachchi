# SasandiHettiarachchi

# please replace the usernames, passwords, urls of the databases with your local credential before running the app
# after executing the cell with the implementation of the dashboard, right-click and select "View Frame Source" to access the URL for the app 

Title: 
Keyword-based analysis of the Academic World database

Purpose: 
  This application provides functionalities to the users to analyze publications, faculty members, universities by keywords of their interest. The users can select their choice of comparison metric. As an example, the publications can be ordered either by the number of citations or the keyword score associated with each publication. Faculty members can be ranked by the keyword associated with the, the total number of citations or the total keyword score of their publications that contains the given keyword. Similarly, universities can be ranked by the combined keyword score of their faculty members, combined number of citations or keyword scores of publications with the given keyword published by their faculty. This can be beneficial for students to identify the best publications to look for, best universities to apply for, and best faculty to reach out when starting to study a new topic. Researchers can also be benefited by this feature because they can identify potential collaborators and potential universities as well as good publications for reference when planning new research.
  The users can also view the trends of how popular the keywords over the course of time. This is calculated by the total number of citations of publications with given keyword in each year. The users can also view top keywords that are related to their keyword of interest, which is ranked by the total number of simultaneous occurrences in publications. If someone is exploring multiple new fields to chose from either to study or research, this feature comes in hand.
  Another feature of this application is to create a list of saved publications, which can be used to create bookmarks to publications of interest for future reference. Users can also delete publications from the saved list if they no longer need those publications. This can be helpful to anyone in academics since it saves them from the burden of browsing through the database each time they want the interested publication. On top of that users of this application can add keywords of their choice to the already existing publications in the databse if they feel like that publications covers the topic area of the keyword. This provides a customized experience allowing users to categorize publications as required.

Demo: 
https://mediaspace.illinois.edu/media/t/1_nj9ef8xq

Installation: 
The given datasets in mySQL, mongodb, and Neo4j are used in this application; hence no additional data installation is required.

Usage:
  It is recommended to run the .ipynb file in the repository using jupyter notebook. Replace the placeholders for the passwords of the databases with the passwords used in your local machine databases.

Design: 
  The backend funtions were implemented using python. To create the User Interface of the application, dash by plotly was used, which does not require an addtional API. The UI changes the outputs dynamically real-time as the user inputs data. There are main 6 components in the UI with seven different functionalities where two of them output data in the format of graphs.

Implementation:
  Python was used as the main programming tool for backend developments. The libraries mysql.connector, pymongo, and neo4j were used to access databases. For the implementation of the UI, dash library was used mainly along with plotly.express, json, pandas, and dash_bootstrap_components.

Database Techniques: 
Three database management systems have been used to implement the components; namely, mySQL, mongoDB, and Neo4j which use relational model, document model, and the graph model respectively.
When it comes to the mySQL database, 
  * Views have been created to simplify the query expressions in joins. 
  * Procedures have been created to calculate and output the best publications and top related keywords for the keyword of interest.       * Prepared Statements have been used for every query in order to prevent sql injection since all components of the dashboard take user     inputs to produce outputs.

Extra-Credit Capabilities: 
In the backend functions which serves the component of adding keywords to an already existing database, before adding the keyword, it is checked whether publication already exists and if so, whether it already has the keyword in it. If the publication exists, it also checks whether the keyword already exists in the database. If not, a new keyword entry is created and then added to the publication, and if the keyword is already in the database, the relationship is created straightforward. This part is queried using both mySQL and Neo4j to manipulate both databases (multi-database querying). 

Contributions: 
Single-member team
