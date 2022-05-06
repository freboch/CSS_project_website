---
title: Sentiment Analysis
prev: word-clouds
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
<h3>
To investigate the mood development through the series we have performed some sentiment analysis on the chapter summaries.

Sentiment analysis uses a happiness score to assess the sentiment of a text. The happiness scores in this analysis are from <a href="https://hedonometer.org/words/labMT-en-v2/">here</a>. The dataset consists of 10,187 words and their corresponding happiness score. We have shifted the scores from a [0;10] scale to a [-5;5] scale so that 0 means neutral.

We have a hypothesis that each book gets less happy as you move from beginning to end, and that the same can be said for the series as a whole. Scroll down to see what we found out.
</h3>

<h2>Overall Series mood</h2>
<div class="line1"></div>
<h3>
First lets look at the entire series. For each chapter we compute the average happiness score and this plot shows these averages for all chapters in the series. The trend line is a linear regression. 

<img src="/images/series_happiness.png" width="700" /> 

This plot shows us that with few exceptions the happiness of the chapter summaries is above zero, that is slightly positive. Some of the peaks and valleys have been annotated with a brief description of what happens in that chapter. Not surprising, chapters where a character dies stand out as particularly unhappy. Conversely, festive chapters like a Christmas, birthday or the Quidditch World Cup (pre death eater attack) stand out as particularly happy. 

The trendline seems to support our hypothesis that the series as a whole gets less happy as it goes on, even if the drop is not very dramatic (less than 0.4 over the whole series).

All of this gets challenged if we add the standard deviation of the mean to our plot. 

<img src="/images/series_happiness_std.png" width="700" /> 

The mean and trendline is of course still the same, but the standard deviation shows us, that the peaks and valleys we see in the mean might not be as clear cut. The happiness score seems to be more accurately described as having a mean of about 0.5 plus/minus 1 for all chapters, with a couple of exception in the negative direction. 

The large standard deviation is due to the plot summaries not being very long, and there therefore not being that many scores to compute the mean over. 

All that being said, the plot does show happy and unhappy chapters that we can recognize from the books. Deaths of important and good characters are some of the valleys: Cedric, Sirius, Dumbledore, Dobby, Harry (though he survives). Festive chapters like Christmases, a birthday, festivities at the Quidditch World Cup are some of the peaks. 
</h3>

<h2>Books</h2>
<div class="line1"></div>
<h3>

Looking at the book-scale instead of the series scale, and focusing only on the trend lines instead of the individual chapter scores we see that the hypothesis holds again. The books do not have the same number of chapters, so for the sake of comparison they have been normalized to a [0;1] depth in book scale.

<img src="/images/book_happiness_trendlines.png" width="700" /> 

Each book has an ever so slight negative development from start to finish. Book 5 has the steepest decline due to the very negative chapters toward the end where Arthur Weasley is attacked by Nagini the snake, Sirius Black is killed by Bellatrix Lestrange, Voldemort returns and fights Dumbledore. Book 7 has the lowest starting happiness of all the books. The wizarding world is in a full blown war. Early chapters include the Death Eaters at Malfoy manor, Hedwig and Mad-Eye Moody dying when transporting Harry from the Dursley's, Voldemort takes over the Ministry of Magic and kills the minister Rufus Scrimgeour. All in all it seems reasonable that this book starts low on happiness.

These happiness scores are subject to the same standard deviations as the above.

<img src="/images/book_happiness_trendlines_std.png" width="700" /> 

With this overlay it is even more clear that the sentiment analysis falls a little short with the limited available data.
</h3>

<h2>Word Shifts for Select Chapters</h2>
<div class="line1"></div>
<h3>

Now lets look closer at some of the chapters that stand out for their high or low happiness scores. We do this with word shifts like the ones they use on https://hedonometer.org/timeseries/en_all .

We compute the word shifts by comparing 4 select chapters with the 3 chapters that precede them. The below plots show which words are causing the biggest change in happiness score either by being present in the chapter in focus and not present in the previous chapters (full colors) or having been present in the previous chapters but not present in the chapter of focus (faded colors). The blue words have negative happiness scores, the yellow words have positive scores. The size of the bar corresponds to the size of the shift caused by the word.

The chapter where Voldemort is "rebirthed" in a full body and Peter Pettigrew kills Cedric Diggory in book 4 is one of the more negative chapters. 

<img src="/images/word_shift_cedric.png" width="700" /> 

Many of the words associated with this chapter are obviously negative like *kill*, *grave* and *horror*. The happiness scores we use are based on English language in general, and not specifically in the context of Harry Potter. So where the word *lord* might be associated with God and therefore has a very positive score in the labMT dataset, in Harry Potter it is always associated with *Lord Voldemort* and therefore not a positive word at all. This chapter also shows us how the word shifts and happiness scores in general fall short on context. The *infant* that is mentioned in this chapter summary is in fact Lord Voldemort in the shape of *a deformed infant*, and the words *right* and *hand* refer to Pettigrew's hand that he cuts off for the potion. These are all words that brings the happiness score of the chapter up when looked at without context.

Another chapter that scores low on happiness is the one where Bellatrix Lestrange kills Sirius Black.

<img src="/images/word_shift_sirius.png" width="700" /> 

Again obvious words are causing the low score: *dead*, *defeated*, *lost* and *death* amongst others. Interestingly we can see that both the word *forbidden* and the word *forest* were used in previous chapters, but that *forbidden* is negative and *forest* is positive, even if they in the wizarding world refers to the same place: the Forbidden Forest. 

Now lets look at some of the positive chapters. In book 6 they celebrate Christmas at the Burrow after Arthur Weasley has been attacked by the snake Nagini.

<img src="/images/word_shift_christmas.png" width="700" /> 

This chapter is another good example of the lack of context in the word shift analysis. 

This is the full text of the chapter summary from the fandom wiki 

> During the Christmas holidays at the Burrow, Harry tells Ron, his father Arthur Weasley and Remus Lupin what he overheard, but they believe that Snape was trying to find out Malfoy's plan so he could tell Dumbledore. Later, Rufus Scrimgeour visits the Burrow, and requests that Harry appear to work alongside the Ministry, to boost the morale of the public. Harry turns it down, knowing that the Ministry is arresting and imprisoning  innocent people and remembering how they persecuted him last year.

We see that the words *ministry*, *boost* and *innocent* are not positive in the context, but contributes to the positive shift. 

Lastly lets look at another positive chapter: in book 7 when its Harry's birthday.

<img src="/images/word_shift_birthday.png" width="700" /> 

It is the day before Bill and Fleur's *wedding* and Harry's *birthday*. Harry also gets a *kiss* from Ginny. Dumbledore has died and Rufus Scrimgeour is there to read his will and *give* the trio the *gifts* he has left them. All this contributes to the positive shift of the chapter.

Across these chapters we see that, even though it falls short on interpreting context, the happiness scores and word-shifts still do a decent job of categorizing the chapters as more positive or negative when the good or bad thing going on is not subtle i.e. death, murder, Christmas, birthdays and weddings. 

The word shifts are subject to the same challenges as the happiness score plots above; the chapter summaries that we are working with are not very long, and therefore they do not have a lot of words to go on.

</h3>