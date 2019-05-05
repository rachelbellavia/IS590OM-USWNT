# Playerdata.csv

## Data Cleaning

No manual cleaning was performed on this file. All data was compiled by web scraping from the U.S. Soccer website. Any missing data or errors are original to the website.

Some code was used to work within the parameters of the data as provided on the U.S. Soccer website. Manual exemptions were used while scraping in order to accomodate name changes or misspellings. [ussoccer.inypb](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2009Data/ussoccer.ipynb)

Since player hometowns as listed on the U.S. Soccer website include non-standardized abbreviations of states, a dictionary was manually created in order to connect these abbreviations to the full name of states in order to connect them with U.S. Census data. [USWNTcode.inypb](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/USWNTCode.ipynb)


## Authorship

All content was gathered from the [U.S. Soccer](https://ussoccer.com) website. Copyrighted content belongs solely to U.S. soccer.

The roster list for 2009 was taken from the [U.S. Soccer Stats Page](https://www.ussoccer.com/womens-national-team/stats/2009-statistics). This page presents stats for each player who appeared in a game for the USWNT in a given year.

Biographical data for each player was taken from their bio page on the U.S. Soccer website. An example biography page can be seen [here for Megan Rapinoe](https://www.ussoccer.com/players/r/megan-rapinoe).

## Semantic Contents

This file contains basic biographical content for each player who appeared in a game for the U.S. Women's National Team in 2009. This data is used to identify players and identify commonalities or trends among players.  

Data was originally collected in May 2019.

## Collection Process

This data was collected using Python 3.7 in a Jupyter Notebook.

Tools used:  

* Requests  
* Lxml  
* Xpath

A list of player names was pulled from the [2009 stats page](https://www.ussoccer.com/womens-national-team/stats/2018-statistics). Xpath was used in order to isolate player names. I then used these names to build links to each player's biographical website on the [U.S. Soccer](https://ussoccer.com) website.

Example player url: <https://www.ussoccer.com/players/r/megan-rapinoe>

After downloading the HTML for each player bio, I again used xpath to isolate the relevant information and organize it into csv format.

## Data Structure

Data is stored in csv format, with each row representing an individual player.

* Number of columns: 9
* Number of rows: 29

Data for each player:

* The roster year in which the player appears
* The name of the HTML file for the player
* First name
* Surname
* Position (Forward, Midfielder, Defender, Goalkeeper)
* Birthdate
* Height
* Hometown
* Club team

All data is recorded as text. Dates are listed in standard date format.

## Description of Column Contents

### Roster Year

This column identifies the roster year on which the player appeared. Since players appear on multiple rosters, this keeps track of which year the player is being represented and allows for sorting by year in the final dataset.

### Filename

This column identifies the name and location for the HTML file for the player's biography page on the [U.S. Soccer](https://ussoccer.com) website.

### Firstname

This column identifies the first name for the player as listed in the header of their biography.

### Surname

This column identifies the surname for the player as listed in the header of their biography.

### Position

This column identifies the position the player generally plays.

Four unique values:

* Forward
* Midfielder
* Defender
* Goalkeeper

### Birthdate

This column identifies the birthdate for the player. The date is recorded in standard YYYY-MM-DD format.

### Height

This column identifies the height of the player in feet and inches.

Height is recorded with a hyphen between the digits. Example: 5-7 representing 5 feet, 7 inches.

### Hometown

This column identifies the hometown of the player as listed on their biographical page.

Hometowns are listed in 'City, State' format. Non-postal code abbreviations are used for states, but the abbreviations are internally consistent within the data.

### Club

This column represents the club team the individual plays for when not with the U.S. Women's National Team.
