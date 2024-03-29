# Plagiarism Project, Machine Learning Deployment

This repository contains code and associated files for deploying a plagiarism detector using AWS SageMaker.

## Project Overview

In this project, I was tasked with building a plagiarism detector that examines a text file and performs binary classification; labeling that file as either *plagiarized* or *not*, depending on how similar that text file is to a provided source text. Detecting plagiarism is an active area of research; the task is non-trivial and the differences between paraphrased answers and original work are often not so obvious.

This project will be broken down into three main notebooks:

**Notebook 1: Data Exploration**
* Load in the corpus of plagiarism text data.
* Explore the existing data features and the data distribution.

**Notebook 2: Feature Engineering**
* Clean and pre-process the text data.
* Define features for comparing the similarity of an answer text and a source text, and extract similarity features.
* Select "good" features, by analyzing the correlations between different features.
* Create train/test `.csv` files that hold the relevant features and class labels for train/test data points.

**Notebook 3: Train and Deploy Your Model in SageMaker**
* Upload the train/test feature data to S3.
* Define a binary classification model and a training script.
* Train a model and deploy it using SageMaker.
* Evaluate the deployed classifier.


# Any cost for running in SageMaker?
The deployment project is intended to be done using Amazon's SageMaker platform. In particular, it is assumed that you have a working notebook instance in which you can clone the deployment repository.

When starting your AWS you will get some free resources. For Sagemaker it is free to use some instances for the first two months. Please check carefully on Free Tier limits https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc and pricing https://aws.amazon.com/sagemaker/pricing/

Attention, in order to avoid incurring unnecesecary cost, please make sure to clean up the Sagemaker resources, such as terminate the end points, delete the instances and trainging jobs, as well as delete the buckets and IAM roles. Below I have provided you with a link to follow https://docs.aws.amazon.com/sagemaker/latest/dg/ex1-cleanup.html 
