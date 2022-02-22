---
title: The back end of connecting to APIs.
description: This is a post on connecting to APIs.
date: 2022-02-03
tags:
  - API
layout: layouts/post.njk
---
In this blog post, I'll be discussing the backend of how websites connect to APIs to visualize its data. 

## **GeoIP**
GeoIP is a free API that can retrieve your IP address data and other location information from your Internet Service Provider(ISP). You can view your location information using GeoIP [here](https://freegeoip.app/json/).

## **Getting data from GEOIP into Google Maps**
First, in our constructor, we set the location endpoint to the GeoIP API. We refer to this API when trying to fetch its data. 
`this.locationEndpoint = 'https://freegeoip.app/json/';`

Next, We instantiate variables we want to retrieve. In this case, we instantiated our longitude, latitude, city, and region_name (AKA State). 

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/vveb1jjbypz42jerfqdl.png)

Then, we will fetch data from the API by using this code block: 

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/iimzbgv604z2um9vkjxi.PNG)

**Fetch()**
In this function, we connect to the API and if successful, it will retrieve the data you specified. If not, it returns false and won't display any information from the API. This is also called a promise. This takes the URL as a parameter. 

Now that we retrieved our longitude and latitude from the API and have it stored into a local variable, we can reference it in our render() function. Whenever a variable in the properties() is updated, this function is run again to obtain the updated information.

In the render() function, we declared a new variable, which will be the Google Maps link. Instead of setting a defined longitude and latitude in the url, we input the local variables, `this.long` & `this.lat` instead, so that it can update by itself. 
Then, we created an iframe where a map of your location will be displayed in a little box on your website.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/nebbfq37yhpl9719c5el.png)
 
We can also create a hyperlink that you can click on to direct you straight to the google maps website that already has your coordinates automatically inputted. This is done in a similar fashion as the iframe, but with a different syntax. In this case, we used an href and set it equal to the Google Maps link with the local variables for latitude and longitude. We have a static zoom level set to 14 at the end of the href link. Then you can set the hyperlink to say whatever you'd like. In this case, it says "Open in Google Maps".

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/qggwzkr1mmys5ucbjtg1.png)

## **Wiring data into wikipedia-query tag**
Now that you successfully retrieved your location data from the GeoIP API, you can use   that to imbed a wikipedia article about your location. 

First, you'll need to add it as a dependency by importing it with this at the top: 

`import '@lrnwebcomponents/wikipedia-query/wikipedia-query.js';`


To automatically show the information about your city and state from Wikipedia, you need to use the wikipedia-query search tag and reference the local city and state variables that were instantiated and set earlier.
 
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/pojx8nmjumbhi88ksj45.png)

Now you have successfully wired the GeoIP API data to Google Maps and Wikipedia!

You can check out my repo [here](https://github.com/briangan123/ip-project/blob/master/src/LocationFromIP.js).

Check out these resources for more information.
[GeoIP API](https://freegeoip.app/json/)
[Wiki API Documentation](https://en.wikipedia.org/w/api.php)
