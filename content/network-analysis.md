---
title: Network analysis
prev: data-description
next: word-clouds
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

<h3>The aim of the network analysis, was to locate communities in the dataset. Furthermore, the analysis should make it possible to indentify the main characters of every book. 
These communities are located by using the Louvain partition. The Louvain partition computes the partition of all the graph nodes in respect to the partition which maximises the modularity by the use of Louvain heuristics. 
In the following sections, multiple graphs of the partition will be presented and analyzed. 
It will be discussed whether the communities, made by the Louvain partition, make sense in regard to the plots of every book. 
This will be done for both all the books and each book individually. 

The main characters in the story are located by calculating the node weight for each character.
This node weight is calculated by counting how many times each character is mentioned in total. 
By using the presented method, one should be able to detect the most important characters of the story based on the specific mention count.
This will be done for both all the books and each book individually. 
</h3>

<h1>Community Detection</h1>
<div class="line"></div>
 
<h3> 
NB! Zoom to view the node labels clearer for all networks in this section.
<br>

The communities detected throughout all the books can be seen on the network below.
</h3>

<img src="/images/AllbooksUW.png" width="700" />

<h3>
It is quite difficult to infer anything from the network. 
However, it is obvious that five communities have been detected. 
The detected communities does not make much sense either, although some tendencies can be spotted. 
An example of such tendencies are that many of the Hogwarts students are within the same community. 
However, none of the tendencies are consistent or obvious enough to make any definite statements. 
</h3>

<h2>Harry Potter and the Philosopher's stone</h2>
<div class="line"></div>
<br>

<img src="/images/Book1UW.png" width="700" />

<h3> 
When looking at the above network, it is noticed, that the Louvain partition still detects five communities. 
One community, consists of the characters introduced or mentioned a lot in Diagon Alley (denoted by the light purple color).
Another community (white color) consists of the Potter/Dursley families. This community also contains characters introduced in the first few chapters of the book such as Piers Polkis and Sirius Black.
Both Minerva McGonagall and Godric Gryffindor can be found in this community as well. Godric Gryffindor is probably mentioned in this community because, Godric's Hollow is mentioned in the first chapter, and classified it as a mention og his name instead, which qualifies as a bug. 
It is a little more difficult to explain why McGonagall is in this community, since she is a Hogwarts teacher. However, she plays an important character in the first few chapters. 
McGonagall is presented in the first chapter when she spies on the Dursleys and when Harry gets his Hogwarts letter, which is signed by her. 
Therefore, it is plausible that McGonagall is clustered in this community. 
The trend of the three remaining communities is not quite clear. However, this could be due to multiple characters only being briefly introduced in this book, since it is the first of seven. 
These introductions would make it difficult to spot communities, unless the trend is obvious. 
</h3>

<h2>Harry Potter and the Chamber of Secrets</h2>
<div class="line"></div>
<br>

<img src="/images/Book2UW.png" width="700" />

<h3>
The first thing to notice about this network, is that only four different communities have been detected for this book. 
One community presented in the above network (light purple), once again consists of Harry Potter and the Dursleys.
However, both Ron and Hermione are now clustered with Harry as well, which makes great sense, since the trio are mentioned together quite often. 
This cluster also contains the characters Mr. Mason, Mrs. Mason, Hedwig, Oliver Wood, Mosag, and Milicent Bulstrode. 
Both Mr. and Mrs. Mason are only mentioned in the two first chapters, which is why they are included in this community, since this is when Harry is at Privet Drive number 4 with the Dursleys. 
Hedwig and Oliver Wood are both characters that are primarily mentioned alongside Harry, making it natural to add them to the community Harry is in. 
The more interesting characters in the community are Mosag and Millicent Bullstrode. Mosag is the wife of Aragog, but since she is only named once in the same chapter as Harry, Ron, and Hermione, her relation to Aragog becomes obsolete. 
Aragog is not in this community since he is linked to Hagrid as well as mentioned by name in more chapters than his wife, giving him more connections to other characters. 
Millicent Bullstrode is the Slytherin girl whom Hermione battled at duelling club and afterwards tried to turn into using Polyjuice Potion. 
Therefore, Millicent is mentioned primarily alongside Harry, Ron, and Hermione, which assigns her to their cluster. 

Many of the characters who are primarily associated with Hogwarts - as student or teachers, are in a community together (Pink). 
This community excludes all the Weasley kids however, even though most of them go to Hogwarts. The two communities are separated, because the Weasley children (Ron excluded)
are assigned to a cluster with their parents, and characters mentioned in Diagon Alley (Dark Red).
The last cluster is quite random, making it hard to say anything specific about it. 

</h3>


<h2>Harry Potter and the Prisoner of Azkaban</h2>
<div class="line"></div>
<br>

<img src="/images/Book3UW.png" width="700" />

<h3>
Once again, only four communities are detected. However, not much sense can be made of the respective communities.
The reason for the confusing state of this network could be, that the book introduces several new characters, that have ties to multiple of the original characters. 
Therefore, it can be difficult to assign these new characters a cluster, since they are not mentioned consistently alongside other characters. 
This can result in a confusing network, with inconsistent communities such as the one shown on this graph.  
</h3>

<h2>Harry Potter and the Goblet of Fire</h2>
<div class="line"></div>
<br>

<img src="/images/Book4UW.png" width="700" />
<h3>
For communities have been detected in this network. 
Harry is once again not in the same community as Ron and Hermione, which can seem strange. 
However, Harry is in a cluster with many characters who are mostly named in connection to Harry Potter (Pink). 
An example of this is Franc Bryce, who is the muggle man Harry sees dying in a dream in the beginning of the book. 
Franc Bryce is named alongside Voldemort and Peter Pettrigrew who are both in the cluster
Bellatrix Lestrange and the entire Longbottom family is also in Harry's community. This is probably because Harry witnessed the trial of Bellatrix for the crime committed to the Longbottoms. 
Furthermore Bellatrix, as well as Lucius Malfoy, is also one of the Death Eaters Voldemort mentions in the graveyard, which is probably why both of the characters are in this community. 
The remaining characters are split between three communities. The partition of the three communities is not all that obvious, and it is quite hard to make any suggestions as to why they are split as such.  
</h3>


<h2>Harry Potter and the Order of the Phoenix</h2>
<div class="line"></div>
<br>

<img src="/images/Book5UW.png" width="700" />

<h3>
While only three communities have been detected in this network, the visualization of the network seems to be more divided that previously, possibly meaning, that the reasoning of the partition will be more obvious. 
The majority of the students associated with Dumbledore's Army, are in a community together (Dark Red). This makes great sense, since these characters are often mentioned alongside each other. 
In the community of Harry Potter (white), one can spot many members of the Order of the Phoenix as well as Harry's family and the Death Eaters present at the ministry of magic during the end of the book. 
This community is pretty explainable as well, though one might argue that characters such as Ron and Hermione should be grouped with Harry. 
The last and final community is pretty confusing and is quite difficult to interpret why the characters are in this community. 
</h3>


<h2>Harry Potter and the Half-Blood Prince</h2>
<div class="line"></div>
<br>

<img src="/images/Book6UW.png" width="700" />

<h3>
This network consists of four communities. Two of these communities (white and pink) are very separated from the rest of the network, which should make it easier to understand why the characters are in these communities. 
The pink community, which contains both Sirius Black and Cornelius Fudge as well as other characters mentioned as dead in the beginning of the book, when Scrimgeour and Fudge visit the prime minister in his office. 
Lord Voldemort is also mentioned multiple times alongside these characters, because he is responsible for their deaths and the general events the minister is informed about. 
Therefore, the pink community is quite easily explained. The white community consists of characters mentioned when Harry and Dumbledore visit old memories of Tom Riddle. 
Both Narcissa Malfoy and Bellatrix Lestrange are in this community as well, but the reason for this is not entirely obvious. However, since most of the community is consistent to the tendency, it is pretty easily explained. 
The reason for the seperation of the last two communities is not all that clear, since both are a mix of teachers and students at Hogwarts as well as some other characters. 

</h3>

<h2>Harry Potter and the Deathly Hollows</h2>
<div class="line"></div>
<br>

<img src="/images/Book7UW.png" width="700" />


<h3>
</h3>

<h2>General Conclusion</h2>
<div class="line"></div>
<br>

<h3>
</h3>

<h1>Character mention development</h1>
<div class="line"></div>

<h3>
</h3>


<h3>
</h3>

<h2>Harry Potter and the Philosopher's stone</h2>
<div class="line"></div>
<br>

<img src="/images/Book1UW.png" width="700" />


<h3>
</h3>


<h2>Harry Potter and the Chamber of Secrets</h2>
<div class="line"></div>
<br>

<img src="/images/Book2UW.png" width="700" />


<h3>
</h3>


<h2>Harry Potter and the Prisoner of Azkaban</h2>
<div class="line"></div>
<br>

<img src="/images/Book3UW.png" width="700" />


<h3>
</h3>

<h2>Harry Potter and the Goblet of Fire</h2>
<div class="line"></div>
<br>

<img src="/images/Book4UW.png" width="700" />


<h3>
</h3>


<h2>Harry Potter and the Order of the Phoenix</h2>
<div class="line"></div>
<br>

<img src="/images/Book5UW.png" width="700" />


<h3>
</h3>


<h2>Harry Potter and the Half-Blood Prince</h2>
<div class="line"></div>
<br>

<img src="/images/Book6UW.png" width="700" />


<h3>
</h3>

<h2>Harry Potter and the Deathly Hollows</h2>
<div class="line"></div>
<br>

<img src="/images/Book7UW.png" width="700" />

<h3>
</h3>
