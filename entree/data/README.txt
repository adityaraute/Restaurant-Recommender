
These files are the data underlying the Entree system (originally, http://infolab.cs.uchicago.edu/entree/ and now http://infolab.ils.nwu.edu/entree/). 
It is of historical significance only due to the volatility of the restaurant industry, but it is the raw data from which Entree generates its recommendations.

Contents:

features.txt - A dictionary mapping from feature ID to descriptive
text. For example, feature 072 corresponds to "Ethiopian" cuisine.

atlanta.txt
boston.txt
chicago.txt
los_angeles.txt
new_orleans.txt
new_york.txt
san_francisco.txt
washington_dc.txt - Data files of the following format:

restaurant id [tab] restaurant name [tab] restaurant features (3 digits ids separated by spaces)
