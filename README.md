# DataStory_global-abortion

#### *In-progress*: 

Groundwork completed (Phase 0: find data, decide on scope, and write a pitch for the write-up for this project). A more concise version of this ReadMe would be updated upon project completion.

### Data Cleaning, Storytelling, Visualization project: 
### Motivation

#### *How do anti-abortion laws and regulations recently passed in certain US states compare with those from other countries around the world?* 

(Hint: it does not look good for the US.)

Inspired by this article: https://www.cnn.com/2019/05/17/world/how-alabama-abortion-compares-to-world-intl/index.html

> "Alabama passed a near-total ban on abortion this week, strict enough to rival abortion rules in countries like Brunei, Guatemala and Syria."

So far I have found some good resources and dedicated groups doing research on women's reproductive health. However, none of the visualizations I've come across have put the abortion regulations by world countries and US States in direct comparison. This is what I'm hoping to achieve with this project. 

There are quite a few challenges including finding and integrating the data (with matching topics and years), reducing the scope and choosing only a handful of key factors in this very complex global and socioeconomic issue, as well as choosing a type of visualization that displays verbal and geographical information well, and allows for some flexibility in scaling (can actually zoom in and see the US States on world map, or might need multiple maps for that), among others.

### Notes

My goal is to generate two sets of visualizations to compare progress (or the lack thereof) among US States and other nations of the world, over the span of the past *x* years (depending on what data I can find - 10 years seems the most reasonable). 

**Phase 1** -- Data Cleaning and Preparation (time-consuming! getting different forms of raw data from NGOs, government websites, and international organizations like the United Nations)

**Phase 2** -- One set of visualizations: US States and World Nations
  - *How many variables to include?* The main one is under what circumstances can a woman in the state/nation get an abortion. 
  But might also need to consider the ease of access (mandatory waiting periods), cost (healthcare coverage and income - can vary by ethnicity)...) 
  
  **Either choose 3 key factors to visualize for Phase 1, or build into a ranking system which would make plotting easier**
  
  
--*Note: Phase 1 and 2 make up a self-contained project, sufficient to write one article on*

--*Phase 3 and 4 are more social science research questions:* dig deeper into the human rights issue out of personal interest (but might need to curb curiosity here to move to machine learning projects in the short term)

**Phase 3** -- Add a second set of visualizations: How policies changed over time (key years for the US: 1973, 2010, 2019) in the US
  - Include more variables during comparison: dig deeper into the possible reasons behind the contrasts; how do the different factors correlate? 
  - also consequences of anti-abortion laws (combine with, or separate from phase 1: infant mortality rates (Status of Women report data)
    * New angle (from New Yorker article, March issue): induced abortion rates worldwide (2018 Guttmacher data) stayed about the same, suggesting anti-abortion laws lead to unsafe underground practices and affect women's health (might be hard to find data to support the second part)
  
**Phase 4** -- Explore more variables on a global scale for a more thorough study (ie. youth crime rates and homelessness, public education, healthcare, cost of raising a child), compare with US policy change over time: more progress? less progress?

### Data Acquisition and Preparation
So far I noticed there are a lot of US data for 2012 and 2013, but few recent data from State governments - the only ones on data.gov are from Illinois from 2012, and all the URLs are broken.

I was able to find World data for 2017 and 2018 (as recent as it gets). I plan to add the new anti-abortion policies from US states manually, to produce a visualization that is more up-to-date than the ones I found. I also plan on monitoring the news and updating the visualization.

  (A bonus feature in the long run (after writing up a blog about the conlcusions) would be to include web scraping of news sites, or creat customized news alerts when the visualizations need to be updated.)

### Data Visualization
Geographic map, by state/country, interactive features

*July 12 Update:*

Edited the entire README, separated Phases 1 - 4, set shorter-term goals, more emphasis on data cleaning before trying Plotly vs. Folium

Even though Folium works for choropleth, noticed Plotly allows easy addition of hovering data boxes which could make understanding the visualizations earlier;
> For example, box next to a state or country could say: 

> no reason given: N, health of woman: Y, rape and incest: Y -- which would mean for this particular location, an abortion request with no reasons provided would not be permitted, but if it threatens the health of the woman, or if the pregnancy is due to rape or incest, then abortion is legal in this state or nation.

Plotly cheatsheet: https://images.plot.ly/plotly-documentation/images/python_cheat_sheet.pdf


*July 1 Update:*

Found out the Choropleth class in Folium has multiple issues and may no longer be supported in the new version after 2018. Consider using Plotly instead? 

Plot.ly: 

https://plot.ly/python/choropleth-maps/

https://community.plot.ly/t/choropleth-map-in-dash/4807

General considerations for making choropleth maps: https://blog.datawrapper.de/choroplethmaps/

Updated to Folium 0.9.1 (Newest, May 26, 2019), now choropleth example works. 

GeoJSON and choropleth: https://nbviewer.jupyter.org/github/python-visualization/folium/blob/master/examples/GeoJSON_and_choropleth.ipynb

*June 19 Update:*

Folium Choropleth Map -- works best when the colour-coded layer represents a column which contains a numerical value (such as %unemployment rate in example) - How to translate text result in data?

Folium documentation: https://python-visualization.github.io/folium/quickstart.html

### Data Analysis

### Further Work

---------------------------
### References:
 #### General

* CNN news article:
https://www.cnn.com/2019/05/17/world/how-alabama-abortion-compares-to-world-intl/index.html

* What to consider when making choropleth maps (good reference): https://blog.datawrapper.de/choroplethmaps/ 


 #### World Data

* UN reproductive health policies 2017 data booklet:
https://www.un.org/en/development/desa/population/publications/pdf/policy/reproductive_health_policies_2017_data_booklet.pdf


* Guttmacher Institute 2017 report:
https://www.guttmacher.org/report/abortion-worldwide-2017

  * Would like to create a visualization similar to this one, but being able to see US states on the same map: https://www.guttmacher.org/abortion-legality-worldwide (not sure yet if a Folium choropleth map is enough, might need to look into interactive elements?)

* Guttmacher Institute 2018 fact sheet:
https://www.guttmacher.org/fact-sheet/induced-abortion-worldwide

* __Guttmacher Data Center data__: 

(unfortunately categories don't match with the ones for US States; abortion data by region not by individual country)

https://data.guttmacher.org/regions

 > Data Source (table: Abortion and outcomes by region): Abortion incidence between 1990 and 2014: global, regional, and subregional levels and trends The Lancet. Sedgh G et al. 2016 https://www.guttmacher.org/article/2016/05/AWW-levels-and-trends-abortion-incidence-1990-2014 https://doi.org/10.1016/S0140-6736(16)30380-4 (can compare 10 year trend for Phase 3 or 4)
 
 > Data Source (table: Unintended pregnancies):  [Global, regional, and subregional trends in unintended pregnancy and its outcomes from 1990 to 2014: estimates from a Bayesian hierarchical model](https://www.guttmacher.org/article/2018/03/unintended-pregnancy-and-its-outcomes-global-regional-and-subregional-trends-1990), Lancet Global Health, 6(4):e380–e389, Bearak J et al., 2018
 
   __*44%__ of pregnancies world wide are unintended!* (https://www.guttmacher.org/infographic/2018/proportion-pregnancies-are-unintended-worldwide) (2018 inforgraphic using 1990-2014 data in source above)

 #### US Data - by State

(Published July 1, 2019 by Guttmacher Institute) *An Overview of (US) Abortion Laws* (the most up-to-date data and report by State):

https://www.guttmacher.org/state-policy/explore/overview-abortion-laws

* __Guttmacher Data Center data__: 

https://data.guttmacher.org/states

  > Data Source (2016 Guttmacher report, for tables: us-abortion-by-state-of-occurence, us-no-of-abortions): [Abortion Incidence and Service Availability in the United States, 2014](https://www.guttmacher.org/journals/psrh/2017/01/abortion-incidence-and-service-availability-united-states-2014), Rachel K. Jones, Jenna Jerman, 2016
  
  > Data Source (for tables: us-pregnancies-ending-in-abortion, abortion-rate-by-state-of-residence): Kost K, Maddow-Zimet I and Kochhar S, Pregnancy Desires and Pregnancies at the State Level: Estimates for 2014, New York: Guttmacher Institute, 2018 https://www.guttmacher.org/reports/pregnancy-desires-and-pregnancies-state-level-estimates-2014
  
 
* (Published June 1, 2019 by Guttmacher Institute) detailed look at US abortion laws by State (detailed, need to summarize and categorize before attempting to visualize): https://www.guttmacher.org/state-policy/explore/overview-abortion-laws

* Status of Women in the States, 2015 report using 2012 and 2013 data: https://statusofwomendata.org/explore-the-data/reproductive-rights/#download-data
  - They mention another report completed in 2004 but do not provide a link (I suspect it's not digitized...Will keep looking).
  - It's good because it also contains economic data and infant mortality data (separate download) which I would also like to incorporate into this data storytelling project
  
* US 5-10 year trend: Guttmacher Institute, Last five years account for more than one-quarter of all abortion restrictions enacted since Roe, News in Context, https://www.guttmacher.org/article/2016/01/last-five-years-account-more-one-quarter-all-abortion-restrictions-enacted-roe (Jan. 2016) 

