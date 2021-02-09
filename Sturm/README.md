# Digital Edition: Sturm Edition 

Source:
Schrade, Torsten: „Startseite“, in: DER STURM. Digitale Quellenedition zur Geschichte der internationalen Avantgarde, erarbeitet und herausgegeben von Marjam Trautmann und Torsten Schrade. Mainz, Akademie der Wissenschaften und der Literatur, Version 1 vom 16. Jul. 2018.

From the Sturm Edition we have built a NER dataset. These are 174 letters from the years 1914-1922, which are available online in TEI format (see https://sturm-edition.de/id/S.0000001). It contains as tagged entities only persons, places and dates. From the original TEI files we build an NER dataset with tags distributed as shown in the following Table
Tag | number of tags 
----|---------------
pers         | 1,206  
date         | 1,178  
place        | 524   
not tagged   | 33,809 

We provide the dataset in two formats. The first one is the classical CONLL-Format and the second one is an easy json format with the following structure:

It consists of a list of samples. Each sample is in turn a list of words or special characters. These in turn are represented as a two-element list, where the first element is the word itself and the second element is the corresponding target tag. Here is an example:

[[['Peter','B-pers'],[Müller,'I-pers'],['lebt','O'],['in','O'], ['Frankfurt','B-place'],['am','I-place'],['Main','I-place'],['.','O']],[['Gebürtig','O'],['stammt','O'],['er','O'],['aus','O'],['Berlin','B-place']] 

