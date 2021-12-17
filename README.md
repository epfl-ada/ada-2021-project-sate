# The eternal debate of the gun culture in the USA

Team name : Sate \
Team members : Servane Lunven, Estelle Chabanel, Arthur Dietrich, Théo Patron

### Abstract 

The aim of this project is to study how the American perceive the right to bear a firearm. The USA is the country with the most guns per person in the world: 32% of americans own one. The gun culture is very lively in the USA but the numerous mass shootings which happened in the last few years have risen a debate in the american society: should the second amendment, which allows everyone to own a gun, be revisited? From quotations of Quotebank extracted from the English-speaking journals, the importance of this subject in the journals will be studied. Then, if they exist, the difference of opinions on the gun permit between different social groups in the American society : gender, age, political affiliation, will be highlighted. This to find patterns, the final goal being to develop a model which could predict if a person is pro or against the Second Amendment. 

### Research questions
In this project we will answer these questions:
- Is the right to own a gun a frequent debate in the american journals?
  We will  study the change of frequency between 2015 and 2020 to highlight events like mass shootings, which could have revived the debate.
- Is there different views on this subject among different groups of the population (between genders, age categories...)? 
- From the wikidata info on the speaker, is it possible to create a model which would give us the probability that a person is in favor of the right to own a gun? 


### Additional dataset  
We will use the Wikidata information given ('speaker_attributes.parquet') as an additional dataset. We added information about the attributed speaker to the quotation dataframe: nationality, gender, occupation, age, ethnic group, religion and political party. The first part of our project will consist in comparing opinions among american on the gun permit. Concerning the genders, we decided to keep only the two main genders: 'female' and 'male', as very few quotations are attributed to other genders, it would have been impossible to balance the genders for the observational studies. 

### Methods 
__Data Preprocessing ('DataSelection.ipynb' and 'NewDatasetAndStats.ipynb'):__  
  
 We will only use quotations of the Quotebank corpus from 2015 to 2020. Certain quotations do not have any speaker, so we got rid of these quotations. For the others we kept the first speaker, as it is the most likely. Moreover we only kept citations which included chosen key words. These kew words have been found using 'Word Bank', which extracts the most used words in articles talking about mass shootings and gun culture in the USA. We then kept the words corresponding the most to our study. We also add additional information about the speaker (age, political party, ...). This is done in the file DataSelection.ipynb that has to be run once for every years' file. We then obtain the new files 'quotes-201_-extended.json.bz2' that are "reunited" in a new dataframe, save in a new data file 'gundata.json.bz2' in the the file 'NewDatasetAndStats.ipynb'. Some basic statistics on te new dataset are also computed in this file : the new dataset contains 69963 different quotations, 62% of which are from American speakers.
 
 __Data Story and Research questions ('Milestone3.ipynb'):__  
   
The project is organized in 3 steps.   
First, a timeline of the gun related quotations is realized. The goal is to check if we can link the high frequency of quotes with  events, our guess being that most peaks will correspond to important mass shootings. The deadliest are highlighted in the timeline. A zoom on two particularly high frequency peaks for October 2017 and February 2018, corresponding to two mass shooting is realized.   
  
The first event is the starting point for our sentiment analysis study. We performed a matching on the characteristics of the speakers for quotations around this period : before and after the 1st of October 2017. The speakers being balanced, a sentiment analysis on the quotations allow us to observe changes in opinions of different groups of speaker before and after the mass shooting. The three different  characteristics of speakers studied are the genre male and female, the ages, and the political party: Republicans and Democrats. The method used for this observational study is better described in the code file.   
  
Finally, once the observational study performed, we tried to implement a model taht will predict some speaker's opinion according to these charasteristics : age, gender and political party. To relate the social characteristics of speakers to their opinion on the right to own guns, we have to perform a sentiment analysis on the citations in order to extract a score for each citation. We use the compound score which is between -1 and 1. A score close to -1 indicates that the quotation speaks negatively (e.g. 'The gun owning is the a curse for the US' has a compound score of -0.7096). A score close to 1 indicates that the quotation speaks positively (e.g. 'The 2nd amendment is the best part of the constitution' has a compound score of 0.6369). A score of 0 indicates neutrality of the quotation.
To do so, we use the VADER-Sentiment-Analysis library which contains a pretrained model to score a sentence.   
  

### Timeline and Organization
Each member of the team performed the data selection on one of the original files. Then, the different tasks and research questions were distributed like this:  
Estelle : Dataset first statistics, Timeline and events linking  
Arthur : Observational study and Sentiment analysis, study of changes in opinion  
Sevane : Study of the new dataset quotations, creation of the model to relate peoples' characteristics to their opinion about gun owning  
Théo : Data selection's algorithm and selection of the lexical field, creation and design of the website   
Each member contributed equally to the writing of the datastory.




