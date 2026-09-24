# 🏠 Airbnb Market Place Analysis Dashboard

## 📌 Project Overview

This project analyzes Airbnb listing data using **Python/Pandas for data cleaning and preparation** and **Power BI for interactive data visualization**.

The project includes:

- Raw Airbnb dataset
- Data cleaning and preprocessing
- Cleaned dataset
- Exploratory analysis
- Interactive Power BI dashboard
- Business insights from listings, pricing, reviews, ratings, and availability

---

# 🎯 Project Objective

The main objective of this project is to analyze the Airbnb marketplace and understand:

- Airbnb listing distribution
- Pricing patterns
- Room types
- Neighbourhoods
- Customer reviews and ratings
- Property availability
- Cancellation policies
- Host verification
- Instant booking

The cleaned data was used to create a **3-page Power BI dashboard**.

---

# 📂 Dataset Information

## 1. Before Cleaning – Raw Dataset

**File:** `Airbnb_Open_Data.csv`

### Dataset Size

| Information | Before Cleaning |
|---|---:|
| Rows | 102,599 |
| Columns | 26 |
| Duplicate Rows | 541 |
| Duplicate IDs | 541 |
| Missing Values | Present |
| Data Types | Mixed |
| Price Format | `$` values stored as text |
| Service Fee Format | `$` values stored as text |
| Date Format | Required conversion |
| Unnecessary Columns | `house_rules`, `license` |

### Main Columns

```text
id
NAME
host id
host_identity_verified
host name
neighbourhood group
neighbourhood
lat
long
country
country code
instant_bookable
cancellation_policy
room type
Construction year
price
service fee
minimum nights
number of reviews
last review
reviews per month
review rate number
calculated host listings count
availability 365
house_rules
license

🧹 Data Cleaning & Preprocessing

The raw dataset was cleaned and prepared before creating the Power BI dashboard.

Cleaning Steps
Checked missing values.
Checked duplicate records and duplicate IDs.
Removed records outside the required price range.
Removed records with missing price values.
Removed records with missing service fee values.
Removed duplicate listing IDs.
Removed unnecessary columns such as house_rules and license.
Converted price and service fee from text format to numerical format.
Converted date fields into proper date format.
Converted numerical columns into appropriate integer/float formats.
Filled remaining missing categorical values using the most frequent value.
Filled remaining missing numerical values using median values.
Filled missing date values using the most frequent date.
Validated the final dataset before importing it into Power BI.


🔄 Before vs After Cleaning
Feature	Before Cleaning	After Cleaning
Rows	102,599	83,813
Columns	26	25
Duplicate Rows	541	0
Missing Values	Many columns	Only 20 remaining
Price	Text with $	Numeric
Service Fee	Text with $	Numeric
Minimum Nights	Float	Integer
Number of Reviews	Float	Integer
Construction Year	Float	Integer
Review Rating	Float	Integer
Availability	Float	Integer
Last Review	Text/Object	Date
Instant Bookable	Text	Boolean
Unnecessary Columns	house_rules, license present	Removed
Power BI Ready	No	Yes


📉 Records Removed During Cleaning
The raw dataset contained records that were not suitable for the final analysis.
Price Filtering

The raw dataset contained:

17,903 records with price greater than 999
247 records with missing price

The final dataset was restricted to the price range:
50 – 999
Service Fee

Records with missing service fee were excluded during the final preparation.

Duplicate Records
Duplicate listing IDs were removed so that each listing appears only once in the cleaned dataset.

Final Dataset
After applying the cleaning, filtering, and duplicate-removal steps:
102,599 rows → 83,813 rows

🧩 Missing Value Treatment

Remaining missing values were handled according to the data type.
Categorical Columns
Missing categorical values were replaced using the most frequent value (mode).

Examples:

host_identity_verified → unconfirmed
neighbourhood_group → Manhattan
country → United States
country_code → US
host_name → Michael
Numerical Columns

Missing numerical values were replaced using median values.

Examples:

construction_year → 2012
minimum_nights → 3
number_of_reviews → 7
reviews_per_month → 0.74
review_rate_number → 3
calculated_host_listings_count → 1
availability_365 → 96
Date Column

Missing values in last_review were filled using the most frequent date:
2019-06-23

📊 After Cleaning – Final Dataset

File: After cleaning.xlsx

Final Dataset Size
83,813 rows
25 columns
0 duplicate rows
Proper numerical data types
Proper date format
Clean categorical values
Ready for Power BI analysis
Columns Used
id
name
host_id
host_identity_verified
host_name
neighbourhood_group
neighbourhood
lat
long
country
country_code
instant_bookable
cancellation_policy
room_type
construction_year
price
service_fee
minimum_nights
number_of_reviews
last_review
reviews_per_month
review_rate_number
calculated_host_listings_count
availability_365


📊 Power BI Dashboard

The cleaned dataset was used to create a 3-page interactive Power BI dashboard.

Page 1 – Airbnb Market Place Overview

Shows:

Total Listings
Average Price
Average Rating
Total Reviews
Top Neighbourhoods
Price Distribution
Listings by Location
Room Type Distribution
Listings by Neighbourhood Group

Slicers:

room_type
neighbourhood
Page 2 – Pricing & Listing Analysis

Shows:

Minimum Price
Maximum Price
Average Price
Average Minimum Nights
Average Price by Neighbourhood Group
Average Price by Room Type
Price vs Minimum Nights
Listings by Neighbourhood
Cancellation Policy by Room Type

Slicers:

cancellation_policy
price
room_type
Page 3 – Reviews, Ratings & Availability

Shows:

Average Rating
Total Reviews
Average Reviews per Listing
Average Availability
Rating by Room Type
Reviews by Neighbourhood Group
Availability by Neighbourhood Group
Reviews vs Rating
Host Identity Verification
Instant Bookable Analysis

Slicers:

instant_bookable
host_identity_verified
room_type
availability_365


🛠️ Tools & Technologies
Python
Pandas
Microsoft Excel
Power BI
Power Query
GitHub
