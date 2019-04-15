# Playerdata.csv

## Data Cleaning Assessment

This data is relevantly clean since it was hand-selected in the curation process. The biggest cleaning need will be standardizing the hometown in order to link it to other geographical data. U.S. Soccer uses non-postal code abbreviations for states (i.e. Calif. for California), but they are consistent within their website. I should be able to make a simple reference file to transform the abbreviated states into either a standard postal code or the full version of the state name.


## Authorship

All content was gathered from the [U.S. Soccer] (https://ussoccer.com) website. Copyrighted content belongs solely to U.S. soccer.

## Semantic Contents

This file contains basic biographical content for each player who appeared in a game for the U.S. Women's National Team in 2018. This data is used to identify players and identify commonalities or trends among players.  

Data was collected in January 2019.

## Collection Process

This data was collected using Python 3.7 in a Jupyter Notebook.

Tools used:  

* Requests  
* Lxml  
* Xpath

A list of player names was pulled from the [2018 stats page](https://www.ussoccer.com/womens-national-team/stats/2018-statistics). Xpath was used in order to isolate player names. I then used these names to build links to each player's biographical website on the [U.S. Soccer] (https://ussoccer.com) website.

Example player url: <https://www.ussoccer.com/players/l/carli-lloyd>

After downloading the HTML for each player bio, I again used xpath to isolate the relevant information and organize it into csv format.

## Data Structure

Data is stored in csv format, with each row representing an individual player.

* Number of columns: 8
* Number of rows: 38

Data for each player:

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

### Filename

This column identifies the name and location for the HTML file for the player's biography page on the [U.S. Soccer] (https://ussoccer.com) website.

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

One player does not have a club team identified. This value is represented as "NoClub".