# Sales Data Analysis

## Overview
This project analyzes sales data to identify key trends in revenue, product categories, and order status distribution. The dataset includes transaction details such as SKU, category, revenue, order status, and date of purchase. The analysis aims to provide insights into product performance and seasonal trends.

## Getting the Data  
This project uses the **"Unlock Profits with E-Commerce Sales Data"** dataset from Kaggle. Since the files are too large to upload to GitHub, follow these steps to download and extract them:

1. **Download the dataset manually:**  
   - Visit [this Kaggle dataset](https://www.kaggle.com/datasets/thedevastator/unlock-profits-with-e-commerce-sales-data).  
   - Click **Download** to get the ZIP file.  

2. **Move the ZIP file to your project directory.**  
   - Ensure the file is named **`unlock-profits-with-e-commerce-sales-data.zip`** for consistency.  

3. **Extract the ZIP file into the `csvs` folder:**  
   Run the following Python script to extract the files:  

   ```python
   import zipfile
   import os

   zip_path = "unlock-profits-with-e-commerce-sales-data.zip"
   extract_folder = "csvs"

   os.makedirs(extract_folder, exist_ok=True)

   with zipfile.ZipFile(zip_path, 'r') as zip_ref:
       zip_ref.extractall(extract_folder)

   print(f"Extracted files to {extract_folder}")
   ```

4. **Verify the extracted CSV files**  
   The dataset should now be available in the `csvs` folder, ready for analysis.  

## Data Cleaning and Processing
- **Standardized SKU names**: Ensured consistency across different datasets.
- **Handled missing values**: Removed or filled missing values where necessary.
- **Converted numeric and date values**: Ensured proper formatting for accurate analysis.
- **Grouped minor categories**: Combined small sales categories into "Other" for clarity.

## Key Findings

### Sales by Category
The revenue distribution among product categories shows clear dominance in a few key areas:
- **Set**: Just below $40 million, making it the highest revenue-generating category.
- **Kurta**: Around $20 million, showing strong performance.
- **Western Dress**: Slightly above $10 million.
- **Top**: Around $5 million.
- **All Other Categories**: Less than $2.5 million combined.

This indicates that "Set" and "Kurta" products are the primary drivers of revenue, while other categories contribute relatively smaller shares.

### Order Status Distribution
The majority of orders follow a predictable fulfillment pattern:
- **Shipped**: 60.3% of orders.
- **Shipped - Delivered to Buyer**: 22.3%.
- **Cancelled**: 14.2%.
- **Other**: 3.2%.

The cancellation rate of 14.2% is noteworthy and could indicate potential issues with order fulfillment, customer satisfaction, or inventory management.

### Monthly Sales Trends
A significant increase in revenue was observed from March to April:
- **March**: Near $0 revenue, indicating either a lack of recorded sales or a slow start.
- **April**: A massive surge to just below $30 million.
- **May**: A slight dip, but still above $25 million.
- **June**: Continued decline, nearing $24 million.

This suggests a strong seasonal or promotional influence driving April's sales. The decline in May and June could indicate either market saturation, reduced promotions, or other external factors.

## Recommendations
1. **Focus on high-performing categories**: Since "Set" and "Kurta" drive most revenue, expanding product lines or marketing efforts for these categories could further increase profitability.
2. **Address cancellation rates**: Investigate reasons behind the 14.2% cancellation rate to improve customer experience and order fulfillment.
3. **Analyze seasonal trends**: Determine what caused the sharp increase in April and plan future campaigns accordingly to sustain higher revenue levels.

## Future Work
- **Deep dive into customer behavior**: Analyzing buyer demographics and repeat purchases.
- **Assess impact of promotions**: Identify whether marketing campaigns influenced the sales spike.
- **Inventory and supply chain analysis**: Optimize stock levels based on category performance.

This analysis provides a foundational understanding of sales performance and sets the stage for more granular insights into consumer trends and business strategies.

