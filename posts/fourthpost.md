---
title: Getting started with Docker
description: This is a post on My Blog about Docker.
date: 2022-02-27
tags: 
layout: layouts/post.njk
---
Docker is an open source containerization platform where developers can package applications into containers. It is becoming more popular due to organization's shift to the cloud, simplifying delivery of applications. Containers make it so that applications can be easily deployed, patched, and scaled.You won't have to install any dependencies because the container will already have everything the application needs to run. Docker provides a single place to set up and manage containers simply and easily. 

## **Getting Started with Play With Docker**
First, you'll want to head over to the Docker site and create an account. After creating an account, head over to this [link](https://labs.play-with-docker.com/) and hit the green start button.
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zxfb82nzg7izmznx7qel.png)
 From here, you can click the "ADD NEW INSTANCE" button on the left hand side to open up the sandbox. 
Now have a command line on Docker that you can play around with to open containers.

## **Connecting this to out NASA API project **
After creating a new instance, we need to clone the GitHub repo and cd into the new directory. 
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/b89eadmqn9c5a9djjo2h.png)
Then we need to create a new file in this directory. This can be done with this command: `touch "dockerfile"`. 
Then we can edit this file by clicking the "Editor" button and searching for the new file. 
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0xbx9gsk2yrsyt064ypp.png)
In the file, we can paste this code:

```
FROM node:10-alpine
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "/app/src/index.js"]
EXPOSE 3000
```
After adding the contents to this file, you can save it. What this does is automate commands that would need to be run in order to run the site like a script.

Now you can run `docker build -t todoapp .` (make sure to include the period)
Now you can create your containers using the command line. For example: `docker run -dp 3000:3000 todoapp`.
You can create as many containers as you want as long as you are using different ports. Otherwise, it will be overwritten.
Now to open the port, you can click the "Open Port" button and entering in the port number. Or if a button with the port number pops up, you can click that instead.
Additionally, you can run `docker-compose up` to run an entire app.
Congratulations, you have created a dockerfile for your container.

## **Images from NEWSAPI Microservice**
*This is the frontend of the NewsAPI microservice*
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/hxo1pjij42oeti561q8w.png)

*This is the backend of the NewsAPI microservice*
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/lh14xzpeviuci5ckv19a.png)
 
