---
layout: default
---
![image](/output/Intro.jpg)

----------------------------------------------------------------
<!---## Abstract--->

The term "male gaze," introduced by filmmaker Laura Mulvey in 1975, refers to the way in which the visual arts, particularly film, depict the world and women from a masculine point of view. This perspective is often characterized by an objectifying and sexualizing portrayal of women, which reinforces traditional gender roles and reinforces the dominant power dynamics between men and women. Mulvey's concept of the male gaze has been influential in feminist film theory and has sparked important discussions about the representation of women in the film industry and broader visual culture.

The study of the representation of women in film is an important area of inquiry because of the significant role that the film industry plays in shaping cultural norms and values. By examining how <strong>women have been portrayed in film over the past century</strong>, we can better understand the changing attitudes towards gender and representation in society. This can be done by looking at both the <strong>perspective of the director</strong>, who plays a key role in shaping the representation of women on screen, as well as the <strong>perspective of the audience</strong>, who consume and are influenced by these representations. Through this analysis, it is possible to better understand the ways in which the film industry has influenced and been influenced by societal attitudes towards women, and to consider the potential for positive change in the representation of women in film and visual culture.

<strong><i>
How have the perspectives of both directors and audiences impacted the evolution of gender bias in character portrayal in film?
</i></strong>



----------------------------------------------------------------

## Is Hollwood the most prolific film production ?

This data story utilizes three datasets from the <i>CMU Movie Summary Corpus</i> to explore the evolution of gender bias in character portrayal in film. The first dataset includes details on a total of <i>81741 movies</i> spanning from <i>1888 to 2012</i>, while the second dataset provides information on the characters that appear in these films. The final dataset includes <i>summaries of 20358 movies</i> from the first dataset. The plot below illustrates the global distribution of the films included in the dataset. By analyzing these datasets, we can gain a better understanding of the portrayal of gender bias in film over time and the representation of male and female characters.

{% include world_map.html %}<!--- World map--->

Our analysis shows that the United States accounts for <i>39%</i> of the films in the dataset, while other countries do not exceed <i>10%</i>. This suggests that the United States plays a central role in the global film industry. However, by focusing solely on American cinema, we may be limiting the scope of our analysis and overlooking the influence of other countries on the representation of gender in film. While this approach allows us to examine the <i>portrayal of male and female characters in American cinema</i> in depth, it also means that our findings may not necessarily be representative of the multiplicity of viewpoints present in the global film industry. Therefore, it is important to keep in mind the potential limitations of this study as we analyze the portrayal of gender bias in American cinema.
Our study also aims to understand the evolution of the perspectives of directors and audiences over time. To gain a fuller understanding of these dynamics, it is important to consider the <i>distribution of movies</i> included in the study across different decades:

{% include plot4.html %}<!--- Movie by decade--->

It is quite clear that there are many more films per decade from 2000, it will be necessary to take this into account for further analysis.

----------------------------------------------------------------
## Are women underrepresented?
Upon initial analysis, it may not be immediately evident whether there is a difference in the amount of screen time given to male and female actors. To uncover this disparity, our study examines the total number of male and female actors in each decade by comparing the number of speaking roles and the amount of screen time they are given.
<!---C'est pas le graph de repartition des main roles ca --->

{% include Charac_decade.html %} <!--- Repartition of male/female actor--->

Our analysis shows that in each decade, there are fewer female actors than male actors, and this trend does not appear to change over time. The table below illustrates the evolution of the percentage of female actors in films from the <i>1930s to the 2010s</i>:

| 1930-1940 | 1940-1950 | 1950-1960 | 1960-1970 | 1970-1980 | 1980-1990 | 1990-2000 | 2000-2010 |
|-----------|-----------|-----------|-----------|-----------|-----------|-----------|------------|
|    36 %   |    32 %   |    30 %   |    31 %   |    30 %   |    33 %   |    34 %   |    36 %    |

As we can see, the percentage of female actors remains fairly constant, hovering between <i>30%</i> and <i>36%</i>. However, we do see a slight increase in the percentage of female actors in each decade starting from the 1980s. This trend suggests that although there has been some progress in increasing the representation of women in film, there is still a long way to go in achieving gender parity in the industry.

----------------------------------------------------------------
## Male and female characters: depicted differently by the director?
We analyzed the summaries of <i>2358</i> American movies from the <i>CMU Movie Summary Corpus</i>. Using natural language processing algorithms, we extracted information about each character in the movies, including their gender and the adjectives and verbs associated with their characterizations. Our analysis suggests that adjectives are a good representation of the physical and mental characteristics of characters, while verbs are a good representation of their actions. This process was conducted for each decade between <i>1930 and 2010</i>. By analyzing the data in this way, we were able to gain insight into the importance and characteristics of male and female characters in each film and how these factors have changed over time.

### Women occupy as many leading roles as supporting roles
To measure the importance of each character in the film, we defined a weighting factor as the number of references to the character in the summary divided by the total number of character references. We then calculated the mean weighting factor for all female characters in each film and found that it varied little between decades, but differed significantly between genres, as shown in the chart below:
{% include plot9.html %}<!--- Weightin male femal charac per decade and genre --->

In addition to go further the weighting factors of male and female characters, we also quantified the importance of characters by ranking them based on the number of references to them in the summary. 

{% include Charac_ranking.html %}<!--- Repartition of roles by gender --->

Our analysis shows that women are equally likely to occupy leading roles as secondary roles, while men are more likely to have leading roles than any other type of supporting role. This suggests that there is a gender imbalance in the distribution of leading and supporting roles in films.


### Not much difference in words at first glance

![image](/output/MF_Adjective_decade.png){:style="display:block; margin-left:auto; margin-right:auto"}<!--- Wordcloud adj --->

![image](/output/MF_Verb_decade.png){:style="display:block; margin-left:auto; margin-right:auto"}<!--- Wordcloud verb --->
The most used adjectives and verbs does not display an obvious difference between men and women. Some words such as ```'old', 'young', 'go', 'find' and 'tell'``` appears as used for women than for men.

Upon examining the most commonly used adjectives and verbs associated with male and female characters, we did not find a clear difference between the two groups. We did notice that certain words, such as ```"old," "young," "go," "find," and "tell,"``` were used equally as often in relation to female and male characters. This suggests that there may not be a significant gender-based difference in the way male and female characters are characterized in films using these specific adjectives and verbs. 

### Appearance of a bias by analyzing the lexical fields
While analyzing individual words can provide useful insights, examining lexical fields allows for a more comprehensive and standardized comparison of films across different decades. To do this, we calculated the scores for 194 lexical fields for each decade. In order to focus on gender-specific language, we excluded lexical fields that were common to both male and female characters and instead highlighted those that were specific to one gender. This approach allowed us to more accurately compare the language used to describe male and female characters across different time periods.

{% include plot10.html %}<!--- Interactive bar plot : male adj --->
{% include plot12.html %}<!--- Interactive bar plot : female adj --->

{% include plot11.html %}<!--- Interactive bar plot : male verb --->
{% include plot13.html %}<!--- Interactive bar plot : female verb --->

It is quite clear that lexical fields such as ```"kill," "heroic," "fight," and "negative_emotion"``` are more commonly associated with men, while lexical fields such as ```"beauty," "attractive," "appearance," and "pain"``` are more commonly associated with women. Additionally, some less expected lexical fields, such as ```"shape_and_size" and "childish"``` for men and ```"white_collar_job" and "royalty"``` for women. This suggests that there may be some gender-based differences in the way male and female characters are characterized in films using specific language. 

### A bias that decreases with time
Now that we have observed differences in the way male and female characters are characterized in film using specific language, it would be interesting to further investigate the factors that contribute to these differences and whether they have changed over time. To identify the most distinguishing features of each decade, we applied a random forest algorithm and selected the most important features based on their importance scores. In addition, we tested the predictive quality of the model by generating confusion matrices for verbs and adjectives. 
{% include plot15.html %}<!--- Confusion matrix adj interactif --->
{% include plot16.html %}<!--- Confusion matrix verb interactif --->

Two notable observations can be made from our analysis:
-The accuracy of adjectives in differentiating male and female characters remains fairly constant between 1930 and 1970 (between 96% and 100%), but decreases thereafter until reaching 80% in 2000-2010. This suggests that it becomes increasingly difficult to distinguish between male and female characters based on their physical or mental descriptions as time progresses. In contrast, the accuracy of verbs in differentiating male and female characters does not show a clear trend over time, with no clear pattern observed across decades. 
- The false p and false n ??????????
These findings highlight the potential changes in language use in portraying gender bias in film over time, but further research is needed to fully understand these dynamics.


After identifying the important features, we used them to reduce the dimensionality of the vectors. To further reduce the dimensionality, we applied principal component analysis (PCA) on each decade to compare the distance between male and female character points. This will allow us to visualize the relationships between male and female characters and see how they have changed over time.

{% include plot14.html %}<!--- PCA adj --->
{% include plot15.html %}<!--- PCA verb --->

When analyzing the distance between male and female characters using adjectives, we found that it fluctuated between 1930 and 1970, making it difficult to draw any meaningful conclusions. However, after 1970, the distance between male and female characters significantly decreased, indicating that adjectives became less divisive over time. In contrast, we did not observe any clear trend when using verbs to analyze the distance between male and female characters, making it difficult to reach a definitive conclusion about the use of verbs in portraying gender bias.



The role of the director in setting the characters and shaping the overall tone and themes of a film cannot be overstated. The director is responsible for interpreting the script and bringing it to life on screen, and this includes the development of the characters and their motivations. In this sense, the director has a significant influence on the portrayal of gender and any biases that may be present in the film.
However, it is also important to consider the audience when analyzing a film for gender bias. The film industry is a business, and filmmakers often have to consider the preferences and expectations of their audience when making creative decisions. This can sometimes lead to the perpetuation of gender stereotypes or biases in order to appeal to a wider audience or to meet certain commercial expectations.



----------------------------------------------------------------
## Do people prefer female characters more?
In order to understand the audience's interest in female characters as main protagonists, we collected data on the ratings given to films by audiences from Wikidata. By examining the relationship between these ratings and the occupation of main roles by women, we can gain valuable insight into how the audience's preferences for female heroes have changed over time. This analysis will allow us to better understand the representation of women in film and how it has evolved over time.
### ??Conclusion reg??
{                        }<!--- Reg decade--->
{                        }<!--- Reg genre--->
```
TEXT
```
----------------------------------------------------------------
## Conclusion
It is important to strike a balance between the creative vision of the director and the needs and preferences of the audience, while also being mindful of the potential impact of the film on societal attitudes and beliefs about gender. It is possible to create compelling and meaningful films that challenge gender biases and stereotypes, while still being commercially successful.
We observed that ???????
----------------------------------------------------------------



















A METTRE DANS README:
The central focus of this project is to thoroughly analyze movie summaries, which hold a vast amount of information about movie characters. In addition to examining the <strong> importance </strong> of characters depending on their gender, we will also delve into the difference of presence according to the genre. Through the analysis of summaries, we can gain a deeper understanding of the description of physical and mental characteristics and actions of male and female characters in the film industry, as well as any potential lexical fields that could differentiate them. The idea is to see the evolution of the gender bias over time and to quantify this gap. 
An additional focus is to explore the influence of women characters on the success of a film with the public. From there, it will be possible to put in parallel the point of view of the spectator and the point of view of the director.


|:-------------------------------------------------------------------------------------------------------------------------------------------
|:-------------------------------------------------------------------------------------------------------------------------------------------

## Do people prefer female characters more?

Country                      |	code |	Number_of_movie |	Percent | Number of act | Male acting | Female acting |
|:---------------------------|:------|:-----------------|:----------|:--------------|:------------|:--------------|	
['United States of America'] |	USA	 | 34408	        | 39.806106	| 226169        | 152713      | 73456         |
['India']                    |	IND  |	8411	        | 9.730561  | 45729         | 30024       | 15705         |	
['United Kingdom']           |	GBR  |	7868	        | 9.102373  | 48592         | 32837       | 16183         |
['France']                   |	FRA	 | 4395	            | 5.084510  | 25429         | 16183       | 9246          |	
['Italy']                    |	ITA	 | 3163	            | 3.659228	| 14750         | 9740        | 5010          |
...                          |	...	 | ...	            | ...	    | ...           | ...         | ...           |
['Republic of China']        |	CHN	 | 1	            | 0.001157  | 3             | 2           | 1             |
['Macau']                    |	MAC	 | 1	            | 0.001157	| 3             | 1           | 2             |
['Palestinian Territories']  |	PSE	 | 1	            | 0.001157	| 0             | 0           | 0             |


{% include world_map.html %}

Thanks to a preliminary study, it has been chosen to focus on American movies in the global cinema industry. This focus is appropriate for this case because Hollywood has produced almost half of the movies in the dataset (see world map above) and has the largest pool of acting talent. 

{% include plot4.html %}<!--- Movie by decade--->


## Are women underrepresented?
The study aims to examine the evolution of female characters as depicted by movie directors. One way to do this is by analyzing summaries of films, as they often contain information about characters and their attributes. This can provide insight into how women have been portrayed and represented in films over time, and how this has changed or evolved. It is important to approach this analysis objectively and consider multiple perspectives, rather than relying on personal opinions or biases.


Here, the objective was to locate and analyze the characters within the summaries in order to determine the main character. A Machine Learning algorithm is used to extract all characters from summaries by identifying and linking pronouns to their corresponding names. This process results in a list of characters for each movie, which is then ranked to identify the main character. It also make differenciation between male and female character.

{% include Charac_ranking.html %}

### Character Repartition by Decade
As part of the analysis, the number of male and female characters was tracked over time to gain a better understanding of their evolution. The goal was to determine if the number of female characters was approaching the number of male characters.

{% include Charac_decade.html %}

{% include plot6.html %}<!--- Number characters by decade --->

{% include plot7.html %}<!--- Weighting of male femal charac per decade --->

This preliminary analysis of summaries provides a quick overview of the subject matter. The main finding is that the number of female characters is roughly half the number of male characters, and there is not a clear trend over time beyond an overall increase in the number of characters. It is worth noting that, while the proportion of female characters increases after the top four characters in a movie, it is still lower than the number of male characters. 

This initial analysis is a necessary first step in gaining a deeper understanding of summaries before moving on to a more complex analysis of the characteristics that define a character.

## What makes a character unique?

Preliminary exploration of the summaries has simplified the analysis of character. The ML algorithm changes all pronouns to the names they are linked to. As a result, a NLP was conducted on all summaries to understand how characters are characterized, resulting in a list of adjectives and verbs summarized by a mean score.

### What describes a character ?
To begin characterizing a character, the most commonly used adjectives and verbs are analyzed and compiled based on their frequency in summaries. The size of each adjective or verb corresponds to its frequency.

#### Adjective link to a character
![image](/output/MF_Adjective_decade.png){:style="display:block; margin-left:auto; margin-right:auto"}
#### Verb link to a character
![image](/output/MF_Verb_decade.png){:style="display:block; margin-left:auto; margin-right:auto"}

### Normalization of character description
It is difficult to differentiate men and women only based on words. This might be due to the significant number of different words. In order to reduce the scope of the data, we chose to analyse lexical the fields. From this, we normalize the data to 194 features (lexical fields) which allows to compare between men and women, also between decades.

#### Adjective normalization
![image](/output/Adj_frequency.png){:style="display:block; margin-left:auto; margin-right:auto"}
#### Verb normalization
![image](/output/Verbs_frequency.png){:style="display:block; margin-left:auto; margin-right:auto"}

Normalization of the verbs shows that the most frequently used verbs are the same for both male and female characters in the movie. These verbs describe the <i>actions taken</i> by the characters rather than their characteristics or personality traits.

Furthermore, the normalization of adjectives also reveals a similarity between males and females for the first few adjectives, which pertain to age ("children, youth, ancient"). However, as the list continues, the adjectives begin to differentiate and characterize males and females, such as <i>"violent," "attractive," "wealthy," and "beautiful</i>.

In order to have a better understanding of the characteristics that are typically associated with male and female characters in movies, we found it interesting to examine the inverse intersection of both male and female normalization adjectives (e.g. verbs that are typically used to describe male and female characters). This will allow us to examine how these characters are typically portrayed in films and how these portrayals may reinforce or challenge societal gender norms.
#### Inverse of the intersect
{% include plot10.html %}<!--- Male most used adj --->
{% include plot12.html %}<!--- Female most used adj --->


{% include plot11.html %}<!--- Male most used verb --->
{% include plot13.html %}<!--- Female most used verb --->

### Predicting a character's gender based on adjectives or verbs
It is possible to predict based on adjectives (e.g. verbs) if a character is male or female. A random forest algorithm was used to classify text samples as male or female. 100 samples were generated for each gender, consisting of 50 randomly selected adjectives or verbs from decade-specific lists of words. These samples were analyzed using a lexical method called empath, resulting in 100 vectors for each gender with 194 features. The labels for the vectors were binary, with <strong>male</strong> represented as <strong>1</strong> and <strong>female</strong> represented as <strong>0</strong>. The random forest algorithm was applied to the resulting 200 vectors, and the importance of each feature was extracted.

```
['independence' 'feminine' 'children' 'sexual' 'youth' 'ancient'
 'dominant_personality' 'achievement' 'timidity' 'strength']
```

```
['traveling' 'family' 'speaking' 'movement' 'wedding' 'communication'
 'art' 'giving' 'vacation' 'order']
 ```

![image](/output/Acc_adj.png){:style="display:block; margin-left:auto; margin-right:auto"}

![image](/output/ACC_verb.png){:style="display:block; margin-left:auto; margin-right:auto"}

To simplify the understanding of the result we decide to do a PCA to 

{% include plot14.html %}<!--- PCA adj --->
{% include plot15.html %}<!--- PCA verb --->

## How does the genre of a movie influence the development of its characters?

### Genre Repartition by Decade
In parallel to analyzing the evolution of characters, we also examined whether the genre of the movie had an impact on the representation of female characters. To do this, we conducted a complementary analysis on the evolution of genres over the decade.

{% include Genre_decade.html %}
{% include plot5.html %}<!--- Number movies by genre and decade --->
{% include plot8.html %}<!--- Weighting of male female charac per genre --->
{% include plot9.html %}<!--- Weightin male femal charac per decade and genre --->

## Comparison to public sentiment 
As a final analysis we wonder

### Public source

### Linear regression

## Conclusion