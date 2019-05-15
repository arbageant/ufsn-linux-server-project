# Linux Server Deployment
Author: Andrew Bageant\
Last Updated: 2019-05-14

## Introduction

This document explains the vital details of the Linux remote server I've configured
to run my simple Item Catalog web app. There are still a few bugs I need to work
out, primarily with Oauth, but the app is basically up and running.

## Accessing the App
To access the server for grading purposes, you can use a special user named
"grader". I've included the SSH key for this user in my project submission.

Right now, you can access the project via its public IP address at 54.185.7.225.
It's hosted in an AWS Lightsail server, and should continue to do so at least until
2019-05-31. To SSH to the server, please use Port 2200.

## Server Configuration
The server has been configured via AWS Lightsail to run Ubuntu 16.04. Its
time zone has been set to UTC. Web app hosting is managed via Apache and mod_wsgi.

The following packages have been installed to create the correct
hosting environment (using apt-get):
postgresql
git
libpq-dev

Along with the following Python packages (using pip):
httplib2
requests
oauth2client
sqlalchemy
flask
psycopg2


## The Hosted Application
The hosted application is a simple Python item catalog app, which was created
for an earler udacity project. You can find the public repository for this
app on my Github, here:\

https://github.com/arbageant/item-catalog-project

## Concluding Notes
I ran into a few difficulties on this project, so there are a few bugs that
need to be worked out. The biggest one is that the OAuth redirect doesn't work,
which prevents users from logging in and editing the item catalog. Right now,
it exists essentially as just a page to browse. For the time being, I will
submit as-is and see if I can find a fix in the next few days. If you have
any suggestions on this subject, I would be glad to hear them.
