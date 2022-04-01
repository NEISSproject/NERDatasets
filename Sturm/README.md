# Digital Edition: Sturm Edition 

Source:
Schrade, Torsten: „Startseite“, in: DER STURM. Digitale Quellenedition zur Geschichte der internationalen Avantgarde, erarbeitet und herausgegeben von Marjam Trautmann und Torsten Schrade. Mainz, Akademie der Wissenschaften und der Literatur, Version 1 vom 16. Jul. 2018.

This NER Dataset is available under the license
[Creative Commons Attribution 4.0 International (CC-BY 4.0)](https://creativecommons.org/licenses/by/4.0/)

We introduced them in our paper:<br/>
Zöllner, J.; Sperfeld, K.; Wick, C.; Labahn, R. Optimizing Small BERTs Trained for German NER. Information 2021, 12, 443.<br/>
https://doi.org/10.3390/info12110443

From the Sturm Edition we have built a NER dataset. These are 174 letters from the years 1914-1922, which are available online in TEI format (see https://sturm-edition.de/id/S.0000001). It contains as tagged entities only persons, places and dates. From the original TEI files we build an NER dataset with tags distributed as shown in the following Table
Tag | # All | # Train | # Test | # Devel 
----|-------|---------|--------|--------
pers         | 930  | 763 | 83 | 84 
date         | 722 | 612 | 59 | 51  
place        | 492 | 374 | 59 | 59   
not tagged   | 33,809 | 27,047 | 3,306 | 3,456

We provide the dataset in two formats together with a partition into a train, dev, and testset. The first one is an easy format similar to the well-known CONLL-X format and the second one is an easy json format with the following structure:

It consists of a list of samples. Each sample is in turn a list of words or special characters. These in turn are represented as a two-element list, where the first element is the word itself and the second element is the corresponding target tag. Here is an example:

[[['Peter','B-pers'],[Müller,'I-pers'],['lebt','O'],['in','O'], ['Frankfurt','B-place'],['am','I-place'],['Main','I-place'],['.','O']],[['Gebürtig','O'],['stammt','O'],['er','O'],['aus','O'],['Berlin','B-place']] 


