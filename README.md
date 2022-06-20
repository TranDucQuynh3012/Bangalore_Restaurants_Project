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

My target client this time is a programmer, who want to move to India - one of the best place for programing career. But he has confused and wonder if Bagalore is the most suitable place for him to live in.He is an foreinger and the first problem is the food in here. Are there any good restaurants that not too expensive? Do they provide popular food like burger and pizza? Or do they only server Indian traditional food? Which location should he live to have more choices of food? To answer these questions and help this programmer making a decision about living in Bangalore, I will use this Zomato data to figure it out.

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

V. Analysing the data:

*All these steps of cleaning the dataset, you can find out in the code file.*





*Have a nice day!*

*Tran Duc Quynh*