## visualizing tweet content  

The three .Rmd files in this folder are a first attempt at visuallzing the content of tweets from our dataset

* [bigram_plots](https://github.com/Science-for-Nature-and-People/soc-twitter/blob/master/tweet_content/bigram_plots.Rmd) uses bigrams create network graphs that visualize the common flow of words among all tweets.  These visualizations are separated into:  
  - the full noRT dataset. 
  - tweets about:
      - soil 
      - forest 
      - rangeland health
      - regenerative agriculture
   - then repeats this for the top 100 tweets based on their RT count
     
     
     
* [word_assoc](https://github.com/Science-for-Nature-and-People/soc-twitter/blob/master/tweet_content/word_assoc.Rmd) histograms of word counts for the words associated with the different API query terms, as well as the most common words associated with our different categories of interest. i.e.:
  - soil, soil health, soil quality
  - rangeland, rangeland health, rangeland quality
  - forest, forest health, forest quality 
    
      
* [word_clouds](https://github.com/Science-for-Nature-and-People/soc-twitter/blob/master/tweet_content/word_clouds.Rmd) creates wordclouds for the tweets within these same ^ categories 

 ***
 
The code in each of these .Rmd's relies on functions that are stored and documented in [text_analysis_functions.R](https://github.com/Science-for-Nature-and-People/soc-twitter/blob/master/text_analysis_functions.R)
  - the functions in here are:
    - word_umbrella() - combines various terms into a single word 'umbrella' (this function is nested and used conditionally within other functions
    - prepare_text() - tokenizes text and provides counts of each word
    - create_wordcloud() - simple function for creating a generic wordcloud
    - create_bigram() - creates a list of bigrams and their counts
    - gram_network() - used in a workflow with create_bigram() to create a network graph of bigrams
    - flag_india() - simple function that creates a new column identying a tweet as being from/related to India
