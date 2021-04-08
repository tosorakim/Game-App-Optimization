# Introduction
It's an iOS game app raw data. It's included postback events which in-app game environment. You can get the real mobile game raw data!

I'd like to share the small dataset that you can practice how to optimize the mobile game using in-app data. I believe that it may help you to practice if you're just a beginner or never seen such a dataset before. You could simulate how to optimize the in-app game data. Which channel is good or bad.

Let's think about it if you are working at a game company and you are a game performance marketer which channel should be optimized ASAP? You could practice following the below KPI. Good Luck!

# Exploratory Analysis
To begin this exploratory analysis, first download the code

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