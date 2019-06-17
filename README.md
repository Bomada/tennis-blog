# Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Project Process](#process)
5. [Licensing, Authors, Acknowledgements](#licensing)

# Installation <a name="installation"></a>
The xgboost library is needed to run the code here beyond the Anaconda distribution of Python. The code should run with no issues using Python versions 3. See the requirements.txt file for details about library versions.

# Project Motivation <a name="motivation"></a>
Since I'm both a big tennis fan and data nerd, I've long wanted to know how a machine learning algorithm would cope against the best fantasy tennis players in the world.

# File Descriptions <a name="files"></a>
Input data used:
- **data/tdc/tdc_2018.csv**: Data about the best fantasy tennis player's predictions for 2018. Manually collected data from www.tennisdrawchallenge.com
- **data/atp** (directory): ATP data provided by Jeff Sackmann on https://github.com/JeffSackmann/tennis_atp
- **tennis-blog.ipynb**: Exploratory notebook with all steps necessary to answer the question if a machine could beat the best fantasy tennis player.

# Project Process <a name="process"></a>
When working with this project I followed the CRISP-DM process. The details are found in the notebook but here is a quick summary:

## Business Understanding
To answer the question if a machine learning model could beat the best fantasy tennis player in the world I set out to do four things:
1. Set the rules for a challenge
2. Create a benchmark prediction for the challenge
3. Test how well the best fantasy tennis player performs for the challenge
4. Build a machine learning model and test it on the challenge

## Data Understanding
To be able to answer the question I manually collected data on the best fantasy tennis player from www.tennisdrawchallenge.com. In addition I got ATP tennis data from Jeff Sackmann's Github repository.

## Prepare Data
Before I could build a model many things were done to the data. Columns were modified, new features created, missing values imputed and much more. Before training the model data was split into a training and a test set.

## Data Modeling
First I choose to use accuracy as the metric to evaluate model performance. Next I trained and tested four supervised learning models:
- Logistic Regression
- Gaussian Naive Bayes
- Random Forest
- XGBoost

## Results
Using a XGBoost model I managed to beat the best fantasy tennis player in the world. More details are found in this blog post:
https://medium.com/@marcusnilsson78/can-a-machine-beat-the-best-tennis-player-in-the-world-79112b47f547

## Deploy
Output of this project was a notebook and a blog post so nothing were deployed into production.

# Licensing, Authors, Acknowledgements <a name="licensing"></a>
## Code
Copyright 2019 Marcus Nilsson

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Data
Give credit to www.tennisdrawchallenge.com for the fantasy tennis data and letting me use screenshots of their site for the blog post.

For the ATP data I must give a huge thank you to Jeff Sackmann. He has provided free high quality tennis data for years. The ATP data from Jeff comes with the following license:

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/Dataset" property="dct:title" rel="dct:type">Tennis databases, files, and algorithms</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://www.tennisabstract.com/" property="cc:attributionName" rel="cc:attributionURL">Jeff Sackmann / Tennis Abstract</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.<br />Based on a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/JeffSackmann" rel="dct:source">https://github.com/JeffSackmann</a>.

In other words: Attribution is required. Non-commercial use only.
