 <h2 align="center">
   Data Cleaning Flipkarts Product Dataset using Excel - Power Query
 </h2>

<p align="center">
  <img src="https://github.com/TendaiPhikiso/Flipkart-Data-Cleaning/assets/57633068/cdd87858-ede9-44c2-8c44-4b022114982d" alt="Image">
</p>

## Introduction 

As we delve into the data cleaning process for the Flipkart Product Dataset, this section outlines the steps taken to prepare the data for meaningful analysis. From dropping irrelevant columns to addressing duplicates and managing missing values, each stage was crucial in ensuring a clean and structured dataset.

## Dropped columns

In alignment with the Data Quality Assessment (DQA) documentation, four columns—Column1, _id, product_details, and crawled_at—were removed. The decision to exclude these columns was guided by their lack of relevance for our future analysis.

For instance, the decision to drop the **`_id`** column was based on a deeper analysis of its role as a unique identifier. While initially assumed to be the primary key, further examination, and mentor advice led to the identification of the **`pid`** column as a more efficient primary key.

## Handling duplicates

Duplicates in the pid column were addressed using Power Query's "Remove duplicate" feature, resulting in the removal of 6.4% of duplicated values. Additionally, duplicates within the image column were managed by splitting the column using commas as delimiters, followed by the removal of redundant links.
![Screenshot 2024-01-21 235933](https://github.com/TendaiPhikiso/Flipkart-Data-Cleaning/assets/57633068/aec598e3-058c-456d-83c3-6745135e4240)


## Missing Values

Identification of missing values in various columns prompted distinct strategies.

(1) Text-based Columns (description, brand, seller):

For text-based columns, the "Replace Value" feature was utilized to fill nulls with meaningful placeholders.

- Description: Null values were replaced with "no description."
- Brand and Seller: Null values were replaced with "Other."

(2) Numerical Columns (actual_price, average_rating, discount, selling_price):

For numerical columns, null values were replaced with 0 to ensure clarity and interpretability.

The percentage values for missing data were as follows:

- Brand: 7%
- Actual Price: 3%
- Average Rating: 8%
- Discount: 3%
- Description: 40%
- Seller: 6%
- Selling Price: <1%


## ****Data Standardization****

Ensuring consistent data formats, key columns like Discount, actual_price, and selling_price underwent standardization. The Discount column transitioned from text to percentage format for analytical ease, while actual_price and selling_price were formatted into currency, incorporating the Indian Rupee symbol (₹) to prevent misinterpretation in future financial calculations & analysis.

Standardizing data formats ensures consistency and facilitates numerical operations, enabling accurate analysis.

## Incomplete Data 

The “brand” column presented incomplete brand names, addressed by utilizing the “url” column to extract brand names between two delimiters. While effective in most cases, challenges arose with multi-word brand names. The **`seller`** column underwent multiple cleaning processes, including delimiting and value replacement, to ensure accurate and uniform data within the column. 

## **Conclusion**

In conclusion, the data cleaning process applied to the Flipkart product dataset involved thoughtful decision-making and the utilization of Power Query's diverse features. Each step was driven by a clear rationale, ensuring that the dataset is prepared for analysis. The experience highlighted the importance of meticulous data handling practices for meaningful insights.
