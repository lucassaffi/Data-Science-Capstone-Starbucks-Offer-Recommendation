# Identifying which groups of people are most responsive to each type of Starbucks offer

![image](https://images.pexels.com/photos/597933/pexels-photo-597933.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940)
Image Credit: [Adrianna Calvo](https://medium.com/r?url=https%3A%2F%2Fwww.pexels.com%2Fpt-br%2F%40adriannaca%3Futm_content%3DattributionCopyText%26utm_medium%3Dreferral%26utm_source%3Dpexels) no Pexels

This project is my Udacity Data Science Nanodegree capstone project and is about finding the best offers sent by Starbucks to consumers. The datailed explanation about each step followed is on [Medium](https://medium.com/@lucassaffi_67427/identifying-which-groups-of-people-are-most-responsive-to-each-type-of-starbucks-offer-c61e8cda7fe6).

### Objective

Starbucks has a program called "My Starbucks Rewards", which lets you earn stars with every purchase that can be redeemed for free drinks or food. The user needs to download the Starbucks app or visit the Starbucks website to create an account and also have a Starbucks card. After that, the client receives stars every time he makes a purchase through the app or with registered Starbucks card. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). 

The objective is answering the following question: **which BOGO and Discount offers should be sent to each user in order to maximize results?**

### Files:

The data is contained in three files:

- portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
- profile.json - demographic data for each customer
- transcript.json - records for transactions, offers received, offers viewed, and offers completed

Here is the schema and explanation of each variable in the files:

portfolio.json

- id (string) - offer id
- offer_type (string) - type of offer ie BOGO, discount, informational
- difficulty (int) - minimum required spend to complete an offer
- reward (int) - reward given for completing an offer
- duration (int) - time for offer to be open, in days
- channels (list of strings)

profile.json

- age (int) - age of the customer
- became_member_on (int) - date when customer created an app account
- gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str) - customer id
- income (float) - customer's income

transcript.json **(Couldn't be add to repository because of the size)**

- event (str) - record description (ie transaction, offer received, offer viewed, etc.)
- person (str) - customer id
- time (int) - time in hours since start of test. The data begins at time t=0
- value - (dict of strings) - either an offer id or transaction amount depending on the record

### Libraries:

- pandas
- numpy
- json
- matplotlib
- seaborn 
- itertools
- scipy
- sklearn

### Results:

Most part of the people should receive discount offers, because most of the cluster consolidated had as the best offer one type of discount as shows the chart below:
![image](https://cdn-images-1.medium.com/max/1000/1*m3R1164XO1H3snkCHLC_1w.png)
