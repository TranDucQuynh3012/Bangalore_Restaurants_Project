# Bangalore Restaurants Project:



![alt text](https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Plot/PowerBIrp.png)


In this project, we have the data of most restaurants in Bangalore, which was collected by Zomato - an Indian multinational restaurant aggregator and food delivery company. Zomato also got an app called 'Zomato: Food Delivery & Dining' for finding information about restaurants and ordering food online in India. Because of that, I'll call it is Zomato dataset from now on.

![alt text](https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Plot/bangalore.png)

*'Bangalore (or Bengaluru) is the capital and largest city of the Indian state of Karnataka. It has a population of more than 8 million and a metropolitan population of around 11 million, making it the third-most populous city and fifth-most populous urban agglomeration in India' - Wikipedia*


This dataset contains the data of Bangalore restaurants and they are:
 - URL: website of the restaurant.
 - address: address of the restaurant.
 - name: name of the restaurant.
 - online_order: the restaurant accepts online orders or not.
 - book_table: is that restaurant accept booking table.
 - rate: the average rate of customers for the services of that restaurant.
 - vote: total votes of customers.
 - phone: phone number of the restaurant.
 - location: where the restaurant is located in Bangalore.
 - rest_type: type of the restaurant.
 - dish_liked: the best dish of the restaurant.
 - cuisine: the main cuisine that restaurant serve.
 - approx_cost(for two people): approximate cost for two people per meal.

For more information and download this dataset, please go to this link: https://www.kaggle.com/datasets/himanshupoddar/zomato-bangalore-restaurants

or: https://drive.google.com/file/d/11rJ2pIVUTn4dQHRus4Tu9sYMYQTX-hnC/view?usp=sharing

This time, my target client is a programmer, who wants to move to India - one of the best places for a programming career. But he has confused and wonders if Bangalore is the most suitable place for him to live in. He is a foreigner and the first problem is the food here. Are there any good restaurants that are not too expensive? Do they provide popular food like burgers and pizza? Or do they only serve Indian traditional food? Which location should he live to have more choices of food? To answer these questions and help this programmer make a decision about living in Bangalore, I will use this Zomato dataset to figure it out.

The main tool I used for this Project is JupyterNotebook and the language is Python.

To run this Notebook on your personal computer, please download & install JupyterNotebook by Anaconda: https://www.anaconda.com/products/distribution

By using Power BI, I create a report that contains the most important visualizations to sum up what we have in this project, which you can see at the top of this Readme.

I. Libraries used in this Project:
1. Numpy: working with data in array type.
2. Pandas: working with data in Series and Data Frame type.
3. Matplotlib, Seaborn, Plotly: create data visualizations.
4. Geopy, Folium: create a heatmap on a geography map.

II. Dataset: 'zomato.csv'

III. Code:

* Notebook: https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Zomato_Restaurants_Project_code.ipynb

* or (to show Plotly chart): https://nbviewer.org/github/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Zomato_Restaurants_Project_code.ipynb

III. Target: 
Helping the target client obtain the information about restaurants in Bangalore, making the decision whether should he move to this city to live or not.

IV. Pre-processing the data:
The work here is very simple. We find out how much missing values of each column in this dataset. 

After that, we delete the columns which have a large amount of missing values (null-values), or we don't need the data of that column for analysing.
For the remaining columns, we will try to replace missing values or wrong values with suitable ones. And then our dataset is ready for analysing.



*All these steps of cleaning the dataset, you can find out in the code file.*


V. Analysing the Bangalore Restaurant data:

**1. What is the average rate of restaurants in Bangalore?**

The rates of the restaurants here are the first thing my customer want to know. Because if the rates of them are too low, there is no need to research at all, he will not choose Bangalore to live in. But take a look at this histogram below:

![alt text](https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Plot/average_rate.png)

*The average rates distribution of restaurants in Bangalore is following the Normal distribution with the mean value is 3.56 (out of 5). This means Bangalore is having many good restaurants. Looking at the histogram, most of the restaurants in Bangalore have a rating from 3 to 4. We can see that the people are really satisfied with the services of the restaurants here. So I can tell my client there is no need to worry about the quality of restaurants here, the citizens really enjoy them so he could love them also.*

**2. What are the top 10 restaurant chains in Bangalore?**

Answering this question means we will find out which restaurant chains are the most popular in Bangalore. A restaurant chain can have many restaurants and the most popular is the one that has the largest number of restaurants. We'll need the 'name' column to answer this question. What we got here is the result after calculating how many restaurants each chain in Bangalore has and then we take out the top 10 of them:

![alt text](https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Plot/top_chain.png)

*The biggest restaurant chain in Bangalore is Cafe Coffee Day. They have 89 restaurants here and they serve cafes and fast food. We can look at other chains in this list and realise most of them serve fast food, Indian food, burger, pizza... They are very popular kinds of food for all people in the world, not only the people in Bangalore. So my client does not have to worry about not being familiar with the traditional food here.*

*The more restaurants in the chain, the more popular it is. Because of that, these restaurants should be on top of my client's restaurants list to visit first if he moves here, to find out which one of them could be his favorite.*

**3. Do the restaurants here accept online orders?**

Being a programmer means my client has very little time to prepare a meal every day. So the best solution for him is to order the food online from the restaurant, that would make him not have to spend too much time on a meal and he could focus on his job. The second reason is he will not know where to go if he moves to Bangalore because he is a foreigner. That's why he really cares about if there are many restaurants here that accept online orders. With this chart below, he will get the answer:

![alt text](https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Plot/online_order.png)

*There are restaurants in Bangalore that accept online orders and they occupy a larger percentage than those not accept. We can see that ordering a meal on the Internet is very popular in Bangalore. And with the popular food here are fast food, cafe, pizza... we can imagine how busy this city is. This is very similar to other modern cities around the world, where the citizens have a busy life, so the demand for the fast, convenient with a reasonable price is obvious.*

*That's why I can tell my client don’t have to worry about not knowing where to go for a meal in Bangalore, just take the smartphone, order his favorite foods and they will be shipped wherever he is in this city.*

**4. Ratio between restaurants accepting booking tables and not accepting**

We will take a quick look at the restaurants which accept booking tables and do not accept booking tables in Bangalore:

![alt text](https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Plot/booking.png)

*What we see here is the overwhelming of restaurants that do not accept booking tables. This is easy to understand because the restaurants accept their guests booking tables before a meal usually are the luxury or very high-quality restaurants. That’s why they just obtain 14.8% of the total restaurants in Bangalore (We will ensure this insight later in this analysing), they are not very popular with the people here because it is hard for normal people to afford a meal from those restaurants. But the number of 14.8 % luxury restaurants in Bangalore is not a small number. That means if you want to have a luxury and high-quality meal, you will have many choices in Bangalore. And if you don't have much money, there still are 37.100 restaurants out there that could satisfy your demand.*

**5. What are the most popular restaurant types in Bangalore?**

There are many types of restaurants in Bangalore such as Casual Dining, Bakery, Bar, Beverage Shop... And what we will find out here is the most popular ones in Bangalore. Because the popularity of restaurant types reflect how the habits of choosing the food of citizen are. Do they usually use Indian traditional restaurants for meals? Or they will choose fast food restaurants instead? Let’s take a look at the chart below:

![alt text](https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Plot/rest_type.png)

*With this chart, we can reaffirm the insight we had in the first question. That the quick bites, casual dining, and cafe are the most popular types of restaurants here. They are the restaurants that provide popular foods such as fast foods, pizza, burgers or Indian traditional foods... which are very similar to the people. This is why a foreigner will feel it easy to find a suitable restaurant for him here because there are various types of food and many of them are popular worldwide.*

**6. Which restaurants have the highest vote in Bangalore?**

When a customer leaves a vote for a restaurant, they give it a rating point, and sometimes there is a comment. Voting is the best way for a customer to express their opinion about restaurant services through an app. And from that, all the others can see how their experiments are so they can decide to have a meal in that restaurant or not. If a restaurant has a lot of votes, it means that restaurant is well-known by the people. The customers really care about it and we can easily get more information about this restaurant online. This chart below shows us the 10 restaurants that have the highest number of votes on Zomato app:

![alt text](https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Plot/top_vote.png)

*The work I should do here is suggest my client to download the Zomato app and read the comments of customers to these 10 restaurants. He will have a high potential of finding out which are the best restaurants that suitable for him*

**7. Which locations have the largest  number of restaurants in Bangalore?**

I may be given this question if my client is a guy who has a hobby of exploration. He wants to try to eat at as many restaurants as he can, so he will find out which one is the best. My work become simple now. What I do is showing him the locations in Bangalore where most of the restaurants were placed. Here is what I got from the dataset:

![alt text](https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Plot/location_1.png)

I will also give him a heatmap, so he can find those locations on the Bangalore geography map easily:

![alt text](https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Plot/location_2.png)

*Look at the map and we can see most of the restaurants located in the central and the north of Bangalore (Bengaluru). That might be those places are where most of the citizens live or most of the companies, schools, markets... were placed. The shiniest heat on the map is BTM Layout, the location has the largest number of restaurants. ‘Try to hire an apartment at BTM Layout and you might be surrounded by a lot of restaurants.’ – That is what I will say to my client*

**8. How are the prices (for two people) of the restaurants in Bangalore?**

After the quality of the restaurant, the price of it is the second problem we should concern about. In this dataset, we have the approximate cost for two people for a meal. We will use this data to evaluate the price of a restaurant and whether it is high or not. Here is a general looking of the price of restaurants in Bangalore:

![alt text](https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Plot/cost.png)

*Those charts above show us that the prices for two people of restaurants here are usually less than 1000 INR (about 12.8 USD) and the number of restaurants that have a cost larger than 2000 INR (about 25.64 USD) is very small. The mean value of the prices is 594.8 INR (about 7.63 USD). This is a proper price for a person if he has an average income to have a meal at a restaurant. Even if that person has a low income, there still is a big number of restaurants that have a price less than 200 INR (about 2.56 USD) for a meal for 2 people. We can conclude that Bangalore is not an expensive city to live in, in contrast, it welcomes all people from every class to live here.*

**9. Do the rates, cost and accepting online orders of a restaurant have any relationship?**

To answer this question, we will need a scatter chart that shows all the variable we need: 'rate', 'cost' and 'accept - not accept online order'. This is how it looks:

![alt text](https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Plot/relationship.png)

*Form the scatter chart above, there are some relationships that we can find out:*
- Luxury restaurants (cost > 2000 INR) are usually rated 3.7 - 4.5/5, higher than restaurants which have lower prices.  So the high prices of the luxury restaurants in Bangalore are followed by the great quality of services. And most of them do not accept online orders. That's why we see most of the points from 3000 INR to 6000 INR on the chart are orange.
- In contrast, the normal restaurants (cost < 2000 INR) usually accept online orders, but the range of the vote is from 1.0 - 5.0/5. That means there are a lot of low-quality restaurants with low prices. They are not the place we want to go to. So the best restaurants that we should visit are shown by the point where the cost < 2000 INR and the rate > 4.0. 
- Take a look at the restaurants having cost < 2000 INR and the rate > 3.5, we can realise most of them accept online orders. The accepting online order restaurants really take advantage over the not accepting ones.

![alt text](https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Plot/relationship_2.png)

*What we can see here is the most accepting online order restaurants have lower prices than the most not accepting ones. That's because the cost to operate a traditional restaurant is higher than the modern restaurant. They have more types of costs such as rent, maintenance, they need more staffs to operate, or their materials are more expensive...*

**10. Which locations have the most affordable restaurants?**

A restaurant that is considered affordable for my client must have a price of less or equal to 500 INR and an average rate higher or equal to 4.0/5. The price of that restaurant is cheap and it is favored by the local customers. The work here is the same as what I did in question 7, but I will add 2 more conditions about cost and rate. This is what we have when we have done those steps:

![alt text](https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Plot/good_rest.png)

*Look like we have a winner here. BTM Layout is not only the location have the most restaurants but also the location have the largest number of most affordable restaurants. Suggesting my client to find an apartment to live in this location is a good idea.*

We still have more data in the Zomato dataset to analyse but in my opinion, answering these 10 questions is enough to help my client, a foreign programmer, know more about the restaurants and find suitable restaurants for him in Bangalore. There still are many things he has to do before the final decision of moving to Bangalore to live or not, but I believe ‘A meal in Bangalore’ is not his problem anymore.

I hope you enjoy this Zomato Restaurant Data Analysing Project and may this project help you a little with your research or learning.

*Have a nice day!*

*Tran Duc Quynh*









