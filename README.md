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
- Is there different views on this subject among different groups of the population (between genders, age categories...)? 
- From the wikidata info on the speaker, is it possible to create a model which would give us the probability that a person is in favor of the right to own a gun? 


### Additional dataset
We will use the Wikidata information given ('speaker_attributes.parquet') as an additional dataset. We added information about the attributed speaker to the quotation dataframe: nationality, gender, occupation, age, ethnic group, religion and political party. The first part of our project will consist in comparing opinions among american on the gun permit. Concerning the genders, we decided to keep only the two main genders: 'female' and 'male', as very few quotations are attributed to other genders, it would have been impossible to balance the genders for the observational studies. 

### Methods 
- Data Preprocessing('DataSelection.ipynb'):
 We will only use quotations of the Quotebank corpus from 2015 to 2020. Certain quotations do not have any speaker, so we got rid of these quotations, for the others we kept the first speaker, as it is the most likely. Moreover we only kept citations which included chosen key words. These kew words have been found using 'Word Bank', which extracts the most used words in articles talking about mass shootings and gun culture in the USA. We then kept the words corresponding the most to our study. 
 
 - Statistics and methods used to answer the questions (Milestone2.ipynb):
To see if our project is feasible, we first extracted the desired quotations from the dataset of the year 2017. We found 58780 quotations talking about gun and mass shooting that had an attributed speaker. 58% of theses quotes are attributed to an American speaker. As the study is being carried over five years, way enough data are available. We performed a few statistics on these quotations in order to check the feasibility of our project. 
We realized a first timeline of quotations speaking about guns for this year and were able to determine two periods for which the topic was particurlarly important (these dates correspond to the ones of tragic events). It confirmed that we will be able to relate the time-distribution of the quotations to some events like the mass shooting of Las Vegas on the 1st of October 2017. 

  Then we implemented a small observational study: difference of opinions between the two main american political party: the Republicans and the Democrats,  to see if it will work at a larger scale in milestone 3. To compare opinions between different parts of the population, one needs these parts to be balanced. We will use the proposentity score  to match each speaker from the treated group (Democrat) with exactly one speaker from the control group (Republican). We balanced these groups with the gender and the age. The method used is better described in the code file. In Milestone 3, we will perform the observational study on the period of the Las Vegas shooting. We will study the evolution of opinions after this shooting. 

  To relate the social caracteristics of speakers to their opinion on the right to own guns, we have to perform a sentiment analysis on the citations in order to extract a score for each citation. We use the compound score which is between -1 and 1. A score close to -1 indicates that the quotation speaks negatively (e.g. 'The gun owning is the a curse for the US' has a compound score of -0.7096). A score close to 1 indicates that the quotation speaks positively (e.g. 'The 2nd amendment is the best part of the constitution' has a compound score of 0.6369). A score of 0 indicates neutrality of the quotation.
To do so, we use the VADER-Sentiment-Analysis library which contains a pretrained model to score a sentence. 


### Timeline and Organization
The project has to be finished before the 17th December. The first week will be dedicated to the download and selection of all the data of interest and to the study of difference of opinions among different social groups in the US and the difference before and after the mass shooting of Orlando. Then we will create the website, as we do not have any experience, we will dedicate it two weeks. In the last two weeks our main goal will be to create a model supported by mathematical modelling behaviour method to see if we can predict the opinion of speakers on the gun permit from their background. 








