# NERDatasets
Contains two NER Datasets builded from existing digital editions
It consists of a list of samples. Each sample is in turn a list of words or special characters. These in turn are represented as a two-element list, where the first element is the word itself and the second element is the corresponding target tag. Here is an example:

Peter & Müller & lebt & in & Frankfurt & am & Main  \\
B-Per & I-Per & O & O & B-Loc & I-Loc & I-Loc 
