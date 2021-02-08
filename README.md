# NERDatasets
Contains two NER Datasets builded from existing digital editions
It consists of a list of samples. Each sample is in turn a list of words or special characters. These in turn are represented as a two-element list, where the first element is the word itself and the second element is the corresponding target tag. Here is an example:

[[['Peter','B-Per'],[Müller,'I-Per'],['lebt','O'],['in','O'], ['Frankfurt','B-Loc'],['am','I-Loc'],['Main','I-Loc'],['.','O']],[['Gebürtig','O'],['stammt','O'],['er','O'],['aus','O'],['Berlin','B-Loc'],] 
 
