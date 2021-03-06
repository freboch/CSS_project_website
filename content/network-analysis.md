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

<h3>The aim of the network analysis was to locate communities in the dataset. Furthermore, the analysis should make it possible to identify the main characters of every book. The Louvain method for community detection is used to partion characters into communities. The Louvain method computes the partition of all nodes in respect to the partition which maximises the modularity by the use of Louvain heuristics. Unweighted graphs for the book series as a whole and the individual books in combination with Louvain communities will be visualized and analysed. Based on these visualizations, it will be discussed whether the communities make sense in relation to the plots of every book. For us, it will be fun to see if the Louvain community detection method supports a pattern that we, as fans, can see makes sense. Furthermore, modularity will be used to measure the the density of connections within a community. High modularity indicates dense connections between the nodes within communities but sparse connections between nodes in different modules. Modularity is in the interval [-1.0,1.0].

Weighted graphs for the book series as a whole and the individual books will also be visualized and analysed. They make it possible to determine the main characters in the book(s). This requires that the node weight of each character is computed. Notice that this node weight is calculated by counting how many times each character is mentioned in total. From this method, one should be able to detect the most important characters of the book(s) based on the specific mention count. To the suprise over everyone, we firmly believe that Harry Potter comes out as the winner at that point.
</h3>

<h1>Nodes</h1>
<div class="line"></div>
<br>

<h3>
Number of nodes in all books is 183 . Thus, there are 183 unique characters in the summaries.</h3>

<img src="/images/Nodes.png" width="700" />


<h3>
Books 1, 2, 3, and 6 mainly revolve around life at school with no new additions to the school life really. Therefore, not many new relationships are introduced across the board.
Book 4 adds life to the school due to the Triwizard Tournament. Additionally, the characters have also become a little more adult in this book and start to date.
Book 5 introduces the Order of the Phoenix and its members which are connected to not only each other but also makes it common for lots of people to appear in chapters with lots of other people instead of only Harry, Ron and Hermonie. 
Book 7 is the showdown between Good and Evil which contain a massive battle where characters from every side of the spectrum (that wouldn't necessarily have met otherwise) battle or help each other.
</h3>

<h1>Edges</h1>
<div class="line"></div>
<br>

<h3>
Number of edges in all books is 3283 . Thus, there are 3283 character relations mentioned in the summaries.
</h3>

<img src="/images/Edges.png" width="700" />


<h3>
Books 1, 2, and 3 mainly revolve around life at school. They each have characters that only appear in that specific book. For instance, it's very known that the Defence Against the Dark Arts teacher is replaced quite frequently  (yearly). Other than that they mainly consist of core characters that appear in every book. 
Book 4 also revolves around the school but characters from other schools are introduced due to the Triwizard Tournament. 
Book 5 introduces the Order of the Phoenix and its members. Furthermore, Death Eaters, who previously only were known as a collective of wizards that support Lord Voldemort, are now mentioned by name. Additionally, the Ministry of Magic plays a more important role as some of the book also takes place there for the first time. 
Book 6 maintains from Book 5 that Death Eaters are mentioned more a individuals. 
Book 7 is to no surprise the book with most unique characters. It basically revolves around the battle between Good and Evil, and both sides have lots of characters.
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
It is quite difficult to infer anything from this network. 
However, it is obvious that five communities have been detected. 
The detected communities does not make much sense either, although some tendencies can be spotted. 
An example of such tendencies are that many of the Hogwarts students are within the same community. 
However, none of the tendencies are consistent or sufficiently obvious to make any definite statements. 
</h3>

<h2>Harry Potter and the Philosopher's Stone</h2>
<div class="line"></div>
<br>

<img src="/images/Book1UW.png" width="700" />

<h3> 
An initial observation is that the Louvain partition still detects five communities. 
One community consists of the characters introduced or mentioned a lot in Diagon Alley (denoted by the light purple color).
Another community (denoted by the white color) consists of the Potter/Dursley families. This community also contains characters introduced in the first few chapters of the book such as Piers Polkis and Sirius Black.
Both Minerva McGonagall and Godric Gryffindor can be found in this community as well. Godric Gryffindor is probably mentioned in this community because, Godric's Hollow is mentioned in the first chapter, and classified it as a mention of his name instead, which qualifies as a hitch. 
It is a little more difficult to explain why McGonagall is in this community, since she is a Hogwarts teacher. However, she plays an important character in the first few chapters. 
McGonagall is presented in the first chapter when she spies on the Dursleys and when Harry receives his Hogwarts letter, which is signed by her. 
Therefore, it is plausible that McGonagall is clustered in this community. 
The trend of the three remaining communities is not quite clear. However, this could be due to multiple characters only being briefly introduced in this book, since it is the first of seven. 
These introductions would make it difficult to spot communities, unless the trend is obvious. 
</h3>

<h2>Harry Potter and the Chamber of Secrets</h2>
<div class="line"></div>
<br>

<img src="/images/Book2UW.png" width="700" />

<h3>
The first observation to notice about this network is that only four different communities have been detected for this book. 
One community presented in the above network (denoted by light purple color), once again consists of Harry Potter and the Dursleys.
However, both Ron and Hermione are now clustered with Harry as well, which makes tremendous sense, since the trio are mentioned together quite often. 
This cluster also contains the characters Mr. Mason, Mrs. Mason, Hedwig, Oliver Wood, Mosag, and Milicent Bulstrode. 
Both Mr. and Mrs. Mason are only mentioned in the two first chapters, which is why they are included in this community, since this is when Harry is at Privet Drive number 4 with the Dursleys. 
Hedwig and Oliver Wood are both characters that are primarily mentioned alongside Harry, making it natural to add them to the community Harry is in. 
The more curious characters in the community are Mosag and Millicent Bullstrode. Mosag is the wife of Aragog, but since she is only named once in the same chapter as Harry, Ron, and Hermione, her relation to Aragog becomes obsolete. 
Aragog is not in this community since he is linked to Hagrid as well as mentioned by name in more chapters than his wife, which results in more connections to other characters than her. 
Millicent Bullstrode is the Slytherin girl whom Hermione battled at Duelling Club and afterwards tried to turn into using Polyjuice Potion. 
Therefore, Millicent is mentioned primarily alongside Harry, Ron, and Hermione, which assigns her to their cluster. 

Many of the characters who are primarily associated with Hogwarts, as student or teachers, are in a community together (denoted by pink color). 
However, this community excludes all the Weasley kids, even though most of them attend Hogwarts. The two communities are separated, because the Weasley children (Ron excluded)
are assigned to a cluster with their parents as well as characters mentioned in Diagon Alley (denoted by the dark red).
The last cluster is quite random, making it hard to say anything specific about it. 

</h3>


<h2>Harry Potter and the Prisoner of Azkaban</h2>
<div class="line"></div>
<br>

<img src="/images/Book3UW.png" width="700" />

<h3>
Once again, only four communities are detected in this network. However, not much sense can be made of the respective communities.
The reason for the confusing state of this network could be, that the book introduces several new characters that have ties to multiple of the original characters. 
Therefore, it can be difficult to assign these new characters a cluster, since they are not mentioned consistently alongside other characters. 
This can result in a confusing network with inconsistent communities such as the one shown in this case.  
</h3>

<h2>Harry Potter and the Goblet of Fire</h2>
<div class="line"></div>
<br>

<img src="/images/Book4UW.png" width="700" />
<h3>
Once again, only four communities are detected in this network. 
Harry is once again not in the same community as Ron and Hermione, which can seem odd. 
However, Harry is in a cluster with many characters who are mostly named in connection to Harry Potter (denoted by pink color). 
An example of this is Franc Bryce, who is the muggle man Harry sees dying in a dream in the beginning of the book. 
Franc Bryce is named alongside Voldemort and Peter Pettrigrew who are both in the cluster
Bellatrix Lestrange and the entire Longbottom family is also in Harry's community. This is probably because Harry witnessed the trial of Bellatrix for the crime committed to the Longbottoms. 
Furthermore Bellatrix, as well as Lucius Malfoy, is also one of the Death Eaters Voldemort mentions at the graveyard, which is probably why both of the characters are in this community. 
The remaining characters are split between three communities. The partition of the three communities is not all that obvious, and it is quite hard to make any suggestions as to why they are split as such.  
</h3>


<h2>Harry Potter and the Order of the Phoenix</h2>
<div class="line"></div>
<br>

<img src="/images/Book5UW.png" width="700" />

<h3>
The first observation to notice about this network is that only three different communities have been detected for this book. 
The majority of the students associated with Dumbledore's Army are in a community together (denoted by dark red color). This makes tremendous sense, since these characters are often mentioned alongside each other. 
In the community with Harry Potter (denoted by white color), one can spot many members of the Order of the Phoenix as well as Harry's family and the Death Eaters present at the Ministry of Magic during the end of the book. 
This community is pretty explainable as well, though one might argue that characters such as Ron and Hermione should be partioned with Harry. 
The last and final community is quite difficult to interpret why the characters are in this community. 
</h3>


<h2>Harry Potter and the Half-Blood Prince</h2>
<div class="line"></div>
<br>

<img src="/images/Book6UW.png" width="700" />

<h3>
Once again, four communities are detected in this network. Two of these communities (denoted by white and pink colors) are very separated from the rest of the network, which should make it easier to understand why the characters are in these communities. 
The pink community, which contains both Sirius Black and Cornelius Fudge as well as other characters mentioned as dead in the beginning of the book, when Scrimgeour and Fudge visit the prime minister in his office. 
Lord Voldemort is also mentioned multiple times alongside these characters, because he is responsible for their deaths and events the minister is informed about. 
Therefore, the pink community is quite easily explained. The white community consists of characters mentioned when Harry and Dumbledore visit old memories of Tom Riddle. 
Both Narcissa Malfoy and Bellatrix Lestrange are in this community as well, but the reason for this is not entirely obvious. However, since most of the community is consistent to the tendency, it is pretty easily explained. 
The reason for the separation of the last two communities is not all that clear, since both are a mix of teachers and students at Hogwarts as well as some other characters. 

</h3>

<h2>Harry Potter and the Deathly Hollows</h2>
<div class="line"></div>
<br>

<img src="/images/Book7UW.png" width="700" />


<h3>
Five communities have been detected in this network, which makes it the most divided individual network. 
Harry Potter is once again not in the same community as Ron and Hermione, but in a community with characters, who are mentioned primarily alongside Harry. 
This community also includes the Dursley family and the two members of the Order of the Phoenix with whom they go into hiding with. 
The trends in the rest of the communities are not sufficiently obvious to make any real conclusions about the nature of connections between the characters in the communities.
</h3>

<h2>Modularity</h2>
<div class="line"></div>

<br>

<img src="/images/Modularity.png" width="700" />

<h3>
People definitely interact with each other across communities which this plot supports as the modularity appears relatively neutral. In Books 5-7 the battle between Good (Harry) and Evil (Voldemort) becomes more clear so does the tendency to interact more closely with one's community.   
</h3>

<h2>General Conclusion</h2>
<div class="line"></div>
<br>

<h3>
In many of the individual networks, it is possible to make conclusions about some of the displayed communities. 
However, the division of many of the communities is not quite obvious. 
The reason for vague nature of the communities could be explained by the fact that the data presented only consists of plot summaries and not the entire chapters. 
Therefore, it can be difficult to detect the communities because the information is simply not extensive enough. 
Furthermore, the drawback of community partition methods is that they have a tendency to let small clusters be absorbed by larger ones. This would make our network communities less nuanced. 
</h3>

<h1>Character mention development</h1>
<div class="line"></div>

<h3>
NB! Zoom to view the node labels clearer for all networks in this section.

All characters mentioned throughout all seven books can be seen in the network below. This network will allow us to distinguish between characters who are mentioned frequently - increase in mentions (frequency) leads to increase in node size.
</h3>

<img src="/images/WG.png" width="700" />

<h3>
It is quite obvious that characters such as Harry Potter, Ron Weasley, Hermione Granger, Albus Dumbledore and Lord Voldemort are mentioned significantly more than other characters.
This makes tremendous sense since many of the books revolve around these characters. 
However, the book as individual networks will hopefully help us to determine the most fundamental characters of each book.
</h3>


<h2>Harry Potter and the Philosopher's Stone</h2>
<div class="line"></div>
<br>

<img src="/images/WG1.png" width="700" />


<h3>
According to this network, the most mentioned characters in Harry Potter and the Philosopher's Stone are
<br>
<br>
<ul>
  <li>Harry Potter</li>
  <li>Rubeus Hagrid</li>
  <li>Hermione Granger</li>
  <li>Ron Weasley</li>
  <li>Vernon Dursley</li>
</ul> 

Out of all the characters, Harry Potter is mentioned the most in this book, which makes tremendous sense since he is the main character of the book series. 
Hagrid interacts with Harry in most chapters in this book, which increases Hagrid's mention count. 
All the Dursleys are actually mentioned quite a lot in the beginning of the book, as well as every time Harry explains his living situations to his new friends at Hogwarts. 
Therefore, even though the Dursleys actually do not play that big of a role in the evolving plot of the book, they are identified as important characters. 
It seems natural that both Ron and Hermione's nodes are large, since they are Harry's best friends. Ron's node is slightly bigger than Hermiones, which is probably because Harry befriended Ron earlier in the book than he did Hermione. 
Other Hogwarts characters such as Dumbledore, Draco Malfoy, McGonagall and Snape also have distinguishable nodes.
Draco is Harry's main student antagonist, which is presumably why he is presented as a larger node.
Both McGonagall and Dumbledore are introduced early and are mentioned fairly regularly during the entire book. 
While Snape is not the final antagonist Harry has to fight, he is mentioned quite often in relation to bullying Harry. 
Even though Quirrell is the main antagonist in this book, his node is fairly small. This is probably because Harry thinks Snape is the bad guy for a considerable part of the books.
This means that the focus is not on Quirrell before the end of the book, and is therefore not mentioned all that much. 


The difference in node size is not quite clear for many of the remaining character.
However, the network seems to have detected the important characters of the book very successfully for this book. 
</h3>


<h2>Harry Potter and the Chamber of Secrets</h2>
<div class="line"></div>
<br>

<img src="/images/WG2.png" width="700" />

<h3>
According to this network, the most mentioned characters in Harry Potter and the Chamber of Secrets are
<br>
<br>
<ul>
  <li>Harry, Ron and Hermione (the trio) </li>
  <li>Gilderoy Lockhart</li>
  <li>Draco- and Lucius Malfoy</li>
  <li>Albus DumbleDore</li>
  <li>Ginny Weasley</li>
</ul> 

Harry, Ron and Hermione are all mentioned a lot, which makes tremendous sense, since Harry is the main character and his best friends are Hermione and Ron. 
Gilderoy Lockhart is the Defence Against the Dark Arts professor in this book, and is mentioned quite a lot. Lockhart is mentioned when Harry is at the Burrow, in Diagon Alley, at Hogwarts and when Harry ventures into the Chamber of Secrets. 
Both the nodes of Draco and Lucius are large. It makes sense, that Draco is large, because the trio suspects he is the Heir of Slytherin for some time. 
While Lucius does not appear for long time periods in the book, he is mentioned frequently by name, when he is with Harry in Diagon Alley, Hagrid's Hut, and Dumbledores Office. 
Ginny Weasley is also an important character in this book, since she is the one to open the Chamber of Secrets.

The difference in node size is not quite clear for many of the remaining character.
However, the network seems to have detected the important characters of the book very successfully for this book. 

</h3>


<h2>Harry Potter and the Prisoner of Azkaban</h2>
<div class="line"></div>
<br>

<img src="/images/WG3.png" width="700" />


<h3>
According to this network, the most mentioned characters in Harry Potter and the Prisoner of Azkaban are
<br>
<br>


<ul>
  <li>Harry, Ron, and Hermione (the Golden Trio) </li>
  <li>Sirius Black, James Potter, Peter Pettigrew, and Remus Lupin (The Marauders)</li>
  <li>Albus DumbleDore</li>
  <li>Buckbeak</li>
  <li>Hagrid</li>
  <li>Snape</li>
</ul> 

Once again, the the Golden Trio is mentioned a lot in this book. Sirius Black is the Prisoner of Azkaban referenced in the book title, which makes it natural for him to be mentioned a lot in this book. 
Sirius Black was friends with the remaining Marauders when they were students at Hogwarts. This book has a lot of focus on history of the Marauders, and they are all mentioned in multiple situations throughout the book. 
Furthermore, Lupin is the Defence Against the Dark Arts professor this year and has a lot of interactions with Harry, especially during Harry's private Dementor Lessons and in the Shrieking Shack.
Buckbeak and Hagrid are also important characters in this book, and both the trial and escape of BuckBeak are used to built tension towards the end of the book. 

The difference in node size is not quite clear for many of the remaining character.
However, the network seems to have detected the important characters of the book very successfully for this book. 

</h3>



<h2>Harry Potter and the Goblet of Fire</h2>
<div class="line"></div>
<br>

<img src="/images/WG4.png" width="700" />


<h3>
Based on previous observations, it is fair to assume that the Golden Trio, along with characters such as Hagrid, Snape, Dumbledore, Draco, and MacGonagall, are all mentioned fairly often in all the books. 
Therefore, the analysis will from now on focus primarily on the more size-varying nodes. If any of the mentioned characters suddenly behaves out of pattern, it will be commented upon.  
<br>
<br>
According to this network, the most mentioned characters in Harry Potter and the Goblet of Fire are
<br>
<br>


<ul>
  <li>Barty Crouch</li>
  <li>Lord Voldemort</li>
  <li>Alastor Moody</li>
  <li>Cedric Diggory</li>
</ul> 

While Alastor Moody is mentioned by name multiple times during this book, the character himself does not play such a big role in this book since the Moody mentioned throughout the book technically refer to Barty Crouch Jr. Barty Crouch Jr is thought to be Alastor Moody for the majority of the book, if the network creation was more intelligent, it should be possible to add 
certain conditions to change this behaviour. However, for now, it makes sense that Alastor Moody is a large node in this book, since he helps Harry a lot before he is revealed as one of the antagonists Barty Crouch.
Lord Voldemort is represented by a much larger node in this book, which is an indication that he is slowly starting to play a more important role. 
Other interesting characters are Ludo Bagman and Rita Skeeter, who both appear quite often during this book, even though neither of them are permanently at Hogwarts.
It is fascinating that characters such as these two have nodes of similar size as the Triwizard Champions Fleur, Krum, and Cedric. 
On a surface level, it may seem weird, but when digging deeper, one must realize that Rita writes a multitude of articles and interviews many people throughout the book. 
Meanwhile, Bagman is present at the Quidditch World Cup, The Twirwizard Tournament, and in Hogsmead. Ultimately, this means that both characters are mentioned many times in the book.

The difference in node size is not quite clear for many of the remaining character.
However, the network seems to have detected the important characters of the book very successfully for this book. 

</h3>


<h2>Harry Potter and the Order of the Phoenix</h2>
<div class="line"></div>
<br>

<img src="/images/WG5.png" width="700" />


<h3>
According to this network, the most mentioned characters in Harry Potter and the Order of the Phoenix are
<br>
<br>


<ul>
  <li>Dolores Umbridge</li>
</ul> 

The only note to change significantly is the node of Dolores Umbridge. Umbridge is the Defence Against the Dark Arts professor in this book. 
She is also one of the main antagonists, which means she is mentioned a lot in the book and explains the size of her node. 
Many characters are mentioned in this book due to the introduction of the Order of the Phoenix, Dumbledores Army and Harry's visit to the Ministry of Magic. 
Because so many characters are mentioned, the individual importance of the characters become less clear, since the node sizes vary less. 

However, it seems fairly correct that Umbridge and the trio are represented by the largest nodes.

</h3>


<h2>Harry Potter and the Half-Blood Prince</h2>
<div class="line"></div>
<br>

<img src="/images/WG6.png" width="700" />


<h3>
According to this network, the most mentioned characters in Harry Potter and the Half-Blood Prince are
<br>
<br>


<ul>
  <li>Draco Malfoy</li>
  <li>Albus Dumbledore</li>
  <li>Severus Snape</li>
  <li>Horace Slughorn</li>
</ul> 

From the looks of the network this book primarily focus on original characters, since it is the nodes of Draco, Voldemort, Dumbledore, and Snape, that are most noticeable.  
This makes tremendous sense, since the book contains a lot of information about Harry and Dumbledore's investigation of Voldemort's past. Furthermore, Snape and Draco are becoming more prominent characters, which aligns with the look of the network. 
Horace Slughorn is also mentioned fairly often, since he is a new professor at Hogwarts, who ultimately helps Harry by giving him an otherwise incomplete memory so Harry can further his investigation of Voldemort. 

The difference in node size is not quite clear for many of the remaining character.
However, the network seems to have detected the important characters of the book very successfully for this book. 

</h3>

<h2>Harry Potter and the Deathly Hollows</h2>
<div class="line"></div>
<br>

<img src="/images/WG7.png" width="700" />

<h3>
Once again, this book seems to focus on the main characters (Voldemort, the Golden Trio, and Dumbledore especially). 
This is pretty consistent with the plot of the book. Many of the book chapters describes the trio's quest to locate the Horcruxes,
only mentioning other characters whn they interact with the trio in some way. Voldemort is the main antagonist in this book and is the character the Golden Trio must defeat. 
It is interesting that Dumbledore still remain a large node, since he dies in the previous book. However, he is mentioned quite a lot, because Harry tries to make sense of hints Dumbledore provided him with while still alive. 

The difference in node size is not quite clear for many of the remaining character.
However, the network seems to have detected the important characters of the book very successfully for this book. 

</h3>

<h2>General Conclusion</h2>
<div class="line"></div>
<br>

<h3>
The method used to create the weighted networks appear to have worked fairly well. 
The most important characters of each book are easy to spot, and it is obvious why the larger nodes are sized as they are presented. 
It is more difficult to make any conclusions about the importance of the characters with smaller notes, since the books introduces a multitude of different characters, which ultimately makes it difficult to distinguish between node size.
</h3>