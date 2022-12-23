---
layout: default
---
![image](/output/Intro.jpg)

----------------------------------------------------------------
<!---## Abstract--->

## The background

The term " <strong> male gaze </strong> ", introduced by filmmaker Laura Mulvey in 1975, refers to the way in which the visual arts, particularly film, depict the world and women from a masculine point of view. This perspective is often characterized by an objectifying and sexualizing portrayal of women, which reinforces traditional gender roles and reinforces the dominant power dynamics between men and women. Mulvey's concept of the male gaze has been influential in feminist film theory and has sparked important discussions about women representation in the film industry and broader visual culture. 

The study of the representation of women in film is an important area of inquiry because of the significant role that the film industry plays in shaping cultural norms and values. By examining how <strong>women have been portrayed in film over the past century</strong>, we can better understand the changing attitudes towards gender and representation in society. This can be done by looking at both the <strong>perspective of the director</strong>, who plays a key role in shaping the representation of women on screen, as well as the <strong>perspective of the audience</strong>, who consume and are influenced by these representations. Through this analysis, it is possible to better understand the ways in which the film industry has influenced and been influenced by societal attitudes towards women, and to consider the potential for positive change in the representation of women in film and visual culture.

<strong><i>
How have the perspectives of both directors and audiences impacted the evolution of gender bias in character portrayal in Hollywood movies?
</i></strong>

----------------------------------------------------------------
## Is Hollwood the most prolific movie production ?

This data story starts with three datasets from the <i>CMU Movie Summary Corpus</i> to explore the evolution of gender bias in character portrayal in film. The first dataset includes details on a total of <i>81741 movies</i> spanning from <i>1888 to 2012</i>, while the second dataset provides information on the characters that appear in these films. The final dataset includes <i>summaries of 20358 movies</i> from the first dataset. By analyzing these datasets, we can gain a better understanding of the portrayal of gender bias in film over time and the representation of male and female characters.

Initially, we aim to analyze the distribution of movies across the globe and observe their evolution over time. 

{% include world_map.html %}<!--- World map--->

It appears that the United States accounts for <i>39%</i> of the films in the dataset, while other countries do not exceed <i>10%</i>. This suggests that the United States plays a central role in the global film industry. Taking a step back, it is logical that Hollywood is the biggest movie industry in the world. This is due to the fact that Hollywood has a long history of producing high-quality films that appeal to a wide range of audiences, and it has a strong reputation for innovation and creativity in the film industry.

However, by focusing solely on American cinema, we may be limiting the scope of our analysis and overlooking the influence of other countries on the representation of gender in film. While this approach allows us to examine the <i> portrayal of male and female characters in American cinema</i> in depth, it also means that our findings may not necessarily be representative of the multiplicity of viewpoints present in the global film industry. Therefore, it is important to keep in mind the potential limitations of this study as we analyze the portrayal of gender bias in American cinema.

As a second point we decide to explore the evolution of the <strong>distribution of movies</strong> included in the study across different decades. It will give us insight of the perspectives of directors and audiences over time.

{% include movie_by_year_usa.html %}<!--- Movie by decade--->

The number of movies produced from the end of the 20th century significantly increased, and this trend should be considered when conducting further analysis. Due to the limited number of films produced between 1880 and 1910, we have chosen to exclude this period in our analysis.

----------------------------------------------------------------

## Are women underrepresented?
Upon initial analysis, it may not be immediately evident whether there is a difference in the amount of screen time given to male and female actors. To uncover this disparity, we move to look at the total number of male and female actors in each decade.


{% include Repartition_of_male_and_female_main_actor_per_decade.html %} <!--- Repartition of male/female actor--->

In each decade, there are fewer female actors than male actors, and this trend does not appear to change over time. The table below illustrates the evolution of the percentage of female actors in films:

|1910-1920|1920-1930|1930-1940|1940-1950|1950-1960|1960-1970|1970-1980|1980-1990|1990-2000|2000-2010|
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|   39 %  |   36 %  |   31 %  |   26 %  |   23 %  |   26 %  |   25 %  |    30 % |   31 %  |   33 %  |

The percentage of women on screen has followed a U-shaped pattern over the past century. It decreased slightly from 1910 to 1980, reaching a low of around 30% during this time period. However, it has been on the rise since 1980. The period between 1950 and 1980 saw the lowest representation of women.


----------------------------------------------------------------

## Male and female characters: depicted differently by the director?

As says before we wanted to look at the "director point of view". For this, we analyzed the summaries of <i>2358</i> American movies from the <i>CMU Movie Summary Corpus</i>. Using natural language processing algorithms, we extracted information about each character in the movies, including their gender and the adjectives and verbs associated with their characterizations. Results suggest that adjectives are a good representation of the physical and mental characteristics of characters, while verbs are a good representation of their actions. This process was conducted for each decade between <i>1910 and 2010</i>. By analyzing the data in this way, we were able to gain insight into the importance and characteristics of male and female characters in each film and how these factors have changed over time.

### Action movies are the black sheep

To measure the importance of each character in the film, we defined a <strong> weighting factor </strong> as the number of references to the character in the summary divided by the total number of character references. We then calculated the mean weighting factor for all female characters in each film and found that it varied little between decades, but differed significantly between genres, as shown in the chart below:

{% include weighting_male_female_genre_decade.html %}<!--- Weightin male femal charac per decade and genre --->

Action and adventure films often have a low percentage of female characters, typically not exceeding 30%. In contrast, romance and drama films tend to have a higher representation of women, with more than 40% of their characters being female.

### Women occupy as many leading roles as supporting roles
To go further the weighting factors of male and female characters, we also quantified the importance of characters by ranking them based on the number of references to them in the summary. 

{% include Repartition_of_roles_per_gender.html %}<!--- Repartition of roles by gender --->

Women are equally likely to occupy leading roles as secondary roles, while men are more likely to have leading roles than any other type of supporting role. This suggests that there is a gender imbalance in the distribution of leading and supporting roles in films.


### Not much difference in words between men and women at first glance

<center>
  <strong> Adjectives </strong>
</center>

![image](/output/MF_Adjective_decade.png){:style="display:block; margin-left:auto; margin-right:auto"}<!--- Wordcloud adj --->

![image](/output/MF_Verb_decade.png){:style="display:block; margin-left:auto; margin-right:auto"}<!--- Wordcloud verb --->

Upon examining the most commonly used adjectives and verbs associated with male and female characters, we did not find a clear difference between the two groups. We did notice that certain words, such as ```"old," "young," "go," "find," and "tell,"``` were used equally as often in relation to female and male characters. This suggests that there may not be a significant gender-based difference in the way male and female characters are characterized in films using these specific adjectives and verbs. 

### Appearance of a bias by analyzing the lexical fields
While analyzing individual words can provide useful insights, examining lexical fields allows for a more comprehensive and standardized comparison of films across different decades. To do this, we calculated the relative scores for <i>194 lexical fields</i> for each decade.


![image](/output/Lexical_fields_for_Adjectives.png){:style="display:block; margin-left:auto; margin-right:auto"}


In order to focus on gender-specific language, we excluded lexical fields that were common to both male and female characters and instead highlighted those that were specific to one gender. This approach allowed us to more accurately compare the language used to describe male and female characters across different time periods.

{% include male_adjectives.html %}<!--- Interactive bar plot : male adj --->
{% include female_adjectives.html %}<!--- Interactive bar plot : female adj --->

{% include male_verbs.html %}<!--- Interactive bar plot : male verb --->
{% include female_verbs.html %}<!--- Interactive bar plot : female verb --->

It is quite clear that lexical fields such as ```"kill," "heroic," "fight," and "negative_emotion"``` are more commonly associated with men, while lexical fields such as ```"beauty," "attractive," "appearance," and "pain"``` are more commonly associated with women. Additionally, some less expected lexical fields, such as ```"emotional"``` for men and ```"shape_and_size"``` for women. This suggests that there may be some gender-based differences in the way male and female characters are characterized in films using specific language. 


### A bias that decreases with time 

Now that we have observed differences in the way male and female characters are characterized in film using specific language, it would be interesting to further investigate the factors that contribute to these differences and whether they have changed over time.

To identify the most distinguishing features of each decade, we applied a random forest algorithm and selected the most important features based on their importance scores. In addition, we tested the predictive quality of the model by generating confusion matrices for verbs and adjectives, over the decades.

{% include Confusion_matrix_for_adjectives.html %}<!--- Confusion matrix adj interactif --->
{% include Confusion_matrix_for_verbs.html %}<!--- Confusion matrix verb interactif --->

Two notable observations can be made from our analysis:

* The accuracy of adjectives in differentiating male and female characters remains fairly constant between <i>1930 and 1970</i> ( between <i>96% and 100%</i> ), but decreases thereafter until reaching <i>80%</i> in <i>2000-2010</i>. This suggests that it becomes increasingly difficult to distinguish between male and female characters based on their physical or mental descriptions as time progresses. In contrast, the accuracy of verbs in differentiating male and female characters does not show a clear trend over time, with no clear pattern observed across decades. 

* It is interesting to notice that there are more instances of men being classified as women (7.9%) than vice versa (5.5%).

These findings highlight the potential changes in language use in portraying gender bias in film over time, but further research is needed to fully understand these dynamics.

After identifying the important features, we used them to reduce the dimensionality of the vectors. To further reduce the dimensionality, we applied a <i>Principal Component Analysis</i> (PCA) on each decade to compare the distance between male and female character points. This will allow us to visualize the relationships between male and female characters and see how they have changed over time.

{% include PCA_2D_projection_of_10_most_important_features_per_decade_for_Adjectives.html %}<!--- PCA adj --->

{% include PCA_2D_projection_of_10_most_important_features_per_decade_for_verbs.html %}<!--- PCA verb --->

When analyzing the distance between male and female characters using adjectives, we found that it fluctuated between <i>1930</i> and <i>1970</i>, making it difficult to draw any meaningful conclusions. However, after <i>1970</i>, the distance between male and female characters significantly decreased, indicating that adjectives became less divisive over time. Therefore, it appears that the physical and mental descriptions of men and women have become more similar since 1970. In contrast, we did not observe any clear trend when using verbs to analyze the distance between male and female characters, making it difficult to reach a definitive conclusion about the use of verbs in portraying gender bias.

The role of the director in setting the characters and shaping the overall tone and themes of a film cannot be overstated. The director is responsible for interpreting the script and bringing it to life on screen, and this includes the development of the characters and their motivations. In this sense, the director has a significant influence on the portrayal of gender and any biases that may be present in the film.
However, it is also important to consider the audience when analyzing a film for gender bias. The film industry is a business, and filmmakers often have to consider the preferences and expectations of their audience when making creative decisions. This can sometimes lead to the perpetuation of gender stereotypes or biases in order to appeal to a wider audience or to meet certain commercial expectations.

----------------------------------------------------------------

## Do people prefer female hero more?
In order to understand the audience's interest in female characters as main protagonists, we collected data on the ratings given to films by audiences from Wikidata. By examining the relationship between these ratings and the occupation of main roles by women, we can gain valuable insight into the audience's preferences.


### No preference observed 
To investigate the relationship between the gender of the hero and the review score of the movie, we proceeded to a matching of male and female hero films and conducted a linear regression analysis.

```

           | Coefficient value |  p-value                       
--------------------------------------------
Intercept  |       52.9084     |   0.000 
-------------------------------------------- 
gender     |       1.9270      |   0.125     
--------------------------------------------

 Regression Results 
============================================
| Intercept | Value of the coeffci |1930-1940|1940-1950|1950-1960|1960-1970|1970-1980|1980-1990|1990-2000|2000-2010|
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|   gender  |   36 %  |   31 %  |   26 %  |   23 %  |   26 %  |   25 %  |    30 % |   31 %  |   33 %  |
```

Based on the results of the linear regression analysis, there is no significant relationship between the gender of the hero and the review score of the movie. The p-value for the gender variable in the model is 0.125, which is greater than the commonly used alpha level of 0.05. This suggests that there is insufficient evidence to reject the null hypothesis that the gender of the hero has no effect on the review score.
It appears that the public does not show a preference for films with either a female or male hero.


## Conclusion

In conclusion, the perspectives of directors have had a <strong>significant impact on the evolution of gender bias</strong> in character portrayal in Hollywood movies. Directors (eg summaries) have the power to create and shape the characters and storylines of films, and their personal beliefs and biases can influence the way that gender is portrayed on screen. But, it is important to strike a balance between the creative vision of the director and the needs and preferences of the audience (eg review scores), while also being mindful of the potential impact of the film on societal attitudes and beliefs about gender. Indeed the <strong>presence of female character does not influence that much the audience</strong>. It could be so many other fact that a movie has a gradereview score (eg blockbuster, word-of-mouth...)


----------------------------------------------------------------
----------------------------------------------------------------
## Meet our team of data scientists

<div class="row">
  <div class="column">
        <img src="/US_Cinema/output/AntoineLap.jpeg" alt="image1" style="width:100%">
        <p><strong>Antoine Laperriere</strong><br> Data Explorer</p>
    </div>
    <div class="column">
        <img src="/US_Cinema/output/Benoit_gaudiot.png" alt="image2" style="width:100%">
        <p><strong>Benoit Gaudiot</strong><br> Data Analyst </p>
  </div>
<div class="column">
    <img src="/US_Cinema/output/Nathan.jpg" alt="image1" style="width:100%">
    <p><strong>Nathan Paillou</strong><br> Data Analyst</p>
</div>
<div class="column">
    <img src="/US_Cinema/output/RomainBezeaud.jpeg" alt="image2" style="width:100%">
    <p><strong>Romain Bezeaud</strong><br> Web developper</p>
</div>
</div>