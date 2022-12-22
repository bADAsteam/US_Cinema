---
layout: default
---
![image](/output/Intro.jpg)

## Abstract

In 1975, the filmmaker Laura Muley highlighted the underrepresentation of women in the film industry and more broadly in visual culture. She introduced the term "male gaze" and allowed people to question the place of women in the cinema industry. The American cinema industry played a strong role on the western society and appears as a good area of study to examine how women's representation has evolved over the period of nearly a century. The study is articulated around two points of view: the director and the audience.

This datastory begins with three datasets from the <strong>CMU Movie Summary Corpus</strong>: the first dataset includes information on 81741 movies from 1888 to 2012, the second dataset features information on the characters who appeared in these movies, and the final dataset includes summaries of 20358 movies in the first dataset.

The central focus of this project is to thoroughly analyze movie summaries, which hold a vast amount of information about movie characters. In addition to examining the <strong> importance </strong> of characters depending on their gender, we will also delve into the difference of presence according to the genre. Through the analysis of summaries, we can gain a deeper understanding of the description of physical and mental characteristics and actions of male and female characters in the film industry, as well as any potential lexical fields that could differentiate them. The idea is to see the evolution of the gender bias over time and to quantify this gap. 
An additional focus is to explore the influence of women characters on the success of a film with the public. From there, it will be possible to put in parallel the point of view of the spectator and the point of view of the director.


## Is Hollwood the most prolific film production ?
```
TEXT
```
{% include world_map.html %}<!--- World map--->
```
TEXT
```
{% include plot4.html %}<!--- Movie by decade--->
```
TEXT
```

## Are women underrepresented?
```
TEXT
```
{% include Charac_decade.html %} <!--- Repartition of male/female actor--->
```
TEXT
```
{% include plot7.html %}<!--- Weighting of male femal charac per decade --->
```
TEXT
```


## Male and female characters: depicted differently by the director?
```
TEXT
```
### Women occupy as many leading roles as supporting roles
```
TEXT
```
{% include Charac_ranking.html %}<!--- Repartition of roles by gender --->
```
TEXT
```
### Not much difference in words at first glance
```
TEXT
```

![image](/output/MF_Adjective_decade.png){:style="display:block; margin-left:auto; margin-right:auto"}<!--- Wordcloud adj --->

![image](/output/MF_Verb_decade.png){:style="display:block; margin-left:auto; margin-right:auto"}<!--- Wordcloud verb --->
```
TEXT
```
### Appearance of a bias by analyzing the lexical fields
```
TEXT
```
{% include plot10.html %}<!--- Interactive bar plot : male adj --->
{% include plot12.html %}<!--- Interactive bar plot : female adj --->
```
TEXT
```
{% include plot11.html %}<!--- Interactive bar plot : male verb --->
{% include plot13.html %}<!--- Interactive bar plot : female verb --->
```
TEXT
```
### A bias that decreases with time
```
TEXT
```
{                        }<!--- Confusion matrix adj --->
{                        }<!--- Confusion matrix verb --->
```
TEXT
```
{% include plot14.html %}<!--- PCA adj --->
{% include plot15.html %}<!--- PCA verb --->
```
TEXT
```



## Do people prefer female characters more?
```
TEXT
```
### ??Conclusion reg??
{                        }<!--- Reg decade--->
{                        }<!--- Reg genre--->
```
TEXT
```

## Conclusion


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