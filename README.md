# Analysis-and-Visualization-of-Covid-19-spread-trend-all-over-the-world


 
Part 2. Design and Discussion 
 
Q1. Analyze the spread trend of this virus all over the world. What is the spread over time? 
 
  
 
 
➢	I am using the Choropleth Map visualization technique to analyze the spread of the Coronavirus and how it has changed over time across the globe.  
 
➢	Since the data is geographic in nature therefore, I decided to use Choropleth Map to visualize the geographic distribution of data. Choropleth is a type of thematic map where the area or regions are shaded in proportion to a given data variable (eg: number of covid cases). There are two types of Choropleth maps, namely static and dynamic maps. 
 
➢	We know the number of cases across the world from our dataset, but to understand the rate at which the virus is spreading, it is also important to consider the date attribute. So, I decided to go ahead with building dynamic map instead of static map. 
 
➢	I have added a date field in this visualization which gives us the advantage of comparing the number of cases by region over time. It makes this visualization more insightful and compelling and tells us how the spread of the Coronavirus started in China and, at first, slowly made its way across the world, picking up pace in a span of weeks. 
 
➢	We can see that each country displays its Population, Total number of cases and Total number of deaths when hovering over each element on the map. 
 
➢	We also created the colour scale to show the data in a more intuitively way. We use red colour to show the most highest number of cases and lighter shade of red and orange to show to the lowest number of covid cases. Darker areas in the map indicates highest number of covid cases in that country and lighter areas indicates lowest number. To make it more understandable for the audience, we also created a legend which explains what each colour means in the map. 
 
 
Q2. Analyze the Unemployment rate in USA for the last 40 years. What was the unemployment rate in USA before and after Covid for all states in the US? 
 
  
 
 
➢	I have designed a dynamic and responsive time series graph which will visualize the unemployment rate in USA from 1980 to 2020.  
 
➢	Time series graphs can be used to visualize trends in counts or numerical values over time. It can answer questions about your data, such as How does the trend change over time? For this reason, I decide to choose this technique to answer my research question number 2.  
 
➢	To make this visualization more interactive and user friendly, I created two things: multi-select box and USA map. Using this, the user can select one or multiple states either from ‘multi-select box’ or ‘USA Country Map’ and accordingly the data will be filtered, and the time-series graph will be populated showing unemployment rate in the USA from 1980 to 2020. 
 
➢	Reason for implementing multi-select box over other available options such as dropdown, radio button, checkbox etc –  
▪	It allows user to select multiple items from the list,  
▪	Scrollable list box takes up less space,   
▪	Allows user to immediately see a sample of the options available, which may aid in quickly understanding the intent of the input.  
 
 
Q3. Analyze the pandemic spike in depression and anxiety in the UK adults 
 
  
 
For this research question, I decided to implement a bar chart to visualize the pandemic spike in depression and anxiety in the UK adults. My reason for choosing a bar chart to answer this research question is that bar charts are easy to understand, widely used, and can show changes over time and works well with the numeric data.  
 
Part 3: Implementation 
Research Question Q1: Analyze the spread trend of this virus all over the world. What is the spread over time? 
I created a dashboard which contains three tabs – Home, Visualization and News.  
  
 
▪	Home – It will give the audience basic understanding about what is Covid-19 and the steps to prevent Covid-19. 
▪	Visualization – It will redirect you to another page where you will find three different visualization designed by me to answer the research question number 1. 
▪	News: This is just to give the audience global update about Covid-19. User can click on ‘View News’ button to read the news article.  
Note: Please run the ‘main.html’ file which you can find inside the folder named ‘webapp’. 
There are 3 different visualizations presented on ‘Visualization’ page of this dashboard to answer the research question – “Analyze the spread trend of this virus all over the world. What is the spread over time?” 
a) First is, Choropleth Map Visualization to analyze the spread trend of the virus all over the world 
 
 
  
 
 
➢	Created a JavaScript Choropleth Map that is visualizing the Covid-19 spread trend all over the world from 1st Dec 2019 to 14th Dec 2020 using data from the European Center for Disease Prevention and Control. I am using the JSON version of the data for this visualization. 
 
➢	I have provided a date input field so that the user can enter a date to visualize the spread of the Coronavirus all over the world on a choropleth map from 1st Dec 2019 to 14th Dec 2020.  
 
 
Data Processing: 
 
To implement the above, you need to write some code. Here is the approach I used to visualize and structure the data: 
 
▪	I will read the JSON data and calculate the total cases for each country. As soon as I am done with one country, I will pass this info into an array that I have named “dataForMap” and then I will continue with the next country. 
 
▪	The JSON data contains data per day for each country. So, I’m first filtering the JSON data by the date entered by the user and then passing the following information: country territory code (the geographic identifier for the country), date, total number of cases, population and total number of deaths into an array that I have named “dataForMap”.   
 
▪	The final part of this step connects the resulting data with the JS choropleth map. 
 
b) Second is the bar chart displaying worldwide active cases in the past 100 days 
 
 
➢	This visualization shows worldwide active cases in the past 100 days. 
 
➢	I have used the data source from this API https://corona.lmao.ninja/v2/historical?lastdays=100. I am using the data directly without filtering it or changing its data structure.  
 
➢	User Level of Interaction – select the country from the dropdown to see the worldwide actives cases in the past 100 days for that country. You can also view number of cases when you mouse over the line chart. 
 
 
c) Third is the table displaying the current covid cases across the world 
 
 
➢	I have used the data from this API-> https://corona.lmao.ninja/v2/countries 
 
➢	This API provides live covid cases data for the current date. 
 
➢	This visualization will provide the user an overall idea on number of cases spread across world. 
 
Acknowledgment & Code reference: 
▪	https://github.com/AbbyXing/covid-glb 
▪	github.com/NovelCOVID/API 
▪	https://corona.lmao.ninja/v2/countries 
▪	https://corona.lmao.ninja/v2/historical?lastdays=100 
▪	https://www.anychart.com/blog/2020/05/06/javascript-choropleth-map-tutorial/ 
 
 
 
 
 
 
