---
title:  Getting started with 11ty
description: This is a post on dev.to.
date: 2022-02-27
tags:
layout: layouts/post.njk
---
11ty is a simple static site generator that uses the files found in the current working directory. You can use many different filetypes such as markdown, html, JavaScript, etc. There are many different ways to go about creating your first 11ty site. 

## **Basic 11ty Site**
To easily get started with 11ty, go to your command line and in the directory you want, run this command: 

```
echo '# Page header' > README.md
npx @11ty/eleventy
```
This will create a blank site in the current directory. To start up the web server, you can run this command: `npx @11ty/eleventy --serve`. After that, you can open `http://localhost:8080/README/` in your web browser to see your local page. You can edit its contents in a code editing program such as VSCode. Then you'll want to create a .eleventy.js file so that you can configure Eleventy to your site's needs. You can edit the files in the directory such as the readme.md and index.html. Here is what my basic site looks like: 
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/aiqavveawofjd2br0cr0.png)
You can view my GitHub code [here].(https://github.com/briangan123/11ty)

## **11ty Blog Template**
Another way to utilize 11ty is by using prebuilt templates. For this example, I used [this](https://github.com/11ty/eleventy-base-blog) template from GitHub. To use this as a template, click the green button that says "use this template". It will prompt you to create a repo name and then you can create your own version. ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/9qe41ss9jvtratdpdhmv.png)
After you created your template on GitHub, you can use your command line to keep track of changes so that you can upload it to GitHub. Again, you can edit the contents by changing some files in VSCode. Here is what my blog looks like:

Homepage
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/3jj5o3n1g6qduhxa48rs.png)
Archive page
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/n072znuwh3y695apxat7.png)
First Blog Post
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ixdtrvn5qwf7sujmwu4j.png)
You can push your changes to GitHub to keep track of changes to your files as you add more to your site. Here is my Github [repo](https://github.com/briangan123/11tyLab).

## **Another Template**
Another template I used was [this](https://github.com/trey/resume-template). 
Following the same procedures to use the template, I created my own resume site and edited the files and page content to fit my needs. Here is what it looks like: 
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/otqay0x4z7cfhr9pag0y.png)
You can see the edits I made in my GitHub repo [here](https://github.com/briangan123/resume11ty).

## **Conclusion**
11ty is a powerful tool to create a static site and there are many ways to go about it. Using a template will get you up and running faster, but if you want full customizability, then you can build your site from the ground up.