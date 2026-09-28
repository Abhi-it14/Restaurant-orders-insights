Here’s a more professional, polished version of your README that keeps your original structure and template while improving clarity, grammar, and readability.

Restaurant Orders and Insights Project

# Restaurant Orders and Insights Project

## Project Description

An exploratory analysis of restaurant sales and customer satisfaction using order data from a food delivery platform. The objective is to identify factors influencing restaurant revenue and customer ratings by analyzing key dimensions such as restaurants, delivery zones, cuisines, delivery time, and food quality.

## Datasets

The dataset contains 500 orders across 20 restaurants on a food delivery platform, recorded on a single day (01/01/2022). It consists of two relational datasets: one containing order details and the other containing restaurant information. Both datasets are linked through the `restaurant_id` key.

* **Source:** [Kaggle – Restaurant Order Details](https://www.kaggle.com/datasets/mohamedharris/restaurant-order-details) (original dataset not created by me).

* The datasets were intentionally modified to introduce data quality issues for cleaning and preprocessing.

---

## Technologies Used

* Kaggle

* Microsoft Excel

* PostgreSQL

* Power BI

* GitHub

---

## Project Files

All project files are organized into the following folders in the GitHub repository:

**/dashboard**

* `dashboard_screenshot.png`

* `restaurant_orders_dashboard.pbix`

**/data**

* `dirty_orders.csv`

* `dirty_restaurants.csv`

**/images**

* `cleaned_orders_table.png`

* `cleaned_restaurants_table.png`

* `dashboard_screenshot.png`

* `dirty_orders_table.png`

* `dirty_restaurants_table.png`

* `q1a.png`

* `q2a.png`

* `q3a.png`

* `q4a.png`

* `q4b.png`

* `q5a.png`

**/sql**

* `01_clean_restaurants.sql`

* `02_clean_orders.sql`

* `03_rank_restaurants_by_revenue.sql`

* `04_avg_customer_food_rating.sql`

* `05_revenue_per_zone.sql`

* `06_avg_per_cuisine.sql`

* `07_restaurants_per_cuisine.sql`

* `08_order_delivery_speed.sql`

* `README.md`

---

## Data Cleaning

### Dirtying Changes Made

| Column                                             | Change                                      |
| -------------------------------------------------- | ------------------------------------------- |
| `restaurant_name`, `payment_mode`                  | Added leading and trailing spaces           |
| `cuisine`, `payment_mode`                          | Introduced inconsistent casing              |
| `order_date`                                       | Mixed date formats using slashes and dashes |
| `customer_rating_food`, `customer_rating_delivery` | Removed selected values                     |

### Cleaning Changes Made

* Standardized text fields such as `cuisine`, `payment_mode`, and `zone` using appropriate text data types (`VARCHAR`).

* Stored numerical fields, including `order_amount` and customer rating columns, as integers, as the dataset contained whole-number values.

* Converted `order_date` to the `DATE` data type.

* Replaced blank customer rating values with `NULL` to represent missing data appropriately.

---

## Analysis Questions

* **Q1a.** Which restaurants generated the highest revenue, and how does revenue relate to the number of fulfilled orders?

* **Q2a.** Is there a relationship between customer food ratings and restaurant sales performance?

* **Q3a.** How does restaurant performance vary across the four delivery zones?

* **Q4a.** Which cuisines generate the highest average order value, and how do they compare in terms of customer food satisfaction?

* **Q4b.** Is there a relationship between cuisine types and the number of restaurants offering them?

* **Q5a.** Does delivery speed influence customer food ratings?

---

## Key Insights

* **Q1a: Restaurant Revenue and Order Volume**
  Veer Restaurant generated the highest revenue of £19,168 from 29 orders, exceeding The Cave Hotel, which fulfilled 32 orders. The Taste ranked 13th in revenue despite fulfilling only 18 orders, generating £12,982. These findings highlight the role of average order value in driving restaurant revenue beyond order volume alone.

* **Q2a: Food Ratings and Sales Performance**
  Vrinda Bhavan recorded the highest average food rating of 3.85 but the lowest total sales of £9,772 among the 20 restaurants. In contrast, Veer Restaurant ranked 19th in average food rating, with a score of 3.0, while generating the highest revenue of £19,168. The findings suggest no clear relationship between average food ratings and total restaurant sales in this dataset.

* **Q3a: Zone-Wise Restaurant Performance**
  Zone D had the highest restaurant count, with 9 restaurants, and generated the highest total sales of £128,163. Zones A and C each had 3 restaurants, generating £40,833 and £53,074 in total sales, respectively. Zone C recorded the highest average restaurant sales of £617.14, indicating that individual restaurant performance can vary across zones regardless of restaurant count.

* **Q4a: Cuisine-Wise Average Order Value and Satisfaction**
  Arabian cuisine recorded the highest average order value of £664.88, along with an average food rating of 3.14. African cuisine had the highest average food rating of 3.5 but ranked fifth in average order value. The results suggest that higher average order values do not necessarily correspond to higher food satisfaction.

* **Q4b: Cuisine Representation and Spending Patterns**
  Less represented cuisines, such as Arabian, Belgian, and Continental, generally recorded higher average order values than more widely represented cuisines, including North Indian, Chinese, and South Indian.

* **Q5a: Delivery Speed and Food Ratings**
  Slow deliveries recorded the highest average food rating of 3.38, followed by medium-speed deliveries at 3.36 and quick deliveries at 3.22. The differences were relatively small, suggesting that delivery speed may have a limited association with food ratings in this dataset.

---

## Dashboard

A Power BI dashboard was developed to visualize the findings from the SQL analysis. Each chart corresponds to a business question, with interactive filters enabling users to explore performance across different cuisines and delivery zones.

---

## Conclusion and Recommendations

The analysis indicates that restaurant revenue is influenced by factors beyond order volume, as some restaurants generated substantial sales from fewer orders through higher average order values. Food ratings showed no clear relationship with total sales, suggesting that other factors, such as pricing, customer preferences, and restaurant positioning, may also contribute to sales performance.

Zones with more restaurants generated higher overall sales, while some zones with fewer restaurants demonstrated strong average performance. Less represented cuisines generally recorded higher average order values, highlighting potential opportunities to explore niche cuisine segments and evaluate their growth potential.

Delivery speed showed only small differences in average food ratings, suggesting that factors such as food quality, preparation standards, packaging, and pricing may also influence customer satisfaction.

---

## Project Limitation

The analysis is based on 500 orders across 20 restaurants recorded on a single day. Therefore, the findings represent a limited snapshot of restaurant activity and may not reflect long-term sales trends, customer preferences, or overall business performance.

---

## Next Steps

This project was primarily developed to demonstrate SQL proficiency and the ability to structure data analysis around business-relevant questions.

Future improvements could include:

* Analyzing data collected over a longer period to identify trends and seasonal patterns.

* Incorporating additional metrics, such as repeat purchases, discounts, and restaurant operating hours.

* Exploring relationships between pricing, customer satisfaction, delivery performance, and revenue.

* Expanding the dataset to improve the reliability and generalizability of the findings.

