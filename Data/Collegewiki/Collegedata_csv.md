# Collegedata.csv

## Data Cleaning Assessment

This data is quite messy due to the lack of consistency between different Wikipedia pages.

The biggest cleaning needs are in the 'Type' and 'Enrollment' columns. Types are not reported consistently for different universities. For example, both "Public" and "Public University" are listed as types. I anticipate using OpenRefine to remove some of these duplicate types.

The enrollment column also includes descriptive text along with the actual number of students. This will need to be removed so numbers can be assessed. Two universities also list two different enrollment numbers; one will need to be removed. I am not entirely sure if OpenRefine will work for this process. Especially for hand-picking the single relevant enrollment number for the two schools, I will likely have to do that by hand.

Luckily this dataset is small, so it probably will not take too much time to clean, even with the learning curve on OpenRefine.

## Authorship

All content was gathered from Wikipedia.

## Semantic Contents

This file contains basic information about colleges attended by U.S. Women's National Team players. This data can be used to compare size, type, and location of schools attended by players.  

Data was collected in March 2019.

## Collection Process

This data was collected using Python 3.7 in a Jupyter Notebook.

Tools used:  

* Requests  
* Beautiful Soup
* Lxml  
* Xpath

Using player names as gathered in **playerdata.csv**, I pulled the Wikipedia page for each player. I then used beautiful soup to isolate the link to the college team for the player.

Next, I downloaded each college team page and used lxml and xpath to extract the link to the general university page.

Finally, I used lxml and xpath again to acquire specific information about each of these universities and organize them into csv format.



## Data Structure

Data is stored in csv format, with each row representing a university.

* Number of columns: 5
* Number of rows: 19

Data for each university:

* The name of the HTML file for the university
* University name
* Location
* Type of university
* Total number of students

Most data is recorded as text. The number of students is listed in numerals, with some text included within the data.

## Description of Column Contents

### File Name

This column identifies the name and location for the HTML file for the college's Wikipedia page.

### School Name

This column identifies the name of the college as listed in the header of their page.


### Location

This column indentifies the location of the college as listed on their Wikipedia page.

Locations are listed as 'City,State'. States are given as the full name.

### Type

This column identifies the type of college as listed on their Wikipedia page. A variety of types are given for each college.

Examples include:

* Private
* Public
* Land-grant
* Sea-grant
* Space-grant

This column will require cleaning, since these types are not all recorded consistently (some do and some do not include 'university' in the type).

Some universities also include types that will not be useful for sorting or organization and will serve as interesting if irrelevant information.

### Enrollment

This column identifies the total number of students enrolled at the university, as reported on their Wikipedia page.

The relevant data is recorded as numbers within this column. Some include extraneous information, such as text identifying the year of the reported enrollment. 

Two universities have two different enrollment numbers, one for the primary campus and one for the entire university system. This will need to be cleaned down to the one number only for the primary campus.

### Additional Note

Not all U.S. Women's National Team players attended college. This dataset only includes information about colleges attended by players who did so. In the final dataset, players who did not attend college will have that indicated with "NoCollege".