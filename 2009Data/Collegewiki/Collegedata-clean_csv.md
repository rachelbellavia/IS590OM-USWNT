# Collegedata.csv

## Data Cleaning

This data was cleaned using OpenRefine, with one column affected: **First College Enrollment**. This column included extra data along with the numerals representing enrollment at the school, such as text indicating the semester in which the enrollment was reported. I used OpenRefine to remove this data to ensure only numerals remained.

The function and regular expression used to transform the data was: value.replace(/\(.*\)/, "")

This captured all data enclosed in parentheses and replaced it with nothing. 22 total cells were changed in the column.

Two cells were also edited manually. Pennsylvania State University reported enrollment numbers for both their entire university system as well as their main campus. I manually selected only the enrollment number for the main campus, making the data consistent with that for the other players. Arizona State University also listed enrollment numbers for multiple campuses. I manually selected the enrollment number for the main campus for this player as well.

## Authorship

All content was gathered from Wikipedia. All typical caveats about Wikipedia data apply, including inconsistencies in formatting and potential for inaccurate data.

## Semantic Contents

This file contains basic information about colleges attended by U.S. Women's National Team players. This data can be used to compare size, type, and location of schools attended by players.  

Data was originally collected in May 2019.

## Collection Process

This data was collected using Python 3.7 in a Jupyter Notebook.

Tools used:  

* Requests  
* Lxml  
* Xpath
* OpenRefine

Using player names as gathered in **playerdata.csv**, I pulled the Wikipedia page for each player ([Example](https://en.wikipedia.org/wiki/Megan_Rapinoe)). I then used xpath to isolate the link to the college team(s) for the player.

Next, I downloaded each college team page ([Example](https://en.wikipedia.org/wiki/Portland_Pilots)) and used lxml and xpath to extract the link to the general university page ([Example](https://en.wikipedia.org/wiki/University_of_Portland)).

Finally, I used lxml and xpath again to acquire specific information about each of these universities and organize them into csv format.



## Data Structure

Data is stored in csv format, with each row representing a player. Columns represent data about the college(s) each player attended and played for.

Since some players attended two colleges, sets of columns are included for both a first and a second college.

* Number of columns: 20
* Number of rows: 29
* Using missing value of: N/A

Data for each player:

* The name of the HTML file for the player's biography on the U.S. Soccer website
* The links for the player's college team(s) and college(s) attended
* The name of the college(s) the player attended
* For each college attended:
	* University name
	* Location
	* Total number of students
	* Type of university:
		* Public
		* Private
		* Community college	 

Most data is recorded as text. The total number of students is listed in numerals. Indicators of 'y' or 'n' are given to identify whether a school is a public university, private university, or a community college.

## Description of Column Contents

### Player Filename

This column identifies the name of the file for the player's U.S. Soccer biography page.

### Firstname

This column identifies the first name of the player, used to generate the url for their Wikipedia page.

### Surname

This column identifies the surname of the player, used to generate the url for their Wikipedia page.

### PlayerWiki Filename

This column identifies the name of the HTML file for the player's Wikipedia page.

### First College Team Link

This column identifies the link (also used for the filename) to the player's first college team's Wikipedia page.

All players attended college.

### Second College Team Link

This column identifies the link (also used for the filename) to the player's second college team's Wikipedia page (if applicable).

No players attended a second college.

### First College

This column identifies the link (also used for the filename) to the player's first college's Wikipedia page.

### Second College

This column identifies the link (also used for the filename) to the player's second college's Wikipedia page (if applicable).

No players attended a second college.

### First College Name

This column identifies the name of the first college attended by the player.

### First College Public

This column identifies whether the Wikipedia page for the university identifies it as a public university.

Coded as:

* y
* n

This column only measures whether the Wikipedia page for the university specifically used "Public" in its description. These values therefore contain some margin of error for negative values.

### First College Private

This column identifies whether the Wikipedia page for the university identifies it as a private university.

Coded as:

* y
* n

This column only measures whether the Wikipedia page for the university specifically used "Private" in its description. These values therefore contain some margin of error for negative values.

### First College Community

This column identifies whether the Wikipedia page for the university identifies it as a community college.

Coded as:

* y
* n

This column only measures whether the Wikipedia page for the university specifically used "Community" in its description. These values therefore contain some margin of error for negative values.

### First College Location

This column indentifies the location of the college as listed on their Wikipedia page.

Locations are listed as 'City,State'. States are given as the full name.

### First College Enrollment

This column identifies the total number of students enrolled at the university, as reported on their Wikipedia page.

The relevant data is recorded as numbers within this column.

### Second College Name

This column identifies the name of the second college attended by the player (if applicable).

No players attended a second college.

### Second College Public

This column identifies whether the Wikipedia page for the university identifies it as a public university.

Coded as:

* y
* n

No players attended a second college.

This column only measures whether the Wikipedia page for the university specifically used "Public" in its description. These values therefore contain some margin of error for negative values.

### Second College Private

This column identifies whether the Wikipedia page for the university identifies it as a private university.

Coded as:

* y
* n

No players attended a second college.

This column only measures whether the Wikipedia page for the university specifically used "Private" in its description. These values therefore contain some margin of error for negative values.

### Second College Community

This column identifies whether the Wikipedia page for the university identifies it as a community college.

Coded as:

* y
* n

No players attended a second college.

This column only measures whether the Wikipedia page for the university specifically used "Community" in its description. These values therefore contain some margin of error for negative values.

### Second College Location

This column indentifies the location of the college as listed on their Wikipedia page.

Locations are listed as 'City,State'. States are given as the full name.

No players attended a second college.

### Second College Enrollment

This column identifies the total number of students enrolled at the university, as reported on their Wikipedia page.

The relevant data is recorded as numbers within this column.

No players attended a second college.