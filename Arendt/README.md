# Digital Edition: Essays from Hannah Arendt
We have created a NER dataset from the digital edition "Sechs Essays" by Hannah Arendt. It consists of 23 documents from the period 1932-1976, which are available as TEI files online (see https://hannah-arendt-edition.net/3p.html?lang=de). 

![licence image](https://upload.wikimedia.org/wikipedia/commons/c/ce/Cc-by-nc-sa_euro_icon.svg "License")

This NER Dataset ist licensed under a  
[Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Germany (CC BY-NC-SA 3.0 DE).](http://creativecommons.org/licenses/by-nc-sa/3.0/de/)

From the original TEI files we build an NER dataset with tags distributed as shown in the following Table:
Tag | # All | # Train | # Test | # Devel
----|-------|---------|--------|---------
person | 1,702 | 1,303 | 182 | 217  
place        | 1,087 | 891 | 111 | 85 
ethnicity    | 1,093 | 867 | 115 | 111 
organisation | 455 | 377 | 39 | 39   
event        | 57 | 49 | 6 | 2    
language     | 20 | 14 | 4 | 2    
not tagged   | 153,223 | 121,154 | 16,101 | 15,968

In the original TEI files the class person is additionally divided into "person", "biblicalFigure", "ficticiousPerson", "deity", and "mythologicalFigure", but some of these different "person" sub classes had too few examples. Therefore we have combined these classes into a general class for persons. Furthermore, the class place was divided into "place" and "country". In the original TEI files some countries are also tagged as places. Therefore we combined both classes into one class for general places. Finally there was a class "ship". But in the whole edition there were only 4 examples of this class. That is why we decided to exclude this class from our NER dataset.

We provide the dataset in two formats together with a partition into a train, dev, and testset. The first one is an easy format similar to the well-known CONLL-X format and the second one is an easy json format with the following structure:

It consists of a list of samples. Each sample is in turn a list of words or special characters. These in turn are represented as a two-element list, where the first element is the word itself and the second element is the corresponding target tag. Here is an example:

[[['Peter','B-person'],[Müller,'I-person'],['lebt','O'],['in','O'], ['Frankfurt','B-place'],['am','I-place'],['Main','I-place'],['.','O']],[['Gebürtig','O'],['stammt','O'],['er','O'],['aus','O'],['Berlin','B-place']] 




