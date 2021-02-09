# Digital Edition: Essays from Hannah Arendt
We have created a NER dataset from the digital edition "Sechs Essays" by Hannah Arendt. It consists of 23 documents from the period 1932-1976, which are available as TEI files online (see https://hannah-arendt-edition.net/3p.html?lang=de). From the original TEI files we build an NER dataset with tags distributed as shown in the following Table:
Tag | number of Tags
----|---------------
person | 1,904  
place        | 1,183  
ethnicity    | 1,143  
organisation | 541   
event        | 123   
language     | 22    
not tagged   | 153,223

In the original TEI files the class person is additionally divided into "person", "biblicalFigure", "ficticiousPerson", "deity", and "mythologicalFigure", but some of these different "person" sub classes had too few examples. Therefore we have combined these classes into a general class for persons. Furthermore, the class place was divided into "place" and "country". In the original TEI files some countries are also tagged as places. Therefore we combined both classes into one class for general places. Finally there was a class "ship". But in the whole edition there were only 4 examples of this class. That is why we decided to exclude this class from our NER dataset.

We provide the dataset in two formats. The first one is the classical CONLL-Format and the second one is an easy json format with the following structure:

It consists of a list of samples. Each sample is in turn a list of words or special characters. These in turn are represented as a two-element list, where the first element is the word itself and the second element is the corresponding target tag. Here is an example:

[[['Peter','B-person'],[Müller,'I-person'],['lebt','O'],['in','O'], ['Frankfurt','B-place'],['am','I-place'],['Main','I-place'],['.','O']],[['Gebürtig','O'],['stammt','O'],['er','O'],['aus','O'],['Berlin','B-place']] 

