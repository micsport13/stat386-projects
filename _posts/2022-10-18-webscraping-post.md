---
layout: post
title:  "Webscraping Stock Market Data"
date:   2022-10-18
author: Noah Lawrence
description: How to pull in Stock Data using an API
image: /assets/images/stockmarket.jpg
---
<div style="align-text: center">
<img src="/stat386-projects/assets/images/how-api-works.png">
</div>

# Introduction to API use
API (application programming interface) is a tool that is built into many web services that allow for applications to retrieve data from a server.  In the data science realm, this most often shows up as get requests, which are requests that pull information from the web server.  This is useful in obtaining the data used within web sites but are formatted in such a way that may make webscraping difficult or only a specific subset of the data is displayed on the website.  API's are also useful in variable data, such as in the BYU app where it will call the API to figure out what your classes are and when they are.  This data will change on a semester basis but the underlying code doesn't need to be changed that much because the application simply calls to the API created by BYU.  In this post, we will show how to use AlphaVantage's API to pull stock data.

# Obtaining an API key
In order to limit the number of requests and limit the data to authorized users, API will often require authentication using keys.  In the case of AlphaVantage, they offer free keys to anyone who signs up for the service.  That can be done <a href="https://www.alphavantage.co/support/#api-key">here</a>.  When you sign up, it will generate an API key that you can save to your file.  Please remember that these keys are sensitive and should not be shared with anyone.  Additionally, remember that one of the best ways to protect your key is to save it in another file and simply read the file from your program.  You should not hard code your API key into your code, especially in the case that you open source the code.  Once you obtain the API key, continue on to the next step.

# Calling the API
The best place to start for API calls is the documentation.  When a company releases an API, it often comes with documentation for the API.  In the case of AlphaVantage, it is extremely simple.  It is structured like this: https://www.alphavantage.co/query?function=FUNCTION&symbol=SYMBOL&apikey=APIKEY.  First is the function keyword, which is included in the API documentation.  Some of these functions are specifically premium features but it is listed in the documentation regarding which are premium and which are not.  Following the function keyword is the SYMBOL keyword which is simply the stock ticker symbol, which can be easily searched on google.  Finally comes the APIKEY keyword which is where the API key is placed.  As mentioned before, <b>DO NOT</b> include this key directly in your code.  Often times, you will read this value in to a variable and that variable can be passed using {} like so ...&apikey={your_api_key_variable_here} which makes it easier to obscure your api key.  When all of these variables are put in place, the API will often return a JSON file with all of the data that you queried.  There are additional parameters that can be passed in but I will not cover them here.  I would refer to the documentation found at the end of this post.
<div style="text-align: center">
<img src="/stat386-projects/assets/images/alpha_vantage.jpg">
</div>
# Why bother?
With the quantity of publicly available data, we may often ask ourselves,"Why bother?" The answer to this is simple.  API's will make it simple in obtaining the data from the source and avoid having to deal with the formatting of certain webpages and will often include more data than is displayed on the website.  For this reason, API's will be extremely helpful in obtaining the most useful and up-to-date data.  Using data pulled using this API, I will create a follow up post that includes analysis of the data obtained from this API.  There, it will be useful to see the connection of API use and data analysis. Stay tuned for more!

# Links
<a href="https://www.alphavantage.co/documentation/">Alpha Vantage Documentation</a>