eBay Sold Items Viewer
This is a web application that allows users to view sold items on eBay It displays each item with the title, image, sale price, and a link to the full item description on ebay. Additionally, the app calculates and displays the maximum, minimum, average, and median prices for the items fetched.


Features:

View Sold Items: Displays a list of sold items from eBay based on a query.
Item Details: For each item, the title, image, sale price, and a link to the item description on eBay are shown.
Price Analysis: The app calculates and displays the maximum, minimum, average, and median sale prices for the fetched items.

Requirements:

A web browser to run the app.
JavaScript enabled in the browser.
eBay API Key to access the eBay API.

How to Use
Get API Access:

Sign up for rapid api and sign up to get your key. https://rapidapi.com/ecommet/api/ebay-average-selling-price/playground
Clone the Repository: Clone this repository to your local machine:

bash
Copy code
git clone https://github.com/yourusername/ebay-price-checker.git
Install Dependencies: If you have additional dependencies, they will need to be installed. For example, if using a package manager like npm, run the following:

bash
Copy code
npm install


Search for Sold Items: Enter a search term (e.g., "laptop", "iphone", etc.) in the search bar. The app will retrieve and display the sold items based on your query.

API Overview
The app fetches data from the eBay Finding API. Specifically, it uses the findCompletedItems operation to get sold items.

Endpoint: https://svcs.ebay.com/services/search/FindingService/v1

Request

Headers
content-type: application/json
x-rapidapi-host: ebay-average-selling-price.p.rapidapi.com
x-rapidapi-key: /YOUR KEY/

Body Data

keywords
Description: Keywords entered into the eBay searchbar to refine results. Seperated by spaces
Example: "iPhone"
Required: Yes

max_search_results
Description: Maximum amount of search results. Only allowed values: 25, 50, 100, 200
Example: 200,
Required: Yes

excluded_keywords
Description: Phrases you would like to exclude from the search. Seperated by spaces
Example: "locked cracked case box read"
Required: No

category_id
Description: A unique ID given to seperate categories of products on eBay. To find a category ID to use, navigate to: https://www.isoldwhat.com/
Example: "9355" - Cell Phones & Smartphones
Required: No (HIGHLY RECOMMENDED)

remove_outliers
Description: If set to true, it will remove all outliers with prices way too high or low from the results.
Example: "false"
Required: No

site_id
Description: The ebay site ID that eBay will use. Different terretories use different sites. To find site ID values, navigate to: https://developer.ebay.com/devzone/finding/callref/Enums/GlobalIdList.html
Example: "0" - United States
Required: No - (defaults to "0")

Each item fetched from the eBay API will display:

Title: The title of the sold item.
Image: The image of the sold item.
Sale Price: The final sale price of the item.
Item Link: A clickable link to the full item description on eBay.
Price Statistics

The app displays the following statistics for the fetched items:

Max Price: The highest price from the fetched items.
Min Price: The lowest price from the fetched items.
Average Price: The average price of all fetched items.
Median Price: The median price of all fetched items.

Technologies Used
JavaScript: For the core functionality of the app.
HTML/CSS: For the basic structure and styling of the web app.
eBay average selling price api: [To fetch the sold items from eBay.](https://rapidapi.com/ecommet/api/ebay-average-selling-price/playground/apiendpoint_c727ff0a-eb1c-468e-bdb1-f85740d0a82f)
