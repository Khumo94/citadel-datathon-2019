# Team 26 Report

Note: This was the report we submitted for Citadel Datathon 2019. Here are the [problem statement](/Instructions/London&#32;Datathon&#32;Problem&#32;Statement.pdf) and [dataset schema](/Instructions/London&#32;Datathon&#32;Data&#32;Schema.pdf) for the challenge.

# How has Brexit impacted citizens and immigrants?

## Non-technical Executive Summary

### Introduction

In this report, we investigate how Brexit has impacted citizens in the United Kingdom as well as immigrants from various regions. More specifically, we set out to answer three questions:

•	How has Brexit affected the flow of people into the UK?

•	Which nationalities were affected the most?

•	How has the availability of jobs been changed by Brexit?

#### How has Brexit affected the flow of people into the UK?

The large number of citizenship applications reflect the level of sentiment of people who wish to immigrate to the UK. The immigration numbers for various regions are shown in the figure below.

|![alt text](https://github.com/hivestrung/citadel-datathon/blob/master/Graphs/immigrationovertheyears.png?raw=true "bigbrain")|
|:--:|
| *Figure 1: Immigration numbers for various continents* |

Figure 1 shows a generally decreasing trend in immigration data from 2008 to 2018. The number of American and Middle Eastern immigrants have been mostly constant, and have been relatively unaffected by Brexit (represented by the dotted line in the figure). Conversely, the Asian and African immigration rates have decreased steadily since Brexit. However, this decreasing trend dates back to 2013, which can be linked to Theresa May's aggressive stance on immigration in 2013 during her stint as Home Office Secretary. In that regard, Brexit has not had much impact on Asian and African immigration numbers.

The most illuminating trend was that of European immigration numbers. Surprisingly, immigrations numbers increased since Brexit in 2016, breaking a general downward trend since 2013. A potential factor is the increased uncertainty faced by Europeans working and living in the UK, and the introduction of the EU Settlement Scheme, which accelerated the process for citizenship applications. This is coupled with steadily brewing anti-EU and anti-immigration sentiments amongst the British public, which Brexit is mostly attributed to in the first place.

|![alt text](https://github.com/hivestrung/citadel-datathon/blob/master/Graphs/nationalities_correlation.png?raw=true "corr")|
|:--:|
| *Figure 2: Immigration numbers for various continents* |

The above heatmap in figure 2 depicts the correlation matrix amongst immigration numbers. The only negative correlations are that of the European immigration number with the rest of the world, indicating a clear dichotomy from the other trends and the potential for investigation down this path.

#### Which nationalities were affected the most?
Following from the previous hypothesis, European immigrations into the UK increased sharply after Brexit. To dissect this trend, we decided to take a more regional view of Europe, segregating the immigration numbers by countries.

|![alt text](https://github.com/hivestrung/citadel-datathon/blob/master/Graphs/chloropleth%20of%20europe.png?raw=true "yourbrain")|
|:--:|
| *Figure 3: Chloropleth of differences in immigration numbers since Brexit* |

The chloropleth above depicts the difference in immigration numbers since the Brexit referendum in 2016. Darker colours represent a greater exodus into the country, while lighter colours represents a greater exodus out of the country.

Despite the large decrease in immigrants from most parts of the region, the number of Polish, Italian, German and Romanian immigrants increased significantly over the three-year period, contrary to initial expectations.  This is indicative of the strong appeal of the UK as a hub for students and skilled labour.



We were also able to run a clustering algorithm that allowed us to obtain important subgroups that were the most impacted by Brexit. It turns out that employment for white men in managerial roles decreased after Brexit, whilst employment for black women in more blue-collar roles increased. This is an interesting trend and worth diving into. Unfortunately we were not able to have enough time to do so.


#### How has the availability of jobs been changed by Brexit?

We also sought to find out more about how job availability has been changed by Brexit, as job availability is a proxy for social mobility and opportunity available to the people, to improve their socioeconomic status.

We first plotted histograms, for every year, how many jobs were available each month, from the job listings dataset.

|![alttext](https://github.com/hivestrung/citadel-datathon/blob/master/Graphs/monthlychangeinjobsavailableeachyear.png?raw=true)|
|:--:|
| *Figure 4: Monthly Change in Jobs Available Within Each Year* |

It is vital to note here that the Brexit referendum occurred in June 2016. Inspecting the histograms prior to 2016, we see that there are usually more jobs crated in the second half of the year. However, in the 2016 histogram, we note that job postings actually declined, indicating that the shock and uncertainty of Brexit dampened the economic opportunities available to workers and potential employees.

However, in 2017 and 18, there are more jobs available across the board, and the shock in 2016's second half was not observed. We decided to investigate this further by plotting histograms comparing the number of jobs available each month across the years.

The rationale for doing so is that there may be reasons that there are generally, for example, fewer jobs available in January, and we wanted to reduce the impact of these month-to-month fluctuations on our findings, and instead try to understand just how job growth was impacted across the years.

|![Change in Jobs Available for Each Month Across Years](https://github.com/hivestrung/citadel-datathon/blob/master/Graphs/month%20on%20month%20change%20in%20jobs%20available.png?raw=true)|
|:--:|
| *Figure 5: Change in Jobs Available for Each Month Across Years* |

To illustrate this point, we consider the trends for January, February and March, which are very similar. However, looking at the numbers, we see that there are much fewer jobs available in January than February, and also fewer in February than March! Thus, by comparing between years for the same months, we are able to adjust for the changes based on the time of the year.

Looking at the overall trend, for many of the months, there seems to be a year-on-year increase in jobs available.

One might look at how there is a decrease between July 2015 and July 2016, and erroneously conclude that Brexit has negatively impacted jobs. However, comparing January-June 2015 and 2016 data, it is clear that there is a drop across the board, showing that 2016 was just a bad year for jobs (perhaps contributing to the Brexit referendum vote turning out as it did!).

In 2017, it seems that Brexit did negatively impact job growth in January and February, but by March and onwards, the number of jobs available started growing again.

Also, it is clearer now that in 2018, there was a strong increase in jobs available compared to previous years.

Lastly, it is also instrumental to scrutinise the 2019 data, as Brexit appears/appeared to be nearing its conclusion in 2019. In the beginning of the year, the number of jobs available is high, even growing, but from May onwards, there is a drop- and the drop is increasing all the way till August, which is the last of the data we have.

We note that at a meeting of the European Council on 10 April 2019, the UK and EU27 agreed to extend Article 50 until 31 October 2019. Thus, perhaps this extension served to dampen companies' optimism and reduce the number of jobs available.

Also of note is that Boris Johnson was elected 24 July 2019, and in August 2019 there was a significant drop in jobs available, suggesting that the public did not have faith in Boris (rightly so!).

We also wanted to refine our analysis further by investigating which cities were impacted by Brexit. We first looked at the 6 cities with the most number of jobs available across the period from 2011 till 2019.

![Yearly Change in Jobs Available for Specific Cities](https://github.com/hivestrung/citadel-datathon/blob/master/Graphs/yearly%20change%20in%20jobs%20available%20by%20place.png?raw=true)

Judging by the overall trend, there does not seem to be a large difference in how job availability was impacted based on localities, suggesting that Brexit has impacted opportunities somewhat equally. Of note is that from 2016 onwards, Oakdale in Wales has suddenly experienced a huge increase in the number of jobs available, which could be due to not having the data from before 2016, or due to Brexit positively impacting the region, which warrants further analysis.

To sum all this up, there does not actually seem to be much of an impact of Brexit on job availability on the whole. While there are short term 'shocks' and fluctuations due to uncertainty surrounding the terms of Brexit, after some time, these level out.

For further analysis, it also would be useful to analyse how Brexit has impacted locations which do not tend to have a lot of jobs available. Also, we can look into how job availability was impacted based on occupation types (using the occupation codes), and what sort of jobs are created in the wake of Brexit. Other areas we can look into are identifying which parts of the UK and EU supported Brexit, and what their prospects are today i.e. to say, were people "correct" in voting for or against Brexit?


## Technical Exposition

### Wrangling and Cleaning Process

• one-hot encoding of gender and nationalities  
• Only considered data where all entries of interest were filled, sufficient quantity of  
complete information to justify this.  
• Reformat data so it was on the same timescale.  
• Looked into PCA components  
• Concenated tables and data to give sufficient datapoints so that analysis could be done individually.  

### Investigative Depth

• We utilised a variant of k-means clustering, called k-prototypes, to detect the most important subgroups for our investigation.  
• K-prototypes enables us to identify important subgroups that faced the greatest impact after Brexit.  
• Weighted averaging of employment data across time to account for differences prior to and after Brexit  
• Using plots to investigate factors and using statistical tests to distinguish between valuable and invaluable relationships to further investigate.  
• Data was investigated in its relation to subgroup characteristics. Coloured europe map easy to interpret.

### Analytical and Modelling Rigor
• Applied a linear regression model for relationships for testing for effects although noting that the relationships are not likely to be linear
