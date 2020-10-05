# Mission-to-Mars Analysis

## Overview of the analysis Mission-to-Mars Analysis

The purpose of this analysis is:
* To use BeautifulSoup and Splinter to scrape full-resolution images of Mars’s hemispheres and the titles.
* To store the scraped data on a Mongo database.
* To use a web application to display the data.
* To alter the design of the web app to accommodate these images.

## Results

### Splinter and BeautifulSoup:
Automating web browsing and scrapping web data is done using the tools *BeautifulSoup* and *Splinters*
* Using the splinter's Broswer package we visit the *URL* from where the web data has to be scraped.
* Using Beautiful soup the html content of the web page is parsed.
* The code to scarpe the web data is written in the file *scraping.py*
* Right click on the web page and using the DevTools the information that has to be extracted is located.
* The hemisphere *image url* and the *title of the image* is extracted.
* The extracted data is stored in the list of dictionary *hemisphere_image_urls*


### Mongo Database:
The non-relational data from the web scrape is stored in the lightweight database MongoDB.
* The MongoDB is started using the command *mongod*.
* New database *mars_app* is created to hold the Mars data that is scraped.
* We have to add the */scarpe* route for the program to automatically scarpe the web data when the scrape button is clicked.
* The *flask* routes all the web scarping data into *MongoDB* that is 


### Web Application:
*Flask* is used to build the freamework for the app to display the data from the web scraping.
* File *app.py* is used to  setup *Flask* and the *MongoDB*
* In the *app.py* file we have to define the routes for *"/"* and *scrape*
* *Index.html* file is setup to be displayed as the home page.
* When the scrape button is clicked the *scarping* in the file scraping.py is executed.
* All the data is inserted into MongoDB.
* The data to be displayed is then acccessed from MongoDB *mongo.db.mars*

## Summary:
