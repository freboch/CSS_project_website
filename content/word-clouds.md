---
title: Word Clouds
prev: network-analysis
next: sentiment-analysis
---
<head>
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
.line2 {
    padding-bottom: 2px;
    border-bottom: 1px solid #9CA3AF; 
}
</style>

</head>

<div class="line1"></div>

<h3>To investigate the plot development throughout the entire series, Natural Language Processing has been
applied to the dataset by visualizing the most commonly used words. This is done for both the dataset as an entirety, as well as individually for each book.
<br/>
The most commonly words throughout the entire series, is visualized as the word cloud, that can be see right below.
</h3>
<br/>
<img src="/images/full_word_cloud.png" width="500" />

<h3> According to the word cloud, the most mentioned words throughout the series, are all character names. 
Some of the largest words in the word cloud are: 

<ul>
  <li>Harry</li>
  <li>Ron</li>
  <li>Hermione</li>
  <li>Dumbledore</li>
  <li>Voldemort</li>
</ul>  

This suggests that, at least, the above characters are important in most, if not all, of the books. 
It has to be noted, that the importance of the characters cannot be directly interpreted from the word cloud.
This is due to the fact, that entire families have similar last names, causing multiple people to be defined by the same word. 
Furthermore, the word cloud does not make the connections between characters first names and last names i.e. a 
character could be mentioned by both first- and last name, and it would count towards to different word counts. 
</h3>

<h1>TF-IDF Wordclouds</h1>
<div class="line"></div>

<h3> This section will focus on words specific to the seven books as individual entities. By doing this, it will 
hopefully be possible to make valid hypothesis about the plots of each book.
This should be possible, since the characters probably won't be mentioned as much in respect to the individual books. Instead, we hope to see, that the 
most used words will be words unique to the specific book and their plots. 
</h3>
<br/>

<h2>Harry Potter and the Philosopher's Stone</h2>
<div class="line2"></div>
<br/>

<img src="/images/wordcloud_book_1.png" width="500" /> 

<h3> 
Some of the largest words in the word-cloud are: 

<ul>
  <li>Quirrel</li>
  <li>Fluffy</li>
  <li>Piers</li>
  <li>Troll</li>
  <li>Turban</li>
  <li>Mirror</li>
</ul>  

From the words above, you get the idea, that the main plot in the book contains subplots about a troll, turban, and a mirror. 
This is not all too wrong, however, it would be quite difficult to infer anything more complex about the plot, without knowing the story beforehand. 
However, since we do know the story, it makes great sense, that these are some of the most common words in the book. 
In Harry Potter and the philosopher's stone the trio (Harry, Ron and Hermione) battles a troll in the dungeons, furthermore they come across another troll, when they try to get the philosopher's stone. Therefore,
it makes great sense, that the word troll is so large, especially since it is a quite unique word. During one of Harry's many explorations of the Hogwarts castle, he finds the Mirror of Erised.
The Mirror of Erised is a key object in the book, which is why Mirror (as well as Erised) is a large word in the word cloud. 
While three of the words are names and refers to characters mentioned in the book (Piers Polkis, Quirinus Quirrell, and Fluffy the three-headed dog), it makes sense, that they have a large mention count in the first book. 
None of the three characters have any role in the following books, and are therefore unique to the first book. Both Fluffy and Quirrel play a large role in the first book - Fluffy as an obstacle to get to the Philosopher's stone, and Quirrel as the main antagonist. 
However, Piers does not play a particularly important character, for the majority of the book, but only in the first few chapters. It is quite interesting, that a character, who is only mentioned in a few chapters, is represented so greatly in the word cloud. 
In conclusion, based on the word cloud it is not possible to infer the entire plot of Harry Potter and the Philosopher's stone, but it is possible to see what aspects of the book are in focus. 
</h3>

<h2>Harry Potter and the Chamber of Secrets</h2>
<div class="line2"></div>
<br/>

<img src="/images/wordcloud_book_2.png" width="500" />

<h3> 
Some of the largest words in the word-cloud are: 

<ul>
  <li>Lockhart</li>
  <li>Heir</li>
  <li>Chamber</li>
  <li>Diary</li>
  <li>Petrified</li>
  <li>Riddle</li>
</ul>  

From the words above, you get the idea, that the main plot in the book contains subplots about a Diary, Chamber, an Heir, and something about petrification. 
This is not all too wrong, however, it would be quite difficult to infer anything more complex about the plot, without knowing the story beforehand. 
However, since we do know the story, it makes great sense, that these are some of the most common words in the book. 
In Harry Potter and the Chamber of secrets the main plot is that the Chamber of Secrets has been opened by the assumed Heir of Slytherin. 
The opening of the chamber causes great distress at Hogwarts school because the monster of Slytherin roams about the school and petrifies the muggle-born students. 
It is later revealed, that Tom Riddle (Lord Voldemort) has possesed one of the students by the use of a diary, and forced the student to open the Chamber of Secrets and attact the muggle-borns. 
Therefore, these words very clearly have great connection to the plot of the book. Furthermore, Gilderoy Lockhart is a character, with great importance in the book, as the new Defence Against the Dark Arts Professor. 
Just like Quirrel in the first book, Lockhart is a character unique to this specific book (although he is mentioned briefly in later books). As a character unique to this book, who, according to the word cloud, gets mentioned a lot, it is fair to assume, that he is an important character for the book's plot. 
In conclusion, based on the word cloud it is not possible to infer the entire plot of Harry Potter and the chamber of Secrets, but it is possible to see what aspects of the book are in focus. 
</h3>

<h2>Harry Potter and the Prisoner of Azkaban</h2>
<div class="line2"></div>
<br/>

<img src="/images/wordcloud_book_3.png" width="500" />

<h3> 
Some of the largest words in the word-cloud are: 

<ul>
  <li>Scabbers</li>
  <li>Lupin</li>
  <li>Pettigrew</li>
  <li>Buckbeak</li>
  <li>Dementors</li>
</ul>  

This word-cloud is very different from the two previously presented word-clouds. The main difference, is that this word-cloud, is focused on characters in the book. 
This makes it quite hard to infer anything about the plot. However, it is makes great sense, when you relate the word-cloud to the actual plot of the book. 
Unlike the previous two books, Harry Potter and the Prisoner of Azkaban focus more on the individual characters and their stories instead of a presented problem. 
Because the character development and character connections are in focus, it is quite natural, that the largest words in the word-cloud are characters. 
This could also be infered by the title of the book alone. While the previous two books have been named in regard to objects/places that appear in the books, the Prisoner of Azkaban refers to a specific person, 
which gives the idea that the plot of the book might be more focused on a character and the character's affiliations. 
In conclusion, while it is not obvious what the plot of the book is based on the word-cloud, it is very obvious that the characters are in focus in this book, meaning the book probably will contain a lot of
information about the respective characters.
</h3>

<h2>Harry Potter and the Goblet of Fire</h2>
<div class="line2"></div>
<br/>

<img src="/images/wordcloud_book_4.png" width="500" />

<h3>Some of the largest words in the word-cloud are: 

<ul>
  <li>Crouch</li>
  <li>Moody</li>
  <li>Bagman</li>
  <li>Champions</li>
  <li>Tournament</li>
  <li>Winky</li>
</ul>  

This word cloud is quite interesting, especially if you have knowledge of the plot presented in Harry Potter and the Goblet of Fire.
The words listed above seem to focus on the characters, and while they play an important role in the books, the plot of the book is based upon the Triwizard Tournament. 
Many of the characters listed (Bagman, Crouch, Winky) are unique to this specific book, since they are barely mentioned in other books, meaning that they play a large role in this book. 
Especially the word Crouch is important, since three characters in this book have that last name, and none of them play a significant role in any of the other books. 
Based on this presented word-cloud, it would be quite hard to infer anything about the plot of the book, if you have not read the book.  
</h3>

<h2>Harry Potter and the Order of the Phoenix</h2>
<div class="line2"></div>
<br/>

<img src="/images/wordcloud_book_5.png" width="500" />

<h3>Some of the largest words in the word-cloud are: 

<ul>
  <li>Umbridge</li>
  <li>Coutroom</li>
  <li>Wizengamot</li>
  <li>Inquisitor</li>
  <li>Grimmauld</li>
</ul>  

This word-cloud is difficult to interpret, since a lot of words are of the same size, making it hard to see anything that stands out.
The largest word in the word-cloud is, by far, Umbridge, which refers to Dolores Umbridge, the Defence against the Dark Arts professor in Harry's fifth year at Hogwarts. 
Umbridge plays a large role in this book, since she changes the life at Hogwarts completely and makes the students rebel against her. 
If is quite interesting, that words such as DA (Dumbledores army), or Prophesy is not larger words, since both are essential to the plot. 
However, the reason for this could be, that Harry Potter and the Order of the Phoenix is the longest book, making the plot extremely extensive.
So much happens throughout this book, and while both the DA and Prophesy are important aspects of the book, they are probably not mentioned as much as many other words, making them appear less significant in the word-cloud. 
However, the words listed manifests the idea, that this particular book might focus more on the corporate life within the Harry Potter universe. 
In conclusion, based on the word cloud it is not possible to infer much about the plot of Harry Potter and the Order of the Phoenix. 

<h2>Harry Potter and the Half-Blood Prince</h2>
<div class="line2"></div>
<br/>

<img src="/images/wordcloud_book_6.png" width="500" />

<h3> 
Some of the largest words in the word-cloud are: 

<ul>
  <li>Slughorn</li>
  <li>Necklace</li>
  <li>Morfin</li>
  <li>Merope</li>
  <li>Locket</li>
  <li>Felicis</li>
</ul>  

Once again, it would be difficult to say anything intelligent about the plot of the book based on the word-cloud if you have not read the book.
However, if you have read the book, the words make a lot of sense. 
For starters, both Felix Felicis and the Cursed Necklace play a role in the book. While neither of the words are the most prominent to focus on in the plot, they are unique to this specific book, making them important in the word cloud. 
Of course, both of the words are mentioned multiple times in the book, because they lay the foundation for the main plot. However, the real interesting words to look at in this word cloud are the characters Merope and Morfin. 
Neither of the two, are the main characters of the book, but they are quite large in the word-cloud. 
While, neither character is really all that important as individuals, the affiliation they have to the story is noticable. 
Both of the characters are related to Lord Voldemort, and a lot of the book plot contains information about Lord Voldemorts background. 
Therefore, it makes sense, that both Merope and Morfin are noticable in the word cloud.
The word Locket is also presented as a large word in the word-cloud. Again, the locket is mentioned in regard to Lord Voldemort's past, but also mentioned as the Horcrux Dumbledore and Harry set out to find. 
Meaning that the locket is a key aspect of the book. 
This word cloud actually explains tells us a lot about the plot of the book, since a lot of the mentioned words are connected to Voldemort's past, meaning that his past will probalby be in focus in the book.
</h3>

<h2>Harry Potter and the Deathly Hallows</h2>
<div class="line2"></div>
<br/>

<img src="/images/wordcloud_book_7.png" width="500" />

<h3> 
Some of the largest words in the word-cloud are: 

<ul>
  <li>Horcrux</li>
  <li>Sword</li>
  <li>Diadem</li>
  <li>Ariana</li>
  <li>Griphook</li>
  <li>Aberforth</li>
</ul>  

The main focus of Harry Potter and The Deathly Hollows is the trio's quest to locate the remaining Horcruxes. 
The seven Horcruxes are: The Locket, The Snake, The Cup, The Diadem, The Diary, The Ring, and Harry Potter himself. 
Out of the seven horcruxes, the only one with a name that is unique to this book is The Diadem, which is why this is the largest one in the word-cloud.
The Horcruxes can be destroyed using the Sword of Gryffindor, and is mentioned a lot in the book. 
It is interesting that Ariana, Griphook, and Aberforth are large words in the word-cloud. All three characters are important to the plot line. However, one could argue, that 
Xenophilius Lovegood or Dobby are important characters as well, but they are only small-sized in the word cloud. This is due to the fact, that both characters have names that are not unique to this specific book. 
While Griphook is mentioned in Harry Potter and The Philosopher's stone, it is only once, and Aberforth or Ariana has not been mentioned before the seventh book. 
These characters are, therefore, unique to this book and of importance to the subplots. Therefore, they are mentioned in the word-cloud as large words.
</h3>

<h1>General Conclusion</h1>
<div class="line2"></div>
<br/>

<h3>
The word-clouds generally contain information unique to each of the books. This can be seen by every year's Defence against the Dark Arts professor being clearly visible in each of the word-clouds. 
Based on the word-clouds it would not be easy to interpret the plot of the books, if you have not read them. However, if you have read the books,
it will probably be clear, why the word-clouds look like they do. The word-clouds give a good overview of important things/characters mentioned in each books. 
If one looked at the word-clouds BEFORE reading the books, this person would know what aspects of each book, would be important to note, and maybe make them remember subplots connected to these aspects. 
</h3>









