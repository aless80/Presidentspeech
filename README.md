# Presidentspeech
Topic analysis of US Presidents' State of the Union Addresses and Messages

The text is scraped from: [The American Presidency Project](http://www.presidency.ucsb.edu/sou.php)

Inspiration for this project: [Topic Modeling the State of the Union: TV and Partisanship](https://www.exaptive.com/blog/topic-modeling-the-state-of-the-union)

---

## US Presidents' State of the Union Addresses and Messages

State of the Union Messages to the Congress are mandated by the US constitution. In modern times messages are orally delivered message presented to a joint session of Congress, but the State of the Union was a written report sent to Congress to coincide with a new Session of Congress. In the texts considered here, Nixon submiited multiiple documents or gave both oral and written messages. 

The text is scraped using urllib2 and BeautifulSoup from this site:

[The American Presidency Project](http://www.presidency.ucsb.edu/sou.php)

To avoid having to scrape the site too often, the scraped texts are stored in documents_raw.pkl using Pickle. 

See Scrape.ipynb for the code doing the scraping. 

---

## Topic analysis

The text is imported
See Presidentspeech.ipynb
