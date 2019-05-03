# Census Data

## Data Cleaning Assessment

The data itself is fairly clean, since most things are represented in specified codes. The biggest issue is that there is a lot of data, and I do not need all of it.

In order to connect this data to player hometowns, I will need to find some way to match the two. The biggest concern is that in this Census data, the incorporated title of the place is included in its name, i.e. "Menlo Park city, California". These will need to be removed or otherwise avoided while trying to connect by hometown.

The other problem is that at least two players are from a location that does not qualify as a place on the census. While I can still identify some basic region data for them according to the state, I cannot pull in population data from this dataset.

Overall I expect this process to take up the biggest chunk of the work I have left to do on this project, trying to make it mesh with the other, hand-curated data.

## Authorship

Data content is from the U.S. Census 2010.

Dataset was downloaded from Social Explorer:  
www.socialexplorer.com New York City, NY: Social Explorer 2019

Dataset link: <http://www.socialexplorer.com/pub/reportdata/HtmlResults.aspx?reportid=R12097354>

Social Explorer was accessed via the University of Illinois at Urbana-Champaign.

## Semantic Contents

This dataset contains basic information about every place in the United States. The dataset includes location identifiers, size, and population totals.

This dataset will be used to identify information about the hometowns for players on the U.S. Women's National Team. Information will be linked by the names, and I can use region identifiers and population totals to present a basic description of those hometowns.

Data was downloaded March 31, 2019.

## Collection Process

Data was collected in the 2010 [U.S. Census](https://www.census.gov).

This particular dataset was curated and downloaded from [Social Explorer](http://www.socialexplorer.com/pub/reportdata/HtmlResults.aspx?reportid=R12097354).

## Data Structure

This data is stored in a csv.

* Number of columns: 12
* Number of rows: 29514

Each record represents a specific location in the United States, with columns identifying and describing that location.

Data are presented as text and numbers. Many of the numbers are used as categorical identifiers.

## Description of Column Contents

Produced using the [Data Profiling Tool](https://github.com/elliewix/data-profile-tool) created by Elizabeth Wickes.

* Number of columns: 12
* Number of rows: 29514

**Geo_NAME**
----------
* Description of column: Area Name-Legal/Statistical Area Description
* Description of data values and units: Text (name of the location)
* Unique values: 24361
* Missing: 0


**Geo_QName**
-----------
* Description of column: Qualifying Name
* Description of data values and units: Text (name of the location including county and state)
* Unique values: 29445
* Missing: 0


**Geo_AREALAND**
--------------
* Description of column: Area (Land)
* Description of data values and units: Land area given in square meters.
* Unique values: 29495
* Missing: 0
* Percent digit: 100%
* Min digit: 13088.0
* Max digit: 7434143788.0

**Geo_AREAWATR**
--------------
* Description of column: Area (Water)
* Description of data values and units: Water area given in square meters.
* Unique values: 16498
* Missing: 0
* Percent digit: 100%
* Min digit: 0.0
* Max digit: 5027287905.0

**Geo_SUMLEV**
------------
* Description of column: Summary Level
* Description of data values and units: Code used to identify the granularity of the data. Specifically, 160 represents Place.
* Unique values: 1
* Unique value content: The values are:
	* 160
* Missing: 0
* Percent digit: 100%
* Min digit: 160.0
* Max digit: 160.0

**Geo_GEOCOMP**
-------------
* Description of column: Geographic Component
* Description of data values and units: N/A
* Unique values: 1
* Unique value content: The values are:
	* 00
* Missing: 0
* Percent digit: 100%
* Min digit: 0.0
* Max digit: 0.0

**Geo_REGION**
------------
* Description of column: Region
* Description of data values and units: Numeral used to represent the region in which the place is located.  
	* 1 = Northeast
	* 2 = Midwest
	* 3 = South
	* 4 = West
* Unique values: 5
* Unique value content: The values are:
	* 1
	* 2
	* 3
	* 4
	* 9
* Missing: 0
* Percent digit: 100%
* Min digit: 1.0
* Max digit: 9.0

**Geo_DIVISION**
--------------
* Description of column: Division
* Description of data values and units: Numeral used to represent the narrower region division in which the place is located.  
	* 1 = New England
	* 2 = Middle Atlantic
	* 3 = East North Central
	* 4 = West North Central
	* 5 = South Atlantic
	* 6 = East South Central
	* 7 = West South Central
	* 8 = Mountain
	* 9 = Pacific
* Unique values: 10
* Unique value content: The values are:
	* 0
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
* Percent digit: 100%
* Min digit: 0.0
* Max digit: 9.0

**Geo_FIPS**
----------
* Description of column: FIPS (Federal Information Processing Series)
* Description of data values and units: A numeric code used to identify each specific location.
* Unique values: 29514
* Missing: 0
* Percent digit: 100%
* Min digit: 100100.0
* Max digit: 7288121.0

**Geo_STATE**
-----------
* Description of column: State (FIPS)
* Description of data values and units: A numeric code used to identify each state.
* Unique values: 52
* Missing: 0
* Percent digit: 100%
* Min digit: 1.0
* Max digit: 72.0

**Geo_PLACE**
-----------
* Description of column: Place (FIPS)
* Description of data values and units: A numeric code used to identify each place.
* Unique values: 19479
* Missing: 0
* Percent digit: 100%
* Min digit: 65.0
* Max digit: 89760.0


**SE-T001_001**
-------------
* Description of column: Total Population
* Description of data values and units: Number representing the total population of the place.
* Unique values: 9858
* Missing: 0
* Percent digit: 100%
* Min digit: 0.0
* Max digit: 8175133.0