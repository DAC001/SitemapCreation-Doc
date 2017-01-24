# Web scraping

## Creating JSON of the base domain:

1. Open Google Chrome and install the extension [Web Scraper Chrome Extension](https://chrome.google.com/webstore/detail/web-scraper/jnhgnonknehpejjnehehllkliplmbmhn) 


2. Create sitemap for each domain. Below are the three sitemaps to create
  3. Creating sitemap of the listing page(Has the content of one listing)
    1. Click on any listing and open the listing page to scrape. 
    2. Go to developer tools (F12) click on Web Scraper tab as shown in [this image](images/image1.PNG) 
    3. Click on create new sitemap. Give sitemap a name and enter the current url as it needs one as [shown here](images/image10.PNG)
    4. Click on add new selector and click select in selector section, click on the element to scrape in the web page and click Done Selecting and give a name for the id(name of the id should be SMALL letters and no spaces and no special chars and should be in the CloudSearch Names in the spreadsheet https://docs.google.com/spreadsheets/d/1ImK3lePyT1j7giEaRzb-1U7dQR3gqevh04HUvQCsPMQ/edit#gid=75558478 in the site schema tab). [Shown here after done selecting](images/image11.PNG)
    5. Try to select all the possible elements.  
    7. After you create all the selectors sitemap looks [like this](images/image12.PNG).
    8. Click on the Sitemap and click export sitemap as [shown here](images/image5.PNG)
    9. Copy the entire sitemap json text as [shown here](images/image6.PNG) and paste it in a file. Name the file as rent-page.json
    
