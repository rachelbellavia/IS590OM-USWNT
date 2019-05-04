# Manifest
This document describes everything included in the IS590OM-USWNT GitHub repo, including links, where relevant.

## Final Dataset
[USWNTPlayerData.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/USWNTPlayerData.csv) - This dataset contains biographical information about players on the USWNT and demographic information about their colleges and hometowns.

**Documentation for this dataset can be found [here](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/USWNTPlayerData_Documentation.md).**

## Final Code
[USWNTCode.ipynb](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/USWNTCode.ipynb) - This Jupyter notebook is used to compile the final dataset from the intermediate datasets.

## Folder: 2009Data

### Code
1. [ussoccer.ipynb](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2009Data/ussoccer.ipynb) - Run this code first to collect 2009 roster player data from the U.S. Soccer website.
2. [WikiData.ipynb](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2009Data/WikiData.ipynb) - Run this code second to collect 2009 roster player data from Wikipedia.

### USWNT subfolder
[playerdata.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2009Data/USWNT/playerdata.csv) - This dataset collects the biographical data from the U.S. Soccer website.

**Documentation for this dataset can be found [here](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2009Data/USWNT/Playerdata_csv.md).**

Other files include HTML files for each player's bio page, and a txt file that is a list of player bio URLs.

### PlayerWiki subfolder

[playerwikidata.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2009Data/PlayerWiki/playerwikidata.csv) - an interim csv with wikipedia filenames.

HTML files for each player's Wikipedia page.

### Collegeteam subfolder

[collegeteamlinks.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2009Data/Collegeteam/collegeteamlinks.csv) - an interim csv with college team links.

HTML files for each college team's Wikipedia page.

### Collegewiki subfolder

[collegedata-clean.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2009Data/Collegewiki/collegedata-clean.csv) - This dataset collects information about each college attended by USWNT players.

**Documentation for this dataset can be found [here](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2009Data/Collegewiki/Collegedata-clean_csv.md).**

[collegedata.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2009Data/Collegewiki/collegedata.csv) - The original version of the above dataset, before cleaning.

[collegelinks.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2009Data/Collegewiki/collegelinks.csv) - an interim csv with college links.

HTML files for each college's Wikipedia page.

### Interim csv

[playersandcensus.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2009Data/playersandcensus.csv) - an interim csv combining player data and census data. Used in the [final code](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/USWNTCode.ipynb).


## Folder: 2018Data
### Code
1. [ussoccer.ipynb](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2018Data/ussoccer.ipynb) - Run this code first to collect 2018 roster player data from the U.S. Soccer website.
2. [WikiData.ipynb](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2018Data/WikiData.ipynb) - Run this code second to collect 2018 roster player data from Wikipedia.

### USWNT subfolder
[playerdata.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2018Data/USWNT/playerdata.csv) - This dataset collects the biographical data from the U.S. Soccer website.

**Documentation for this dataset can be found [here](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2018Data/USWNT/Playerdata_csv.md).**

Other files include HTML files for each player's bio page, and a txt file that is a list of player bio URLs.

### PlayerWiki subfolder

[playerwikidata.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2018Data/PlayerWiki/playerwikidata.csv) - an interim csv with wikipedia filenames.

HTML files for each player's Wikipedia page.

### Collegeteam subfolder

[collegeteamlinks.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2018Data/Collegeteam/collegeteamlinks.csv) - an interim csv with college team links.

HTML files for each college team's Wikipedia page.

### Collegewiki subfolder

[collegedata-clean.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2018Data/Collegewiki/collegedata-clean.csv) - This dataset collects information about each college attended by USWNT players.

**Documentation for this dataset can be found [here](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2018Data/Collegewiki/Collegedata-clean_csv.md).**

[collegedata.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2018Data/Collegewiki/collegedata.csv) - The original version of the above dataset, before cleaning.

[collegelinks.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2018Data/Collegewiki/collegelinks.csv) - an interim csv with college links.

HTML files for each college's Wikipedia page.

### Interim csv

[playersandcensus.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/2018Data/playersandcensus.csv) - an interim csv combining player data and census data. Used in the [final code](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/USWNTCode.ipynb).

## Folder: Census
### Intermediate Dataset
[censusplace.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/Census/censusplace.csv) - This dataset contains information about each 'place' in the U.S. Census.

**Documentation for this dataset can be found [here](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/Census/CensusData.md).**

### Census key

[geocodes.csv](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/Census/geocodes.csv) - This file was used as a key to connect state names with the official U.S. Census state, division, and region codes.

