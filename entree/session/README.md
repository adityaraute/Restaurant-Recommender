
This data records interactions with the Entree system (originally, http://infolab.cs.uchicago.edu/entree/ and now http://infolab.ils.nwu.edu/entree/) from September, 1996 to April, 1999. 
The data is organized into files roughly spanning a quarter year -- with Q3 1996 and Q2 1999 each only containing one month.

Each line in a session file represents a session of user interaction with the system.  

The (tab-separated) fields are as follows:

#### Date, IP, Entry point, Rated restaurant1, ..., Rated restaurantN, End point

Some potentially useful data is missing.  
In many cases, we don't know the starting point because the user input a set of selection criteria (such as "inexpensive traditional Mexican") using a form submission, rather than startin from a known restaurant.  
These queries were not recorded. This is denoted by a 0 in the entry point field. Some sessions don't have a known end point. This is marked by -1 in the end point field.

#### Semantics of the data:
 
##### Entry point:
    
     Users can use a restaurant from any city as a entry point, but they always get recommendations for Chicago restaurants.  
     The entry point therefore draws from a larger universe of restaurants than the rest of the data.
     Entry points have the form nnnX, where nnn is a numeric restaurant ID and X is a character A-H that encodes the city.
     - A = Atlanta
     - B = Boston
     - C = Chicago
     - D = Los Angeles
     - E = New Orleans
     - F = New York
     - G = San Francisco
     - H = Washington DC

##### Rated Restaurant:

     These are all Chicago restaurants.
     These entries have the form nnnX, where nnn is a numeric restaurant ID and X is a character L-T that encodes the navigation operation.
     -  L = browse (move from one restaurant in a list of recommendations to another)
     -  M = cheaper (search for a restaurant like this one, but cheaper)
     -  N = nicer   (search for a restaurant like this one, but nicer)
     -  O = closer  (unused in the production version of the system)
     -  P = more traditional (search for a restaurant like this, but serving more traditional cuisine)
     -  Q = more creative (search for a restaurant serving more creative cuisine)
     -  R = more lively (search for a restaurant with a livelier atmosphere)
     -  S = quieter (search for a restaurant with a quieter atmosphere)
     -  T = change cuisine (search for a restaurant like this, but serving a different kind of food) 
        Note that with this tweak, we would ideally like to know what cuisine the user wanted to change to, but this information was not recorded.

##### End point:
  Just the numeric id for the (Chicago) restaurant that the user saw last. In our experiments, we are assuming that this was a good suggestion, but it is also possible that user just gives up. 





