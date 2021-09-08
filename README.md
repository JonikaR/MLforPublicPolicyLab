# MLforPublicPolicyLab

**Part 1 : Get Data**

In this assignment I have used 5 year US Census Data from 2019 (A description of variables can be found - https://www.socialexplorer.com/data/ACS2019_5yr/metadata/?ds=SE&table=A15001)

In order to access the data, I used the Python library called 'censusdata' -- https://pypi.org/project/CensusData/
This package is designed to provide easy access to the U.S. Census Bureau’s API (https://www.census.gov/developers/) in Python. It supports pulling data from the American Community Survey (ACS) and the Census Summary File.

I want to compare educational attainment for each gender.
For this I am using 3 variables that describe 'EDUCATIONAL ATTAINMENT FOR THE POPULATION BY SEX' :
 1. 'B15002_013E' - total males by 25 with some college
 2. 'B15002_030E' - total females by 25 with some college
 3. 'B15002_001E' - total population by 25 with some college

I also want to see if there were any difference in Median earnings between both the genders which could be further explored to see if the educational attainment is causal. Variables used for Median earnings:
1. 'B20002_003E' - Estimate!!Median earnings in the past 12 months (in 2019 inflation-adjusted dollars) --!!Male'),
2. 'B20002_002E' - Estimate!!Median earnings in the past 12 months (in 2019 inflation-adjusted dollars) --!!FeMale'),


**Part 2 : Transform Data**

Prepared Data to load into the PostgreSQL database.
Renamed the dataframe columns.
Converted the dataframe to CSV.

**Part 3 : Load Data**

Used 'psycopg2' package for connecting to PostgreSQL database. -- https://pypi.org/project/psycopg2/
Used 'copy_from' command to load data from CSV to Database efficiently.
