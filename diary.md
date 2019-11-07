This document relates everything we have done on the dataset each time we met.

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

# 05/11/19:
_Andrea and Ludo_
* Remove useless `State` filter because all remaining inspections are located in Illinois.
* Cast `License \#` and `Zip` from float to int as they are integers.
* Put `Facility Type`, `Risk`, `Address`, `Inspection Type` and `Results` to uppercase.
* Convert `Facility Type`, `Risk`, `Inspection Type` and `Results` from string to category.
