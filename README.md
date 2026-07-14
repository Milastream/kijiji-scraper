[Kijiji Scraper](https://apify.com/memo23/kijiji-scraper?fpr=data)

# Kijiji.ca Scraper

**Empower Your Market Intelligence Pipelines** – Capture, analyze, and monitor Kijiji.ca classified listings at scale with enterprise-grade reliability. Whether you are tracking marketplace trends, monitoring product availability, conducting price research, or aggregating local services, our scraper delivers fresh, structured classified data while minimizing manual effort.

*"From newly posted listings to deep-dive detail pages, we turn Kijiji's classifieds into your competitive advantage."*

## Overview

The Kijiji.ca Scraper is your all-in-one utility for extracting classified data from Kijiji.ca. Ideal for market researchers, price analysts, resellers, and data aggregators, it tracks search result pages and individual listing details across all categories. With straightforward configuration and structured outputs, it's perfect for anyone building marketplace intelligence pipelines or competitive analysis tools.

## What does Kijiji.ca Scraper do?

The Kijiji.ca Scraper is a powerful tool that enables you to:

### Comprehensive Data Collection

- **Listing Search Results**

- Capture structured listing cards from Kijiji.ca search result pages
- Track pagination automatically to cover entire result sets
- Extract metadata such as title, price, location, seller information, and posting date
- **Listing Detail Pages**

- Scrape full descriptions and specifications from individual listings
- Collect seller contact information and communication preferences
- Preserve images, attributes, and listing metadata
- **Market Insights**

- Monitor pricing trends across categories, locations, and product types
- Build time-series datasets to benchmark marketplace activity
- Feed downstream analytics, price monitoring, and inventory tracking workflows

### Advanced Scraping Capabilities

- **Pagination Handling**: Automatically navigates through Kijiji search results
- **Efficient Processing**: Processes only new or updated listings in subsequent runs
- **Change Detection**: Detects new listings and updates to existing ads
- **Incremental Data Collection**: Build comprehensive marketplace datasets over time

### Flexible Scraping Options

- **Listing Search Results**: Extract listings by keywords, location, category, and filters

- Rentals: `https://www.kijiji.ca/b-for-rent/ontario/c30349001l9004`
- Real Estate Sales: `https://www.kijiji.ca/b-real-estate/ontario/c34l9004`
- Cars & Vehicles: `https://www.kijiji.ca/b-cars-vehicles/ontario/honda/k0c27l9004`
- **Individual Listing Details**: Target specific listings using direct URLs

- Rental Listing: `https://www.kijiji.ca/v-apartments-condos/ottawa/specious-4-1-bedroom-alta-vista-home-available-nov-1st/1726015583`
- House for Sale: `https://www.kijiji.ca/v-house-for-sale/norfolk-county/4-season-mobile-home/1719362464`
- Vehicle Listing: `https://www.kijiji.ca/v-cars-trucks/city-of-toronto/2015-honda-civic-ex/1234567890`

This tool is ideal for:

- Market research and competitive pricing analysis
- Product availability monitoring across regions and categories
- Price tracking and trend analysis for resellers
- Building marketplace data pipelines for e-commerce platforms
- Monitoring classified trends for business intelligence

## Features

- **Comprehensive Data Extraction**: Listing metadata, descriptions, images, and seller information
- **Dual Scraping Modes**:

- **Search Results**: Scrape all listings from Kijiji search result pages
- **Individual Listing Details**: Target specific listings using detail URLs
- **Flexible Input**: Supports multiple input formats:

- Search result URLs (keyword, location, category, filters)
- Direct listing detail URLs
- **Automatic Pagination**: Handles multi-page result sets automatically
- **Efficient Processing**: Concurrent scraping with configurable concurrency settings
- **Reliable Performance**: Built-in retries, throttling, and proxy support
- **Structured Data Export**: Download listing data in JSON or CSV for analytics

## Supported Scenario Types

The Kijiji.ca Scraper can extract data from multiple marketplace flows:

1. **Rental Search Results** – Apartments, condos, and houses for rent

- Example: `https://www.kijiji.ca/b-for-rent/ontario/c30349001l9004`
- Fields: `listing_id`, `title`, `price`, `location`, `bedrooms`, `bathrooms`, `posted_date`, `seller_type`, etc.
2. **Real Estate Sales Search** – Houses, condos, and properties for sale

- Example: `https://www.kijiji.ca/b-real-estate/ontario/c34l9004`
- Fields: `listing_id`, `title`, `price`, `location`, `property_type`, `square_footage`, `posted_date`, etc.
3. **Individual Rental Listings** – Full details for a rental property

- Example: `https://www.kijiji.ca/v-apartments-condos/ottawa/specious-4-1-bedroom-alta-vista-home-available-nov-1st/1726015583`
- Fields: `listing_id`, `description`, `images`, `attributes`, `lease_terms`, `utilities`, `seller_details`, `contact_info`, etc.
4. **Individual Sale Listings** – Full details for a property for sale

- Example: `https://www.kijiji.ca/v-house-for-sale/norfolk-county/4-season-mobile-home/1719362464`
- Fields: `listing_id`, `description`, `images`, `attributes`, `property_details`, `seller_details`, `contact_info`, `neighbourhood_info`, etc.
5. **Filtered Category Searches** – Listings narrowed by price range, date posted, or specific attributes

- Rentals with price filter: `https://www.kijiji.ca/b-for-rent/ontario/c30349001l9004?price=1000__2000`
- Sales with price filter: `https://www.kijiji.ca/b-real-estate/ontario/c34l9004?price=200000__500000`
- Fields: `listing_id`, `filter_context`, `price_range`, `category_attributes`, `posting_recency`, etc.

Each scenario returns a structured payload consistent across runs, making it straightforward to pipe into your analytics stack.

## Quick Start

1. **Sign up for Apify**: Create your free account at [apify.com](https://apify.com/).
2. **Find the Scraper**: Search for "Kijiji.ca Scraper" in the Apify Store.
3. **Configure Input**: Set your search URLs or direct listing URLs in the input schema.
4. **Run the Scraper**: Execute the scraper on Apify or locally with Node.js/TSX.
5. **Data Collection**: Export raw listing data as JSON or CSV for downstream processing.

## Sample Output

The scraper provides structured information about Kijiji.ca listings. Below is an example output for a real estate listing:

```
{
    "id": "1724657290",
    "title": "$359,000 - Semi-detached for sale in Gatineau (Masson-Angers)",
    "description": "<p>Charmant semi-détaché à Gatineau secteur Angers, sortie Laurentides de l'autoroute 50.</p>\n<p>3 chambre à coucher dont 2 au rez-de-chaussée et une au sous-sol. Sans voisin arrière.  </p><p>---</p><p>Automatic translation</p><p>Charming semi-detached house in Gatineau Angers sector, exit Laurentides from highway 50.</p>\n<p>3 bedrooms including 2 on the ground floor and one in the basement. No neighbours in the back.</p>",
    "url": "https://www.kijiji.ca/v-house-for-sale/gatineau/359-000-semi-detached-for-sale-in-gatineau-masson-angers/1724657290",
    "activationDate": "2025-09-06T14:13:55.000Z",
    "sortingDate": "2025-10-12T00:23:35.000Z",
    "status": "ACTIVE",
    "endDate": "3000-01-01T00:00:00.000Z",
    "type": "OFFER",
    "categoryId": 35,
    "adSource": "ORGANIC",
    "imageUrls": [
        "https://media.kijiji.ca/api/v1/ca-prod-dealer-ads/images/a9/a93a7048-f217-4348-bd29-1c44c6dad881?rule=kijijica-640-webp",
        "https://media.kijiji.ca/api/v1/ca-prod-dealer-ads/images/ea/ea20f2b9-650c-4b80-a229-40ca3acaf753?rule=kijijica-640-webp",
        "https://media.kijiji.ca/api/v1/ca-prod-dealer-ads/images/2d/2d978c87-3edc-4b3d-8d57-ebed54cf9e6a?rule=kijijica-640-webp",
        "https://media.kijiji.ca/api/v1/ca-prod-dealer-ads/images/5e/5efb9308-fe82-46a6-afc7-9008037524cf?rule=kijijica-640-webp",
        "https://media.kijiji.ca/api/v1/ca-prod-dealer-ads/images/4c/4ca4337a-91db-4117-816a-c63fe3b3f4b6?rule=kijijica-640-webp",
        "https://media.kijiji.ca/api/v1/ca-prod-dealer-ads/images/d1/d1d707e3-80ab-4b35-ac17-5a0608f4761a?rule=kijijica-640-webp"
    ],
    "price": {
        "type": "FIXED",
        "amount": 35900000,
        "currency": "CAD",
        "originalAmount": null
    },
    "attributes": [
        {
            "canonicalName": "numberbathrooms",
            "label": "Bathrooms",
            "canonicalValues": [
                "20"
            ],
            "values": [
                "2"
            ]
        },
        {
            "canonicalName": "numberbedrooms",
            "label": "Bedrooms",
            "canonicalValues": [
                "3"
            ],
            "values": [
                "3"
            ]
        },
        {
            "canonicalName": "forsalebyhousing",
            "label": "For Sale By",
            "canonicalValues": [
                "ownr"
            ],
            "values": [
                "Owner"
            ]
        }
    ],
    "flags": {
        "__typename": "RealEstateListingFlags",
        "categorySpecificBadge": false,
        "highlight": false,
        "hpGallery": null,
        "topAd": false,
        "priceDrop": false,
        "showcase": false,
        "isFromAutosDealer": false,
        "isFromDealer": false,
        "isMoVe": false,
        "isPint": true,
        "isSM360": false,
        "isVerticalCategory": true,
        "comfree": true
    },
    "metrics": {
        "__typename": "ListingMetrics",
        "views": 118
    },
    "location": {
        "id": 1700186,
        "name": "Gatineau",
        "address": "rue des Hauts-Bois, Gatineau (Masson-Angers), QC, J8M 1J3",
        "showPinOnMap": false,
        "coordinates": {
            "latitude": 45.53,
            "longitude": -75.48
        },
        "neighbourhood": {
            "id": "g10_f24742jt",
            "name": "Bassin-de-la-Lièvre",
            "summary": "Bassin-de-la-Lièvre offers a relaxed ambience. Bassin-de-la-Lièvre is very quiet overall, as there isn't a lot of street noise or city clamour.",
            "transportation": "The car is very often the preferred approach to get around in this part of Gatineau. The majority of properties for sale are a short car ride from the nearest highway, such as Autoroute de l'Outaouais, and it is especially convenient to park. However, getting around by transit can be difficult in Bassin-de-la-Lièvre due to the low service level. Nonetheless, homeowners benefit from a few bus lines, and the closest bus stop is usually very close. Getting around by bicycle is difficult in this part of Gatineau because there are a good number of slopes, and the cycling infrastructure is not very comprehensive. Travelling on foot is also not very feasible for house buyers in Bassin-de-la-Lièvre because running common errands is inconvenient.",
            "scores": {
                "__typename": "NeighbourhoodScores",
                "transportation": {
                    "__typename": "TransportationScore",
                    "cycle": {
                        "__typename": "TransportationScoreData",
                        "score": 4,
                        "description": "Not very suitable for bicycle commuting and/or recreational cycling"
                    },
                    "walk": {
                        "__typename": "TransportationScoreData",
                        "score": 2,
                        "description": "Other transportation modes are needed to reach day-to-day needs"
                    },
                    "transit": {
                        "__typename": "TransportationScoreData",
                        "score": 3,
                        "description": "Transit is available for some trips"
                    }
                }
            }
        }
    },
    "poster": {
        "posterId": "1045859411",
        "sellerType": "KMB",
        "websiteUrl": "https://duproprio.com/1112057",
        "phoneNumber": null,
        "profile": null
    },
    "externalSource": {
        "__typename": "ExternalListingSource",
        "sourceProviderId": "9001"
    },
    "rentalBadge": null,
    "virtualTourUrl": null,
    "youtubeVideoId": null,
    "basicInfo": {
        "__typename": "StandardListing",
        "id": "1724657290",
        "title": "$359,000 - Semi-detached for sale in Gatineau (Masson-Angers)",
        "description": "Charmant semi-détaché à Gatineau secteur Angers, sortie Laurentides de l'autoroute 50. 3 chambre à coucher dont 2 au rez-de-chaussée et une au sous-sol. Sans voisin arrière. --- Automatic translation ...",
        "imageCount": 6,
        "imageUrls": [
            "https://media.kijiji.ca/api/v1/ca-prod-dealer-ads/images/a9/a93a7048-f217-4348-bd29-1c44c6dad881?rule=kijijica-200-jpg",
            "https://media.kijiji.ca/api/v1/ca-prod-dealer-ads/images/ea/ea20f2b9-650c-4b80-a229-40ca3acaf753?rule=kijijica-200-jpg",
            "https://media.kijiji.ca/api/v1/ca-prod-dealer-ads/images/2d/2d978c87-3edc-4b3d-8d57-ebed54cf9e6a?rule=kijijica-200-jpg",
            "https://media.kijiji.ca/api/v1/ca-prod-dealer-ads/images/5e/5efb9308-fe82-46a6-afc7-9008037524cf?rule=kijijica-200-jpg",
            "https://media.kijiji.ca/api/v1/ca-prod-dealer-ads/images/4c/4ca4337a-91db-4117-816a-c63fe3b3f4b6?rule=kijijica-200-jpg"
        ],
        "categoryId": 35,
        "url": "https://www.kijiji.ca/v-house-for-sale/gatineau/359-000-semi-detached-for-sale-in-gatineau-masson-angers/1724657290",
        "activationDate": "2025-09-06T14:13:55.000Z",
        "sortingDate": "2025-10-12T00:23:35.000Z",
        "adSource": "ORGANIC",
        "location": {
            "__typename": "RealEstateListingLocation",
            "id": 1700186,
            "name": "Gatineau",
            "address": "rue des Hauts-Bois, Gatineau (Masson-Angers), QC, J8M 1J3",
            "distance": null,
            "nearestIntersection": [
                "Chemin de Montréal Ouest",
                "Rue de la Forteresse"
            ],
            "coordinates": {
                "__typename": "LocationCoordinates",
                "latitude": 45.52827,
                "longitude": -75.48194
            },
            "neighbourhoodInfo": null
        },
        "price": {
            "__typename": "StandardAmountPrice",
            "type": "FIXED",
            "amount": 35900000,
            "originalAmount": null
        },
        "flags": {
            "__typename": "RealEstateListingFlags",
            "categorySpecificBadge": false,
            "priceDrop": false,
            "showcase": false,
            "topAd": false,
            "highlight": false,
            "shippedBySeller": null,
            "isPromotionProvTopAd": null,
            "isPromotionTopAd": null,
            "virtualTour": false
        },
        "posterInfo": {
            "__typename": "PosterInfo",
            "posterId": "1045859411",
            "rating": null
        },
        "attributes": {
            "__typename": "StandardListingAttributes",
            "all": [
                {
                    "__typename": "ListingAttributeV2",
                    "canonicalName": "numberbathrooms",
                    "canonicalValues": [
                        "20"
                    ]
                },
                {
                    "__typename": "ListingAttributeV2",
                    "canonicalName": "numberbedrooms",
                    "canonicalValues": [
                        "3"
                    ]
                },
                {
                    "__typename": "ListingAttributeV2",
                    "canonicalName": "forsalebyhousing",
                    "canonicalValues": [
                        "ownr"
                    ]
                },
                {
                    "__typename": "ListingAttributeV2",
                    "canonicalName": "srpLogoUrl",
                    "canonicalValues": [
                        "https://media.kijiji.ca/api/v1/ca-prod-statics/images/6b/6b7e851a-2668-46f7-9341-2b79daa7fe75?rule=kijijica-60-jpg"
                    ]
                }
            ]
        }
    }
}
```

## Output Fields Explanation

### Core Listing Fields

- **`id`**: Unique Kijiji listing identifier (e.g., `1724657290`).
- **`title`**: Display title of the listing.
- **`description`**: Full HTML description with bilingual content (English/French for Quebec listings).
- **`url`**: Direct link to the listing detail page.
- **`activationDate`**: ISO timestamp when the listing was first posted.
- **`sortingDate`**: ISO timestamp used for search result ordering.
- **`status`**: Current lifecycle state (e.g., `ACTIVE`, `EXPIRED`).
- **`endDate`**: Expiration date of the listing.
- **`type`**: Listing type (e.g., `OFFER`, `WANTED`).
- **`categoryId`**: Numeric category identifier (e.g., `35` for real estate).
- **`adSource`**: Source of the ad (e.g., `ORGANIC`, `DEALER`).

### Media & Images

- **`imageUrls`**: Array of high-resolution image URLs (640px webp format).
- **`virtualTourUrl`**: Link to virtual tour if available.
- **`youtubeVideoId`**: YouTube video ID for listings with video tours.

### Pricing Information

- **`price.type`**: Price type (e.g., `FIXED`, `NEGOTIABLE`, `PLEASE_CONTACT`).
- **`price.amount`**: Price in cents (e.g., `35900000` = $359,000 CAD).
- **`price.currency`**: Currency code (e.g., `CAD`, `USD`).
- **`price.originalAmount`**: Original price if reduced.

### Listing Attributes

- **`attributes`**: Array of category-specific attributes:

- **`canonicalName`**: Internal attribute identifier (e.g., `numberbedrooms`, `numberbathrooms`).
- **`label`**: Human-readable attribute name.
- **`canonicalValues`**: Normalized values for filtering.
- **`values`**: Display values.

### Flags & Badges

- **`flags.topAd`**: Premium placement indicator.
- **`flags.highlight`**: Highlighted listing flag.
- **`flags.priceDrop`**: Price reduction indicator.
- **`flags.showcase`**: Showcase listing flag.
- **`flags.isFromDealer`**: Dealer vs. private seller indicator.
- **`flags.comfree`**: ComFree/DuProprio integration flag.

### Metrics

- **`metrics.views`**: Number of times the listing has been viewed.

### Location Data

- **`location.id`**: Kijiji location identifier.
- **`location.name`**: City/region name.
- **`location.address`**: Full street address.
- **`location.coordinates`**: Latitude and longitude.
- **`location.neighbourhood`**: Detailed neighbourhood information including:

- **`name`**: Neighbourhood name.
- **`summary`**: Neighbourhood description.
- **`transportation`**: Transportation accessibility details.
- **`scores`**: Walk, transit, and cycle scores.

### Seller Information

- **`poster.posterId`**: Unique seller identifier.
- **`poster.sellerType`**: Seller classification (e.g., `FSBO`, `KMB`, `DEALER`).
- **`poster.websiteUrl`**: External website link.
- **`poster.phoneNumber`**: Contact phone number (if available).
- **`poster.profile`**: Seller profile details including name, rating, and listing count.

### External Source

- **`externalSource.sourceProviderId`**: External listing provider ID (e.g., DuProprio, ComFree).

### Basic Info (Search Results)

- **`basicInfo`**: Condensed listing data from search result pages:

- **`imageCount`**: Total number of images.
- **`imageUrls`**: Thumbnail images (200px jpg format).
- **`nearestIntersection`**: Nearest cross streets.
- **`posterInfo.rating`**: Seller rating.

These fields provide comprehensive listing data suitable for market analysis, price tracking, inventory monitoring, and competitive intelligence workflows.

---

## Explore More Scrapers

If you found this Apify Scraper useful, be sure to check out our other powerful scrapers and actors at [memo23's Apify profile](https://apify.com/memo23). We offer a wide range of tools to enhance your web scraping and automation needs across various platforms and use cases.

## Support

- For issues or feature requests, please use the [Issues](https://console.apify.com/actors/B9QxpGHylsP0guHns/issues) section of this actor.
- If you need customization or have questions, feel free to contact the author:

- Author's website: [https://muhamed-didovic.github.io/](https://muhamed-didovic.github.io/)
- Email: [muhamed.didovic@gmail.com](mailto:muhamed.didovic@gmail.com)

## Additional Services

- Request customization or whole dataset: [muhamed.didovic@gmail.com](mailto:muhamed.didovic@gmail.com)
- If you need anything else scraped, or this actor customized, email: [muhamed.didovic@gmail.com](mailto:muhamed.didovic@gmail.com)
- For API services of this scraper (no Apify fee, just usage fee for the API), contact: [muhamed.didovic@gmail.com](mailto:muhamed.didovic@gmail.com)
- Email: [muhamed.didovic@gmail.com](mailto:muhamed.didovic@gmail.com)