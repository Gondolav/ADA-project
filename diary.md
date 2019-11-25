This document relates everything we have done on the dataset each time we met.
We worked a lot individually in between these meetings.

# 05/11/19:
_Andrea, Ludo and Thomas_
* Remove duplicates on the `Inspection ID` so that this column becomes a unique index. Consequently, set index to `Inspection ID`.
* Delete the six last rows as the five last are always empty and the sixth before the end (`Location`) is just a combination of two other columns (`Longitude` and `Latitude`).
* Slice the inspection dates to drop the hour of the inspection (never specified) and change them into proper pandas dates so that we can use them easily.
* Remove all rows with an inspection date posterior to __July 1st, 2018__, when changes to the food inspection procedures happen. We decided to only work on food inspections before that date to keep a homogeneous dataset.
* Drop rows with a NaN `City`, `State`, `Zip`, `Latitude` and `Longitude`.
* Drop rows with a 0 `License \#` as we consider it as a NaN value.
* Delete rows with no state or a state far from Chicago (__NY__, __WI__). We checked that the only facility in Wisconsin was far from the border with Illinois.
* Clean up the city names:
  * by normalizing them, e.g. Chicago, CHICAGO and CHICAGOI are the same city. We decided to put all the names to uppercase for simplicity.
  * by deleting the name __INACTIVE__, which doesn't exist.

# 07/11/19:
_Andrea and Ludo_
* Remove useless `State` filter because all remaining inspections are located in Illinois.
* Cast `License \#` and `Zip` from float to int as they are integers.
* Put `Facility Type`, `Risk`, `Address`, `Inspection Type` and `Results` to uppercase.
* Convert `Facility Type`, `Risk`, `Inspection Type` and `Results` from string to category.

# 25/11/29:
_Andrea, Ludo, Hugo and Thomas_
* Finish answering the different questions we addressed in the first milestone:
    * Answer the question about licenses. how?
    * Are establishments more likely to fail? Must choose our way of answering
    * Provide insightful comments on every question
    * Elaborate on the violation analysis
    * how far are we going on the evolution over time and space? Need to make our plot more readable

# Research questions
## Inspections' effects on establishments
- [x] Does an inspection have a positive effect on the future inspections? i.e. does inspecting increase an establishment’s quality?
- [x] Are inspections requested by the establishments usually favorable?
- [x] What is the evolution of the overall inspection frequency over the last decade?

## Establishments' predispositions to inspection failure
- [x] Which facility type is more likely to fail?
- [ ] Are restaurants having already failed once more likely to fail again than the others? And are they more likely to close definitively?
- [x] Compare the inspection results of the different fast-food restaurant chains against themselves or other restaurants.

## Neighbourhood and food quality correlation
- [ ] How are the inspection results evolving over time and space?
- [x] Is there a relationship between the location of the restaurant and the quality? (economic and social causes)
- [x] What is the most encountered violation category for each neighborhood?

## Violation analysis
- [x] What are the frequencies of each violation?
- [x] Are some violations more frequent than others in an establishment’s failure?
- [x] What are the most frequent violations encountered during complaint-caused inspections?
