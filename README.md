# The eternal debate of the gun culture in the USA

Team name : Sate \
Team members : Servane Lunven, Estelle Chabanel, Arthur Dietrich, Théo Patron

### Abstract 

A REMPLIR : 150 mots \
The aim of this project is to study how the American perceive the right to bear a firearm. The USA is the country with the most guns per person in the world: 32% of Americans own one. The gun culture is very lively in the USA but the numerous mass shootings which happened in the last few years have risen a debate in the American society: should the second amendment, which allows everyone to own a gun, be revisited? From quotations of Quotebank extracted from the English-speaking journals, the importance of this subject in the journals will be studied. Then, if they exist, the difference of opinions on the gun permit between different social groups in the American society : gender, age, political affiliation, will be highlighted. This to find patterns, the final goal being to develop a model which could predict if a person is pro or against the Second Amendment. 

### Research questions
In this project we will answer these questions:
- Is the right to own a gun a frequent debate in the american journals?
  We will  study the change of frequency between 2015 and 2020 to highlight events like mass shootings, which could have revived the debate.
- Does it exist different views on this subject and among different groups of the population (between genders, age categories...)? 
- From the wikidata on the speaker, is it possible to create a model which would give us the probability that a person is pro the right to own a gun? 


### Additional dataset
We will use Wikidata as an additional data set. For each speaker, we added to the  data frame of the quotations, information about the attributed speaker: nationality, gender, occupation, age, ethnic group, religion and political party. The first part of our project will consist in comparing opinions among american on the gun permit, so in milestone 2 we only kept the american speakers. Concerning the genders, we decided to keep only the two main genders: 'female' and 'male'. As very few quotations are attributed to other genders, it would have been impossible to balance the genders for the observational studies. 

### Methods 
- Data Preprocessing:
 We will only use quotations of the Quotebank corpus from 2015 to 2020. Certain quotations do not have any speaker, so we got rid of these quotations, for the others we kept the first speaker, as it is the most likely. Moreover we only kept citations which included key words. These kew words have been found using 'Word Bank'. In articles about mass shootings and  gun culture in the USA, 'Word Bank' extracted the most used words, then we kept the ones corresponding the most to our study. 
 - Statistics about the frequency of the subject:
To see if our project is feasible, we need enough data. For 2017, approximately 36000 quotations talked about gun and mass shooting. The study, being carried on 5 five years, enough data are available. As the dataset of 2017 already contians a large amount of data, we performed a few statistics on these quotations in order to check the feasibility of our project.
We realized a first timeline of quotations speaking about guns for this year and were able to determine two periods for which the topic was particurlarly important. It confirmed that we will be able to relate the time-distribution of the quotations to some events like the mass shooting of Las Vegas on the 1st of October 2017.

- speak about observational studies

- speak about sentiment analysis


### Timeline and Organization
The project has to be finished before the 17th December. The first week will be dedicated to the download and selection of all the data of interest and to the study of difference of opinions among different social groups in the US and the difference before and after the mass shooting of Orlando. Then we will create the website, as we do not have any experience, we will dedicate it two weeks. In the last two weeks our main goal will be to create a model supported by mathematical modelling behaviour method to see if we can predict the opinion of speakers on the gun permit from their background.








