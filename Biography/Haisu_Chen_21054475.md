# Data Biography

### Declaration of Authorship

I, [Haisu Chen], confirm that the work presented in this assessment is my own. Where information has been derived from other sources, I confirm that this has been indicated in the work.

[Haisu Chen]

Date of signature: 25/11/2021
Assessment due date: 26/11/2021
Student Number: 21054475

_Please write your answer immediately below the level-3 headers and delete the guidance prior to submission._

---

### 1. Who collected the data?

#### 25 words; 2 points; Consider the source of the data and its relation to the underlying data generating process.

Dataset was collected and established responsibly by Murry Cox, an activist and a software engineer, who also built the investigatory website Inside Airbnb (IA) [1].

---

### 2. Why did they collect it?

#### 50 words, 4 points; Consider the purposes for which the data was collected and how this might shape its form/content.

The primary purposes are to provide the dataset that allows public to locate and examine the entire listings of short-term rentals on housing in London [2], and to explore the underlying negative effects of Airbnb on the residential communities out of worries about housing affordability and supply in the city [3, 4].  

---

### 3. How was it collected?

#### 75 words; 7 points; What was the method by which the data was collected and how might this shape its form/content?

The firsthand data including every detail of each available listing, which directly and publicly shown on its own page on the Airbnb’s site, were snapshotted and obtained by the website scraper using python scripts [5]. Although the source code was not provided, the general process of collection shared by IA was that the web scraper identified the unique ID of each listing within London and extracted all the potential information in the page source, respectively [2, 5]. 

---

### 4. What useful information does it contain?

#### 100 words; 12 points; Discuss how the data might support subsequent analysis.

The complied dataset had 74 columns, covering the extracted or calculated data of housing description, details of the host, location, property conditions, price, availability, reviews and scores of reviews [6]. The detailed descriptions that containing interesting characteristics for target customers could be filtered through text mining, which allows the classifications of listings in various topics [7, 8]. The combination of price, availability and number of reviews may predict the possible annual yields and the housing vacancy rate [8]. Descriptions and scores of reviews may contribute to reflect the degree of preferences and perceived trust of guests on housing [9]. Location under any reasonable condition X could reveal certain geographic patterns.

---

### 5. To what extent is the data 'complete'?

#### 200 words; 25 points; Reflecting on your earlier answers, to what extent is this data a ‘complete’ picture of the process that it claims to allow us to examine?

Limitation of the scraper may sometimes randomly cause errors and inevitably lead to missing of data [4] or export no value when no data matched. A certain fraction of listings presented a series of missing data in the fields. For different purposes when utilizing the dataset, the missing data in certain fields have unequal explanatory power on ‘complete’. The absence of data can also be considered as a form of data. For instance, when examining reviews, listings that missing scores of reviews should be marked and considered separately.

Structural omission of data is systematically existed. Data of gender, reviews and available language options about the host were not included and specified. In the field of amenities, the term that describes check-in services was missing. The number of positive and negative reviews of each listing were not given in the dataset, although it may not be accessed directly. Affected by the potential purpose of seeking negative impacts of short-term rentals, sort of data such as data listed above were unconsciously avoided. Such omission of data that may be attributed to the limited consideration of the process or potential bias could impact on the integrity and quality of the data [10].

---

### 6. What kinds of analysis would this support?


#### 200 words; 15 points; Given the issues discussed above, what kinds of analysis would this data support?
Simple establishment of two models would be supported by this dataset: one is the estimated occupancy model based on the data of room type, availability 90 days in the future, reviews per month, average booking nights in London [5, 11]; the other one is the income model that could simulate the annual yields through price per night and occupancy rate. In consideration of the limitation of scraper and the omission of books per listing, the established models have great limitation in estimating the occupancy rate and the income. But a series analysis following these two models could still be subsequently proceeded.

Example project [8] showed a nice  analysis on averages of price, income, scores of reviews within listings groups that filtered by topic tag that involved in the description. This analysis contributes to the exploration of relationship among reputation, customers’ expectation and popularity. Geographic patterns of aggregation of low-occupancy-rate and high-income are possible to be examined and investigated. Also, by comparing the average income from local rent with the short-term rental income from tourism, the contrast might make the process of gentrification much more visualized. In addition, by ranking the total counts of listings that a host has, it is possible to detailly check whether or not a host is against the law of short-term rental [12].

---

### 7. Which of the uses presented in Q.6 are _ethical_?

#### 350 words; 35 points; Which of the uses presented in Q.6 are ethical?  Justify the ethics of these analyses with reference to examples drawn from both your earlier answers and to the literature. 35 points

As for the modelling of occupancy rate and income, it could be largely considered as ethical. As illustrated above, the collected data from Airbnb’s site were publicly transparent, which can be accessed by anyone. Although it may be argued that web mining raises privacy issues as customers are analyzed unknowingly [13]. The mentioned analysis associated with reviews that only focuses on scores and number should be anonymous, which should avoid the issues of personal privacy. In IA’s disclaimers, it was stated that location information of each listing was also anonymized by Airbnb [5]. Though it was claimed that Airbnb calendar might not be accurate, it is the currently optimal approach to obtain the occupancy rate. 

The outcome of such analysis mainly concentrates on the short-term rental in the scale of the whole city instead of the locality. However, the exploration of trends in gentrification and of geographic patterns of condition X in London might over emphasize the role of some certain trend and pattern.

The investigations on the hosts that occupy great number of listings on Airbnb may not be ethical. Due to the uncertainty and randomly occurred errors of website scrapers [2], it is not appropriate and ethic to accuse the potential violation against short-term rental laws without full validation of the data. For instance, the host ID 58828772 showed 116 counts of total listings in the dataset but in fact this host only had 2 listings on the website (could also be attributed to the difference between snapshot and updated web page). Although the intention of this analysis is good, it is undeniable that such ‘accusation’ may cause unpredictable impacts on specific individual [14]. 

---
## Bibliography
[1]<a>&emsp;D.D. Lehr, “An analysis of the changing competitive landscape in the hotel industry regarding Airbnb,” Graduate Master's Theses, Capstones, and Culminating Projects, Dominican University of California, California, 2015.</a>

[2]<a>&emsp;M. Cox and T. Slee, “How Airbnb’s data hid the facts in New York City,” Inside Airbnb., 2016. Available: http://insideairbnb.com/reports/how-airbnbs-data-hid-the-facts-in-new-york-city.pdf</a>

[3]<a>&emsp;M. Han. (2018 Feb. 26). *Murray Cox, the Australian 'data activist' taking on Airbnb* [Online]. Available: https://www.afr.com/property/residential/murray-cox-the-australian-data-activist-taking-on-airbnb-20180226-h0wn4g</a>

[4]<a>&emsp;A. Alsudais. (2021 Feb.). “Incorrect data in the widely used Inside Airbnb dataset.” *Decision Support Systems* [Online]. vol. 141, 113453. Available: https://www.sciencedirect.com/science/article/pii/S0167923620302086?via%3Dihub</a>

[5]<a>&emsp;Inside Airbnb. *Disclaimers* [Online]. Available: http://insideairbnb.com/about.html#disclaimers</a>

[6]<a>&emsp;Inside Airbnb, “Data Dictionary for listings.csv detailed file,” Version 4, Aug. 2020. Available: https://docs.google.com/spreadsheets/d/1iWCNJcSutYqpULSQHlNyGInUvHg2BoUGoNRIGa6Szc4/edit#gid=982310896</a>

[7]<a>&emsp;Y. Chung and S. Sarnikar. (2020, Oct) “Understanding host marketing strategies on Airbnb and their impact on listing performance: a text analytics approach.” *Information Technology and People* [Online]. Available: https://www.emerald.com/insight/content/doi/10.1108/ITP-10-2020-0718/full/html?casa_token=voFa18wFZnAAAAAA:LEF7Pg2qWHWg3Ltqe27H0oeyZCU_D0P-qAJ2laIW__eP27_ILDSGA-hRQVQetcsfy6_VA2LxTtcQ9C38DC6fd5fLEcPluVa1rSK75KvaBuzhR2MYENCw</a>

[8]<a>&emsp;J. Chew. (2017, Nov. 23). *Machine Learning Engineer Nanodegree: Capstone Project* [Online]. Available: https://github.com/joaeechew/airbnb_nlp/blob/master/archives/Capstone%20Project%20Report%20171009.ipynb</a>

[9]<a>&emsp;L. Zhang, Q. Yan and L. Zhang. (2020, March). “A text analytics framework for understanding the relationships among host self-description, trust perception and purchase behavior on Airbnb”. *Decision Support Systems* [Online]. Vol. 133. Available: https://www.sciencedirect.com/science/article/pii/S0167923620300439?casa_token=QYHczA0KWwwAAAAA:5M1rFC1vx7glnGBvN0X3jFWEVxqtV8FwePYpFcx33G-AbZ5phKJo9zTnsfwM84HzxAEVkSrDhOU</a>

[10]<a>&emsp;H, Kang. (2013, May). “The prevention and handling of the missing data.” *Korean J Anesthesiol* [Online] vol. 64, issue 5. Available: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3668100/</a>

[11]<a>&emsp;C. Y. Heo, I. Blal and M. Choi. (2019, Feb.). “What is happening in Paris? Airbnb, hotels, and the Parisian market: A case study.” *Tourism Management* [Online]. vol. 70. Available: https://www.sciencedirect.com/science/article/pii/S0261517718300785?casa_token=obmpSq_0jhIAAAAA:QgSGXiTFC3hvu6PrHmCjvv25wOiFZ_qKLVKltw2LQS2PYzqG9c6f65Fa28-H5TXWszEj81rLITw</a>

[12]<a>&emsp;A. Cocola-Gant and A. Gago. (2021). “Airbnb, buy-to-let investment and tourism-driven displacement: A case study in Lisbon.” *Environment and
Planning A: Economy and Space* [Online]. vol. 53, issue 7. Available: https://journals.sagepub.com/doi/10.1177/0308518X19869012</a>

[13]<a>&emsp;L. Wel and L. Royakkers. (2004). “Ethical issues in web data mining.” *Ethics and Information Technology* [Online]. vol. 6. Available: https://link.springer.com/article/10.1023/B:ETIN.0000047476.05912.3d</a>

[14]<a>&emsp;C. Cote. (2021, Mar. 16). *5 Principles of Data Ethics for Business* [Online]. Available: https://online.hbs.edu/blog/post/data-ethics</a>


