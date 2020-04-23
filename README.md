# Disasters-pipeline-project

This repo contains project Disaster pipeline as a part of udacity  Data science nanodegree 

## Table of Contents.

1. [Project Motivation](#motivation)
2. [Libraries and Installation](#lib)
3. [File Descriptions](#files)
4. [Dataset](#data)
5. [Instructions](#instructions)
6. [Licensing](#lis)

### Project Motivation:<a name="motivation"></a>

I applied the data pipeline skills learned to analyze disaster data from Figure Eight to build a model for an API that classifies disaster messages. I built a machine learning pipeline to categorize emergency messages based on the needs communicated by the sender.


### Libraries and Installation:<a name="lib"></a>

This project requires Python 3.x and the following Python libraries installed:

- [Numpy](https://numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [Seaborn](https://seaborn.pydata.org/)
- [Scikit-learn](http://scikit-learn.org/stable/_)
- [matplotlib](http://matplotlib.org/)
- [Collections](https://docs.python.org/2/library/collections.html)
- [NLTK](https://www.nltk.org/)
- [sqlalchemy](https://www.sqlalchemy.org/)
- [re](https://docs.python.org/3/library/re.html)
- [pickle](https://docs.python.org/3/library/pickle.html)

### File Descriptions:<a name="files"></a> 

`process_data.py`: A ETL Pipeline that:

- loads the `messages` and `categories datasets`
- merges the two datasets
- cleans the data
- stores it in a SQLite database

`train_classifier.py`: A Machine Learning Pipeline that

- loads data from the SQLite database
- splits the dataset into training and test sets
- builds a text processing and machine learning pipeline
- trains and tunes a model using GridSearchCV
- outputs results on the test set
- exports the final model as a pickle file

`run.py`: A Flask Web App that visualizes the results


### Dataset:<a name="data"></a>

In this project we have **Two** datasets from which are posted by **Figure-eight company**

- **disaster_messages.csv** which contain different messages from different disaster messages sent by people in region of a natural disaster
- **disaster_categories.csv** which clarify categories of these disasters messages


### Instructions:<a name="instructions"></a>
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/


### Licensing:<a name="lis"></a>

This project is apart of Udacity's Data Science Nanodegree Program, which provides initial starter code for the project. Additionally, the original datasets are provided in part by FigureEight.