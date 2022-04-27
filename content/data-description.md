---
title: Data description
prev: "/"
next: network-analysis
---

The data for the project consists of chapter plot summaries of all the chapters in the 7 Harry Potter books. The plot summaries are from [*harrypotter.fandom.com*](https://harrypotter.fandom.com/wiki/Main_Page). We also got a character overview from [*hp-api.herokuapp.com*](*https://hp-api.herokuapp.com/*). 

The books consist of **198** chapters, and the plot summaries of these totals **57,382** words.

The character overview contains information on **403** characters, but only **183** of these are actually mentioned in the plot summaries.

# Getting the Data

The chapter summaries were scraped from  [*harrypotter.fandom.com*](https://harrypotter.fandom.com/wiki/Main_Page) using [*BeautifulSoup*](https://www.crummy.com/software/BeautifulSoup/). 

The .csv file with our webscraped data can be downloaded [here](/static/plot_summary_df.csv) and made into a pandas dataframe in python with the lines

```python
import pandas as pd
from ast import literal_eval
df = pd.read_csv('plot_summary_df.csv', index_col=0, 
                 converters={'plot_tokens':literal_eval})
```



