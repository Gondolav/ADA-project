# Where to eat safely in Chicago: gaining insight from food establishments inspections

# Abstract
Chicago is home to 16,000 food establishments like restaurants, grocery stores, bakeries, wholesalers, lunchrooms, mobile food vendors and more. In this project, we would like to give an overview of the city's food safety over the last decade. To do so, we are using a dataset of all the food inspections performed by the Chicago Department of Public Health's Food Protection Program. The main idea is to identify patterns at the social and geographical levels throughout time. More specifically, we want to study the frequency of the different violations, the way inspections influence the quality of food establishments, the relationship between violations and facilities location as well as the potential differences between the restaurants' types. With our work, we hope to raise awareness about the Chicago's food safety landscape and instruct people on the quality of the establishments they regularly visit.

# Research questions
## Inspections' effects on establishments
- Does an inspection have a positive effect on the future inspections? i.e. does inspecting increase an establishment’s quality?
- Are inspections requested by the establishments usually favorable?
- ~~Do these establishments still receive regular inspections? i.e. is requesting an inspection advantageous to an establishment to avoid subsequent inspections?~~
- What is the proportion of successful inspections needed in order to obtain a license? i.e. assess the difficulty to obtain such a license (per facility type).
- What is the evolution of the overall inspection frequency over the last decade?

## Establishments' predispositions to inspection failure
- ~~Which facility type is more likely to fail?~~
- ~~Is the inspection frequency indeed correlated with the risk category?~~
- Are restaurants having already failed once more likely to fail again than the others? And are they more likely to close definitively?
- Compare the inspection results of the different fast food restaurant chains against themselves or other restaurants.
- ~~How are the inspection and establishment types linked with the inspection results?~~
- ~~Is there a relationship between the type of the restaurant and the quality?~~

## Neighbourhood and food quality correlation
- How are the inspection results evolving over time and space?
- Is there a relationship between the location of the restaurant and the quality? (economic and social causes)
- What is the most encountered violation category for each neighborhood?
- ~~Is there a correlation between the violation n°38 (INSECTS, RODENTS, & ANIMALS) and the location?~~

## Violation analysis
- What are the frequencies of each violation?
- Are some violations more frequent than others in an establishment’s failure?
- What are the most frequent violations encountered during complaint-caused inspections?

# Dataset
The [Chicago Department of Public Health's Food Protection Program website](https://www.kaggle.com/chicago/chicago-food-inspections#food-inspections.csv) provides us with a well-documented dataset of all the food inspections they have done over the past decade. After a first glance at the dataset, we noticed a small number of outliers, missing values and duplicates, except for the five last columns, where there is absolutely no data. Nevertheless, we have several ideas to manage and enrich the dataset. At first, we are going to categorize some columns such as "Facility Type" or "Risk" which take a finite number of values and are stored as strings. Also, to avoid mismatches, we will standardize values to have unique format (e.g. Chicago, CHICAGO, chicago).

# A list of internal milestones up until project milestone 2
We will try to have a well-documented and working code after each internal milestone.
- 04/11/2019: clean and parse the dataset to get a nice workspace; work on the first set of questions (Inspection' effects on establishments)
- 11/11/2019: work on the second set of questions (Establishments' predispositions to inspection failure)
- 18/11/2019: work on the third set of questions (Neighbourhood and food quality correlation)
- 25/11/2019: work on the last set of questions (Violation analysis); include at the end of the notebook a more structured informed plan for what comes next

# Updates on reaearch questions
We decided to remove a good number of questions so that we can ellaborate more on the ones we kept. Besides, most of the discarded questions were in fact redundant with other questions. Others were simply found irrelevant after we took a closer look to them.

# A list of internal milestones up until project milestone 2
Our goal is to tell a data story on where to eat safely in Chicago. To do so, our idea is to create several maps that help the customers find the safest places to eat in Chicago.


# Questions for TAs
- 
