#Coffee in New York with Google Places API

## Where to find good coffee in New York?:

This project attempts to locate all the coffee outlets in Manhattan and Brooklyn, obtain their Google Places review scores, and find the areas and stores with the best coffee. A summary of the results can be found on my blog 'www.datadino.ghost.io' with results plotted to a geoJSON file by postcode, for example.

## Files:

* 5_hists_by_reviewer_number.png - 5 Histograms showing how the scores recorded by 1-5+ reviewers differ from the global distribution of Google Places Scores.

* all_score_hist.png - A histogram of the full distribution of Google Places scores.

* coffee_data.ipynb - IPython Notebook to generate some plots from the data and to analyse results.

* data.csv - CSV file of all unique 'coffee' places in Manhattan and Brooklyn.

* data_with_review_count.csv - Appended CSV file with the average review from the individual user reviews and the number of reviews for each establishment.

* getplaces.py - Uses a Place search from the Google Places API to search the latitude and longitude bounds of Manhattan and Brooklyn for search term 'coffee'. Many API calls are required to obtain all the unique establishments. Results are written to data.csv.

* getreviews.py - Uses the results in data.csv to make a different API call to retrieve details about an establishment. This gives us up to 5 reviews, and allows us to add in the number of user reviews and the average score.

* slides.* - Presentation of results.

## Places API summary:

There are two separate components to the searches in this project: 1) Search for a keyword 'coffee' using a Place search on location. 2) Use the unique identifier from each establishment identified in 1) to extract further information via a Place detail search.

* Usage limits - 1000 calls an hour which may be increased to 100000 by 'verifiying your identity' by providing your credit card to Google...

* Place search call -



* Place details call

* Other - Another way similar results might be achieved is to use a 'Radar search' from the Places API which will return up to 200 results for a given location and radius. There is a 5-times multiplier on the number of API calls for one of these requests and it returns fewer details.

## TODO:
* Asynchronous version to improve speed.
* Restrict calls to those that only fall within a geoJSON polygon definition to improve speed / decrease API calls.
* Cover all of New York City in the search.
* Find other methods to get the actual number of reviewers for a Place, rather than just up to 5.
* Find other methods to get the actual reviews from individuals for sentiment analysis or predictive capabilities.


