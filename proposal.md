# Research Proposal: Analysis of Boston Airbnb Listings
### Big Picture Question: What attributes about a Boston Airbnb listing are most influential to its list price?

By Tommy McDade, Brooks Walsh, and Taylor Sheridan

## Research Question

After finding correlations and testing different influences, can we predict future Airbnb list prices?
   - This project will be about relationships as well as prediction. 
       - We will do a thorough EDA on our data set (including visuals) to represent the many relationships between different listing attributes and price.
       - After the important relationships are determined, we will use regression models and machine learning to create an accurate predictor of list prices
       - The metrics for success in this project include:
           - A dashboard to visually represent different metrics based on geographic location
           - A maximized R-Squared value (*or a different maximized/minimized measurement statistic, based on our choice of model*)

## Necessary Data

1. The Data will be primarily collected from [kaggle](https://www.kaggle.com/datasets/airbnb/boston):
- sample period: 9/5/2016 - 9/4/2017
    - There are 3 data sets included:
    1. calendar.csv
        - observation: Airbnb listings
        - rows: 1.31 million
        - columns: 4
        - index: "listing_id" and "date"
        - variables: "available (Bool)", "price(continuous)"
            - price is missing 51% of values
    2. listings.csv
        - observation: Airbnb listings
        - rows: 3585
        - columns: 95
        - index: "id", "scrape_id"
        - variables: too many to reasonably include in a proposal
            - a few examples:
                - "host_since", "maximum_nights", "require_guest_profile_picture"
    3. reviews.csv
        - observation: reviews based on Airbnb listings
        - rows: 68.3k
        - columns: 6
        - index: "listing_id", "id", "reviewer_id"
        - variables: "date", "reviewer_name", "comments"

2. To display maps and geographic data, we will need [census data on districts](https://hub.arcgis.com/datasets/15650d31b88646a2ac64a68c3701f655_0/explore?location=42.360613%2C-71.052250%2C13.27).
    - We will likely be using the shapefile version
    - If voting districts doesn't work, we should try [census tract data](https://www.arcgis.com/home/item.html?id=5628bfda9466438491219f4d07488a1e)
    

3. The **raw inputs** for this project will be 3 of the 4 data sets described above in .csv format. Potentially also a shapefile for use in geographic data.
    - All of these data sets will be saved to a folder called "inputs"
    - Any important dataframes/visuals that are created will be saved to a folder called "outputs"

4. High-level data cleaning plan:
- The 3 datasets that are obtained from Kaggle (calendar.csv, listings.csv, reviews.csv) are already fairly clean
    - There are several variables that may need to be a different data type to work
    - Some variables are full of text, and will likely need parsing to be used
- The last data set is from the 2010 (or 2020) census, and is not in a usable format
    - luckily there is a package for python that reads shapefiles effectively:
        - ```import geopandas as gpd```
        






# BELOW IS A TEMPLATE, DELETE BEFORE SUBMISSION 

## Research Question

This section should cover:
1. What do we want to know or what problems are we trying to solve? As in the midterm, you should list (1) the "bigger" question/debate/problem you're interested in, and also (2) the specific research question(s) you'll actually try to answer. 
    - The research question will be smaller in scope than the big picture question. But the answer to your specific research question should _shed light_ on the bigger question (although it likely won't conclusively answer it).
    - The answer to your specific research question should _shed light_ on the bigger question (although it likely won't conclusively answer it).
2. If your project is about relationships, what are the hypotheses you're testing?
3. If your project is about prediction, what is your metrics of success? [(What are you maximizing?)](https://ledatascifi.github.io/ledatascifi-2022/content/05/03d_whatToMax.html) Can you find a baseline from prior work to give you a ball park to aim for?

## Necessary Data

This section should cover:
1. What does the final dataset need to look like (mostly dictated by the question and the availability of data):
   - What is an observation, e.g. a firm, or a firm-year, etc.
   - What is the sample period?
   - What are the sample conditions? (Years, restrictions you anticipate (e.g. exclude or require some industries)
   - What variables are absolutely necessary and what would you like to have if possible?
1. What data do we have and what data do we need?
2. How will we collect more data? 
1. What are the raw inputs and how will you store them (the folder structure(s) for each input type)? 
1. Speculate at a high level (not specific code!) about how you'll transform the raw data into the final form.

