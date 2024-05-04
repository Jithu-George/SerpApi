# SerpApi 
 Learn to return images for a keyword on a html page.

Using a Custom API to return images from a  google search. the images returned are printed on a html page.

## Step - 1

Go to SerpApi.com.  Create an account. Copy the key provided from the login page

## Step - 2

Create a Custom html page with a Textfield to input the keyword to search for. 
It should also have an output div to print the images returned from the API. A custom HTML page is provided in this repo.

### HTML page Explanation:
 
A textfield is placed on the top of the page with an id inputstring. When a user types in this textfield and click enter a eventlistener is activated. This eventlistener then sends the keyword from the textfield to the SerpApi. 

The response from the SerpApi is returned as data. Them images from the data is in "images.results". The Resultbox(Output-Div) is updated with the images from the Data. It is limited to the first 5 images by using slice function

A custom css is written for the car type display of the returned images

## Step - 3

Create  a JS file to send request to the SerpApi and to return the images from it. 

### JS file Explanation

Import modules into the file by using require. Set CORS headers as given to prevent any cors errors. Cors is a security feature used by websites to prevent access.

Now to handle the post request to the upload endpoint. The inputstring from the textfield (client) is parsed into body. A variable inputstring is used to define the input from the parsed body. This inputstring is send to the SerpApi using ```response = await JSON```. Here the q,engine,ijn and api_key are parameters. Q is the string to search for. **Api_key** is the key that is obtained from the website.

## Running the Website

First initialise the node. Remmeber to install node from website.   
```npm init -y```   
Now install all the required modules by using    
```npm install express formidable axios serpapi fs ```   
Run the node app   
```npm main.js```   
Run the html page.   
Type anything in the textfield and click enter.
