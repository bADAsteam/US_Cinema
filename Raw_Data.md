---
doc: default
---

[comment]: <> (a reference style link.)

## Uncovering insights from Raw data

 The dataset consists of 42,306 movie plot summaries extracted from Wikipedia, along with aligned metadata extracted from Freebase. This metadata includes information about the movie's box office revenue, genre, release date, runtime, and language.

In addition to this, the dataset also includes character names and information about the actors who portray them, including their gender and estimated age at the time of the movie's release.

We also have a supplement to the dataset in the form of Stanford CoreNLP-processed summaries. This includes all of the plot summaries from above, run through the Stanford CoreNLP pipeline, which includes tagging, parsing, NER, and coref.

### Movie metadata
The movies in this dataset are organized and stored using the following categories:  
```
Wikipedia ovie ID
Freebase movie ID
Movie name
Movie release date
Movie box office revenue
Movie runtime
Movie languages
Movie countires
Movie genres
```

### Character metadata
The Character dataset includes the following categories: Wikipedia movie ID, Freebase movie ID, character name, actor DOB, actor gender, actor height, actor ethnicity, actor name, actor age at movie release, and Freebase character map.

Example of the dataset:
<table>
  <thead>
    <tr>
      <th>Wikipedia Movie ID</th>
      <th>Freebase Movie ID</th>
      <th>Character Name</th>
      <th>Actor DOB</th>
      <th>Actor gender</th>
      <th>Actor height</th>
      <th>Actor ethnicity</th>
      <th>Actor Name</th>
      <th>Actor age at movie release</th>
      <th>Freebase character map</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>54166</td>
      <td>/m/0f4yh</td>
      <td>Dr. Marcus Brody</td>
      <td>1922-05-31</td>
      <td>M</td>
      <td>1.816</td>
      <td></td>
      <td>Denholm Elliott</td>
      <td>59</td>
      <td>/m/02nwzzv</td>
    </tr>
    <tr>
      <td>54166</td>
      <td>/m/0f4yh</td>
      <td>Simon Katanga</td>
      <td>1949-10-20</td>
      <td>M</td>
      <td>1.87</td>
      <td>/m/02w7gg</td>
      <td>George Harris</td>
      <td>31</td>
      <td>/m/02nw_18</td>
    </tr>
    <tr>
      <td>54166</td>
      <td>/m/0f4yh</td>
      <td>Dr. René Belloq</td>
      <td>1943-01-18</td>
      <td>M</td>
      <td>1.77</td>
      <td></td>
      <td>Paul Freeman</td>
      <td>38</td>
      <td>/m/02nwzzg</td>
    </tr>
    <tr>
      <td>54166</td>
      <td>/m/0f4yh</td>
      <td>Major Arnold Toht</td>
      <td>1935-09-28</td>
      <td>M</td>
      <td></td>
      <td></td>
      <td>Ronald Lacey</td>
      <td>45</td>
      <td>/m/02nwzyz</td>
    </tr>
    <tr>
      <td>54166</td>
      <td>/m/0f4yh</td>
      <td>Indiana Jones</td>
      <td>1942-07-13</td>
      <td>M</td>
      <td>1.85</td>
      <td>/m/01qhm_</td>
      <td>Harrison Ford</td>
      <td>38</td>
      <td>/m/0k294p</td>
    </tr>
  </tbody>
</table>

### Summary dataset
This is the summary of Mermaids: The Body Found:

"Two former National Oceanic Atmospheric Administration scientists, after investigating mass stranding of whales, claim to have recorded mysterious underwater noises coming from an unknown source. This sound resembled a sound previously recorded in 1997, called the "bloop" . They recovered 30% of the remains of an unknown creature from inside a great white shark which was said to possess attributes of the human body. They alleged that the marine creature had hands, not fins, and the hip structure of an upright animal. These findings, along with many others led the team to determine that this unknown animal was very closely related to humans a mermaid.
"

## How to treat the data ?

### Data preparation for movie and character analysis
<p> <strong> Movie metadata dataset </strong> <br>
To focus our analysis on the US cinema industry, we first had to exclude all non-US movies. We then wanted to incorporate review scores from wikidata, so we created a mapping dataset with rows containing the freebase ID, wikidata ID, review score, and source of the review score.<br>
After accessing the dataset, we conducted some data exploration and found that the US is the top producer of movies by a large margin.
</p>

<p> <strong> Character metadata dataset </strong> <br>
Upon reviewing the dataset, we discovered that some information was missing or incorrect. The actor gender was incorrect in some cases, and the ethnicity column only contained freebase IDs without labels. We gathered missing values from wikidata and incorporated them into the dataset. The actor age at release was also corrected, as there were some negative values which we replaced with their opposite or with NaN for larger outlier values. Finally, we filtered the dataset to include only US movies.
</p>

<p> <strong> Movie summary dataset </strong> <br>
Movie summary dataset represents a great source of data for analyzing the representation of woman in the cinema industry. It has been decided to perform a pronoun analysis on each summary. The pronoun are separated in two categories: male and female. The occurence of each pronoun is counted and added into a dataframe. The principal and secondary characters are also extracted from the summaries. The occurence of the character's name are counted and the most frequent one is considered to be the principal character. The next step is to identify if the actor behind the character is a male or a female and to extract his name.
</p>

### Analysis 

Encore à remplir, ici je voudrais faire un peu comme une recette de tout ce qu'on a fait sur les données.


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
