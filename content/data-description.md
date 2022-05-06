---
title: Data description
prev: _index
next: network-analysis
---
<head>
<style>
<style>
h1 {text-align: left; font-size:25px,font-family: Verdana, sans-serif}
h2 {text-align: left; font-size:20px,font-family: Verdana, sans-serif}
h3 {text-align: left; font-size:15px,font-family: Verdana, sans-serif}
</style>

<style>
.line {
    padding-bottom: 20px;
    border-bottom: 1px solid #9CA3AF; 
}
.line1 {
    padding-bottom: 20px;
    border-bottom: 3px solid #9CA3AF; 
}
</style>

</head>

<div class="line1"></div>

<h3>The main dataset utilized consists of chapter plot summaries of all the chapters in the seven Harry Potter books. The plot summaries are from 
<a href="http://harrypotter.fandom.com/">this website</a>.
We also used a secondary dataset with a character information from
<a href="https://hp-api.herokuapp.com/">this website</a>
<br>
<br>
Book numbers and their titles:
<ul>
  <li>Book 1: Harry Potter and the Philosopher's Stone</li>
  <li>Book 2: Harry Potter and the Chamber of Secrets</li>
  <li>Book 3: Harry Potter and the Prisoner of Azkaban</li>
  <li>Book 4: Harry Potter and the Goblet of Fire</li>
  <li>Book 5: Harry Potter and the Order of the Phoenix</li>
  <li>Book 6: Harry Potter and the Half-Blood Prince</li>
  <li>Book 7: Harry Potter and the Deathly Hollows</li>
</ul> 

The books consist of <strong>198</strong> chapters in total, and the plot summaries of these totals to <strong>57,382</strong> words.

The character overview contains information on **403** characters, but only **183** of these are actually mentioned in the plot summaries.
</h3>

<h1>Getting the data</h1>
<div class="line"></div>
<h3> Requests and Beautiful Soup was used to webscrape the book summaries and collect the information in a dataframe with book number, chapter number, chapter title and chapter summary. To do so, it only the hyperlinks for each book summary was needed. The summaries were cleaned and only includes actual words. The text analysis required the summaries to be tokenized which made it possible to look at word individually. The tokenized text where collected in a column of its own. These tokens where also made lower case and stopwords were removed such that irrelevant word were not included in the sentiment analysis.

<br>

A dataset which contained character information was used to identify characters in the summaries easily. Two columns that contained first- and last name was added which made it possible to identify characters by either full-, first- or last name as well as alternate name which was also already in the dataset. Even though the dataset had many more attributes such as house affiliation, ancestry etc. these where not used and thus not relevant for our analysis. 
The chapter summaries were scraped using BeautifulSoup <a href="https://www.crummy.com/software/BeautifulSoup/">here</a>.
The .csv file with our webscraped data can be downloaded <a href="/plot_summary_df.csv">here</a>.
It was made into a pandas dataframe in Python with the lines:
</h3>

```python
import pandas as pd
from ast import literal_eval
df = pd.read_csv('plot_summary_df.csv', index_col=0, 
                 converters={'plot_tokens':literal_eval})
```

<h3>The character overview is a .json file that can be downloaded <a href="/characters.json">here</a>
It was made into a pandas dataframe in Python with the lines</h3>

```python
import pandas as pd
char = pd.read_json('characters.json')
```

