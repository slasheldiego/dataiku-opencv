# Using OpenCV framework in Dataiku

This project is focused in provide a guide to integrate the OpenCV framework with the Dataiku platform. 

The project is composed by a set of subprojects where it will 

## Why is important?

We believe that this project will help some users (developers, data scientist or data engineers) the currently works with OpenCV framework to understand how to migrate your OpenCV project to Dataiku seamlessly.

## What are the different between Dataiku and other tools?

Dataiku provide a framework (based on APIs) to access data through objects like Datasets or Managed Folders. So, it is possible that your current developmens does not works well.

### Dataiku Dataset overview

A dataset is a data structure with direct connection to a data source (Database, object storage, etc). For example, we can create a dataset based on a connection to a AWS S3 Bucket in order to access to a CSV file.

<b>Figure 1: Dataset section</b>

<img src="/images/dataiku-dataset-1.png?raw=true" width="600" height="300" alt="Dataset section"/>

<b>Figure 2: Dataset list loading Iris dataset as an example</b>

<img src="/images/dataiku-dataset-2.png?raw=true" width="600" height="160" alt="Dataset list"/>

<b>Figure 3: Dataset with Iris data</b>

<img src="/images/dataiku-dataset-3.png?raw=true" width="300" height="360" alt="Dataset example"/>

### Managed folders overview

Another way to access data is the managed folders in Dataiku. Against Dataset, managed folders creates a structure to access to list of the files contained in the data source.

We can create a managed folder through dataset creation options.


<b>Figure 4: Create a managed folder through NEW DATASET option</b>

<img src="/images/dataiku-managed-folders-1.png?raw=true" width="600" height="360" alt="Create a managed folder"/>

As a part of the creation process we need to fill the name label and select a data source connection (e.g. AWS S3 Bucket). In this case, we will use the File System of the Dataiku Design node server.

<b>Figure 5: Fill the creation form for managed folder</b>

<img src="/images/dataiku-managed-folders-2.png?raw=true" width="350" height="230" alt="Creation form"/>
