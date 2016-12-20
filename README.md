# Web scraping

## Creating JSON of the base domain:

1. Open Google Chrome and install the extension [Web Scraper Chrome Extension](https://chrome.google.com/webstore/detail/web-scraper/jnhgnonknehpejjnehehllkliplmbmhn) 


2. Create three sitemaps for each domain. Below are the three sitemaps to create
  1. Creating sitemap of the input page(Where users inputs data to the page). This page can be anything where user inputs data submits the form.
    1. Open the base domain page. Eg: Let us consider http://rent.com
    2. Go to developer tools (F12) click on Web Scraper tab as shown in [this image](images/image1.PNG) 
    3. Click on create new sitemap. Give sitemap a name and enter any url as it needs one as [shown here](images/image2.PNG). 
    4. Click on add new selector and click select in selector section, click on the input element in the web page and click Done Selecting. [Shown here after done selecting](images/image3.PNG)
    5. In id field give an id for the selector. This id should be in the follwing format.  
      1. If it is an input text element then, id should be text-id1 or text-id2 or text-id3 .....
      2. If it is a checkbox element then, id should be checkbox-id1 or checkbox-id2 ......
      3. If it is a radiobutton element then, id should be radiobutton-id1 or radiobutton-id2 ......
      4. If it is a submit button then, id should be submit-button
      5. If it is a submit text i.e if you type in the text box and press enter key to submit the form then, id should be submit-text
    6. After you finish creating selectors for all the elements[(Like this)](images/image4.PNG) you can proceed to the next step. 
    7. Click on the Sitemap and click export sitemap as [shown here](images/image5.PNG)
    8. Copy the entire sitemap json text as [shown here](images/image6.PNG) and paste it in a file. Name the file as rent-input.json
  2. Creating sitemap of the listings page(has all the listings)
    1. Open the base domain page. Eg: Let us consider http://rent.com and enter sensible data and go to the listings page. 
    2. Go to developer tools (F12) click on Web Scraper tab as shown in [this image](images/image1.PNG) 
    3. Click on create new sitemap. Give sitemap a name and enter any url as it needs one as [shown here](images/image7.PNG)
    4. Click on add new selector, check the multiple checkbox as [shown here](images/image8.PNG), click selector in selector section and  select atleast 2-3 links of the listings then all the listings are automatically selected. Then, click on done selecting and give the selector an id. id should be "listings" as [shown here](images/image9.PNG) and save the selector. 
    5. Again, click on add new selector, click select in selector section and select next page button in the pagination bar.Then, click on done selecting and give the selector an id. id should be "page" as [shown here](images/image91.png) and save the selector. 
    6. Click on the Sitemap and click export sitemap as [shown here](images/image5.PNG)
    7. Copy the entire sitemap json text as [shown here](images/image6.PNG) and paste it in a file. Name the file as rent-listings.json
  3. Creating sitemap of the listing page(Has the content of one listing)
    1. Click on any listing and open the listing page to scrape. 
    2. Go to developer tools (F12) click on Web Scraper tab as shown in [this image](images/image1.PNG) 
    3. Click on create new sitemap. Give sitemap a name and enter any url as it needs one as [shown here](images/image10.PNG)
    4. Click on add new selector and click select in selector section, click on the element to scrape in the web page and click Done Selecting and give a name for the id. [Shown here after done selecting](images/image11.PNG)
    5. As of now, we can only srape only these fields and this must be the id name. (Select any of the following) 
      1. title
      2. rent
      3. address
      4. phonenumber
      5. beds
      6. description
      7. deposit
      8. price
      9. cost
    6. Cloudsearch only accepts if the fields are added in the indexing option. If you need an other field to scrape. Let us know we will add it to the index fields. 
    7. After you create all the selectors sitemap looks [like this](images/image12.PNG).
    8. Click on the Sitemap and click export sitemap as [shown here](images/image5.PNG)
    9. Copy the entire sitemap json text as [shown here](images/image6.PNG) and paste it in a file. Name the file as rent-page.json

## Starting the scraper
1. Upload the three sitemaps here http://54.161.188.243:8081/uploadsitemap.htm and name your sitemap. 
2. Open http://54.161.188.243:8081/ and click on "Choose from the sitemaps and crawl" and select your sitemap that you just uploaded and click initialize crawler
3. Type http://rent.com in Base URL and type number of pages to crawl. 
4. Give inputs. These are the inputs that are created while page sitemap. 
5. Click submit to start scraping. Log id is displayed when clicked on submit. Log id is to know the status of the scraper. 
