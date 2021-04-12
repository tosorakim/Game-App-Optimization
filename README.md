# Introduction
It's the raw data of iOS game app. It's included postback events which in-app game environment.

# Environment
Python, Linux, Hadoop, SQL, and MySQL

# Description of data
=====Subject=====</br>
[Question] Optimize the app following the KPI</br>
(1)day1 retention rate below 10%</br>
(2)nru(new registered users) below 30%</br>
</br>
[Information of App]</br>
Publisher: -</br>
Category: Game</br>
OS: iOS</br>
Language: Korean</br>
Age: 12+</br>
Price: Free</br>
</br>
[Information of Event Postback]</br>
open: app open</br>
afcompleteregistration: registration</br>
jointheguild: join the guild</br>
purchase: purchase</br>
aflevel5achieved: achieved level 5 aflevel8achieved: achieved level 8</br>
aflevel10achieved: achieved level 10 aflevel15achieved: achieved level 15</br>
aflevel20achieved: achieved level 20 autoplay : after level5, it’s allowed autoplay</br>
</br>
=====Collect data(.csv file)=====</br>
Raw data</br>
(1)channel_event.csv</br>
(2)d1.csv</br>
</br>
Pivoting data (using raw data)</br>
(1)gagong.csv</br>
</br>
[Information of channel_event.csv]</br>
event: postbacked event name</br>
channel: channel name</br>
country: country</br>
language: language</br>
os: mobile phone operating system</br>
device: mobile device</br>
</br>
[Information of d1.csv]</br>
channel: channel name</br>
install: counted installs</br>
day1: day 1 retention</br>
</br>
[Information of gagong.csv]</br>
channel: channel name</br>
install: counted installs</br>
afcompleteregistration: once a user completed the registration it's pushed(counted)</br>
aflevel5achieved: achieved level5</br>
aflevel8achieved: achieved level8</br>
afpurchase day1: purchase nru: new registered user rate Lv5: achieved level 5 rate purchaserate: purchase rate</br>
day1_retention: day 1 retention rate</br>

# Exploratory Analysis
To begin this exploratory analysis, first import libraries and define functions for plotting the data using matplotlib. Depending on the data, not all plots will be made. Once you visualized the data as a graph(the graph file has attached as PNG file), you will find each character of channels.

KPI Option1 : day1_retention
As you analyzed the data, you could see the Channel A, C, D, E, and F were not following KPI #1(day1 RR below 10%). On the other hand, the channel B, G are satisfied the KPI so that they need to be optimization

KPI Option 2 : NRU(New Registered Users)
You could see the Channel A, B were not following KPI #2(nru below 30%). On the other hand, the channel C, D, E, F, and G are satisfied the KPI so that they need to be optimization

# Conclusion
 <img src="Total_install_pie.png" width="300"> 
Except for channel A, other channels B, C, D, E, F, and G are needed to be optimized following the KPI. It's around 76.7% of total installs. 
(Total_install_pie.png) In order to reduce this ratio, you would be better channel G with the most installs (number of cases) will be optimized first, followed by channels F, D, E, B, and C in order.

