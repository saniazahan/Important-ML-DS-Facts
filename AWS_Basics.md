## Free AWS basic course
https://explore.skillbuilder.aws/learn/course/1851/AWS%2520Technical%2520Essentials

Ways to interact with the AWS APIs
- AWS management console
- AWS command line interface
- AWS software development kits

## AWS Identity and Access Management

## EC2 launch user data

##!/bin/bash -ex
#Update yum
yum -y update
# Add node's source repo
curl -sL https://rpm.nodesource.com/setup_15.x | bash-
# Install nodejs
yum -y install nodejs
# Create a dedicated directory for the application
mkdir -p /var/app
# Get the app from S3
wget https://aws-tc-largeobjects.s3-us-west-2.amazonaws.com/ILT-TF-100-TECESS-5/app/app.zip
# Unzip it into a specific folder
unzip app.zip -d /var/app/
cd /var/app/
#install dependencies
npm install
# Start your app
npm start


