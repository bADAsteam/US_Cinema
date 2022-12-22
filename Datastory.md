---
layout: default
---
![image](/output/Intro.jpg)

# Introduction

In 1975, the filmmaker Laura Muley highlighted the underrepresentation of women in film industry and more broadly in visual culture. She introduced the term "male gaze" and allow people to question the place of women in the cinema industry. The American cinema industry played a strong role on the western society and appears as a good area of study to examine how women's representation has changed over the period of nearly a century.

This datastory begins with a trio of datasets from the <strong>CMU Movie Summary Corpus</strong>: the first dataset includes information on 81741 movies from 1915 to 2012, the second dataset features information on the characters who appeared in these movies, and the final dataset includes summaries of the movies in the first dataset

The central focus of this project is to thoroughly analyze movie summaries, which hold a vast amount of information about the films. In addition to examining the <strong>main character</strong> and other key details, we will also delve into the representation of <strong>male and female actors in the movies</strong>. Through the analysis of summaries, we can gain a deeper understanding of the roles and portrayal of male and female characters in the film industry, as well as any potential biases or trends in the depiction of these characters.


How has the women places evolves in the US cinema industry ? Does the cinema represent more men than women and has there been a change over the years ? Has the role played by woman and the attributes of their characters evolves through the year ? And finally how the place of actresses evolve for the public ?

Given all of these factors, several questions come to mind:

* Is it possible to define the main character from a summary ?
* Does the genre of the movie impacts how women are represented ?
* 

## Project pipeline

## The world of cinema through American eyes ?

Thanks to a preliminary study, it has been chosen to focus on American movies in the global cinema industry. This focus is appropriate for this case because Hollywood has produced half of the movies made worldwide and has the largest pool of acting talent.

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
{% include plot4.html %}<!--- Movie by decade--->
## What can a director's point of view reveal in a summary ?
The study aims to examine the evolution of female characters as depicted by movie directors. One way to do this is by analyzing summaries of films, as they often contain information about characters and their attributes. This can provide insight into how women have been portrayed and represented in films over time, and how this has changed or evolved. It is important to approach this analysis objectively and consider multiple perspectives, rather than relying on personal opinions or biases.

### Who are the characters that can be found within summaries?
Here, the objective was to locate and analyze the characters within the summaries in order to determine the main character. A Machine Learning algorithm is used to extract all characters from summaries by identifying and linking pronouns to their corresponding names. This process results in a list of characters for each movie, which is then ranked to identify the main character. It also make differenciation between male and female character.

{% include Charac_ranking.html %}

### Character Repartition by Decade
As part of the analysis, the number of male and female characters was tracked over time to gain a better understanding of their evolution. The goal was to determine if the number of female characters was approaching the number of male characters.

{% include Charac_decade.html %}

{% include plot6.html %}<!--- Number characters by decade --->

{% include plot7.html %}<!--- Weighting of male femal charac per decade --->

This preliminary analysis of summaries provides a quick overview of the subject matter. The main finding is that the number of female characters is roughly half the number of male characters, and there is not a clear trend over time beyond an overall increase in the number of characters. It is worth noting that, while the proportion of female characters increases after the top four characters in a movie, it is still lower than the number of male characters. 

This initial analysis is a necessary first step in gaining a deeper understanding of summaries before moving on to a more complex analysis of the characteristics that define a character.

## How are character are linked to ?

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

{% include plot10.html %}<!--- Male most used adj --->
{% include plot12.html %}<!--- Female most used adj --->


{% include plot11.html %}<!--- Male most used verb --->
{% include plot13.html %}<!--- Female most used verb --->

## Does the genre have an impact ob the result ?

### Genre Repartition by Decade
In parallel to analyzing the evolution of characters, we also examined whether the genre of the movie had an impact on the representation of female characters. To do this, we conducted a complementary analysis on the evolution of genres over the decade.

{% include Genre_decade.html %}
{% include plot5.html %}<!--- Number movies by genre and decade --->
{% include plot8.html %}<!--- Weighting of male female charac per genre --->
{% include plot9.html %}<!--- Weightin male femal charac per decade and genre --->
## Comparison to public sentiment 
## Use grade on each movie

## Conclusion




