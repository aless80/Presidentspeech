# Presidentspeech
Topic analysis of US Presidents' State of the Union Addresses and Messages

The text is scraped from: [The American Presidency Project](http://www.presidency.ucsb.edu/sou.php)

Inspiration for this project: [Topic Modeling the State of the Union: TV and Partisanship](https://www.exaptive.com/blog/topic-modeling-the-state-of-the-union)

---

## US Presidents' State of the Union Addresses and Messages

State of the Union Messages to the Congress are mandated by the US constitution. In modern times messages are orally delivered message presented to a joint session of Congress, but the State of the Union was a written report sent to Congress to coincide with a new Session of Congress. 

In the texts considered here, Nixon submited multiple documents or gave both oral and written messages. Roosevelt's last (1945) and Eisenhower's 4th (1956) were technically written messages although they also addressed the American people via radio.


## Scraping

The text is scraped using [urllib2](https://pymotw.com/2/urllib2/) and [BeautifulSoup](https://pypi.python.org/pypi/beautifulsoup4) from this site:
[The American Presidency Project](http://www.presidency.ucsb.edu/sou.php)

To avoid having to scrape the site too often, the scraped texts are stored in [documents_raw.pkl](https://github.com/aless80/Presidentspeech/blob/master/documents_raw.pkl) using Pickle. 

See [Scrape.ipynb](https://github.com/aless80/Presidentspeech/blob/master/Scrape.ipynb) for the code doing the scraping. 

---

## Topic analysis

The text is imported from [documents_raw.pkl](https://github.com/aless80/Presidentspeech/blob/master/documents_raw.pkl) and  preprocessed. Preprocessing includes removing removing non-unicode characters, words starting and ending with non-letter characters ("1st" is ok, "123" not), removing punctuation and stop words ("and",  "won't"), lemmatization. 

After that Latent Dirichlet Allocation [LDA](http://scikit-learn.org/stable/modules/generated/sklearn.decomposition.LatentDirichletAllocation.html) and Non-Negative Matrix Factorization [NMF](http://scikit-learn.org/stable/modules/generated/sklearn.decomposition.NMF.html) are applied. The topics and the analysis are plotted using [pyLDAvis](http://nbviewer.jupyter.org/github/bmabey/pyLDAvis/blob/master/notebooks/sklearn.ipynb) and [WordCloud](https://github.com/amueller/word_cloud).

See [Presidentspeech.ipynb](https://github.com/aless80/Presidentspeech/blob/master/Presidentspeech.ipynb)
