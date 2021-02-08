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
