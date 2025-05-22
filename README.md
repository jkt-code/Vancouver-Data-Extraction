# Vancouver-Data-Extraction
This is a notebook displaying data extraction of marketing agencies, web development &amp; SEO agencies in Vancouver Canada.
### Link to the notebook: https://anaconda.cloud/share/notebooks/5df2ab32-af0f-4835-935c-a2332b37aad3/overview

## Libraries used
#### Python - Scripting 
#### Pandas - Data tarnsformation, manipulation and exporting
#### BeautifulSoup - Webpage(Html) extraction 
#### Requests - Requests data from source using an api that returns response in json format 
#### time - time.sleep() to delay the intervals of calling an api for a request 

## Municipalities Extraction
Vancouver has a total of 21 municipalities and I wanted to extract the entire Vancouver. So I used https://www.municipality-canada.com/ wbsite to extract all the municipalities and their respective location coodinates so that I can feed them to google api to fetch the respective data. I used https://www.municipality-canada.com/en/regional-district-greater-vancouver.html to extract the municipalities and respective link to further details extraction. The link was in this format https://www.municipality-canada.com/en/city-vancouver.html and I proceeded to use it to extract respective coordinates.

## Google Api
After extracting the cities with the respective location coordinates, I fed each of the location to the google api parameters in this format https://maps.googleapis.com/maps/api/place/nearbysearch/json? {parameters: location=<latitude and longitude>&radius=<radius to search in meters>&keyword=<business to search>&key=<api_key>} where I specified the parameters as : the extracted location (latitude,longitude), radius= radius of search as 3000m (3km), keyword = business Keywords to search for, key = your respective api from google. I also added a delay of 2 seconds for each request so as not to overload the api

## Export
After scraping and extraction. I dropped duplicates, further manipulated and transformed the data into a dataframe that i used to export as csv.

## Usages
This extracted data can be used to further analyze the market to get leads in that area, that is Vancouver Canada and in those specific fields that is Marketing, Web development & SEO.
