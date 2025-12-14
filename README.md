**The Detail**

Food Panda Data Set from Pakistan
Link : https://www.kaggle.com/datasets/nabihazahid/foodpanda-analysis-dataset-2025

The Detail

This dataset contains customer-level transactional and behavioral data from a food delivery platform.Each record represents one customer, summarized from their historical order activity.

This Data Captures
- Purchasing behavior (price, quantity, order frequency)
- Customer engagement over time (recency, tenure)
- Loyalty and value indicators
- Basic contextual attributes (payment method, city)

The target variable, churn_flag, indicates whether a customer has become inactive. This dataset is used to analyze customer behavior, identify churn drivers, and build predictive churn models.

**Executive Summary**

The analysis identifies customer churn driven primarily by declining engagement rather than pricing. Exploratory Data Analysis shows that Recency and Frequency are the strongest indicators of churn, while price per order has minimal impact.The outcome is a data-driven early warning system, integrating RFM analysis with predictive modeling, enabling prioritized retention actions and more sustainable churn reduction.


**The Purpose**

Key Objectives

- Analyze behavioral patterns of churned Foodpanda customers to uncover the true drivers of disengagement beyond price
- Identify and validate key churn drivers through exploratory data analysis to understand who the core customers are and why they leave
- Develop a churn prediction model (≥75% accuracy) to enable early identification of high-risk customers

What This Project Delivers

- Clear identification of behavioral churn signals (e.g., recency and frequency decline)
- A predictive early warning system to flag customers before they churn
- Customer segmentation combining churn risk and customer value (CLV)
- Actionable insights that guide who to retain, when to act, and how to personalize engagement

Value Proposition 

These insights enable the business to act earlier, target smarter, and grow revenue sustainably through data-driven customer decisions.


**Data Dictionary**

<img width="529" height="530" alt="image" src="https://github.com/user-attachments/assets/2b07be73-beff-4fbb-8c3e-91d7c7783b34" />

Link https://docs.google.com/spreadsheets/d/1srnmpO-yM5rV1-iT0rWhTP16h0Qvr0ruV2nE_0aN3jc/edit?usp=sharing

**The questions** 

<img width="719" height="270" alt="image" src="https://github.com/user-attachments/assets/21e0ccb9-8d29-40e4-9e35-79a93662b0ab" />

**Exploratory Data Analysis**
<img width="833" height="434" alt="image" src="https://github.com/user-attachments/assets/4e605035-1046-4f5b-bc12-848ca795fc09" />

(The above visualization is selected for this topic analysis)

**Key Findings**

- **High Churn Risk**: Churn rate is as high as 46%, indicating that nearly half of customers leave the platform, directly impacting revenue and business stability.
- **Loss of High-Value Customers**: Churned customers have a higher AOV than active customers (805 vs 797), showing that the business is losing high-value (VIP) customers, not low-quality ones.
- **Weakening Key Revenue Markets**: High-income cities such as Multan and Lahore experience churn rates above 47%, signaling revenue risk in strategic geographic markets.
- **Behavioral Decline Before Churn**: Churned customers exhibit lower purchase frequency, higher days since last order, and longer tenure, confirming that churn is preceded by a gradual decline in engagement rather than sudden exit.

**Hypothesis:**

H₀ (Null Hypothesis):
Customer churn rate has no significant relationship with the business’s total revenue.

H₁ (Alternative Hypothesis):
Customer churn rate has a significant relationship with the business’s total revenue,
such that an increase in churn leads to a decrease in total revenue.

**Cleaning Data**

1. Data Quality & Integrity
Assessed completeness, logical consistency, and duplicates
Identified critical issues affecting churn and revenue analysis
2. Temporal & Behavioral Validation
Corrected date inconsistencies and invalid order sequences
Revalidated Recency, Frequency, and engagement metrics
3. Feature & Target Standardization
Standardized churn into binary format for modeling
Corrected misclassified categories and loyalty indicators
4. Revenue & Value Construction
Created revenue and monetary features
Enabled CLV and value-based analysis
5. Model Readiness
Encoded categorical and demographic variables
Final validation to ensure EDA- and ML-ready data

**Analysis**

<img width="480" height="283" alt="image" src="https://github.com/user-attachments/assets/0004ce0c-7f25-47be-bebb-4264460933a1" />

- Customer heterogeneity and skewed revenue distributions make average-based analysis insufficient for decision-making.
- Behavioral signals (recency, frequency, engagement) emerge as early indicators of churn, outperforming price and rating variables.
- The analysis must shift from descriptive patterns to individual churn risk estimation.
- Integrating churn risk with Customer Lifetime Value (CLV) enables prioritization of value-destructive churn rather than churn volume alone.

Next Step 
- RFM analysis is the necessary next step to convert exploratory behavioral insights into structured, business-interpretable customer segments.





**FoodPanda: วิเคราะห์ข้อมูลลูกค้า, Churn และการทำนายด้วย Machine Learning
โปรเจกต์นี้เป็นงาน Exploratory Data Analysis (EDA) + Statistical Testing + Machine Learning
 โดยใช้ข้อมูลแพลตฟอร์ม Food Delivery (FoodPanda-like dataset) เพื่อศึกษาพฤติกรรมลูกค้า
 วิเคราะห์ปัจจัยที่ส่งผลต่อ Churn (การเลิกใช้งาน) และสร้างโมเดลทำนาย**

 
**- วัตถุประสงค์ของโครงงาน**
วิเคราะห์รูปแบบการใช้จ่ายและพฤติกรรมการสั่งอาหาร


เปรียบเทียบความแตกต่างระหว่างลูกค้า Active vs Inactive (Churn)


ทดสอบสมมติฐานเชิงสถิติ (T-test)


คัดเลือก Feature สำคัญที่สัมพันธ์กับ Churn


สร้างโมเดล Logistic Regression  ,Random Forest ,XGBoost,LightGBM  เพื่อทำนายโอกาส Churn



**- ภาพรวมชุดข้อมูล**

** แหล่งที่มาของข้อมูล **  
https://www.kaggle.com/datasets/nabihazahid/foodpanda-analysis-dataset-2025


**จำนวนข้อมูล: 6,000 ออเดอร์**


**จำนวนตัวแปร: 20 ตัวแปร**
<img width="1171" height="605" alt="image" src="https://github.com/user-attachments/assets/88460a82-6148-4d8f-9db3-4a4a35cf1199" />




**ตัวแปรสำคัญ**


ราคา (price), จำนวน (quantity)


ความถี่การสั่ง (order_frequency)


คะแนนสะสม (loyalty_points)


ระยะห่างจากการสั่งล่าสุด (days_since_last_order)


สถานะลูกค้า (churned: Active / Inactive)


คะแนนรีวิว (rating)


สถานะการจัดส่ง (delivery_status)



** การตรวจสอบและทำความสะอาดข้อมูล**


ตรวจสอบชนิดข้อมูลและค่า missing (ไม่พบ missing values)


จัดการค่า Null


ลบ duplicates


แปลงประเภทข้อมูล (date → datetime, string → numeric)


เตรียมข้อมูลให้อยู่ในรูปแบบพร้อมวิเคราะห์และทำโมเดล



**Descriptive Statistics**

**ผลสถิติพื้นฐานของตัวแปรเชิงตัวเลข: **

<img width="359" height="290" alt="{BE2B4D9B-3322-4F92-96AA-A8E6BC66FA5F}" src="https://github.com/user-attachments/assets/aebc4cbd-a0d0-49d8-97c1-eb620aeae2d2" />


จากการวิเคราะห์สถิติเชิงพรรณนา พบว่าลูกค้าส่วนใหญ่มักสั่งอาหารเฉลี่ยประมาณ 3 รายการต่อออเดอร์ โดยมีมูลค่าเฉลี่ยประมาณ 800 บาท
ข้อมูลแสดงให้เห็นความแตกต่างของพฤติกรรมการใช้จ่าย และพบว่าตัวแปร days_since_last_order มีค่าเฉลี่ยสูง ซึ่งสะท้อนถึงความเสี่ยงในการเกิด churn

มีการแสดง:
Histogram


Bar chart (Rating)


Boxplot เพื่อตรวจสอบ outliers



🔗 Correlation Analysis
วิเคราะห์ความสัมพันธ์ของตัวแปรเชิงตัวเลขด้วย Correlation Matrix


แสดงผลด้วย Heatmap  จำนวนลูกค้าในแต่ละกลุ่ม Customer

<img width="855" height="447" alt="{EDAD1F67-2F1C-4635-A0FE-B46BFE1EFBF5}" src="https://github.com/user-attachments/assets/92c81b7a-9030-426c-b8d9-d9cd20f092c4" />
<img width="390" height="355" alt="image" src="https://github.com/user-attachments/assets/4df5063f-cc93-4943-91e1-bee539f2bd2a" />


การแสดงยอดการ Churn แยกตามปี

<img width="331" height="506" alt="{645E33D3-8686-43CE-9A41-A32C1CE4FDA9}" src="https://github.com/user-attachments/assets/dedef551-9e12-4910-8ace-dd1eb39dc9ec" />

Royalty Point Vs Churn 

<img width="312" height="359" alt="image" src="https://github.com/user-attachments/assets/7bb42336-dcfc-462a-9dc9-61729f634f43" />

จากการวิเคราะห์ Loyalty Points พบว่า Active และ Inactive มีค่าเฉลี่ยใกล้เคียงกันมาก
(249 vs 251) แสดงว่า Loyalty Points ไม่ได้มีความสัมพันธ์ชัดเจนกับการ Churn
จึงไม่ใช่ปัจจัยสำคัญในการตัดสินว่าลูกค้าจะเลิกใช้บริการหรือไม่


<img width="1652" height="423" alt="image" src="https://github.com/user-attachments/assets/bcc7942a-17fd-4630-80a5-b57c617a420b" />

1️⃣ Average Loyalty

Inactive สูงกว่า Active (≈ 251 vs 249)
👉 แปลว่า ลูกค้าที่ churn ไม่ได้เป็นลูกค้าใหม่ แต่เป็นลูกค้าที่เคยอยู่กับบริษัทมานาน
⇒ เสียลูกค้าเก่าที่มีคุณค่า

2️⃣ Average Order Frequency

Active สั่งซื้อบ่อยกว่า Inactive (≈ 25.36 vs 25.24)
👉 ลูกค้าที่ไม่ churn ยังมี engagement ต่อเนื่อง
⇒ ความถี่ในการสั่งซื้อเป็นตัวแยก churn ได้ดี

3️⃣ Average Days Since Last Order

Inactive เว้นช่วงนานกว่ามาก (≈ 197 วัน vs 169 วัน)
👉 ลูกค้าที่ churn เริ่มหายไปก่อนแล้ว (early warning signal)
⇒ ระยะเวลาตั้งแต่การสั่งซื้อล่าสุดเป็นตัวชี้ churn ที่ชัดเจน

4️⃣ Tenure (รวม)

Inactive มี tenure รวมสูงกว่าอย่างชัดเจน
👉 ลูกค้าที่ churn เป็นกลุ่มที่อยู่กับบริษัทมานาน
⇒ Churn ส่งผลกระทบต่อฐานรายได้ระยะยาว

📌 Insight เชิงธุรกิจ (ตอบโจทย์ “Churn มีผลต่อยอดขายหรือไม่?”)

Churn ไม่ได้เกิดจากลูกค้าใหม่ แต่เกิดจาก ลูกค้าเก่าที่เคยมีคุณค่า

ลูกค้าที่ churn:

สั่งซื้อน้อยลง

ห่างหายจากการสั่งซื้อนานขึ้น

⇒ ส่งผลให้ ยอดขายในอนาคตลดลงอย่างมีนัยสำคัญ


**สรุปผล fail to reject the hypothesis**

p-value = 0.43 (> 0.05)


