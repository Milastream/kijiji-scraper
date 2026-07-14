[Kijiji Scraper](https://apify.com/caprolok/kijiji-scraper?fpr=data)

# 🛒 Kijiji Scraper

The **Kijiji Scraper** is designed to extract detailed listings, including titles, prices, descriptions, and other key data points from Kijiji. This scraper is ideal for buyers, sellers, market researchers, and anyone looking to analyze Kijiji listings based on search criteria such as category, location, and price filters.

## 🚀 Features

- **Comprehensive Data Extraction**: Extracts detailed listing information such as titles, prices, descriptions, and more.
- **Customizable Search**: Allows you to search Kijiji listings based on keywords, category, and location.
- **Scalability**: Scrapes a maximum number of listings at once.
- **Pagination Support**: Automatically handles pagination to scrape multiple pages of listings.

## 🔍 Scraped Data

The scraper extracts a wide range of data points from Kijiji listings, including:

- **Title**: Title of the listing.
- **Price**: Price of the item or service.
- **Location**: City/Area where the listing is located.
- **Description**: Detailed description of the listing.
- **Images**: URLs of images associated with the listing.
- **Category**: Category of the listed item.
- **Posted Date**: Date when the listing was posted.
- **Seller Information**: Name or contact information of the seller.
- **Vehicle-specific Information**: For car listings, includes additional details like model, year, brand, color, and body type.

## 📋 Input Parameters

| Field | Description | Example Input |
| --- | --- | --- |
| **startUrls** | Array of Kijiji URLs to scrape listings from | `["https://www.kijiji.ca/"]` |
| **query** | Keywords for the item or service you're searching for | `"laptops, cars, apartments"` |
| **category** | The category to narrow the search (e.g., Cars & Vehicles) | `"Cars & Vehicles"` |
| **location** | Specify the city, state, or area for the Kijiji search | `"Toronto, Ontario, Canada"` |
| **max_results** | Maximum number of listings to scrape | `100` |

## 📊 Sample Input

```
{
  "startUrls": ["https://www.kijiji.ca/"],
  "query": "laptops, cars, apartments",
  "category": "Cars & Vehicles",
  "location": "Toronto, Ontario, Canada",
  "max_results": 100
}
```

## 📊 Output Format

The scraper returns a structured dataset with the following fields for each Kijiji listing:

| Field | Description |
| --- | --- |
| **listing_id** | Unique identifier for the listing on Kijiji |
| **title** | Title of the listing |
| **description** | Description of the listed item |
| **price** | Price of the item in the specified currency |
| **location** | Geographic location of the listing |
| **posted_date** | Date when the listing was posted |
| **category** | Category of the listed item |
| **url** | Direct URL to the Kijiji listing |
| **seller_name** | Name of the seller or entity offering the product |
| **images** | Array of URLs to the images of the listed item |
| **car_title** | Title of the car (for vehicle listings) |
| **date_posted** | Date the listing was posted |
| **vehicle_model_date_year** | Year of the vehicle model |
| **vehicle_brand** | Brand of the vehicle |
| **vehicle_model** | Model of the vehicle |
| **vehicle_configuration** | Configuration details of the vehicle |
| **vehicle_color** | Color of the vehicle |
| **body_type** | Body type of the vehicle |
| **vehicle_overview_details** | Array of additional vehicle details |
| **vehicle_description** | Detailed description of the vehicle |

### Example Output

```
{
  "car_title": "2015 Honda Civic",
  "date_posted": "2024-09-24",
  "vehicle_model_date_year": "2015",
  "vehicle_brand": "Honda",
  "vehicle_model": "Civic",
  "vehicle_configuration": "LX Sedan",
  "vehicle_color": "Silver",
  "body_type": "Sedan",
  "vehicle_overview_details": [
    "Automatic transmission",
    "4-cylinder engine",
    "Front-wheel drive",
    "100,000 km"
  ],
  "vehicle_description": "Well-maintained 2015 Honda Civic LX Sedan for sale...",
  "price": "$15,000",
  "location": "Toronto, Ontario",
  "images": [
    "https://example.com/image1.jpg",
    "https://example.com/image2.jpg"
  ],
  "url": "https://www.kijiji.ca/item123457"
}
```

## 🛠️ Customizable Scraping Options

- **Location**: Input specific cities or areas for targeted searches.
- **Search Terms**: Customize the search terms to refine the results.
- **Category**: Select the category to narrow down the search.
- **Pagination**: Automatically handles pagination to scrape all available listings.

## 📊 Use Cases

- **Market Research**: Gather data for market research on product availability and pricing.
- **Competitor Analysis**: Analyze competitors' offerings in specific categories.
- **Investment Analysis**: Evaluate listings for potential investment opportunities.
- **Personal Shopping**: Compare and analyze listings for personal purchases.
- **Automotive Market Analysis**: Detailed insights into vehicle listings, including specifications and pricing trends.

## 🆘 Support

If you encounter any issues or need assistance with the Kijiji Scraper, feel free to reach out via the Issues tab on the actor's page. Our support team is here to assist with any concerns or questions you may have.

## 📄 Summary of Key Sections

- **Features and Scraped Data:** Aligned with Kijiji’s offerings.
- **Input Parameters:** Clearly defined to match your Kijiji input schema.
- **Output Format:** Described in a table format for clarity.
- **Performance, Customizable Options, and Use Cases:** Focused on practical applications of the scraper.