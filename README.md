# Tesla Superchargers Data Web Scrape
This project focuses on scraping the Tesla.com and Supercharfer.info web pages to get locations and other data on superchargers


`Tesla_Superchargers_Data_Scrape.ipynb`

This code uses the BeautifulSoup modules to scrape information about Tesla supercharger locations in the United States from a website. It first makes a request to the website using the requests module and then uses BeautifulSoup to parse the HTML content. It then extracts the address information for each location and removes any punctuation characters. Finally, it uses the Google Maps API to get the latitude and longitude coordinates for each location and adds them to the DataFrame.

`Tesla_Superchargers_Extended_Data.ipynb`

This code uses the Selenium module to navigate to a webpage and extract information from a table on that page. It launches a new Chrome browser window and navigates to the specified URL. It then waits for a select element to be available, creates a Select object from it, and selects an option with a specific value. It waits for a table to load, extracts the headers and data from the table, and saves them to a DataFrame. 


## Project Deliverable

Tableau public dashboard: https://public.tableau.com/app/profile/ksenia7036/viz/TeslaSuperchargerNetwork/Dashboard1

![image](https://user-images.githubusercontent.com/73604041/226205164-e4735b57-9d6b-4081-aae2-0e23439e3bd1.png)
