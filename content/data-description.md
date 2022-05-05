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

<h3>The data for the project consists of chapter plot summaries of all the chapters in the 7 Harry Potter books. The plot summaries are from </h3>

<http://harrypotter.fandom.com>. 
<h3>We also got a character overview from</h3>

<http://hp-api.herokuapp.com>. 

<h3>
The books consist of <strong>198</strong> chapters, and the plot summaries of these totals <strong>57,382</strong> words.

The character overview contains information on **403** characters, but only **183** of these are actually mentioned in the plot summaries.
</h3>

<h1>Getting the Data</h1>
<div class="line"></div>
<h3> Requests and Beautiful Soup was used to webscrape the book summaries and collect the information in a dataframe with book number, chapter number, chapter title and chapter summary. To do so, it only the hyperlinks for each book summary was needed. The summaries were cleaned and only includes actual words. The text analysis required the summaries to be tokenized which made it possible to look at word individually. The tokenized text where collected in a column of its own. These tokens where also made lower case and stopwords were removed such that irrelevant word were not included in the sentiment analysis. </h3>

<br>

<h3>A dataset which contained character information was used to identify characters in the summaries easily. Two columns that contained first- and last name was added which made it possible to identify characters by either full-, first- or last name as well as alternate name which was also already in the dataset. Even though the dataset had many more attributes such as house affiliation, ancestry etc. these where not used and thus not relevant for our analysis.</h3>

<h3>The chapter summaries were scraped from</h3>

<https://harrypotter.fandom.com> 
<h3>using BeautifulSoup </h3>

<https://www.crummy.com/software/BeautifulSoup/>

<h3>The .csv file with our webscraped data can be downloaded</h3>

[here](/plot_summary_df.csv)
<h3>and made into a pandas dataframe in Python with the lines</h3>

```python
import pandas as pd
from ast import literal_eval
df = pd.read_csv('plot_summary_df.csv', index_col=0, 
                 converters={'plot_tokens':literal_eval})
```

<h3>The character overview from</h3>

<http://hp-api.herokuapp.com> 
<h3>is a json file that can be downloaded</h3>

[here](/characters.json)

<h3>and made into a pandas dataframe in Python with the lines</h3>

```python
import pandas as pd
char = pd.read_json('characters.json')
```

