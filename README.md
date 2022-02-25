# Using OpenCV framework in Dataiku

This project is focused in provide a guide to integrate the OpenCV framework with the Dataiku platform. 

## Why is important?

We believe that this project will help some users (developers, data scientist or data engineers) the currently works with OpenCV framework to understand how to migrate your OpenCV project to Dataiku seamlessly.

## What are the different between Dataiku and other tools?

Dataiku provide a framework (based on APIs) to access data through objects like Datasets or Managed Folders. So, it is possible that your current developmens does not works well.

### Dataiku Dataset overview

A dataset is a data structure with direct connection to a data source (Database, object storage, etc). For example, we can create a dataset based on a connection to a AWS S3 Bucket in order to access to a CSV file.

<b>Figure 1: Dataset section</b>

<img src="/images/dataiku-dataset-1.png?raw=true" width="600" height="400" alt="Dataset section"/>

<b>Figure 2: Dataset list loading Iris dataset as an example</b>

<img src="/images/dataiku-dataset-2.png?raw=true" width="600" height="180" alt="Dataset list"/>

<b>Figure 3: Dataset with Iris data</b>

<img src="/images/dataiku-dataset-3.png?raw=true" width="300" height="400" alt="Dataset example"/>

### Managed folders overview

Another way to access data is the managed folders in Dataiku. Against Dataset, managed folders creates a structure to access to list of the files contained in the data source.

We can create a managed folder through dataset creation options.

<img src="/images/dataiku-folder-1.png?raw=true" width="300" height="400" alt="Create a managed folder"/>
