# An-analysis-on-the-The-GitHub-History-of-the-Scala-Language

##mIntroduction
Scala is a mature programming language that has recently become popular among data scientists. It is a general-purpose programming language that has been in existence for over ten years with almost 30k commits. Scala is also an open source project, meaning that its development history, including code reviews and changes made, are publicly available.

In this project, we aim to analyze the real-world project repository of Scala by reading, cleaning, and visualizing the data from a version control system (Git) and a project hosting site (GitHub). We aim to find out who has had the most impact on the development of Scala and identify the experts in the field.

## Dataset
The dataset used in this project was mined and extracted from GitHub and comprises three files:

* pulls_2011-2013.csv contains the basic information about the pull requests from the end of 2011 up to (but not including) 2014.
* pulls_2014-2018.csv contains the same information as the previous file and spans from 2014 up to 2018.
* pull_files.csv contains the files that were modified by each pull request.
## Data Preparation and Cleaning
The first step in preparing the data is to combine the two pull dataframes into one. The dates in the raw data are in ISO8601 format and are imported as strings by pandas. To make the analysis easier, we need to convert these strings into Python's DateTime objects, which have the property that they can be compared and sorted.

The pull request times are in UTC, while the commit times are in the local time of the author with time zone information. To make comparisons easy, all times are converted to UTC.

Next, the two separate files are merged into one dataframe to make it easier to analyze the data in future tasks.

## Analysis of Project Activity
Before committing to contributing to a project, it is important to understand its state. Is the project still active, or has development slowed down? Has the project been abandoned altogether?

The data used in this project was collected in January 2018. We are interested in the evolution of the number of contributions up to that date. To do this, we will plot a chart of the project's activity by calculating the number of pull requests submitted each (calendar) month during the project's lifetime and plotting these numbers to see the trend of contributions.







