
Refactor Monolith to Microservices
Contributors Forks Stargazers Issues MIT License LinkedIn

Table of Contents
About The Project
Built With
Getting Started
Prerequisites
Installation
Usage
Contact
Acknowledgements
About The Project
The project application, Udagram - an Image Filtering application, allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice. It has two components:

Frontend - Angular web application built with Ionic framework
Feed backend RESTful API - Node-Express application to get photos.
Auth backend RESTful API - Node-Express application for authentication.
In this project you can also:

Set up each microservice to be run in its own Docker container
Set up a Travis CI pipeline to push images to Dockerhub
Deploy the Dockerhub images to the Kubernetes cluster
A reverse proxy server is added to add an extra layer of protection to the application
Getting Started
This is an example of how you may give instructions on setting up your project locally. To get a local copy up and running follow these simple example steps.

Prerequisites
Install Git for your Mac/Linux/Windows. Git is used to interface with GitHub.

PostgreSQL client, the psql command line utility, installed locally. Using PostgreSQL involves a server and a client. The server hosts the database while the client interfaces with it to execute queries. Because we will be creating our server on AWS, we will only need to install a client for our local setup. The easiest way to set this up is with the PostgreSQL Installer. This installer installs a PostgreSQL client in the form of the psql command-line utility. You can see the complete (server and client) installation instructions for Mac, Linux, and Windows.

NodeJS v12.14 or greater up to v14.15 - Node.js is used to run JavaScript-based applications and NPM is a package manager used to handle dependencies. NodeJS installer will install both Node.js and npm on your system. Verify the installation using the commands:

# v12.14 or greater up to v14.15
node -v
# v7.19 or greater
npm -v
Ionic command-line utility v6 framework to build and run the frontend application locally. In general, Ionic Framework is used to make cross-platform applications using JavaScript. Verify the installation as:

# v6.0 or higher
ionic --version
Docker Desktop for running the project locally in a multi-container environment.

AWS CLI v2 for interacting with AWS services via your terminal. After installing the AWS CLI, you will also have to configure the access profile locally.

Create an IAM user with Admin privileges on the AWS web console. Copy its Access key.

Configure the access profile locally using the Access key generated above:

aws configure
Kubectl command-line utility to communicate with Kubernetes clusters

Installation
Clone the repo

git clone https://github.com/edcsu/project.git
Cd into each of the respective projects to install their respective dependencies.

npm install