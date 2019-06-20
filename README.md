# car-accident-analysis

<p align="center">
<img src="https://github.com/ianjeffries/car-accident-analysis/blob/master/images/uk_accidents.png" alt="Map of Accidents in the UK" width="250" height="430">
</p>

## Index 
1. [Summary](https://github.com/ianjeffries/text-sentiment-analysis#summary)
2. [File Directory](https://github.com/ianjeffries/text-sentiment-analysis#file-directory)
3. [Language and Packages Used](https://github.com/ianjeffries/text-sentiment-analysis#language-and-packages-used)
4. [Credits](https://github.com/ianjeffries/text-sentiment-analysis#credits)
5. [License](https://github.com/ianjeffries/text-sentiment-analysis#license)

## Summary 
The following project utilizes R to mine sentiment from over 21,000 hotel reviews on resorts located in the Republic of Maldives, a South Asian country located in the Indian Ocean. 

## File Directory

1. [**data**](https://github.com/ianjeffries/text-sentiment-analysis/tree/master/data) - contains the three files used in analysis:  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. [maldives_hotel_reviews.csv](https://github.com/ianjeffries/text-sentiment-analysis/blob/master/data/maldives_hotel_reviews.csv) - Hotel reviews of resorts in the Republic of Maldives.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b. [negative-lexicon.txt](https://github.com/ianjeffries/text-sentiment-analysis/blob/master/data/negative-lexicon.txt) - Negative lexicon used to locate "negative" words.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;c. [positive-lexicon.txt](https://github.com/ianjeffries/text-sentiment-analysis/blob/master/data/positive-lexicon.txt) - Positive lexicon used to locate "positive" words.  
     
2. [**images**](https://github.com/ianjeffries/text-sentiment-analysis/tree/master/images) - contains vizualizations:  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. [body_wordcloud.png](https://github.com/ianjeffries/text-sentiment-analysis/blob/master/images/body_wordcloud.png) - Wordcloud showing commonly occuring words in the review body.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b. [header_wordcloud.PNG](https://github.com/ianjeffries/text-sentiment-analysis/blob/master/images/header_wordcloud.PNG) - Wordcloud showing commonly occuring words in the review header.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;c. [monthly_sentiment.png](https://github.com/ianjeffries/text-sentiment-analysis/blob/master/images/monthly_sentiment.png) - Overall sentiment by month for all hotels in the Republic of Maldives.   
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;d. [reviews_by_year.png](https://github.com/ianjeffries/text-sentiment-analysis/blob/master/images/reviews_by_year.png) - Count of reviews by year.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;e. [sentiment_comparison.png](https://github.com/ianjeffries/text-sentiment-analysis/blob/master/images/sentiment_comparison.png) - Comparision of negative and positive wordcounts.   
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;f. [top_12_hotels.png](https://github.com/ianjeffries/text-sentiment-analysis/blob/master/images/top_12_hotels.png) - Top 12 resorts sentiment comparison.   
  
3. [**text_mining.Rmd**](https://github.com/ianjeffries/text-sentiment-analysis/blob/master/text_mining.Rmd) - R Markdown detailing the text mining process.  
  
4. [**text_mining.pdf**](https://github.com/ianjeffries/text-sentiment-analysis/blob/master/text_mining.pdf) - PDF that shows R code and the outputted results, for easy viewing.
  
5. [**results.pdf**](https://github.com/ianjeffries/hotel-review-text-mining/blob/master/results.pdf) - A full write-up comparing text mining in R vs SAS.

## Language and Packages Used

R is used for all model building - the results are compared in R vs SAS.

The following packages are used:
  
  ```
#list of packages used
packages <- c("tm", "wordcloud", "lubridate", "SnowballC", "ggplot2", "dplyr", "tidyr")

#check to see if package is already installed
for(p in packages){
  if(!require(p, character.only = TRUE)) {
    install.packages(p)
    library(p, character.only = TRUE)
  }
}
```

## Credits

1. Would like to thank Dr. Mo Saraee from the University of Salford for the maldives_hotel_reviews.csv dataset.
2. Would like to thank Bing Liu and Minqing Hu for the negative-lexicon.txt and positive-lexicon.txt files, which were taken off of [their website](https://www.cs.uic.edu/~liub/FBS/sentiment-analysis.html#lexicon).

## License 

MIT License
Copyright (c) 2019 Ian Jeffries
