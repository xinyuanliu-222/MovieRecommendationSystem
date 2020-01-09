# MovieRecommendationSystem

## Overview
I implemented a movie recommender system based on Item Collaborative Filtering using Hadoop MapReduce and Java language.
This recommender Systems helps people find information that may interest them.

## Principle
coOccurence matrix × A user's rating matrix = A user's predicted rating matrix

## Main Steps
### Data Processing
Raw data is from Netflix Prize Challenge

Data preprocess:
* Change the format of data in each movie file into: UserID, MovieID, Rating.
* Merge 17770 movie files into one input file since Hadoop is not good for dealing with lots of small files. And this input file is the input of our recommender system.

### Methods:
* Divide data by user id
* Build co-occurrence matrix
* Normalize the co-occurrence matrix
* Build rating matrix
* Multiply co-occurrence matrix and rating matrix

### Deploy
- args0: original dataset
- args1: output directory for DividerByUser job
- args2: output directory for coOccurrenceMatrixBuilder job
- args3: output directory for Normalize job
- args4: output directory for Multiplication job
- args5: output directory for Sum job
