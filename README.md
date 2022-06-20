# Bangalore Restaurants Project:
*'Bagalore (or Bangaluru) is the capital and largest city of the Indian state of Karnataka. It has a population of more than 8 million and a metropolitan population of around 11 million, making it the third most populous city and fifth most populous urban agglomeration in India' - Wikipedia*

In this project, we have the data of the most restaurants in Bangalore, which was collected by Zomato - an Indian multinational restaurant aggregator and food delivery company. Zomato also got an app called 'Zomato: Food Delivery & Dining' for finding information about restaurant and order food online in India. Becasue of that I'll call it is Zomato dataset from now on.

This dataset contains the data of Bangalore restaurants and they are:
 - url: website of the restaurant.
 - address: address of the restaurant.
 - name: name of the restaurant.
 - online_order: the restaurant accept online order or not.
 - book_table: is that restaurant accept booking table.
 - rate: the average rate of customers for the services of that restaurant.
 - vote: total votes of customers.
 - phone: phone number of the restaurant.
 - location: where the restaurant located in Bangalore.
 - rest_type: type of the restaurant.
 - dish_liked: the best dished of the restaurant.
 - cuisine: the main cuisine that restaurant serve.
 - approx_cost(for two people): approximate cost for two people per meal.

For more infomation and download this dataset, please go to this link: https://www.kaggle.com/datasets/himanshupoddar/zomato-bangalore-restaurants

or: https://drive.google.com/file/d/11rJ2pIVUTn4dQHRus4Tu9sYMYQTX-hnC/view?usp=sharing

My target client this time is a programmer, who want to move to India - one of the best place for programing career. But he has confused and wonder if Bagalore is the most suitable place for him to live in. He is an foreinger and the first problem is the food in here. Are there any good restaurants that not too expensive? Do they provide popular food like burger and pizza? Or do they only server Indian traditional food? Which location should he live to have more choices of food? To answer these questions and help this programmer making a decision about living in Bangalore, I will use this Zomato data to figure it out.

The main tool I used for this Project is JupyterNotebook and the language is Python.

To run this Notebook on your personal computer, please download & install JupyterNotebook by Anaconda: https://www.anaconda.com/products/distribution

By using Power BI, I creat a report that contain the most important visualizations to sum up what we have in this project, which you can see on the top on this Readme.

I. Libraries used in this Project:
1. Numpy: working with data in array type.
2. Pandas: working with data in Series and Data Frame type.
3. Matplotlib, Seaborn, Plotly: create data visualizations.
4. Geopy, Folium: creat heatmap on a geography map.

II. Dataset: 'zomato.csv'

III. Code:

* Notebook: https://github.com/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Zomato_Restaurants_Project_code.ipynb

* or (to show Plotly chart): https://nbviewer.org/github/TranDucQuynh3012/Bangalore_Restaurants_Project/blob/main/Zomato_Restaurants_Project_code.ipynb

III. Target: 
Helping the target client obtaining the information about restaurants in Bangalore, making desicion wheather should he move to this city to live or not.

IV. Pre-processing the data:
The work here is very simple. We find out how much missing values of each columns in the dataset. 

After that, we delete the columns which have a large amout  of missing values (null-values) or the we don't need the data of that column for  analysing.
For the remaining columns, we will try to replace missing values or wrong values with suitable ones. And then our dataset is ready for analysing.



*All these steps of cleaning the dataset, you can find out in the code file.*


V. Analysing the Bangalore Restaurant data:

**1. What is the average rate of restaurants in Bangalore?**

The rate of the restaurants here is the first thing my customer want to know. Because if the rate of them are too low, there is no need to research at all, he will not choose Bangalore to live. But take a look at this histogram below:

![alt text]()

*The distribution of  average rates restaurants in Bangalore is following Normal distribution with the mean values is 3.56 (out of 5). This means Bangalore restaurants is having many good restaurant. Look at the histogram, most of restaurants in Bangalore have the rating from 3 to 4, we can see that the people really satisfy with the services of the restaurants here. So I can tell my client there is no need to worry about the quuality of restaurants here, the citizen really enjoying them so he could like them also.*

**2. What are top 10 restaurant chains in Bangalore?**

Answering this question mean we will find out which restaurant chains are the most polular in Bangalore. One restaurant chain can have many restaurant and our mission is finding out which chains got the largest number. We'll need the 'name' column for this. What we got here is the result after calculating how many restaurants that each chains in Bangalore have and then we take out top 10 of them:

![alt text]()

*The biggest restaurant chain in Bangelore is Cafe Coffee Day. They have 89 restaurants in Bangalore and they serve cafe and fastfood. We can look at another chains in this list and realise most of them serve fast food, Indian food, burger, pizza... They are very popular kind of food for all people in the world, not only the citizen. So my client do not have to worry about not being familiar with traditional food in here.*

*The more restaurants in the chain, the more popular it is. Because of that, these restaurants should be on top of my client's restaurants list to visit first if he move here, to find out which one of them could be his favourite.*

**3. Do the restaurants here accept online order?**

Being a programmer means my client have very few time to prepair a meal everyday. So the best solution for him is ordering the food online from restaurant, that would make him not have to spend too much time for a meal and he could focus on his job. And the second reason is he will not know where to go if he moves there because he is an foreigner. That's why he really care about if there are many restaurants here in Bangalore accept online order. With this chart below he will get the answer:

![alt text]()

*There are restaurants in Bangalore that accept online order and they occupy the lager percentage than not accepting one. We can see that order for the meal by the Internet is very popular in Bangalore. And with the popular food in here are fast food, cafe, pizza... we can imagine how busy this city is. This is very similar with another mordern cites around the world, where the citizen have a busy life, so the demand of the fast, convinient with a resonable price is very obvious.*

*That's why I can tell my client not to worry about not knowing where to go for a meal in Bangalore, just take your smart phone and order his favorite foods and they will be shipped wherever he is in this city.*

**4. Ratio between restaurants accpepting booking table and not accepting**

We will take a quick look at the restaurants which accept booking table and do not accept booking table in Bangalore:

![alt text]()

*What we see here is the overwhelming of the restaurant that not accept booking table. This is easy to understand because the restaurants accpept their guests booking the table before a meal are the luxury or very high quality restaurant. That why they just obtain 14.8% in total restaurant in Bangalore (We  will ensure this insight in the next steps of this analysing), they are not very polular with the people here because it is hard for normal people to afford a meal from those restaurants. But the number 14.8 % of luxury restaurant in Bangalore is not a small number. That means if you want to have a luxury and high quality meal, you have many choices in Bangalore. And if you don't have much money, there are 37.100 restaurants out there could satisfy your demand.*

**5. What are the most popular restaurant types in Bangalore?**

There are many types of restaurant in Bangalore such as Casual Dining, Bakery, Bar, Beverage Shop... And what we will find out here are the most popular ones in Bangalore. Because the popular of restaurant types reflect how the habit in choosing food of citizen here. Do they usually use Indian traditional restaurants for meals? Or they will choose fast food restaurants instead? Let take a look at this chart below:

![alt text]()

*With this chart, we can reaffirm the insight we have in the first question. That the quick bites, casual dining and cafe are the most popular types of restaurants here. They are the restaurants where provide popular foods such as fast foods, pizza, burger or Indian traditional foods... which are very similar with the people. This is why a foreign will feel it easy to find a suitable restaurant here, because there are variety types of food and many of them are popular worldwide.*

**6. Which restaurants have the highest vote in Bangalore?**

When a customer leave a vote for a restaurant, they give it a rate poin and sometimes there is a comment. Voting is the best way for a customer express their oppinion about restaurant services by an app. And from that, all the other can see how their experiment is so they can decide to have a meal in that restaurant or not. If a restaurant has a lot of votes, it means that restaurant are well-known by the people. The customers really care about it and it is easy to get more information of this restaurant online. Here are 10 restaurants have the highest number of vote on Zomato app:

![alt text]()

*The work I should do here is suggest my client to download Zomato app and read the comments of customers to these 10 restaurant. He will have high potential of finding out which is the best restaurants that suitable for him*

**7. Which location have the largest  number of restaurants in Bangalore?**

I may be given this question if my client is guy who have hobby of exploration. He want to try as many restaurants as he can, so he will find out which one is the best himself. My work become sipmle now. What I do is showing him the locations in Bangalore which most of the restaurants were placed there. Here is what I got from the dataset:

![alt text]()

I will also give him a heatmap, so he can find those location on Bangalore geography map easily:

![alt text]()

*Look at the map and we can see most of the restaurants located in the central and the north of Bangalore (Bengaluru). That might be those place are where most of the citizen live or most of the company, school, market... are placed. The most shiny heat on the map is BTM Layout, which have the largest number of restaurant.*

**8. How is the prices (for two people) of the restaurants in Bangalore?**

After the quality of the restaurant, the price of it is the second problem we should concern. In this dataset, we have the approximate cost for two people for a meal, so we will use this data to 









