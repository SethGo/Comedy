# Data Mining, NLP, LSTM: Stand-Up Comdey Dataset 
#### Scraped from Scraps From The Loft (https://scrapsfromtheloft.com/tag/stand-up-transcripts/)
This python script crawls the Scraps From The Loft web archive for a directory of links and other data
          relating to transcripts from a large number of comedians' stand-up performances. Collected links are then iterated through to
          scrape sub-pages which contain the actual transcripts. Some light cleaning and tagging is done using Regex and an IMDb api. 

### The resulting dataset contains the following columns: 
          [title, 
          tags, 
          date_posted, 
          link, 
          name, 
          year, 
          transcript, 
          language, 
          runtime, 
          rating,
          sentences,
          words,
          sent_polarity,
          sent_subjectivity,
          word_polarity,
          word_subjectivity,
          word_count,
          sent_count,
          words_per_sentence,
          f_words,
          s_words]
##
The script will work to grab as many transcripts as
          are available at runtime... when
          the site adds more performances to their archive, the resulting csv output will grow.
