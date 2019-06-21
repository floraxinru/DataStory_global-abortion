# DataStory_global-abortion

#### In-progress: Preparation mostly completed (find data, decide on scope, and write a pitch for the write-up for this project), Phase 2 by the end of June or early July

Data Storytelling and Data Visualization project: 
### *How do anti-abortion laws and regulations recently passed in certain US states compare with those from other countries around the world?* 

(Hint: it does not look good for the US.)

Inspired by this article: https://www.cnn.com/2019/05/17/world/how-alabama-abortion-compares-to-world-intl/index.html

> "Alabama passed a near-total ban on abortion this week, strict enough to rival abortion rules in countries like Brunei, Guatemala and Syria."


### Notes
I am in the process of selecting and cleaning data from various resources online. 

My goal is to generate two sets of visualizations to compare progress (or the lack thereof) among US States and other nations of the world, over the span of the past 5, 10, 20 years (depending on what data I can find - 10 years seems the most reasonable). 

**Phase 1** -- One set of visualizations: US States and World Nations
  - *How many variables to include?* The main one is under what circumstances can a woman in the state/nation get an abortion. 
  But might also need to consider the ease of access (mandatory waiting periods), cost (healthcare coverage and income - can vary by ethnicity)...) 
  
  **Either choose 3 key factors to visualize for Phase 1, or build into a ranking system which would make plotting easier**
  
**Phase 2** -- Add a second set of visualizations: How policies changed over time (key years for the US: 1973, 2010, 2019) in the US 
  - Include more variables during comparison: dig deeper into the possible reasons behind the contrasts; how do the different factors correlate? 
  - also consequences of anti-abortion laws (combine with, or separate from phase 1: infant mortality rates (Status of Women report data)
    * New angle: induced abortion rates worldwide (2018 Guttmacher data) about the same, anti-abortion laws lead to unsafe underground practices and affect women's health (might be hard to find data to support the second part)
  
**Phase 3** -- Explore more variables on a global scale for a more thorough study (ie. youth crime rates and homelessness, public education, healthcare, cost of raising a child)

### Data Acquisition and Preparation
So far I noticed there are a lot of US data for 2012 and 2013, but few recent data from State governments - the only ones on data.gov are from Illinois from 2012, and all the URLs are broken.

I was able to find World data for 2017 and 2018 (as recent as it gets). I plan to add the new anti-abortion policies from US states manually, to produce a visualization that is more up-to-date than the ones I found. I also plan on monitoring the news and updating the visualization.

  (A bonus feature in the long run (after writing up a blog about the conlcusions) would be to include web scraping of news sites, or creat customized news alerts when the visualizations need to be updated.)

### Data Visualization
Geographic map, by state/country, interactive features

*June 19 Update:*

Folium Choropleth Map -- works best when the colour-coded layer represents a column which contains a numerical value (such as %unemployment rate in example) - How to translate text result in data?

Folium documentation: https://python-visualization.github.io/folium/quickstart.html

### Data Analysis

### Further Work


#### References:
* CNN news article:
https://www.cnn.com/2019/05/17/world/how-alabama-abortion-compares-to-world-intl/index.html

> #### World Data

* UN reproductive health policies 2017 data booklet:
https://www.un.org/en/development/desa/population/publications/pdf/policy/reproductive_health_policies_2017_data_booklet.pdf


* Guttmacher Institute 2017 report:
https://www.guttmacher.org/report/abortion-worldwide-2017

  * Would like to create a visualization similar to this one, but being able to see US states on the same map: https://www.guttmacher.org/abortion-legality-worldwide (not sure yet if a Folium choropleth map is enough, might need to look into interactive elements?)

* Guttmacher Institute 2018 fact sheet:
https://www.guttmacher.org/fact-sheet/induced-abortion-worldwide


> #### US Data - by State

* Status of Women in the States, 2015 report using 2012 and 2013 data: https://statusofwomendata.org/explore-the-data/reproductive-rights/#download-data
  - They mention another report completed in 2004 but do not provide a link (I suspect it's not digitized...Will keep looking).
  - It's good because it also contains economic data and infant mortality data (separate download) which I would also like to incorporate into this data storytelling project
  
* (Published June 1, 2019 by Guttmacher Institute) detailed look at US abortion laws by State (detailed, need to summarize and categorize before attempting to visualize): https://www.guttmacher.org/state-policy/explore/overview-abortion-laws

