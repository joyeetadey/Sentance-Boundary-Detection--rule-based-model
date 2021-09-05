# Sentance-Boundary-Detection--rule-based-model
SBD-rule-based model

## Objective
* Develop a rule based or ML based sentence boundary disambiguation system for the language of your choice.
* Write observations on the accuracy of your model and also elucidate any methods you can suggest to improve the model.

## Sentance Boundary Disambiguation
Sentence boundary disambiguation (SBD), also known as sentence breaking, sentence boundary detection, and sentence segmentation, is the problem in natural language processing of deciding where sentences begin and end. Natural language processing tools often require their input to be divided into sentences; however, sentence boundary identification can be challenging due to the potential ambiguity of punctuation marks. In written English, a period may indicate the end of a sentence, or may denote an abbreviation, a decimal point, an ellipsis, or an email address, among other possibilities.

#### References
* https://grammar.yourdictionary.com/punctuation/what/fourteen-punctuation-marks.html
* https://aclanthology.org/J97-2002.pdf
* https://dbpedia.org/page/Sentence_boundary_disambiguation

## Steps followed:
* First split sentances into words based on space.
* Then based on the terminating punctuations (.?!) split the sentances into leftword + punctuation + rightword and add ending marker at the potential boundary places
* Then past the split sentances through rules and check if the boundaries are correct. Store the correct boundaries in a boundary list
* Depending on the final boundary list obtained add boundary marker
* Split the string based on the boundary marker

## Helper Functions
Making helper functions for checking certain conditions like:
* terminating punctuations
* numeric character
* double quotes
* abbreviation type 1
* abbreviation type 2
* word is capital 
* word starting and ending with double quotes
* checking url
* checking email
* check elipsis
* check decimals

## Sentance helper functions
making sentance helper functions like:
* splitting the paragraph to list for making initial list based on **Terminating punctuations** 
* converting list to strings
* initial splitter of string which combines boith the above functions

## Finding Sentance Boundaries
* first we find the boundary by giving the initial strings list as input
* we get output of the boundary words 
* then we split the final sentance based on the boundary and add sentance markers '$$'
