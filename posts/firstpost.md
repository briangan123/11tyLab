---
title: Building a basic web component with Open-wc.
description: This is a post on My Blog about open-WC.
date: 2022-01-18
tags:
  - open-wc
layout: layouts/post.njk
---
Hi, my name is Brian Gan and this is my first time coding in JavaScript. In this tutorial, I am going to show you how to build a basic web component using open-wc. If I was able to accomplish this, then so can you!

## **What to install**
**VSCode**
First, you'll need to install [VSCode](https://code.visualstudio.com/download) for your respective operating system. This is where you'll write most of your Javascript code for your web component.

**NodeJS**
Next, you'll need to install [NodeJS LTS](https://nodejs.org/en/). This is a runtime environment for developing your application and provides a library that will make developing web applications simple. Make sure you are downloading the Long-term support (LTS) version so that you won't have any critical bugs that haven't been discovered yet. You can learn more about NodeJS [here] (https://www.tutorialspoint.com/nodejs/nodejs_introduction.htm).

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/isncdq4yuhq5wc14syx7.PNG)

**npm**
This is a package manager that comes preinstalled along with NodeJS. npm puts modules in one place so that NodeJS can find them and also helps manage dependencies so that you won't have to download them manually. 

You can check to see if NodeJS installed npm by typing `npm -v` in the command line. This will show you what version you have. If it doesn't recognize the command, then you will need to manually install npm by typing `npm install -g npm`. You can learn more about npm [here] (https://docs.npmjs.com/cli/v6/commands/npm).

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/yt1to8b8gzhubwd7vhpn.PNG)

NodeJS and npm are popular among developers because it is based on JavaScript, which has been the most popular web development coding language. NodeJS is easy to learn, scalable, cross-platform friendly, light & fast, and takes advantage of caching. You can learn more about the origins and why it is so popular [here] (https://www.section.io/engineering-education/why-node-js-is-popular/).

**Yarn**
Yarn is similar to npm and is another package manager that is optional for this tutorial. You can also check to see if you have yarn installed with the command `yarn -v`.

## **Creating a place for all of your projects**
Now, you'll want to create a directory so that you can store all of your projects. This can be done through the command line or through the GUI. For this project, my files are stored in my `Documents/git/edtechjoker/` directory, but you can name it whatever you'd like. This can be done through the command line by typing `mkdir -p ~/Documents/git/edtechjoker` on most operating systems. For reference, I am using a Windows 10 machine and I created my directory by using the GUI.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/dh7893fobw33vi3ugoxp.PNG)

## **Version Control using GitHub**
If you would like to use GitHub for version control, then make sure to clone your repo into the newly created folder. 

1. In your command line, navigate to the newly created directory by using the cd command. In my case, this would be `\Users\brian\Documents\git\edtechjoker\`

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0o9hd8vet685zos53tj5.PNG)
2. Create a new repo on GitHub. I named my repo `edtechjoker-lab1`.
3. Clone your repo by running `git clone git@github.com:YOURUSERNAME/YOURREPO.git`. 
Make sure to replace your username and the name of your repo.

## **Getting connected to Open-wc**
Now that we have everything installed, we can begin to connect to Open-wc. 

1. In your command line, navigate to the newly created directory. If you want to keep track of version with GitHub, make sure you're in the repo folder. In my case, that would be `\Users\brian\Documents\git\edtechjoker\edtechjoker-lab1`.
2. Use the command `npm init @open-wc`. You Should see something like this:

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ktb8pyvr3yazaomj7t3s.PNG)
3. Initialize your project with the following settings: (Hint: you must use your arrow keys to navigate through the different settings)

- New project scaffold
- Web Component
- Linting, Testing, and Demoing all enabled. 
- No TypeScript
- Name it "hello-world" --You can name it whatever you'd like.
- Install depencies using yarn -- if you were unable to install yarn, you can use npm instead.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xy1ihpb4ra1h58zb1apz.PNG)

Congratulations! You have successfully created a web component using Open-wc. You can view your site by going into the new folder. In my case, hello-world. Then use the command `npm run start` or `npm start` or if you installed yarn, `yarn start`.
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/pa0x78cuc5qyz1deajro.PNG)
 If successful, it should open a new window/tab displaying your web component.
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/yoqqwem7dttb50fd0z7g.PNG)
To exit, press [control] + c

## **Tweaking your code**
This is where VSCode comes into play. Now that you have your basic web component, you can go to VSCode and open up the project folder. In my case, this is called hello-world. If you navigate to the src folder, you will see a JavaScript file. You can play around with this file to see how it changes your web component. 
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/086pc7xfueixyl2smewx.png)
 If you are using version control, make sure to commit and push your changes to your online repository. For example, after finishing up my changes, in my command line, I would make sure I'm in my hello-world directory (the one created using open-wc) and use the following commands: 
1. `git commit -am "YOUR MESSAGE HERE"`
2. `git push origin main`
3. If prompted, you may need to enter your passphrase.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/z40ic9hx9in16digpu2l.PNG)

Now if you go to your GitHub repo, you'll see the changes in your code.

This is my [GitHub repo](https://github.com/briangan123/edtechjoker-lab1) for this project.

If you want to practice and learn more about different web components and how to integrate them into your code, I suggest you check out [Lit's tutorial] (https://lit.dev/tutorial/) and play around with it.

Good luck and have fun building!
