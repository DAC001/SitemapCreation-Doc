# Web scraping

## Creating JSON of the base domain:

1. Open Google Chrome and install the extension [Web Scraper Chrome Extension](https://chrome.google.com/webstore/detail/web-scraper/jnhgnonknehpejjnehehllkliplmbmhn) 


2. Create sitemap for each domain. Below are the three sitemaps to create
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
