# Tesla Superchargers Data Web Scrape
This project focuses on scraping the Tesla.com and Supercharfer.info web pages to get locations and other data on superchargers


`Tesla_Superchargers_Data_Scrape.ipynb`

This code uses the BeautifulSoup modules to scrape information about Tesla supercharger locations in the United States from a website. It first makes a request to the website using the requests module and then uses BeautifulSoup to parse the HTML content. It then extracts the address information for each location and removes any punctuation characters. Finally, it uses the Google Maps API to get the latitude and longitude coordinates for each location and adds them to the DataFrame.

`Tesla_Superchargers_Extended_Data.ipynb`

This code uses the Selenium module to navigate to a webpage and extract information from a table on that page. It launches a new Chrome browser window and navigates to the specified URL. It then waits for a select element to be available, creates a Select object from it, and selects an option with a specific value. It waits for a table to load, extracts the headers and data from the table, and saves them to a DataFrame. 

Because the webpage is only showing 50 rows at default we would need to implement the following additional steps.

1. Wait for the select element with the name 'supercharger-data-table_length' to be available. This is done using the WebDriverWait function from the selenium.webdriver.support.ui module with an expected condition of presence of element located by the name selector.

``` python 
select_element = WebDriverWait(driver, 60).until(
    EC.presence_of_element_located((By.NAME, 'supercharger-data-table_length'))
)
```
2. Create a Select object from the select element to interact with the dropdown list of number of items to be displayed in the table.
``` python
select_object = Select(select_element)
```
3.Select the option with value "10000" in the dropdown list.
``` python
select_object.select_by_value('10000')
```

## Project Deliverable

Tableau public dashboard: https://public.tableau.com/app/profile/ksenia7036/viz/TeslaSuperchargerNetwork/Dashboard1

![image](https://user-images.githubusercontent.com/73604041/226205164-e4735b57-9d6b-4081-aae2-0e23439e3bd1.png)
