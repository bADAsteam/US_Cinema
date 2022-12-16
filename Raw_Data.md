---
doc: default
---

test 

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
Example of summary

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
