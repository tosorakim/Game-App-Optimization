# game-app-optimization
How to optimize the game app

It's an iOS game app raw data. It's included postback events which in-app game environment. You can get the real mobile game raw data!

I'd like to share the small dataset that you can practice how to optimize the mobile game using in-app data. I believe that it may help you to practice if you're just a beginner or never seen such a dataset before. You could simulate how to optimize the in-app game data. Which channel is good or bad.

Let's think about it if you are working at a game company and you are a game performance marketer which channel should be optimized ASAP? You could practice following the below KPI. Good Luck!

=====Subject=====
[Question] Optimize the app following the KPI
(1)day1 retention rate below 10%
(2)nru(new registered users) below 30%

[Information of App]
Publisher: -
Category: Game
OS: iOS
Language: Korean
Age: 12+
Price: Free

[Information of Event Postback]
open: app open
afcompleteregistration: registration
jointheguild: join the guild
purchase: purchase
aflevel5achieved: achieved level 5 aflevel8achieved: achieved level 8
aflevel10achieved: achieved level 10 aflevel15achieved: achieved level 15
aflevel20achieved: achieved level 20 autoplay : after level5, it’s allowed autoplay

=====Collect data(.csv file)=====

Raw data
(1)channel_event.csv
(2)d1.csv

Pivoting data (using raw data)
(1)gagong.csv

[Information of channel_event.csv]
event: postbacked event name
channel: channel name
country: country
language: language
os: mobile phone operating system
device: mobile device

[Information of d1.csv]
channel: channel name
install: counted installs
day1: day 1 retention

[Information of gagong.csv]
channel: channel name
install: counted installs
afcompleteregistration: once a user completed the registration it's pushed(counted)
aflevel5achieved: achieved level5
aflevel8achieved: achieved level8
afpurchase day1: purchase nru: new registered user rate Lv5: achieved level 5 rate purchaserate: purchase rate
day1_retention: day 1 retention rate
