#Coffee in New York with Google Places API

## Files:

* 5_hists_by_reviewer_number.png - 5 Histograms showing how the scores recorded by 1-5+ reviewers differ from the global distribution of Google Places Scores.

* all_score_hist.png

* coffee_data.ipynb - IPython Notebook to generate some plots from the data and to analyse

* data.csv - CSV file of all unique 'coffee' places in Manhattan and Brooklyn

* data_with_review_count.csv - Appended CSV file with the average review from the individual user reviews and the number of reviews for each establishment

* getplaces.py - Uses a Place search from the Google Places API to search the latitude and longitude bounds of Manhattan and Brooklyn for search term 'coffee'. Many API calls are required to obtain all the unique establishments. Results are written to data.csv

* getreviews.py - Uses the results in data.csv to make a different API call to retrieve details about an establishment. This gives us up to 5 reviews, and allows us to add in the number of user reviews and the average score.

* slides.* - Presentation of results

## Places API summary:

* Place search

* Place details


