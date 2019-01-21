# por.rst.cstn

Cross-document Structure Theory News Corpus

Citation: Cardoso, P.C.F.; Maziero, E.G.; Jorge, M.L.C.; Seno, E.M.R.; Di Felippo, A.; Rino, L.H.M.; Nunes, M.G.V.; Pardo, T.A.S. (2011). CSTNews - A Discourse-Annotated Corpus for Single and Multi-Document Summarization of News Texts in Brazilian Portuguese. In the Proceedings of the 3rd RST Brazilian Meeting, pp. 88-105. October 26, Cuiabá/MT, Brazil. 

## Introduction

The CSTNews corpus was annotated by groups of computational linguists from NILC. The corpus is avaiable for download and use for research purposes.

The sucinto project aimed at investigating and exploring generic and topic-focused multi-document summarization strategies for providing a more feasible and intelligent access to on-line information provided by news agencies. This commitment brought back old and well-known scientific challenges from the first studies in summarization in the 50s as well as introduced several new and exciting challenges, e.g., to deal with redundant, complementary and contradictory information, to normalize different writing styles and referring expression choices, to balance different perspectives and sides of the same events and facts, to properly deal with evolving events and their narration in different moments, and to arrange information pieces from different texts to produce coherent and cohesive summaries, among several others. An ultimate goal of this project was to pull the developed tools together as on-line applications for final users.

This project took into consideration not only classical approaches to single and multi-document summarization, but also new ones, following different paradigms and using knowledge of varied nature ranging from empirical and statistical data to semantic and discourse models. Research interests included (i) the modeling of the summarization process (content selection, planning, aggregation, generalization, substitution, information ordering, etc.) by means of Cross-document Structure Theory (CST), Rhetorical Structure Theory (RST), ontologies, and language and summarization statistical models, (ii) the investigation of related tasks as discourse parsing, topic detection, temporal annotation and resolution, coreference resolution, text-summary alignment, and multilingual processing, and (iii) the linguistic characterization of multi-document summaries and their manual production.

The project was developed at NILC (Interinstitutional Center for Computational Linguistics), one of the biggest research groups on Natural Language Processing and Computational Linguistics in Brazil. It started in 2007 as a natural follow up to some previous projects on single-document summarization carried out at NILC (FAPESP #2006/02887-9; see also related projects). It was supported by the research agencies FAPESP, CNPq, and CAPES, which have granted scholarships for undergraduate and graduate students and regular financial support for the project (FAPESP# 2015/17841-3, FAPESP #2012/03071-3, FAPESP #2009/05603-0). The project was officially over at the end of 2017.

## DISRPT 2019 shared task information

Data was automatically parsed using the UDPipe Portuguese model. Note that the data includes .conllu multitokens, for example fused articles and prepositions are decomposed, and that NoSpace annotations may appear in the tenth column together with segmentation information:

```
# text = Presença constante na cena política brasileira nas últimas quatro décadas, o senador Antonio Carlos Magalhães (DEM-BA) morreu na manhã desta sexta-feira, em São Paulo, vítima de insuficiência cardíaca.
1	Presença	presença	NOUN	_	Gender=Fem|Number=Sing	22	obl	_	BeginSeg=Yes
2	constante	constante	ADJ	_	Gender=Fem|Number=Sing	1	amod	_	_
3-4	na	_	_	_	_	_	_	_	_
3	em	em	ADP	_	_	5	case	_	_
4	a	o	DET	_	Definite=Def|Gender=Fem|Number=Sing|PronType=Art	5	det	_	_
5	cena	cena	NOUN	_	Gender=Fem|Number=Sing	1	nmod	_	_
6	política	político	ADJ	_	Gender=Fem|Number=Sing	5	amod	_	_
7	brasileira	brasileira	ADJ	_	Gender=Fem|Number=Sing	5	amod	_	_
8-9	nas	_	_	_	_	_	_	_	_
8	em	em	ADP	_	_	12	case	_	_
9	as	o	DET	_	Definite=Def|Gender=Fem|Number=Plur|PronType=Art	12	det	_	_
10	últimas	último	ADJ	_	Gender=Fem|Number=Plur|NumType=Ord	12	amod	_	_
11	quatro	quatro	NUM	_	NumType=Card	12	nummod	_	_
12	décadas	década	NOUN	_	Gender=Fem|Number=Plur	1	nmod	_	SpaceAfter=No
...
```