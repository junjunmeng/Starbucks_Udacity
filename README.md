# Starbucks Offers: How to design offers strategy to increase revenue by customer segmentation

The blog could find in [Medium](https://medium.com/@jjunmeng/how-to-sending-offers-to-the-target-customer-to-increase-revenue-8668218e7774)

## Table of Contents
1. [Project purpose](#motivation)
2. [Dataset preview](#data)
3. [Main methods and evaluation](#method)
4. [Data exploration and visualization](#exploration)
5. [unsupervised clustering](#clustering)
6. [Business Suggestions](#suggestion)


## Project purpose and problem statement<a name = 'motivation'></a>
This project is trying to disign digital marketing stratgy to Starbucks customers. Different customers will react different for promotion offers. This project used one month simulated customer data, including demographic and user behavior data to segment customers, which will guide the digital marketing strategy. 

## Dataset Preview<a name='data'></a>
The datasets including three separate JSON files
1. Customer profiles (Demographic data): including age, gender, income and date of becoming a member
2. Porfolio (Experiment data): recorded the offers sent during the 30-day test period. The channel including web, email, mobile or social media, or a combination of those. The offers have different levels of difficulty (minimum spend) and reward, which fall into three categories: Discount, BOGO(Buy-one-got-one) and informational
3. Transcript (User behavior): recorded the interactions (receive/view/complete) and all other transactions by customers within the test period. 


## Main methods and evaluation metrics<a name = 'method'></a>
We used unsupervised clustering methods to cluster customers by the similarity of demographic and user behavior data within customers. I used principle component analysis (PCA) and k-means unsupervised Machine learning algorithm to group customers into four main groups. I used elbow method to choose the best number of groups. 

view rate(% of customers who viewed the offer) and conversion rate (% of customers who complete an offer after viewed it) were used to assess how applicable those segments to Starbucks business. 


## Data exploration and visualization<a name = 'exploration'></a>

After cleaning this dataset, I explored the demographic distribution of customers, male customer is about 25% more compared to female. And the average income of male customer is also higher than female. The age of customer is between 40-70, and the biggest group is around 60 years old. 

Income and the spending had some position relationship for a cluster of customer. 

![image](https://user-images.githubusercontent.com/26633604/142346953-35611229-25df-4bc5-86b3-459369ea8230.png)


## Metrics 
I uses view rate and completion rate to compares the performance of different offers. 
![image](https://user-images.githubusercontent.com/26633604/142346242-eda77c60-8778-46be-8ae4-de4331d24b28.png)


According to funnel analysis for three types of offers (BOGO, Discount and informational), BOGO got the best view rate, but Discount made the best completion rate. 


## Unsupervised clustering<a name = 'clustering'></a>
![image](https://user-images.githubusercontent.com/26633604/141930461-2ab80480-601a-4285-99ff-136ecdf537d4.png)

## Business Suggestions<a name = 'suggestion'></a>
![image](https://user-images.githubusercontent.com/26633604/141930554-5e08df34-9d38-484e-ab42-e7c17b6c4e83.png)

Segment 1 (Red): Mean Age: 56, bogo_cr: 0, discount_cr:0.66, exposures_completed: 0.50, income ~ 69k, recency: 20.45, mainly joined in 2016 and 2017, received very few BOGO offers. discount completion rate (0.66), exposures completion rate (0.50), most of them joined before 2018, total completion rate (0.65).

Seqment 2 (blue): Age : 56, mean income: 70k, total completion rate: 0.79. BOGO completion rate (0.78), discount cr(0.23), exposure completed(0.76) Female > Male, prefer mobile > web > social, year joined Y2Y increase from 2013-2017, decrease in 2018. This group received regular BOGO, but few discount offers, BOGO converted pretty well

Segment 3 (green): Age: 55, average income: ~68K, Male > Female, total completion rate(0.86), bogo_cr(0.75), discount_cr(0.9), channel: mobile > web > social. Join the year, Y2Y joined number increased from 2013-2017, but trend changed direction in 2018. A main group for targeting with discount offers

segment 4 (Purple): Age: 50, average income ~57K, Male >> Female, total completion rate: 0.16. BOGO_cr (0.09), discount_cr(0.17), recency ~ 15, lowest, most joined in 2017-2018, and the Y2Y still increase, channel: email > mobile > web > social

