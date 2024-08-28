# Ukrainian Apartment Price Prediction and Visualization

This project aims to predict apartment prices in Ukraine using a dataset containing information about various apartment features. The predicted prices are then visualized on an interactive map, with colors and markers representing different price ranges.

## Project Overview

The main objectives of this project are:

1. **Data Collection**: Use a dataset containing details about apartments, including address, price, number of rooms, square footage, and additional features.
2. **Geocoding**: Convert apartment addresses into latitude and longitude coordinates using OpenStreetMap's Nominatim service.
3. **Data Analysis and Prediction**: Analyze the data to understand the factors affecting apartment prices and implement a predictive model.
4. **Visualization**: Create an interactive map using Folium to visualize apartment locations based on their prices.

## Dataset

The dataset used for this project is called **House Pricing in Ukraine**, and it provides various details about apartments for sale across Ukraine. The dataset was sourced from Kaggle.

- **Dataset Name**: [House Pricing in Ukraine](https://www.kaggle.com/datasets/vovabunga/house-pricing-in-ukraine)
- **Source**: Kaggle, contributed by Vovabunga

The dataset used for this project contains the following columns:

- `title`: The street name or specific address of the apartment.
- `price`: The price of the apartment.
- `squer`: The square footage of the apartment.
- `room`: Number of rooms in the apartment.
- `city`: The city where the apartment is located.
- `addres`: Additional address information, if available.
- `floor`: The floor number of the apartment.
- `metr`: Additional metric data about the apartment.
- `new_rem`: Boolean indicating if the apartment is a new or a remodeled one.
- `auction`: Boolean indicating if the apartment is up for auction.
- `quiet_area`: Boolean indicating if the apartment is in a quiet area.
- `furniture`: Boolean indicating if the apartment comes with furniture.
- `center`: Boolean indicating if the apartment is near the city center.
- `parking`: Boolean indicating if the apartment includes a parking space.

### Sample Data

```plaintext
| title                        | price   | squer | room | city | addres                | floor | metr | new_rem | auction | quiet_area | furniture | center | parking |
|------------------------------|---------|-------|------|------|-----------------------|-------|------|---------|---------|------------|-----------|--------|---------|
| вул. Віри Надії Любові       | 120000  | 77    | 2    | Львів| Шевченківський\n ·    | 4     | 1527 | 1       | 0       | 0          | 0         | 0      | 0       |
| вул. Любінська               | 55000   | 44    | 2    | Львів| Залізничний\n ·       | 1     | 1259 | 0       | 0       | 1          | 0         | 0      | 0       |
```

## Getting Started
Prerequisites
To run this project, you will need to have the following installed:

Python 3.6 or higher
Required Python packages listed in requirements.txt
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/ukraine-apartment-price-prediction.git
cd ukraine-apartment-price-prediction
Create a virtual environment and activate it:

bash
Copy code
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
Install the required packages:

bash
Copy code
pip install -r requirements.txt

## Dataset Preparation
Make sure your dataset is in the correct format as described above. Save it as apartments.csv in the project directory.
Use the full_address column for geocoding, which combines title and city to create a full address string.

### Notes:

1. **User-Agent**: When using OpenStreetMap's Nominatim service for geocoding, ensure you set a proper `User-Agent` to comply with the service's usage policy.
2. **Data Cleaning**: Ensure that the address data is cleaned and formatted properly for accurate geocoding.
3. **Rate Limiting**: Be mindful of the rate limits when using free services like Nominatim.
4. **Dependencies**: Ensure `requirements.txt` includes all necessary packages like `pandas`, `geopy`, `folium`, and `scikit-learn`.

This `README.md` provides an overview, installation instructions, usage, and a brief description of the project's objectives and code structure, which should help users understand and work with the project effectively.
