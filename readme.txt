One day I was cooking, and I wondered what spices normally go together, and as an avid data scientist, I decided to answer this question using data. So I scraped a website having more than 50,000 recipes (01_url_scraper.ipynb), and downloaded all recipes and their ingredients (02_recipe_scrape.ipynb). However, the ingredients were somehow messy and it was difficult to make sense out of them. For example, there would be "whole skinless, boneless chicken breasts", and for me that counts as "chicken"! So I simplified the ingredients with a rather tedious script (03_simplify_ingredients.ipynb).

Having all the ingredients simplified, I chose 40 spices from a website, and clustered all recipes based on the spices using K-Means algorithm (04_spices.ipynb), and plot the results as word clouds.

In order to use these scripts, you need the following packages:

- pickle (to store the recipes and ingredients in the class Recipe)
- urllib2 (to download pages)
- multiprocessing (to accelerate the scraping process)
- nltk (to clean the ingredients, and remove adjectives)
- scipy (to use sparse matrix)
- sklearn (to use KMeans)
- pandas
- wordcloud (very cool wordcloud package)

If you want to see the results, check out "04_spices.ipynb" here:

http://nbviewer.ipython.org/github/alireza202/recipes/blob/master/04_spices.ipynb