# 1. Title
Give me your London ZIP, I'll judge how you eat!
# 2. Abstract
When reading the original paper, we noticed that not all the data at hand was being examined. We wish to analyze the relation between alcohol and macronutrient consumptions and several social indicators provided by the London statistics such as income rates, unemployment or education.

We will be computing correlation coefficients for those features, at lsoa area levels and using area's representativeness as a way to make sure alcohol and macronutrient consumption is representative of the area.

To go further, we will try to look for features that are correlated with the desired indicators (such as age or ethnic groups), those features being likely to introduce undesired biases. We will then perform a matching study.

Moeover, we will collect macronutient intake recommendations (like sugar, fat, protein...) stated by the WOH and other sources for a good Health diet. We will compute a score for each area from 0 to 1. If they have one, it means they fully follow the recommendations. This score will be shown in a map of London.
Finally, we will try to correlated these final scores to social and demographic indicators as Household Income, level of education...
# 3. Research questions
- Does an area’s general wealth reflect its average alcohol consumption ?
- More broadly, is it possible to predict an average alcohol’s consumption depending on the characteristics of an area ?
- Which are the area following the WOH recommendation ?
- Is there a link betwneen a healthy diet and social indicators ?
# 4. Proposed datasets
- Current LSOA boundaries post 2011 [(link)](https://data.london.gov.uk/download/lsoa-atlas/b8e01c3a-f5e3-4417-82b3-02ad271e6ee8/lsoa-data.xls): ‘The LSOA atlas provides a summary of demographic and related data for each Lower Super Output Area in Greater London.’ This data set gives us information such as the mean annual income of areas, % of employments, level of qualification, fatal road casualties...
- lsoa-data.csv (provided by TAs): contains the aggregated information on food purchases, enriched with information coming from the census for the full year 2015 at LSOA level. From this data we will use the alcohol and macronutrient consumed by areas and other information in our last analysis such as sex, age...
# 5. Methods
1. Data collection: Download the data and keep only the columns we need for our study. We will then merge them. Collect WOH macronutrient intake recommendations.
2. Data Processing:  First compute representativeness of each area to filter the data used. Make spearman correlation between alcohol and macronutrient consumption and chosen indicators. Then compute a linear regresion and matching for the case of alcohol consumption in order to improve our results and decrease possible biases.
For each macronutrient, compute a score based on WOH recommendation for each area and plot them in the map of London.
Finally compute spearmann correlations between final scores and social indicators.
3. Data analysis: Comment on the results. Plot a map of London with diet score. This will allow us to visualize geographically and adds a third information which is area proximity. Comment on the correlation results to determine if the diet score is influenced by social indicators
# 6. Proposed timeline
(For Part A, Part B to be done individually in parallel)

- November 30th - December 6th : Extension Analysis Notebook
- December 7th - 13th : Data story and Report
- December 14th - 18th : Form submission, video recording and submitting (by the end of the week to avoid working around Christmas)
# 7. Organization within the team
- Ken : Extension Analysis Notebook (propensity and plotting). Data Story.
- Nathan K. : Extension Analysis Notebook (matching). Report.
- Nathan M. : Downloading and merging the data. First “basics” correlation studies. Then focus on writing the data story and preparing all needed figures and examples. Finally work on the video with the 2 other team members.
# 8. Questions for TAs (optional)
We are mainly using 2 datasets but one is from 2011 to 2013 and the other one is from 2015. Is it an issue ? We believe we can use the dataset from 2011-2013 because what is important to us are the relative values of the data from the neighborhood. This is unlikely to change drastically in a few years time (i.e. a rich neighborhood doesn’t rapidly become poor).
