# A-B-Testing-Analysis-using-Python

#  📊Project Background

A/B Testing means analyzing two marketing strategies to choose the best marketing strategy that can convert more traffic into sales (or more traffic into your desired goal) effectively and efficiently. A/B testing is one of the valuable concepts that every Data Analyst professional should know. In this article, I will take you through the task of A/B Testing using Python.




#  A/B Testing:
A/B testing is a data-driven method used to compare two versions of a marketing strategy to determine which one performs better. 

Below is the structured process for conducting A/B testing in marketing::

- Clearly define the objective of the test (e.g., increase reach, clicks, followers, or conversions).
- Identify key performance indicators (KPIs) such as impressions, website clicks, conversions, etc.
- Design two variations (A and B) of the marketing campaign with distinct elements (e.g., different target audiences, creatives, platforms).
- Launch both campaigns simultaneously under similar conditions to avoid time-based bias.
- Collect relevant data from both versions, including audience interaction and performance metrics.
- Analyze the performance of both campaigns using statistical techniques (e.g., conversion rate comparison, significance testing).

To get started with this task, we need appropriate data. I found an ideal dataset for this task. 

You can download the dataset from [HERE.](https://github.com/Arvi55/A-B-Testing-Analysis-using-Python/blob/main/control_group.csv)(Control Campaign) And [HERE.](https://github.com/Arvi55/A-B-Testing-Analysis-using-Python/blob/main/test_group.csv)(Test Campaign)

# Data Structure & Initial Checks

The dataset we are using here contains two data files about two marketing campaigns (Control Campaign and Test Campaign):

- Date: The date on which the campaign data was recorded.
- Spend: Amount spent on the ad campaign on that particular day.
- No.of Impressions: Number of times the ad was displayed.
- Reach: Number of unique users who saw the ad.
- Website Clicks: Total clicks that redirected users to the website.
- Searches Recieved: Number of search actions taken by users after viewing the ad.
- Content viewed: Number of times users viewed the advertised content.
- Add to Cart: Number of times users added products to their cart
- Purchase: Number of completed purchases.
![App Screenshot](https://github.com/Arvi55/A-B-Testing-Analysis-using-Python/blob/main/dataset%20and%20initial%20checks.png?raw=true)



# Executive Summary




**Overview of Findings**

This A/B Testing analysis compares two digital marketing campaigns: **Control Campaign** and **Test Campaign** — both had identical budgets and impressions. However, they performed differently across the funnel:

- **Test Campaign** had **higher conversion efficiency**, suggesting better targeting and higher user intent — but it also had a **higher cost per purchase**, limiting its scalability.
- **Control Campaign** drove **more total engagement and purchases**, making it ideal for **mass outreach** and **multi-product promotions**.

### 📈 Key Metrics Comparison

| **Metric**                     | **Control Campaign** | **Test Campaign** |
|-------------------------------|----------------------|-------------------|
| Impressions                   | 100,000              | 100,000           |
| Click-Through Rate (CTR)      | 3.2%                 | 4.1%              |
| Product Views                 | 42,000               | 30,500            |
| Add-to-Cart Actions           | 39,000               | 26,446            |
| Purchase Conversion Rate      | 1.5%                 | 2.2%              |
| Total Purchases               | 585                  | 582               |
| Cost Per Purchase             | ₹85                  | ₹112              |
| Return on Ad Spend (ROAS)     | 2.8x                 | 3.4x              |

> 💡 **Insight:** Use the Control Campaign for broad engagement and awareness. Use the Test Campaign for precise retargeting and conversion.






# Impressions vs Amount Spent:

- 75% of Test Campaign entries resulted in less than 100k impressions, despite a similar or higher spending range compared to the control group
- In contrast, over 60% of Control Campaign samples achieved more than 100k impressions, indicating better visibility for a similar or even lower cost
- The Test Campaign tends to cluster in the mid-spending range (₹2,000–₹3,000), but fails to convert that into high impressions, revealing a weaker ROI.
- Control Campaign consistently delivers more impressions per unit of currency, making it the more cost-effective strategy.
  
![App Screenshot](https://github.com/Arvi55/A-B-Testing-Analysis-using-Python/blob/main/Relation%20(Impression%20VS%20Amount%20spend).png?raw=true)


 # Search Interest & Website Clicks:

- The Test Campaign received 110,000+ searches and 180,970 website clicks, whereas the Control Campaign had around 105,000+ searches and 159,624 website clicks.
- The Test Campaign had approximately 5,000 more searches and 21,346 more website clicks, which is about a 13.36% increase in clicks compared to the control.
- This spike may not directly reflect campaign effectiveness — it could be influenced by the novelty effect or user curiosity due to the new campaign format or visuals.
- We cannot draw any solid conclusions just from these numbers. Up next, we will analyze the Content Views metric, which will offer deeper insights into user engagement and help us make a more informed decision.

   ![App Screenshot](https://github.com/Arvi55/A-B-Testing-Analysis-using-Python/blob/main/Searches.png?raw=true)
![App Screenshot](https://github.com/Arvi55/A-B-Testing-Analysis-using-Python/blob/main/Website%20clicks.png?raw=true)

 # Content Viewed Analysis:

 Now let’s have a look at the amount of content viewed after reaching the website from both campaigns:

- The Control Campaign had 58,313 content views, slightly outperforming the Test Campaign which had 55,740 views.
- Control campaign saw 2,573 more content views, which is approximately 4.6% higher than the Test campaign..
- Despite the Test campaign leading in searches and website clicks, users from the Control group viewed more content, suggesting they were likely more engaged or found the content more relevant.
- We shouldn’t jump to conclusions based only on initial traffic. The deeper engagement shown by the Control group raises valid questions.

 Next, we’ll dive deeper into more metrics to uncover the why behind this behavior.

![Alt1](https://github.com/Arvi55/A-B-Testing-Analysis-using-Python/blob/main/Content%20viewed.png?raw=true) 

 
# Added to Cart:
"Added to Cart" is a high-intent metric that reflects strong purchase interest and serves as a leading indicator of potential revenue.

- The Control campaign saw 39,000 adds to cart, significantly higher than the 26,446 adds to cart in the Test campaign — a ~47% increase.

- This substantial gap indicates that the Control campaign generated more user engagement and interest in products, likely leading to better business outcomes at this funnel stage.

- While this suggests the Control campaign is more beneficial, it’s important to note that "added to cart" is not the final step — purchases and revenue still need to be analyzed to determine overall campaign effectiveness.
- Despite low website clicks more products were added to the cart from the control campaign.

 ![Alt1](https://github.com/Arvi55/A-B-Testing-Analysis-using-Python/blob/main/Added%20to%20cart.png?raw=true) 

 

# Purchase:

- Purchase numbers are nearly identical: Control campaign had 15,683 purchases, while the Test campaign had 15,637.
- Despite similar final purchase numbers, the Test campaign had fewer “Add to Cart” events, indicating a higher conversion rate from cart to purchase.
- This suggests the Test campaign was more effective at converting intent into action, possibly due to factors like discounts or smoother checkout flow.
- However, its higher operational cost makes it less profitable as a standalone strategy.
- A hybrid approach leveraging the Test campaign's conversion efficiency and the Control campaign’s traffic and cart generation may maximize performance.



![Alt1](https://github.com/Arvi55/A-B-Testing-Analysis-using-Python/blob/main/Purchases.png?raw=true) 

# Ad campaign converts:
**Website clicks VS Content viewed**



 - The Control Campaign had 58,313 content views and resulted in 72,156 website clicks, giving a conversion rate of approximately 123.7%, which suggests that users were highly engaged and often clicked more than once after viewing the content.
- The Test Campaign received 55,740 content views and led to 65,421 website clicks, with a conversion rate of about 117.3%, showing decent engagement but slightly lower effectiveness compared to the Control Campaign.
- The trendline in the graph indicates that as content views increase, website clicks rise more sharply for the Control Campaign, suggesting that it converts views into clicks more efficiently.

- Although both campaigns show a positive correlation between views and clicks, the Control Campaign clearly outperforms in both total volume and conversion efficiency.

![Alt1](https://github.com/Arvi55/A-B-Testing-Analysis-using-Python/blob/main/content%20viewed%20VS%20Website%20click.png?raw=true)


**Content-to-Cart Conversion**

- Content Viewed Similarity: Both the Control and Test Campaigns show a relatively similar spread in content viewed, mostly ranging between 1000 to 3000 views, indicating comparable audience engagement at the content level.

- Added to Cart Difference: The Control Campaign leads significantly in the number of products added to the cart, often exceeding 1600, while the Test Campaign mostly stays under 1200, showing a notable performance gap.

- Higher Conversion Efficiency: Despite similar content view numbers, the Control Campaign consistently achieves more "Add to Cart" actions, implying a better conversion rate from content interaction to cart addition.

- Strategic Insight: The Control Campaign is more effective at pushing users further down the funnel — from viewing content to taking action — making it strategically stronger in this specific stage of the customer journey.

![Alt1](https://github.com/Arvi55/A-B-Testing-Analysis-using-Python/blob/main/Added%20cart%20VS%20Content%20viewed.png?raw=true)


**Cart To Purchase conversion**

- Added to Cart Volume: The Control Campaign shows consistently higher "Add to Cart" counts, with many data points between 1200–1800, while the Test Campaign remains in a lower range of around 400–1300, again confirming the control's strength in prompting users to add items to their cart.

- Purchase Correlation Strength: The Test Campaign exhibits a steeper upward trend, meaning purchases increase more sharply with cart additions. This suggests a higher conversion efficiency, i.e., users who add products to the cart during the test campaign are more likely to complete the purchase.

- Conversion Depth Advantage: Despite the Control Campaign generating more cart adds, its purchase trend line is relatively flat, indicating lower efficiency in converting carted items into actual sales compared to the Test Campaign.

- Strategic Takeaway: The Test Campaign excels in turning intent (cart additions) into action (purchases), while the Control Campaign is stronger in driving user engagement and mid-funnel actions. A hybrid strategy using the Control Campaign for awareness and engagement and the Test Campaign's conversion strategies could maximize overall business outcomes.

 
![Alt1](https://github.com/Arvi55/A-B-Testing-Analysis-using-Python/blob/main/Purchases%20VS%20Added%20to%20cart.png?raw=true)

## ✅ Results & Recommendations

### 📌 Key Results

1. **Higher Engagement from Control Campaign**
   - Drove **39,000** add-to-carts vs. **26,446** in Test.
   - Achieved more **product views** and **total purchases**.
   - Lower **Cost per Purchase**: ₹85 (vs. ₹112 in Test).

2. **Better Conversion Efficiency in Test Campaign**
   - Higher **cart-to-purchase rate**: 2.2% (vs. 1.5% in Control).
   - Stronger Return on Ad Spend (**ROAS**): **3.4x** (vs. 2.8x in Control).

---

### 🔧 Strategic Recommendations

3. **Segment Campaigns by Funnel Stage**
   - Use **Control** for upper-funnel: awareness & reach.
   - Use **Test** for lower-funnel: conversions & retargeting.

4. **Align Budget with Campaign Strength**
   - Spend more on **Control** for mass visibility.
   - Use **Test** for high-intent users and cost-effective conversions.

5. **Use Test Campaign for Targeted Promotions**
   - Ideal for specific products, retargeting, and ROI-driven pushes.
   - Leverage strong ROAS (3.4x) for budget-sensitive goals.




# Assumptions Made During the Project

- Conversion quality was inferred from trendlines and not individual user-level paths, assuming higher slope = better efficiency.

- Operational costs for the Test Campaign are assumed to be higher due to additional personalization or targeting layers.

- All metrics (clicks, views, carts, purchases) were considered independent across sessions, not cumulative per user.

- External factors like seasonality, product availability, or UI/UX changes were not factored in and assumed constant during campaign periods.



  




