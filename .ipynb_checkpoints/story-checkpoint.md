---
layout: page
title: Beer Quest - On Finding the Bobos
subtitle: Looking into the World of Glutenree Beer
cover-img: /assets/figures/Story/Cover_photo_1.png
share-img: /assets/figures/Story/Cover_photo_1.png
author: adarescueteam
---

## Investigation Overview

Our adventure takes place during the 2010s, glutenfree food made a breakthrough in popularity and was much more available in general shops. Interestingly, in France and Belgium, people came up with stereotypes regarding glutenfree consumers and products, describing such a trend as a flash in a pan. One of those stereotypes is about the persona of glutenfree buyers, often described as urban snobbish people who want to distinguish themselves socially by consuming non-usual products, called "Bobo" in European French-speaking areas.

> The international Beer league (IBL) sent us, the renowned elite beer detectives to unveil what was going on with glutenfree beers, study their characteristics and who drink them, and determine if they are a threat to the International Beer Drinker Community (IBDC) like bobos would be (according to the IBL).

To investigate, the IBL has given us two sources of information: datasets from BeerAdvocate and RateBeer websites. Those contains reviews of numerous beers worldwide, including numerical ratings and written comments.

### Identifying the Spatiotemporal Distribution of Glutenfree Beers

As seasoned detectives, and to start our quest, we need to gather all the information relevant to investigate the different aspects of glutenfree beers consumers, and hence whether they are any of those infamous "Bobo"s hidden amongst them.

Glutenfree beers are identified by containing "gluten" in their name. This is not the most effective way to find them, but the IBL did not seem to have a database indicating what beers are glutenfree. This works however for beers from country speaking languages of European origin, as gluten is said "gluten" in French, German, Dutch, and Spanish, but not Italian. These analyses will then be somewhat European-origin centered. Nevertheless, this is also the case for the databases kindly given by the IBL.

This way, we have identified this number of glutenfree beers (duplicates were removed from the total):


<div align="center">
  <table>
    <tr>
      <th>Dataset</th>
      <th>Glutenfree beers</th>
      <th>Non-glutenfree beers</th>
    </tr>
    <tr>
      <td>RateBeer</td>
      <td>213</td>
      <td>396484</td>
    </tr>
    <tr>
      <td>BeerAdvocate</td>
      <td>121</td>
      <td>211688</td>
    </tr>
    <tr>
      <td>Total</td>
      <td>313</td>
      <td>592069</td>
    </tr>
  </table>
</div>

Now that we know glutenfree beers, we can start looking at how they are consummed, this is done in two step:

- Step 1. Analyze the number of reviews given per year for glutenfree beers globally.
- Step 2: Analyze the number of reviews given per year for glutenfree beers as a function of the location.

If we take a look at the amount of reviews for glutenfree beers, we can see that it is clearly increasing. The datasets goes up to August 2017, which explains a lower amount of reviews for 2017.  However, seasoned detectives like us must always stay vigilant: is the reason for this increase because of the increase of the popularity of the websites? Or is it because of the increase of total number of reviews in the dataset? To look at that, we look at the proportion of total reviews that are made on glutenfree beers for each year. With that we are sure: the increase of glutenfree beers reviews is not due to the increase of the total number of reviews in the dataset. The increase in other glutenfree products in early 2010's has then been translated into the beer-drinking world, assuming that the number of reviews is a good proxy to see the consumption of one product. This increase is especially impressive as the proportion of glutenfree triples in 2012! However, this proportion stays low, only reaching 0.2% at most.

![GF_temporal_amount](./assets/figures/Spatiotemporal_analysis/GF_temporal.png)

But, where are those reviews from? We now need to go to investigate the spatial distribution of the glutenfree beers drinker through their beer reviews.

Here we define `ratio` as the ratio of the number of reviews for glutenfree beers to the non-glutenfree beers. For each country, the ratio is a representative of how much present are glutenfree reviews among the total reviews, reflecting the popularity of glutenfree beers in that country.French Guiana and Corsica are associated to the french region, but they are only minorly represented in the dataset of the reviews.

<iframe src="https://jay4biopz.github.io/adarescueteam-beerquest/assets/html/gf_reviews_map.html" height="600px" width="100%" style="border:none;"></iframe>

The size of the human icon represents the number of users, but the size-scaling follows a cubic root function to avoid the dominance of large countries. Whereas the color of the country represent this ratio.

With this analysis, we can see that the ratio is the highest in France, reaching 0.66% of all reviews from France, which is the country known to be the main home of bobos, along with Belgium (ranked 3rd with 0.34%). On the American continent, in Canada the ratio is of 0.28% whereas in the US it is only 0.06%. From this, we can see that countries with high number of glutenfree reviews (e.g. Canada, Denmark, USA) are not always the ones with high glutenfree/non-glutenfree.

<div align="center">
  <table>
    <tr>
      <th>Country</th>
      <th>Rank</th>
      <th>Ratio</th>
      <th>Glutenfree reviews number</th>
    </tr>
    <tr>
      <td>France</td>
      <td>1</td>
      <td>0.006610</td>
      <td>116</td>
    </tr>
    <tr>
      <td>Latvia</td>
      <td>2</td>
      <td>0.003757</td>
      <td>10</td>
    </tr>
    <tr>
      <td>Belgium</td>
      <td>3</td>
      <td>0.003385</td>
      <td>100</td>
    </tr>
    <tr>
      <td>Canada</td>
      <td>9</td>
      <td>0.002826</td>
      <td>799</td>
    </tr>
    <tr>
      <td>Denmark</td>
      <td>17</td>
      <td>0.001504</td>
      <td>409</td>
    </tr>
    <tr>
      <td>USA</td>
      <td>41</td>
      <td>0.000607</td>
      <td>892</td>
    </tr>
  </table>
</div>

However, if we dive into the evolution of the number of glutenfree reviews per country, we can see that different dynamics occur. For the USA, there was a big boom of glutenfree beers in 2012, that then fell down from 2014. Seeing this, we could say that there was a **trend** of glutenfree consumption in the US, that then passed aways as trends do. This is not the case for Canada, that we could think as close culturally to the USA, were a first boom in 2012 was supplied by another increase in 2014 and 2015, and then decreasing immensely after. In Europe, for Belgium, this increase occured in 2013 and stayed relatively constant, even thoug a second increase in 2015 could be seen. In denmark, two waves occured in 2013 and 2016, with an important decrease inbetween. Even though Denmark has way higher number of glutenfree reviews than Belgium, it is worth remenbering that their glutenfree/non-glutenfree ratio is low (a quarter of French one and half of Belgian one). In France, the dynamic is a bit different, as the first wave of glutenfree in 2012 was very dim, and glutenfree consumption increased year-by-year from 2013. This dynamic is then very country-specific, however most top performing country ratio-wise have low number of glutenfree reviews (e.g. Latvia) that doesn't enable a precise analysis.

<div align="center">
<iframe src="https://jay4biopz.github.io/adarescueteam-beerquest/assets/html/spatiotemporal_line_curve.html" height="400px" width="100%" style="border:none;"></iframe>
</div>

Then we can see two main dynamics here: one with one or two big booms in consumption that then decrease a lot, and another one that is more long-lasting and less subject to those booms. This first dynamic can be called a peak trend, changing rapidly, whereas the second one must be driven by longer dynamics, such as the adoption of this kind of beer by a specific social group. However, as this rise in glutenfree reviews is still quite new, especially in France, we advise the IBL to continue monitoring these glutenfree dynamics.

It is important to note that 98% of the people who reviewed glutenfree beers also reviewed beers containing gluten, so do not have to drink glutenfree beers for health reason (or are not strictly prohibiting gluten in their diet). This number is quite surprising, but could be explained because people who have to follow a glutenfree diet are not used to beer-drinking and so would less comment on websites such as BeerAdvocate or RateBeer.

> Our investigation has uncovered some characteristics of what we can call a glutenfree trend. It has exploded in 2012 but not equally in every-country. Some countries still were "highly" consuming glutenfree beers in 2017. Those countries happen to be the ones known to be home of "bobos". However, that might also be a coincidence, and so it is required to take a deeper look before reporting to the IBL.  


### Decoding the Rating Conundrum and Perception of Glutenfree Beers

Most of the reviews posted for glutenfree beers are done by people who have reviewed "normal" beers too. Thus, those reviewers are not gluten-intolerant and must be attracted to glutenfree beer for another reason. Could that reason be a better taste or a better quality of the gluten-free beer? In the International Beer League(IBL) headquarters, corridor rumors say that glutenfree beers are generally worse than "normal" ones. Those rumors might be wrong then. To make this clearer, the IBL asks us to give a clearer view on the glutenfree reviews.

As the reviews metrics (rating, appearance, taste, aroma, palate, overall) are dependent on the dataset used, the RateBeer and BeerAdvocate dataset were analyzed independently. Only Ratebeer results are shown but similar ones were found for BeerAdvocate.

To investigate this, the first things we did was to look at all the reviews metrics throughout the years for both glutenfree and non-glutenfree beers in the RateBeer dataset.

![Reviews_metrics_RB](./assets/figures/MetricsRB.png)

Represented are the mean value of each review metrics +/- SEM per year. For RateBeer, appearance and palate are scored out of 5, aroma and taste are scored out of 10 whereas overall is scored out of 20. The rating score is calculated linearly from the other scores and is out of 5.

From this analysis, it seems that the glutenfree beers are worse from usual beers for all metrics considered. Although those metrics are increasing for glutenfree beers around 2011, when the glutenfree trend was starting for beers, they stay lower than usual beers. It is also interesting to see that those metrics also increase over time, more smoothly, for usual beers. Could the rumors spread in the IBDC HQs be true?

As reliable IBDC investigators, we think it is not clear yet. The beerstyle are very different between glutenfree beers and non-glutenfree ones. One type of beer could be more appreciate, more tasteful or have more aroma than another one. It is then possible that the beerstyle is a confounding factor in this analysis. 

<iframe id="myIframe" src="https://jay4biopz.github.io/adarescueteam-beerquest/assets/html/beer_styles.html" width="100%" height="600px" style="border:none;"></iframe>

To adress this issue, we repeat the same analysis with a subsetted RateBeer dataset that contains the same beerstyle as the glutenfree ratings.

![Reviews_metrics_RB_adjstyle](./assets/figures/MetricsRB_adjustedstyle.png)

No difference is visible between the ratings of the subset adjusted in beerstyle and the original one. We can thus conclude that the difference between glutenfree and conventional beer ratings cannot be explained by a change in the beerstyle. 

The ratings given to glutenfree beers do seem to be lower than the ones for usual beers. There could however be two explanations for this. The first and obvious one is that the glutenfree beers would actually be worse than "normal" beers. Verifying this would require the IBL to send beer experts to objectively rate glutenfree beers. However, beer experts cost a lot of money and, given its political landscape, the IBL does not seem to finance science this much. The second explanation would be that people would have heard the same rumors as the one spreading among the IBL, and would have a made-up mind about glutenfree beers. People would then be harsher in the reviews.

To give better strength to out findings, we think that it is a good idea to investigate the written reviews and see whether how positive or negative they are and whether they show the same dynamic as the numeric ratings. To achieve this, we conduct a sentiment analysis worldwide accross the years. A higher sentiment score describes that a more positive vocabulary was used. We found that the sentiment score was initially higher for glutenfree beer reviews than for other reviews. However, this elevated score quickly decrease to go below the score of non-glutenfree beer reviews. We suspect an initial product hype followed by a decreased sentiment score, stemming from initial optimism for glutenfree beers.

![Sentiment_evolution_over_time](./assets/figures/Sentiment_study/sentiment_evolution_over_time.png)
Mean +/- SEM of the sentiment score for the RB dataset is shown.


**Our conclusion, directed to the IBL, asserts that glutenfree beers indeed exhibit lower performance across all metrics compared to regular beers. This is also visible in the written review, even though a very initial hype could be seen in the first years of glutenfree beers, before the described trends happenned and bobos putatively get implicated. There could however be two explanations for this worse perception of glutenfree beers. The first and obvious one is that the glutenfree beers would actually be worse than "normal" beers. Verifying this would require the IBL to send beer experts to objectively rate glutenfree beers. However, beer experts cost a lot of money and, given its political landscape, the IBL does not seem to finance science this much. The second explanation would be that people would have heard the same rumors as the one spreading among the IBL, and would have a made-up mind about glutenfree beers. This would make people rate harder the glutenfree beers as they were expecting the beer to be worse, thus changing their perception of the beer. To assess this, better means of investigation should be performed.**

> Yet, even though the numeric ratings are lower for glutenfree beers, we boserve that for some countries (France, Belgium), their consumption increased and kept increasing in 2017 . Could this be because people do not seek to drink a good and tasteful beer when trying a glutenfree one, but to distinguish themselves socially? This is actually a characteristic of the "Bobo"s, even more intriguing as France and Belgium are the home of the locally famous "Bobo parisiens" and "Bobo bruxellois".

### Deciphering the Vocabulary used by Glutenfree Beers Drinkers

According to the informations gathered by the IBL spies, one of the distinction of the bobo is their way of speaking. Coming from more culturally and intellectually "heightened" background, their vocabulary would be more rich and "fancy" than regular persons, using words like "floral" or "zestful" naturally to describe tastes. Those infos made us wonder whether there are linguistic distinctions between glutenfree beer drinkers and other beer drinkers, which would be another hint that bobos are among this glutenfree beer drinker community.

This part of the investigation begins by looking at the languages used by the glutenfree beer drinkers.

![EDA_GF_languages](./assets/figures/EDA/EDA_lang_dstrbt_gf.png)

We find that the most represented languages by the glutenfree drinkers are English and French. We will continue our analysis only on those languages, as they are also languages spoken by most members of the investigation team. Each analysis will be performed independently on the reviews in English and the reviews in French.

First, we define a glutenfree user as someone who has reviewed at least one glutenfree beer. We aim at seeing whether those have a different way of speaking than persons who never commented on glutenfree beers. To do so, we will focus on adverbs and adjectives as we think they are the most likely to vary between putative bobos and other persons, and try to cluster the reviewes on the vocabulary used performing a dimensionality reduction with t-SNE.

![t_sne_map](./assets/figures/NLP/tsne_map.png)

We find two things. First, that the former overlap just a little with the latter, which means that the glutenfree users only share a linguistic similarity with a small proportion of the conventional beers users. Second, that the glutenfree users are very close to each other linguistically

As the t-SNE axes are not directly interpretable, we wanted to use the text data to better characterize the differences between a glutenfree and a conventional user. That is why we needed to go deeper in the analysis of the vocabulary that each of the two uses. Enter our guiding light: ‘El Logressor’ (a logistic regression classifier), our hope in unraveling this mystery. 
Indeed, El Logressor is a logistic classifier that predicts whether or not a person is a glutenfree user based on the adjectives and adverb he uses. 

El Logressor proved to be a formidable weapon: with a remarkable accuracy of 94%, it was able to distinguish between the glutenfree and conventional consumers.  
However, it can not distinguish between the "Bobo"s and the "non-Bobo"s amongst the glutenfree users. 

As our investigation zeroed in on a cohort possibly standing out amidst the realm of glutenfree consumers, our certainty grew—we sensed we were threading the right path. Our findings highlighted a captivating set of users, yet the enigmatic ‘Bobo’s’ remained evasive, slipping beyond our reach. That is why we needed to go deeper in the analysis of the vocabulary, separating the glutenfree users' vocabulary from the conventional beer users to better highlight the fluten-free users. This would then enable us to see if there is Bobo's amongst the glutenfree users. 

Enter our second guiding light: the glutenfree bag of words.
In fact, this 'BoW' contains words that were only used by glutenfree users in their reviews. 

![wordcloud](./assets/figures/NLP/wordcloud.png)

We then analysed their fanciness by asking our Special agent Chatgpt to rank the fanciness of each word in that BoW.

![fanciness](./assets/figures/NLP/fanciness.png)

Our analysis shows that glutenfree user and conventional beer user have different linguistics particularities. However, it seems that glutenfree users are not really 'BOBO' in the sense that the specific adjectives and adverbs that glutenfree user employed are not really fancy. Some of them are not very commom such as the French word 'remous', or the word 'gibbous' in english, but not necessarily fancy. The main difficulty we face here is to have an objective metric to describe fanciness. 




### Conclusion
We hereby present our final report to the IBL. 
Indeed, we have seen that glutenfree beers are less appreciated than conventional beers. This leads us to investigate why do glutenfree beer drinkers continue to drink them. We found that these consumers mostly are not allergic to gluten since they consume also conventional beers. So we investigated what drives them to drink glutenfree beers. Our hypothesis was that part of these persons were in fact the bobos, who drink glutenfree beers to distinguish themselves from other people in the society. To access if glutenfree users were indeed bobo, we made a text analysis to evaluate the fanciness of the vocabolary used by glutenfree users.

Finally, We did find a particulaity of gluten-free users compared to their conventional counterparts, however, we can not conclude with certainty that that difference was due to the actions of the Bobos.

