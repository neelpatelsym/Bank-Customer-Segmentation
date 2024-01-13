# Bank-Customer-Segmentation
The project deals with transactional data of bank's customers. The goal is to uncover insights revealing customer's behaviour and categories customers into groups so that bank can aim flexible targeted marketing campaigns to each customer for increasing their revenue. 

### Dataset:
* This dataset encompasses over one million transactions conducted by more than 800,000 customers at a bank in India.
* The information includes details such as customer age (date of birth), location, gender, account balance during the transaction, transaction specifics, transaction amount, and more.

### Objective
* Understanding customer transaction behaviour.
* Segment the customer into logical groups using k-means and PCA, to approach them with targeted marketing campaign.
* Recency, Frequency and Monetary(RFM) analysis.
* Uncover crucial business insights.

### Data Cleaning
The data consists of about 1048567 entries.
The step consists of checking null and duplicate records.
The data cleaning was concluded by deleting outliers or out of the class values for the features.

### Feature Generation and Exploratory Data Analysis (EDA)
RFM analysis is a marketing technique that categorizes customers based on their recentness of purchase (Recency), frequency of purchase (Frequency), and monetary value of purchases (Monetary). This approach helps businesses segment their customer base to identify and target high-value customers, understand their behavior, and tailor marketing strategies accordingly. By analyzing these three key dimensions, RFM analysis enables businesses to identify and prioritize customer segments for more effective and personalized marketing efforts.

After deriving Recency, Frequency and Monetary features, an outlier detection task was performed.
The result shows significant number of outliers for each feature. However, upon close examination it can concluded that those data points reflect specific customer groups and not outliers.

Following is the main insights extracted from Exploratory Data Analysis (EDA)
<br>1.High correlation prevails between frequency and recency.
<br>![image](https://github.com/neelpdesai/Bank-Customer-Segmentation/assets/137664550/abe8fa0f-b2f2-4b76-a50d-0ce939b9934c)
<br>2.The number of repeat customers are only 16.14%. Thus bank has to extensively focus in providing incentives to encourage customers for carrying out repeated transactions.
<br>![image](https://github.com/neelpdesai/Bank-Customer-Segmentation/assets/137664550/d89474fa-c126-415b-840c-3dddc72b75e9)
<br>3.There is not much difference between both gender groups with respect to Frequency, Recency and Transaction Amount.
<br>![image](https://github.com/neelpdesai/Bank-Customer-Segmentation/assets/137664550/60469325-5bd3-4e26-be95-a8a773bd9fc5)
<br>4. Most of the customers having high bank account balance are less likely to use platform frequently.
<br>![image](https://github.com/neelpdesai/Bank-Customer-Segmentation/assets/137664550/196f9576-81f6-4e17-a45f-964816fc673b)
<br>5.The transaction amount hiked in the month of May because childeren have summer vacation in their school. So people use to travel in this months causing them to spend more in May.
<br>![image](https://github.com/neelpdesai/Bank-Customer-Segmentation/assets/137664550/322d3df5-3829-436e-869d-c54411d92712)

### Model Building and Segmentation
The distribution of chosen features like Frequency, Recency, TransactionAmount (INR) and CustAccountBalance is not normal.
Before carrying out clustering it is required for data to be near normal.
Hence data is projected on logarithmic scale to convert them to normal distribution.
Performed clustering using k-means.Elbow method is used to select optimum number of clusters.
<br>![image](https://github.com/neelpdesai/Bank-Customer-Segmentation/assets/137664550/e28e41dd-dbc2-467c-aa87-1b66ffdcf950)
Based on the results the customers are segmented into 5 groups.
Following is the charecteristics of clusters:
* Cluster 4 has high frequency. Such customers are loyal customers who carryout transactions frequently. They should be provided incentives for this behaviour.
* Cluster 5 are the customers who are having higher transaction amount, recency, account balance but lesser frequency. Those customers should be encouraged to carryout more transactions by providing them offers like cashback for frequently doing transaction through the bank account.
* While customers in cluster 1, 2 and 3 are more sort of churned customers. They should be provided offers and discount coupons to encourage transactions from their bank account. Moreover marketing team can focus on contacting these customers and retaining them.  
<br>![image](https://github.com/neelpdesai/Bank-Customer-Segmentation/assets/137664550/5295a3b8-ec2d-4e29-a4a8-a390a8cbb057)

To further analyze, PCA (Principal Component Analysis) is performed. 
According to PCA, 3 Principal components can explain the 90% variation. 
<br>![image](https://github.com/neelpdesai/Bank-Customer-Segmentation/assets/137664550/65f3e1d1-5694-48cf-b263-90fbb65c05e8)
The reduced principal dimension are used to perform clustering to get better results.
The optimum number of clusters using elbow technique in this case is 3.
<br>![image](https://github.com/neelpdesai/Bank-Customer-Segmentation/assets/137664550/78e7edd9-64da-4182-a204-501771a709c5)
Thus this analysis also confirms that there are mainly 3 types of customer groups. 
<br>![image](https://github.com/neelpdesai/Bank-Customer-Segmentation/assets/137664550/782da0a5-12dd-478a-b2f7-a064b239cfd0)







