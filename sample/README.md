# Sample data

Sample data for the DISRPT2019 shared task

## Formats

The main shared task data will be provided in two formats: with dependency syntax trees / other annotations in CoNLL-U format, and in a tokenization-only 'plain' format.

### Treebank format (*.conll)

Files are given in the 10 column, tab delimited CoNLL-U format, with three kinds of lines:
  * Token lines (10 columns, word form in column 2) - the last column (CoNLL-U MISC field) may include an annotation `BeginSeg=Yes` to indicate the beginning of a discourse unit - this is the annotation systems should predict. *Note*: Other annotations from the original treebanks may also be present in this field, in which case they will be pipe separated.
  * Blank lines between sentences
  * Comment lines (some optional) - begin with `#` and contain one of three key-value pairs, e.g.:
    * `# newdoc id = GUM_academic_art`  [This is the identifier indicating a new corpus document]
    * `# sent_id = GUM_academic_art-1`  [If the treebank has native sentence IDs, there are included in this way for reference]
    * `# text = Aesthetic Appreciation and Spanish Art:` [Original, untokenized sentence text - not available for all treebanks]

Example:

```
# newdoc id = GUM_fiction_veronique
# sent_id = GUM_fiction_veronique-1
# text = The Cost to Be Wise
1	The	the	DET	DT	Definite=Def|PronType=Art	2	det	_	BeginSeg=Yes
2	Cost	cost	PROPN	NNP	Number=Sing	0	root	_	_
3	to	to	PART	TO	_	5	mark	_	_
4	Be	be	AUX	NNP	Number=Sing	5	cop	_	_
5	Wise	Wise	PROPN	NNP	Number=Sing	2	xcomp	_	_

# sent_id = GUM_fiction_veronique-2
# text = Veronique stayed with me that night, lying next to me in my blankets and furs.
1	Veronique	Veronique	PROPN	NNP	Number=Sing	2	nsubj	_	BeginSeg=Yes
2	stayed	stay	VERB	VBD	Mood=Ind|Tense=Past|VerbForm=Fin	0	root	_	_
3	with	with	ADP	IN	_	4	case	_	_
4	me	me	PRON	PRP	Case=Acc|Number=Sing|Person=1|PronType=Prs	2	obl	_	_
5	that	that	DET	DT	Number=Sing|PronType=Dem	6	det	_	_
6	night	night	NOUN	NN	Number=Sing	2	obl:tmod	_	SpaceAfter=No
7	,	,	PUNCT	,	_	8	punct	_	_
8	lying	lie	VERB	VBG	VerbForm=Ger	2	advcl	_	BeginSeg=Yes
9	next	next	ADJ	JJ	Degree=Pos	8	advmod	_	_
10	to	to	ADP	TO	_	11	case	_	_
11	me	me	PRON	PRP	Case=Acc|Number=Sing|Person=1|PronType=Prs	9	obl	_	_
12	in	in	ADP	IN	_	14	case	_	_
13	my	my	PRON	PRP$	Number=Sing|Person=1|Poss=Yes|PronType=Prs	14	nmod:poss	_	_
14	blankets	blanket	NOUN	NNS	Number=Plur	8	obl	_	_
15	and	and	CCONJ	CC	_	16	cc	_	_
16	furs	fur	NOUN	NNS	Number=Plur	14	conj	_	SpaceAfter=No
17	.	.	PUNCT	.	_	2	punct	_	_

# sent_id = GUM_fiction_veronique-3
# text = She didn't sleep, I don't think.
1	She	she	PRON	PRP	Case=Nom|Gender=Fem|Number=Sing|Person=3|PronType=Prs	4	nsubj	_	BeginSeg=Yes
2	did	do	AUX	VBD	Mood=Ind|Tense=Past|VerbForm=Fin	4	aux	_	SpaceAfter=No
3	n't	n't	PART	RB	Polarity=Neg	4	advmod	_	_
...
```

### Plain format (*.tok)

This format contains one token per line, with a running ID and word form in the first two tab delimited columns, and the possible annotation BeginSeg=Yes in the tenth and last column (if a new segment boundary is present). Document boundaries are indicated by comments, but other annotations are not used:

```
# newdoc id = GUM_fiction_veronique
1	The	_	_	_	_	_	_	_	BeginSeg=Yes
2	Cost	_	_	_	_	_	_	_	_
3	to	_	_	_	_	_	_	_	_
4	Be	_	_	_	_	_	_	_	_
5	Wise	_	_	_	_	_	_	_	_
6	Veronique	_	_	_	_	_	_	_	BeginSeg=Yes
7	stayed	_	_	_	_	_	_	_	_
8	with	_	_	_	_	_	_	_	_
9	me	_	_	_	_	_	_	_	_
10	that	_	_	_	_	_	_	_	_
11	night	_	_	_	_	_	_	_	_
12	,	_	_	_	_	_	_	_	_
13	lying	_	_	_	_	_	_	_	BeginSeg=Yes
14	next	_	_	_	_	_	_	_	_
15	to	_	_	_	_	_	_	_	_
16	me	_	_	_	_	_	_	_	_
17	in	_	_	_	_	_	_	_	_
18	my	_	_	_	_	_	_	_	_
19	blankets	_	_	_	_	_	_	_	_
20	and	_	_	_	_	_	_	_	_
21	furs	_	_	_	_	_	_	_	_
22	.	_	_	_	_	_	_	_	_
23	She	_	_	_	_	_	_	_	BeginSeg=Yes
24	did	_	_	_	_	_	_	_	_
25	n't	_	_	_	_	_	_	_	_
...
```
