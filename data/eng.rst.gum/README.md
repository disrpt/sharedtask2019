# eng.rst.gum

The Georgetown University Multilayer (GUM) corpus

To cite this corpus, please refer to the following article:

Zeldes, Amir (2017) "The GUM Corpus: Creating Multilayer Resources in the Classroom". Language Resources and Evaluation 51(3), 581–612.

## Introduction

a corpus of English texts from eight text types:

interviews
news
travel guides
how-to guides
academic writing
biographies
fiction
online forum discussions

The corpus is created as part of the course LING-367 (Computational Corpus Linguistics) at Georgetown University. 

For more details see: http://corpling.uis.georgetown.edu/gum.

## DISRPT 2019 shared task information

For the DISRPT 2019 shared task on elementary discourse unit segmentation, only the 7 open text genres are included (to obtain data in the 8th genre, containing reddit forum discussions which is not included in the shared task, see the corpus website). The data follows the normal division into train, test and dev partitions used for other tasks (e.g. for the conll shared task on UD parsing).  

POS tags and syntactic parses are the UD version of the manually annotated gold data. Morphological tags are generated automatically using CoreNLP.

### Notes on segmentation

GUM RST guidelines treat any non-argument clauses as EDUs (i.e. adverbial clauses, including to-infinitives, are EDUs, but subject and object clauses are not). Adverbial clauses and other EDU structures nested within direct speech object clauses are **not** segmented. VP coordination is not segmented, unless one of the coordinate VPs has its own adverbial clause, in which case all segments are created. Full coordination of finite structures or adverbial clauses is segmented. Prepositional phrases and segments interrupting a syntactic clause are **not** segmented. See the corpus guidelines for more details.
