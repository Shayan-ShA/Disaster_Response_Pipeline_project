# Disaster_Response_Pipeline_project-Udacity_Data_Science
<h2>Overview</h2>
In this project, I analyze disasterd the data from Figure Eight to build a model for an API that classifies disaster messages. The data set contains real messages that were sent during disaster events. A machine learning pipeline is created to categorize these events so that one can send the messages to an appropriate disaster relief agency.
The project also includes a flask web app where an emergency worker can input a new message and get classification results in several categories.

<h2>File Descriptions</h2>
  -<b>process_data.py</b>: The ETL script, process_data.py, runs in the terminal without errors. The script takes the file paths of the two datasets and database, cleans the datasets, and stores the clean data into a SQLite database in the specified database file path.
  -<b>train_classifier.py</b>: The machine learning script, train_classifier.py, runs in the terminal without errors. The script takes the database file path and model file path, creates and trains a classifier, and stores the classifier into a pickle file to the specified model file path.
  -<b>run.py</b>: The web app, run.py, runs in the terminal without errors. The main page includes at least two visualizations using data from the SQLite database.

<h2>How to Run</h2>
  1. Create a virtual environment in python, activate it and put all the files in this repository inside it.
  2. Create a SQLite database named DisasterResponse.db in the file data by running the code below.
      python process_data.py disaster_messages.csv disaster_categories.csv DisasterResponse.db  
  3. Then create a pickle file containing the classifier trained by running the command below in models file.
      python train_classifier.py ../data/DisasterResponse.db classifier.pkl
  4. Run the command below in app file.
      python run.py
  5. In a browser window, type in the link provided as a result of running run.py 
