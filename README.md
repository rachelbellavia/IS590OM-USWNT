# Creating a dataset of USWNT players
This was created as a project for Elizabeth Wickes' Open Data Mashups course.


## Purpose
This project aims to create a general biography of U.S. Women's National Soccer Team players in the form of a comprehensive dataset.

The dataset combines data from the U.S. Soccer website, Wikipedia, and the U.S. Census. It contains data about the players themselves as well as the colleges they attended and where they were born. Ultimately this data can be used to tell a story about who these players are and where they came from.

## How it works

For each roster year, two programs need to be run.

1. **ussoccer.ipynb** - This reads in the statistics page, creating a list of players, then scraping those players' bio pages.
2. **WikiData.ipynb** - This takes the player names and connects to their Wikipedia page, locating their college and scraping data about that school.

Then run **USWNTCode.ipynb** to combine all the data together with the U.S. Census.

## Requirements

Code was written in a Python 3.7 environment in Jupyter notebooks.

Tools used: Pandas, requests, lxml, xpath

Full list of environment requirements: https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/requirements.txt

## Manifest

A manifest of files in this repo can be found [here](https://github.com/rachelbellavia/IS590OM-USWNT/blob/master/Manifest.md). This includes links to documentation for all datasets.
