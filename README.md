# Building a CI/CD Pipeline (using Azure)

### Creating a Linux Based Python WebApp and managing deployment using CI/CD and Agile Methodology

## Overview

This project is going to detail the cycle of a production application from Planning to Deployment. We are going to investigate the Agile Methodology and utilize it in developing this Webapp. In this project, we will learn how to use spreadsheets to effectively plan the project by creating an estimated time duration for the tasks. We will use Trello to identify and track the steps identified in the project plan. The code environment will have to be set up, we intend to use Azure Cloud shell as our environment for code development. We will use Github as our repository. Azure Pipelines will be used establish the CI/CD pipeline however, we will do a test with GitHubs to verify that we can do remote tests on Python application.
All our work with python will be done in a virtual python environment within Azure Shell.
To allow Azure cloud shell access Github we will create SSH keys in Azure Cloud Shell and it will be used to interface with Github to eliminate the need for persistent login authorizations. 
A Webapp will be developed using Azure. the purpose of the WebApp is to serve as an API to provide predictions on House Values in Boston given a set of parameters and attributes, using Machine Learning. A Flask (Python package) will be used for the Web Server.

An Architecture of the project is shown below.

![<insert Architecture Drawing>](https://content.screencast.com/users/ChiGbugu/folders/Default/media/2bd73dcd-223c-4195-9e63-1318641db1dc/CICDAzurePipeline.jpg)



## Planning
### Spreadsheet
To plan this project, we will be utilizing spreadsheets. The spreadsheet will identify the project plans on tasks and activities to be delivered on a weekly basis. Each task will assigned an estimated difficulty level and/or a time duration. We will use Microsoft Excel for this purpose. A quarterly and yearly plan will also be covered with the spreadsheet.
<Insert link to the spreadsheet>

### Trello
Trello will be used as our task board for this project. The Key tasks as identified in the project plan will be assigned a Card. Each card will pass throught the following process in order: To Do, In Progress and Down.
_Please visit the link below to access the Trello board._

## Coding Environment (Azure Cloud Shell/ Github)
### Azure Cloud Shell
The coding environment we will utilize for this project is the Azure Cloud Shell. The Azure Cloud Shell is a service from Azure Cloud so it will make it swifter to intergrate with the components of the Azure shell like creating a Web App, creating a Resource group and Creating an App service - which is needed for the WebApp to run.

You can access Azure Cloud Sheel via serval means, but we will focus on 2 main ways. The first option is to log on to Azure portal (portal.azure.com) and click the Cloud shell Icon as shown below.
![Azure Cloud Shell Icon](https://content.screencast.com/users/ChiGbugu/folders/Default/media/7013c63b-d74c-42c5-97f5-08699339064f/AzureCloudShell.jpg)

The second option is to log on directly to the Azure Cloud Shell at https://shell.azure.com/. When you go to this link, you will be required to sign on.


### Github
To hold the project code repository, we will use Github. 
The Github will be strutured as follows:
```
MainRepoFolder 
	|-------> CI Tests Folder
	|-------> CI/CD Deployment Folder
```
### Interface/Interaction 
Azure Cloud Shell can interact with Github in several ways most notably via HTTPS or SSH. We will setup SSH in Azure for communication as HTTP communications will require authenticating username and password before interaction.

#### Let's set up our Github and Azure Cloud Shell Environment:
