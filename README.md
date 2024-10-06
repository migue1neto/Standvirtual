# Standvirtual
Standvirtual Web Scraping &amp; Data Analysis

## Sraping the website 

The project began with scraping the *Standvirtual* website. This was achieved with Selenium (for pagination purposes) and Beautiful Soup (to parse and extract the HTML).

Standvirtual is a relatively easy website to scrape. As with all scrapers, what was important to ensure was that the  scraper interacted with the website akin to a human. For *Standvirtual* this meant that the scrape how to be done by filtering/parameters, which in this case meant filtering the search by "Brand" (hence the Dictionary) - brand was sufficient.

Even though it is possible to access *htts://www.standvirtual.com/carros/*, where you seamingly have access to the +1.200 pages of ad listings (+40.000 ads, with 32 ads per page), it is not possible to scrape this data with no filter. This is because when going to page 501 the website simply return page 500. And it does so for all pages after page 500. Furthermore, even in the first 500 pages, the website tends to return duplicates.

As such, the brand parameter was used to scrape the listings. To scrape the listings itself it was a question of parsing the data with Beautiful Soup and then extracting the desired information. The scraper only returns information of the general ad listings, i.e., it does not open the ad listings itself and scraper for further characteristics/information about the car.

## Data Analysis

The data analysis began by cleaning some of the data, of which there wasn't much to clean - 27 rows in a total of 41.106 rows.

Afterwards, a univariate analysis was done, followed by linear regression models (some including categorical variables like Gas Type and Car Model) which allowed us to create a linear regression model capable of delivering decent price predictability.
