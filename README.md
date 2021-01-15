# NLP with Stand-Up Comdey Dataset: Data Mining, LSTM Text Generation, LDA Topic Modeling, Classification, Clustering 
#### Scraped from Scraps From The Loft (https://scrapsfromtheloft.com/tag/stand-up-transcripts/)
Read the paper: https://sethgory.com/img/Clustering-For-Classification-Using-KMeans.pdf
1) Gather data: The notbook `get_transcripts.ipynb` crawls the Scraps From The Loft web archive for a directory of links and other data
          relating to transcripts from 330+ comedians' stand-up performances. Collected links are then iterated through to
          scrape sub-pages which contain the actual transcripts. Some cleaning and tagging is done using Regex and an IMDb api. 
          
2) Clean data: ...and do some feature engineering with `cleaning.ipynb`.

3) Text generator: Use `LSTM_text_gen.ipynb` to generate text using a LSTM neural network.

4) Topic modeling: Perform topic modeling with Latent Dirichlet Allocation in `topic_modeling_LDA.ipynb`. Result is a vector for each transcript that indicates probabilities for the presence of different topics.

5) Predict IMDb rating: Use the LDA vector along with a handmade binary target feature `rating_type` (1 for above average and 0 for below average IMDb rating) to train an ensemble classifier in `predict_rating.ipynb`.


### The dataset that results from running `get_transcripts,ipynb` then `cleaning,ipynb` contains the following columns: 
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
          words,
          word_count,
          f_words,
          s_words,
          diversity,
          diversity_ratio]
##
The script will work to grab as many transcripts as
          are available at runtime... when
          the site adds more performances to their archive, the resulting csv output will grow.
