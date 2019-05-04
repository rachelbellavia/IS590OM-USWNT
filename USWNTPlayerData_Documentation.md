# USWNT Player Data

**Note**: Please see [Manifest.md]() for links to the documentation for all intermediate datasets.

## Data Cleaning

No cleaning was performed directly on this data.

## Authorship

Data was curated from the U.S. Soccer website, Wikipedia, and the U.S. Census. Please see documentation on individual intermediate datasets for full citation and authorship information.

## Semantic Contents

This dataset contains biographical information about players on the U.S. Women's National Soccer Team and demographic information about the colleges they attended and their hometowns.

Data was compiled in May 2019.

## Collection Process

This data was collected using Python 3.7 in a Jupyter Notebook.

Tools used:

* Requests
* Lxml
* Xpath
* Pandas

This data is accumulated from multiple datasets. One dataset is from the U.S. Census, and it is used to determine the population of the hometown for USWNT players.

Two other datasets are used for each roster year represented in this final dataset.

* Player biographical data was scraped from the U.S. Soccer website, with xpath used to isolate the relevant information from each player's bio page.
* Player names were used to connect to their Wikipedia page. From the player Wikipedia page, I could then locate the college team they played for and therefore the school they attended. I used xpath to isolate information about colleges from their Wikipedia pages.

U.S. Census data was connected to the U.S. Soccer data based on the player's hometown. A key was used to determine the census code for the player's state, region, and division, and then I searched for the town name within the individual state to connect the data.

Once these datasets were incorporated, I could combine the U.S. Soccer data with Wikipedia data according to the original file name for the player bio, from which all other data was derived.

## Data Structure

Data is stored in csv format, with each row representing an individual player.

* Number of columns: 24
* Number of rows: 67
* Using missing value of: null

Data for each player:

* Roster year
* Player first name and surname
* Player position
* Player birthdate
* Player height
* Player hometown
	* State Code
	* Division Code
	* Region Code
	* Hometown Population
* First college attended
	* college name
	* college location
	* college enrollment
	* whether the college is public/private/community
* Second college attended
	* college name
	* college location
	* college enrollment
	* whether the college is public/private/community

Most data is recorded as text. Roster years are recorded as numerals. Birthdates are given in standard date format. Population and enrollment are given as numerals. Census codes are given as numerals representing a particular location.

**Roster Year**
-------------
* Description of column: Represents the roster year on which the player appears. Players will appear in the dataset multiple times for each roster year.
* Description of data values and units: Year
* Reason for missing values: Should not be missing
* Unique values: 2 (this includes missing values)
* Unique value content: The values are:
	* 2009
	* 2018
* Missing: 0
* Percent missing: 0%
* Percent digit: 100%
* Min digit: 2009.0
* Max digit: 2018.0

**Player Filename**
-----------------
* Description of column: Represents the original HTML file for the biography webpage for the player. The file name is directly derived from the URL of their bio on the U.S. Soccer website. This is used as the player ID, since each player must have a unique URL on the website.
* Description of data values and units: Text representing a single file name
* Reason for missing values: Should not be missing
* Unique values: 63 (this includes missing values)
* Unique value content: Not reported (More than 10 unique values)
* Missing: 0
* Percent missing: 0%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**Firstname**
-----------
* Description of column: Represents the first name of the player, as given on their bio page on the U.S. Soccer website.
* Description of data values and units: Text representing a person's name
* Reason for missing values: Should not be missing
* Unique values: 59 (this includes missing values)
* Unique value content: Not reported (More than 10 unique values)
* Missing: 0
* Percent missing: 0%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**Surname**
---------
* Description of column: Represents the surname of the player, as given on their bio page on the U.S. Soccer website.
* Description of data values and units: Text representing a person's name
* Reason for missing values: Should not be missing
* Unique values: 63 (this includes missing values)
* Unique value content: Not reported (More than 10 unique values)
* Missing: 0
* Percent missing: 0%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**Position**
----------
* Description of column: Represents the soccer position the player primarily plays.
* Description of data values and units: Text representing a playing position
* Reason for missing values: Should not be missing
* Unique values: 4 (this includes missing values)
* Unique value content: The values are:
	* Defender
	* Forward
	* Goalkeeper
	* Midfielder
* Missing: 0
* Percent missing: 0%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**Birthdate**
-----------
* Description of column: Represents the birthdate of the player.
* Description of data values and units: Date representing a person's birthdate
* Reason for missing values: Should not be missing
* Unique values: 62 (this includes missing values)
* Unique value content: Not reported (More than 10 unique values)
* Missing: 0
* Percent missing: 0%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**Height**
--------
* Description of column: Represents the height of the player in feet and inches.
* Description of data values and units: Hyphenated numerals, with the first digit representing feet and the second representing inches. Example: 5-7 representing 5 feet, 7 inches.
* Reason for missing values: Should not be missing
* Unique values: 12 (this includes missing values)
* Unique value content: Not reported (More than 10 unique values)
* Missing: 0
* Percent missing: 0%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**Hometown**
----------
* Description of column: Represents the hometown of a player as listed on their biographical page.
* Description of data values and units: Text listed in 'City, State' format
* Reason for missing values: Should not be missing
* Unique values: 59 (this includes missing values)
* Unique value content: Not reported (More than 10 unique values)
* Missing: 0
* Percent missing: 0%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**State Code**
------------
* Description of column: Represents the state code used by the U.S. Census to identify a state.
* Description of data values and units: Numeral representing a state
* Reason for missing values: Should not be missing
* Unique values: 27 (this includes missing values)
* Unique value content: Not reported (More than 10 unique values)
* Missing: 0
* Percent missing: 0%
* Percent digit: 100%
* Min digit: 1.0
* Max digit: 55.0

**Division Code**
---------------
* Description of column: Represents the division code used by the U.S. Census to identify a division.
* Description of data values and units: Numeral representing a division
* Reason for missing values: Should not be missing
* Unique values: 9 (this includes missing values)
* Unique value content: The values are:
	* 1
	* 2
	* 3
	* 4
	* 5
	* 6
	* 7
	* 8
	* 9
* Missing: 0
* Percent missing: 0%
* Percent digit: 100%
* Min digit: 1.0
* Max digit: 9.0

**Region Code**
-------------
* Description of column: Represents the region code used by the U.S. Census to identify a division.
* Description of data values and units: Numeral representing a division
* Reason for missing values: Should not be missing
* Unique values: 4 (this includes missing values)
* Unique value content: The values are:
	* 1
	* 2
	* 3
	* 4
* Missing: 0
* Percent missing: 0%
* Percent digit: 100%
* Min digit: 1.0
* Max digit: 4.0

**Hometown Population**
---------------------
* Description of column: Represents the total population of a player's hometown
* Description of data values and units: Numeral representing number of people
* Reason for missing values: The player's hometown was not identified as a 'place' on the U.S. Census. These are typically unincorporated communities or townships.
* Unique values: 57 (this includes missing values)
* Unique value content: Not reported (More than 10 unique values)
* Missing: 5
* Percent missing: 7%
* Percent digit: 93%
* Min digit: 1445.0
* Max digit: 945942.0

**First College Name**
--------------------
* Description of column: Name of the first college attended by a player
* Description of data values and units: Text representing the name of a school
* Reason for missing values: The player elected not to attend college
* Unique values: 26 (this includes missing values)
* Unique value content: Not reported (More than 10 unique values)
* Missing: 2
* Percent missing: 3%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**First College Public**
----------------------
* Description of column: Identifies whether the first college attended was a public university
* Description of data values and units: 'y' or 'n' indicating whether 'Public' was found in the description of the school
* Reason for missing values: The player elected not to attend college
* Unique values: 3 (this includes missing values)
* Unique value content: The values are:
	* [missing code]
	* n
	* y
* Missing: 2
* Percent missing: 3%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**First College Private**
-----------------------
* Description of column: Identifies whether the first college attended was a private university
* Description of data values and units: 'y' or 'n' indicating whether 'Private' was found in the description of the school
* Reason for missing values: The player elected not to attend college
* Unique values: 3 (this includes missing values)
* Unique value content: The values are:
	* [missing code]
	* n
	* y
* Missing: 2
* Percent missing: 3%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**First College Community**
-------------------------
* Description of column: Identifies whether the first college attended was a private university
* Description of data values and units: 'y' or 'n' indicating whether 'Private' was found in the description of the school
* Reason for missing values: The player elected not to attend college
* Unique values: 3 (this includes missing values)
* Unique value content: The values are:
	* [missing code]
	* n
	* y
* Missing: 2
* Percent missing: 3%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**First College Location**
------------------------
* Description of column: Identifies the location of the first college
* Description of data values and units: Text representing the name of a place
* Reason for missing values: The player elected not to attend college
* Unique values: 26 (this includes missing values)
* Unique value content: Not reported (More than 10 unique values)
* Missing: 2
* Percent missing: 3%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**First College Enrollment**
--------------------------
* Description of column: Represents the number of students who attended the first college
* Description of data values and units: Numeral representing the number of students
* Reason for missing values: The player elected not to attend college
* Unique values: 26 (this includes missing values)
* Unique value content: Not reported (More than 10 unique values)
* Missing: 2
* Percent missing: 3%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**Second College Name**
---------------------
* Description of column: Name of the second college attended by a player
* Description of data values and units: Text representing the name of a school
* Reason for missing values: The player did not attend a second college
* Unique values: 3 (this includes missing values)
* Unique value content: The values are:
	* Texas A&M University
	* University of North Carolina at Chapel Hill
	* [missing code]
* Missing: 64
* Percent missing: 96%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**Second College Public**
-----------------------
* Description of column: Identifies whether the second college attended was a public university
* Description of data values and units: 'y' or 'n' indicating whether 'Public' was found in the description of the school
* Reason for missing values: The player did not attend a second college
* Unique values: 2 (this includes missing values)
* Unique value content: The values are:
	* [missing code]
	* y
* Missing: 64
* Percent missing: 96%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**Second College Private**
------------------------
* Description of column: Identifies whether the second college attended was a private university
* Description of data values and units: 'y' or 'n' indicating whether 'Private' was found in the description of the school
* Reason for missing values: The player did not attend a second college
* Unique values: 2 (this includes missing values)
* Unique value content: The values are:
	* [missing code]
	* n
* Missing: 64
* Percent missing: 96%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**Second College Community**
--------------------------
* Description of column: Identifies whether the second college attended was a community college
* Description of data values and units: 'y' or 'n' indicating whether 'Community' was found in the description of the school
* Reason for missing values: The player did not attend a second college
* Unique values: 2 (this includes missing values)
* Unique value content: The values are:
	* [missing code]
	* n
* Missing: 64
* Percent missing: 96%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**Second College Location**
-------------------------
* Description of column: Identifies the location of the second college
* Description of data values and units: Text representing the name of a place
* Reason for missing values: The player did not attend a second college
* Unique values: 3 (this includes missing values)
* Unique value content: The values are:
	* Chapel Hill,North Carolina
	* College Station,Texas
	* [missing code]
* Missing: 64
* Percent missing: 96%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

**Second College Enrollment**
---------------------------
* Description of column: Represents the number of students who attended the second college
* Description of data values and units: Numeral representing the number of students
* Reason for missing values: The player did not attend a second college
* Unique values: 3 (this includes missing values)
* Unique value content: The values are:
	* 29,847 
	* 69,367 
	* [missing code]
* Missing: 64
* Percent missing: 96%
* Percent digit: 0%
* Min digit: no digits
* Max digit: no digits

