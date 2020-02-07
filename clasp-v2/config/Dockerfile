# Version 1
FROM ubuntu:16.04
MAINTAINER Juan Pablo Donayre

# Update Ubuntu image
RUN apt-get update && apt-get install -y

# Install sudo and curl
RUN apt-get install sudo
RUN apt-get install curl -y

# Install NodeJs
RUN curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
RUN apt-get install -y nodejs

# Update NodeJs to Latest Version
#RUN npm install n -g
#RUN n latest

# Install Google CLASP
RUN npm i @google/clasp -g

# Create directory
RUN mkdir /var/project
WORKDIR /var/project

# Install GIT (For version control)
RUN apt-get install git -y