# Case Study 1: Amazon Product Review Analysis

## 1. Project Overview
You are working as a Junior Data Analyst at RetailTech Insights, a company that provides e-commerce analytics solutions to sellers on platforms like Amazon. Your team has been tasked with analysing product and customer review data to generate insights that can guide product improvement, marketing strategies, and customer engagement.

## 2. Dataset Description
The dataset contains information scraped from Amazon product pages, including:
* Product details: name, category, price, discount, and ratings
* Customer engagement: user reviews, titles, and content
* Each row represents a unique product, with aggregated reviewer data stored as comma-separated values
Total Records: 1,465 rows TotalFields: 16columns

## 3. Analysis Tasks & Findings

#### Question 1: What is the average discount percentage by product category?

* **Methodology/Approach:** Utilized an Excel Pivot Table. 'Product Category' was placed in the Rows area, and 'Discount (%)' was placed in the Values area, set to show the 'Average'.

* **Result:**
    ```
    Row Labels                 Average of Discount (%)
    -------------------------  -----------------------
    Car & Motorbike            41.52
    Computers & Accessories    55.24
    Electronics                52.33
    Health & Personalcare      52.68
    Home & Kitchen             40.12
    Homeimprovement            57.95
    Musicalinstruments         45.81
    Officeproducts             12.36
    Toys & Games               0.00
    Grand Total                49.52
    ```

* **Insight/Interpretation:**
    The average discount percentage varies significantly across product categories. **"Homeimprovement"** products lead with the highest average discount (57.95%), followed closely by **"Computers & Accessories"** (55.24%), "Health & Personalcare" (52.68%), and "Electronics" (52.33%). This suggests aggressive pricing strategies or competitive markets within these categories.
    In contrast, **"Toys & Games"** are listed with no average discount (0.00%), and **"Officeproducts"** have a very low average discount (12.36%). This could indicate stronger pricing power, lower competitive pressure, or a different sales strategy for these categories. Sellers might be using discounts strategically to move inventory or attract customers in specific high-discount categories.




#### Question 2: How many products are listed under each category?

* **Methodology/Approach:** Utilized an Excel Pivot Table. 'Product Category' was placed in the Rows area, and 'product_name' was placed in the Values area, set to show the 'Count'.

* **Result:**
    ```
    Row Labels                 Count of product_name
    -------------------------  ---------------------
    Car & Motorbike            1
    Electronics                598
    Health & Personalcare      1
    Home & Kitchen             448
    Homeimprovement            2
    Musicalinstruments         2
    Officeproducts             31
    Toys & Games               1
    Grand Total                1084
    ```

* **Insight/Interpretation:**
    The product listing count varies dramatically across categories. **"Electronics"** dominates with 598 products, followed by **"Home & Kitchen"** with 448 products. These two categories represent the vast majority of products in the dataset, indicating they are core offerings for sellers.
    Conversely, several categories like "Car & Motorbike," "Health & Personalcare," "Toys & Games," and "Musicalinstruments" have only 1 or 2 products listed. This could suggest either niche offerings, unexploited market potential, or potentially incomplete data for these categories. "Officeproducts" has a moderate presence with 31 products. This distribution highlights KMS's current focus areas and potential gaps in product diversification.




#### Question 3: What is the total number of reviews per category?

* **Methodology/Approach:** Utilized an Excel Pivot Table. 'Product Category' was placed in the Rows area, and 'rating_count' was placed in the Values area, set to show the 'Sum'.

* **Result:**
    ```
    Row Labels                 Sum of rating_count
    -------------------------  -------------------
    Car & Motorbike            1118
    Electronics                18919709
    Health & Personalcare      3663
    Home & Kitchen             2991069
    Homeimprovement            8566
    Musicalinstruments         88882
    Officeproducts             149675
    Toys & Games               15867
    Grand Total                22178549
    ```

* **Insight/Interpretation:**
    The total number of reviews per category dramatically highlights customer engagement levels. **"Electronics"** absolutely dominates with over 18.9 million reviews, reinforcing its position as the most popular and actively reviewed product category. **"Home & Kitchen"** follows as a distant second with nearly 3 million reviews.

    Categories like "Car & Motorbike," "Health & Personalcare," and "Toys & Games" have very low review counts, which correlates with their low product counts (as seen in Question 2). This indicates either very low customer engagement, niche products with limited reach, or possibly less popular items within those categories. The high review volume in "Electronics" suggests a highly active customer base and strong product visibility within that segment, offering valuable feedback for product improvement and marketing strategies.



#### Question 4: Which products have the highest average ratings?

* **Methodology/Approach:** Utilized an Excel Pivot Table. 'product_name' was placed in the Rows area, and 'rating' was placed in the Values area, set to show the 'Average'. The results were then sorted in descending order by 'Average of rating'.

* **Result:**
    ```
    Row Labels         Average of rating
    -----------------  -----------------
    Instant            4.80
    Oratech            4.80
    Swiffer            4.80
    Campfire           4.70
    FIGMENT            4.70
    Multifunctional    4.70
    Grand Total        4.75
    ```

* **Insight/Interpretation:**
    Several products stand out with exceptionally high average ratings. **"Instant," "Oratech," and "Swiffer"** achieved the highest average rating of **4.80**. Close behind were "Campfire," "FIGMENT," and "Multifunctional" with an average rating of 4.70. This indicates strong customer satisfaction and positive product experiences for these specific items.
    These highly-rated products represent a significant asset for RetailTech Insights' clients. Further analysis into what makes these products so successful (e.g., specific features, unique selling propositions, effective marketing, quality of customer support) could provide valuable lessons to apply to other products or categories, potentially improving overall ratings and customer loyalty.



#### Question 5: What is the average actual price vs the discounted price by category?

* **Methodology/Approach:** First, a calculated column for 'Discounted Price' was created using the formula `actual_price * (1 - discount_percentage)`. Then, an Excel Pivot Table was used with 'Product Category' in the Rows area, and 'actual_price' and 'discounted_price' were placed in the Values area, both set to show the 'Sum'.

* **Result:**
    ```
    Row Labels                 Sum of actual_price    Sum of discounted_price
    -------------------------  ---------------------  -----------------------
    Car & Motorbike            ₹ 4,000.00             ₹ 2,339.00
    Computers & Accessories    (Missing)              (Missing)
    Electronics                ₹ 5,771,176.00         ₹ 3,313,008.00
    Health & Personalcare      ₹ 1,900.00             ₹ 899.00
    Home & Kitchen             ₹ 1,864,609.00         ₹ 1,044,115.81
    Homeimprovement            ₹ 1,598.00             ₹ 674.00
    Musicalinstruments         ₹ 2,694.00             ₹ 1,276.00
    Officeproducts             ₹ 12,313.00            ₹ 9,349.00
    Toys & Games               ₹ 150.00               ₹ 150.00
    Grand Total                ₹ 7,658,440.00         ₹ 4,371,810.81
    ```
    *Note: "Computers & Accessories" category shows missing values for sum of prices, which could indicate no products found or data issues for this specific metric.*

* **Insight/Interpretation:**
    This analysis reveals the significant impact of discounts on potential revenue across categories. Overall, the total actual price of products is **₹7,658,440.00**, but after discounts, the total discounted price drops to **₹4,371,810.81**, representing a substantial reduction in potential revenue.

    **"Electronics"** shows the largest absolute difference between actual and discounted prices (approx. ₹2.46 million), reflecting its high volume and significant average discount (as seen in Question 1). **"Home & Kitchen"** also has a large difference (approx. ₹0.82 million). This indicates that while discounts in these categories are effective in driving sales, they also significantly impact the immediate revenue intake.

    Categories like **"Toys & Games"** show no difference, as they have 0% average discount, and "Officeproducts" show a minimal difference, aligning with their low discount percentages. Sellers need to balance the attraction of discounts with their impact on overall profitability, especially in high-volume, heavily discounted categories.



#### Question 6: Which products have the highest number of reviews?

* **Methodology/Approach:** Utilized an Excel Pivot Table. 'product_name' was placed in the Rows area, and 'rating_count' was placed in the Values area, set to show the 'Sum'. The results were then sorted in descending order by 'Sum of rating_count'.

* **Result:**
    ```
    Row Labels         Sum of rating_count
    -----------------  -------------------
    boAt               4096773
    AmazonBasics       1890192
    Redmi              1968957
    JBL                1261283
    Samsung            1211218
    Amazon             906576
    MI                 891734
    Noise              849566
    SanDisk            832341
    Fire-Boltt         771787
    Grand Total        14680427
    ```

* **Insight/Interpretation:**
    The analysis of review counts by product name reveals the most popular and highly engaged products. **"boAt"** stands out significantly with over 4 million reviews, making it the product with the highest customer engagement. Other products with a very high number of reviews include **"Redmi"**, **"AmazonBasics"**, **"JBL"**, and **"Samsung"**, each exceeding 1 million reviews.

    These products are highly visible and trusted by a large customer base. For RetailTech Insights' clients, these products represent strong performers that can be leveraged in marketing campaigns, used as benchmarks for product development, or serve as anchor products to drive traffic and cross-selling opportunities. The sheer volume of reviews for these products also provides a rich source of customer feedback for product refinement and service improvement.



#### Question 7: How many products have a discount of 50% or more?

* **Methodology/Approach:** A calculated field or helper column was created to categorize products based on whether their 'Discount (%)' was 50% or more (Yes/No). An Excel Pivot Table was then used to count the occurrences within these 'Yes' and 'No' categories.

* **Result:**
    ```
    Row Labels      Count of Discount (%)2      Count of Discount (%)
    --------------  --------------------------  ---------------------
    Yes             497                         45.85%
    No              587                         54.15%
    Grand Total     1084                        100.00%
    ```
    *Note: 'Count of Discount (%)2' represents the raw count of products.*

* **Insight/Interpretation:**
    A significant portion of products, **497 out of 1084 (approximately 45.85%)**, are offered with a discount of 50% or more. This indicates that nearly half of the product listings are subjected to aggressive pricing strategies. This could be a response to high market competition, an effort to clear inventory, or a deliberate strategy to attract price-sensitive customers. The relatively even split between highly discounted and less discounted products suggests a diversified pricing approach by sellers on Amazon.



#### Question 8: What is the distribution of product ratings?

* **Methodology/Approach:** Utilized an Excel Pivot Table. 'rating' was placed in the Rows area, and 'product_name' was placed in the Values area, set to show the 'Count'.

* **Result:**
    ```
    Row Labels    Count of product_name
    ------------  ---------------------
    4.5           42
    4.4           79
    4.3           151
    4.2           170
    4.1           196
    4             133
    3.9           94
    3.8           78
    3.7           38
    3.6           28
    Grand Total   1009
    ```

* **Insight/Interpretation:**
    The distribution of product ratings shows a strong positive skew, indicating that the majority of products have high ratings. The highest concentration of products falls within the **4.1 to 4.3 rating range**, with 196 products at 4.1, 170 at 4.2, and 151 at 4.3. This highlights generally good customer satisfaction across the listed products.
    As ratings decrease, the number of products also significantly drops (e.g., only 28 products at 3.6). This positive trend in ratings is a strong indicator of perceived product quality and customer loyalty for sellers on Amazon. It also suggests that products falling below the 4.0 mark might require attention for improvement.



#### Question 9: What is the total potential revenue (actual_price × rating_count) by category?

* **Methodology/Approach:** First, a calculated column named 'Estimated Sales' (representing potential revenue) was created using the formula `actual_price * rating_count`. Then, an Excel Pivot Table was used with 'Product Category' in the Rows area and 'Estimated Sales' was placed in the Values area, set to show the 'Sum'.

* **Result:**
    ```
    Row Labels                 Sum of Estimated Sales
    -------------------------  ----------------------
    Car & Motorbike            ₹ 4,472,000.00
    Electronics                ₹ 111,414,333,343.00
    Health & Personalcare      ₹ 6,959,700.00
    Home & Kitchen             ₹ 10,459,722,337.00
    Homeimprovement            ₹ 6,163,434.00
    Musicalinstruments         ₹ 151,117,062.00
    Officeproducts             ₹ 60,778,817.00
    Toys & Games               ₹ 2,380,050.00
    Grand Total                ₹ 122,105,926,743.00
    ```

* **Insight/Interpretation:**
    The total potential revenue by category reveals immense market opportunities, particularly dominated by **"Electronics"** with an astounding **₹111.4 billion**. This colossal figure underscores the massive scale of this category on Amazon and its potential for high sales volume, driven by both high prices and extensive customer engagement (as seen in review counts). **"Home & Kitchen"** follows as a distant but significant second with over **₹10.4 billion** in potential revenue.

    Other categories, while much smaller in comparison, still represent substantial markets (e.g., "Musicalinstruments" with ₹151 million, "Officeproducts" with ₹60 million). This analysis helps prioritize categories for investment, marketing spend, and inventory management, focusing resources on areas with the highest revenue-generating potential. The high potential in Electronics, even with significant discounting, highlights its strategic importance.



#### Question 10: What is the number of unique products per price range bucket?

* **Methodology/Approach:** First, a calculated column named 'Price Bucket' was created based on the `actual_price` to categorize products into '< ₹200', '₹200-₹500', and '> ₹500'. Then, an Excel Pivot Table was used with 'Price Bucket' in the Rows area and 'product_name' was placed in the Values area, set to show the 'Count'.

* **Result:**
    ```
    Row Labels    Count of product_name
    ------------  ---------------------
    > 500         961
    200-500       97
    < 200         26
    Grand Total   1084
    ```

* **Insight/Interpretation:**
    The distribution of unique products across price ranges reveals a clear focus on higher-priced items. A dominant majority of products, **961 out of 1084 (approximately 88.6%)**, fall into the **"> ₹500"** price bucket. Products in the "₹200-₹500" range are significantly fewer (97 products), and there are very few products in the "< ₹200" range (only 26 products).

    This suggests that sellers on Amazon, or at least within this dataset, primarily target the mid-to-high price segments. This could be due to the nature of the dominant categories (Electronics, Home & Kitchen often feature higher-priced items) or a strategic decision to focus on higher-value products. While this indicates a strong presence in premium segments, it also suggests potential opportunities or gaps in the very budget-friendly product offerings if market demand exists there.



#### Question 11: How does the rating relate to the level of discount?

* **Methodology/Approach:** First, a calculated field or helper column was created to categorize products into specific discount ranges ('<10%', '10–25%', '25–50%', '>50%'). Then, an Excel Pivot Table was used with these 'Discount Range' categories in the Rows area and 'rating' was placed in the Values area, set to show the 'Average'.

* **Result:**
    ```
    Row Labels    Average of rating
    ------------  -----------------
    <10%          4.25
    >50%          4.03
    10–25%        4.15
    25–50%        4.08
    Grand Total   4.07
    ```

* **Insight/Interpretation:**
    Surprisingly, products with the **lowest discount range (<10%) have the highest average rating (4.25)**. Conversely, products with the **highest discount range (>50%) have a slightly lower average rating (4.03)**. The mid-range discounts (10–25% and 25–50%) fall in between, with averages of 4.15 and 4.08 respectively.

    This counter-intuitive finding suggests that high-quality or highly demanded products might not require aggressive discounting to achieve excellent ratings and attract buyers. It implies that customers are willing to pay closer to the actual price for products they perceive as superior. Conversely, while deep discounts can attract buyers, they might be slightly associated with products that receive marginally lower satisfaction scores, or they are strategically used for products that need a stronger push to sell. This challenges the notion that heavily discounted items are necessarily of lower quality, but rather highlights that strong products can maintain high ratings even without significant price cuts.




#### Question 12: How many products have fewer than 1,000 reviews?

* **Methodology/Approach:** A calculated field or helper column was created to categorize products into 'review count buckets' (e.g., '0-999', '1000-1999', '2000-2999', and '>10000'). An Excel Pivot Table was then used with these 'Review Count Buckets' in the Rows area and 'product_name' was placed in the Values area, set to show the 'Count'.

* **Result:**
    ```
    Row Labels    Count of product_name
    ------------  ---------------------
    0-999         247
    1000-1999     117
    2000-2999     65
    3000-3999     61
    4000-4999     50
    5000-5999     33
    6000-6999     27
    7000-7999     33
    8000-8999     20
    9000-10000    20
    >10000        411
    Grand Total   1084
    ```

* **Insight/Interpretation:**
    The analysis reveals that **247 products have fewer than 1,000 reviews**. This constitutes a notable portion of the total products (approximately 22.8% of the 1084 products in the analyzed dataset).

    The distribution of reviews is highly polarized:
    * A significant number of products (`411`) have **over 10,000 reviews**, indicating highly popular and established items with massive customer engagement.
    * In contrast, the `247` products with fewer than 1,000 reviews suggest they might be newer listings, niche products, or struggling to gain visibility and traction.

    For RetailTech Insights' clients, these low-review products present an opportunity for targeted marketing, review generation campaigns, or re-evaluation of their product-market fit. Understanding this distribution helps in prioritizing which products need attention to boost their online presence and customer feedback.




#### Question 13: Which categories have products with the highest discounts?

* **Methodology/Approach:** This analysis re-evaluated the average discount percentages by product category (similar to Question 1) to identify which categories consistently feature higher discount levels. An Excel Pivot Table was used with 'Product Category' in the Rows area, and 'Discount (%)' was placed in the Values area, set to show the 'Average', then sorted in descending order.

* **Result:**
    ```
    Row Labels                 Average of Discount (%)
    -------------------------  -----------------------
    Homeimprovement            57.95
    Health & Personalcare      52.68
    Electronics                52.33
    Musicalinstruments         45.81
    Car & Motorbike            41.52
    Home & Kitchen             40.12
    Officeproducts             12.36
    Toys & Games               0.00
    Grand Total                46.08
    ```

* **Insight/Interpretation:**
    Reconfirming findings from Question 1, **"Homeimprovement"** (57.95%), **"Health & Personalcare"** (52.68%), and **"Electronics"** (52.33%) are the categories where products carry the highest average discount percentages. This indicates these are highly competitive categories where sellers frequently employ aggressive pricing strategies to attract customers or manage inventory.

    For RetailTech Insights' clients, these categories represent areas where consumers expect significant price reductions. Strategic discounting is crucial here, but it also necessitates careful margin management. Understanding these discount trends helps in advising clients on competitive pricing, promotional planning, and potentially identifying categories where deeper discounts might be necessary to capture market share.



#### Question 14: Identify the top 5 products in terms of rating and number of reviews combined.

* **Methodology/Approach:** A new calculated column named 'Combined Score' was created to evaluate products based on both their 'rating' and 'rating_count'. This score likely involved a formula that gave weight to both metrics (e.g., multiplying rating by a scaled version of the review count) to provide a single metric representing overall product strength and popularity. An Excel Pivot Table was then used with 'product_name' in the Rows area and 'Sum of Combined Score' in the Values area, sorted in descending order to identify the top 5.

* **Result:**
    ```
    Row Labels    Sum of Combined Score
    ------------  ---------------------
    boAt          4318.18
    Redmi         2082.77
    AmazonBasics  1954.29
    Samsung       1366.86
    JBL           1297.8
    Grand Total   11019.9
    ```

* **Insight/Interpretation:**
    The top 5 products that excel in both customer satisfaction (rating) and popularity (review count) are: **boAt, Redmi, AmazonBasics, Samsung, and JBL**.

    * **boAt** stands out significantly with the highest combined score, reinforcing its position as a highly popular and well-regarded product.
    * **Redmi** and **AmazonBasics** also show strong performance, indicating a large, engaged, and satisfied customer base.
    * **Samsung** and **JBL** round out the top 5, demonstrating consistent quality and appeal.

    These products are invaluable assets for RetailTech Insights' clients. They represent flagship items that drive sales, build brand reputation, and foster customer loyalty due to their combination of high quality (high rating) and widespread adoption (high review count). Management should focus on maintaining the success of these products through continued quality assurance, active community engagement, and leveraging their popularity in marketing strategies (e.g., featuring them prominently, encouraging user-generated content).


# Case Study 1: Amazon Product Review Analysis

## 1. Project Overview
You are working as a Junior Data Analyst at RetailTech Insights, a company that provides e-commerce analytics solutions to sellers on platforms like Amazon. Your team has been tasked with analysing product and customer review data to generate insights that can guide product improvement, marketing strategies, and customer engagement.

## 2. Dataset Description
The dataset contains information scraped from Amazon product pages, including:
* Product details: name, category, price, discount, and ratings
* Customer engagement: user reviews, titles, and content
* Each row represents a unique product, with aggregated reviewer data stored as comma-separated values
Total Records: 1,465 rows TotalFields: 16columns

## 3. Dashboard Creation

The Excel Dashboard provides an interactive overview of product performance and customer engagement. Key Performance Indicators (KPIs) presented include **Total Profit** (likely derived from price and cost), **Average Rating**, and **Total Reviews**. The dashboard also features a **High Discount Flag**, allowing quick identification of heavily discounted products. All analysis results from the pivot tables are visually represented in accompanying charts, and a **slicer for Product Category** enables dynamic filtering and deeper exploration of category-specific insights.

## 4. Key Findings & Recommendations

This Amazon product review analysis for RetailTech Insights provides a comprehensive understanding of product performance, pricing dynamics, and customer engagement across various categories.

### Key Findings:

* **Dominant Market Categories:** **Electronics** and **Home & Kitchen** are the primary drivers of sales, product listings, and overwhelmingly dominate in total customer reviews (over 18.9 million for Electronics alone) and potential revenue (over ₹111 billion for Electronics). These categories represent the core business and significant growth opportunities.
* **High Product Quality & Customer Satisfaction:** The overall product ratings are skewed positively, with a high concentration of products (especially 4.1 to 4.3 average rating). Specific products like **"Instant," "Oratech," and "Swiffer" (4.8 average rating)** demonstrate exceptional customer satisfaction.
* **Strategic & Aggressive Discounting:**
    * A substantial portion of products (**~46% or 497 products**) are offered with discounts of 50% or more, indicating a highly competitive pricing environment or a strategy for inventory movement.
    * Categories like **"Homeimprovement," "Health & Personalcare," and "Electronics"** consistently feature the highest average discounts, suggesting aggressive competition or strategic efforts to drive sales in these segments.
    * Interestingly, products with the **lowest discounts (<10%) have the highest average ratings (4.25)**, suggesting that high-quality, in-demand products may not require deep price cuts to perform well.
* **Valuable & Popular Products:** Products such as **"boAt," "Redmi," "AmazonBasics," "Samsung," and "JBL"** stand out as top performers when combining both high ratings and massive review counts. These are highly visible and trusted products.
* **Price Segment Focus:** The vast majority of products (**over 88%**) fall into the **> ₹500 price range**, indicating a focus on mid-to-high value items rather than budget-tier products.
* **Visibility & Engagement Gaps:** A significant number of products (**247 products, or ~23%**) have fewer than 1,000 reviews, highlighting a "long tail" of products that may be newer, niche, or struggling to gain customer visibility and feedback.

### Overall Recommendations:

1.  **Leverage Core Categories:**
    * **Invest Heavily in Electronics & Home & Kitchen:** Given their market dominance in products, reviews, and potential revenue, prioritize inventory, marketing, and new product development within these categories.
    * **Analyze High-Rated Products:** Study the attributes, marketing, and customer service strategies behind consistently high-rated products (e.g., Instant, Oratech) to replicate their success across other listings.

2.  **Optimize Pricing & Promotional Strategies:**
    * **Strategic Discounting:** Advise clients to analyze the impact of deep discounts on profitability vs. sales volume, especially in high-discount categories like Homeimprovement and Electronics. Encourage a nuanced approach where high-quality products might not need aggressive cuts.
    * **Price Range Exploration:** Investigate potential market demand and competitive landscape for products in the `< ₹200` and `₹200-₹500` price ranges to identify untapped opportunities for product diversification.

3.  **Enhance Product Visibility & Customer Engagement:**
    * **Review Generation Campaigns:** Implement targeted campaigns for the 247 products with fewer than 1,000 reviews to boost their visibility and gather valuable customer feedback. This could include post-purchase email sequences, incentivized reviews, or improved product descriptions.
    * **Showcase Top Performers:** Actively use the top 5 combined-score products (boAt, Redmi, etc.) in marketing campaigns and storefronts as "bestsellers" or "customer favorites" to drive traffic and cross-selling.

4.  **Continuous Monitoring & Adaptation:**
    * Regularly monitor key performance indicators (KPIs) related to sales, customer segments, shipping costs, and returns to ensure ongoing strategic alignment and identify new opportunities or challenges.
