# DISRPT/sharedtask2019

Repository for the DISRPT2019 shared task on Discourse Unit Segmentation

## Introduction

The DISRPT 2019 workshop introduces the first iteration of a cross-formalism shared task on discourse unit segmentation. Since all major discourse parsing frameworks imply a segmentation of texts into segments, learning segmentations for and from diverse resources is a promising area for converging methods and insights. We provide training, development and test datasets from all available languages and treebanks in the RST, SDRT and PDTB formalisms, using a uniform format. Because different corpora, languages and frameworks use different guidelines for segmentation, the shared task is meant to promote design of flexible methods for dealing with various guidelines, and help to push forward the discussion of standards for discourse units. For datasets which have treebanks, we will evaluate in two different scenarios: with and without gold syntax, or otherwise using provided automatic parses for comparison.

https://sites.google.com/view/disrpt2019/

**Shared task participants are encouraged to follow this repository in case bugs are found and need to be fixed** 

## Types of data

The tasks are oriented towards finding the locus of discourse relations in texts. For frameworks that segment text into non-overlapping spans covering each entire documents (RST and SDRT), the task corresponds to finding the starting point of each discourse unit. For PDTB-style datasets, the task is to identify the spans of discourse connectives that explicitly identify the existence of a discourse relation.

## Important dates

  * Fri, December 28, 2018 - shared task sample data release
  * Mon, January 21, 2019 - training data release
  * Fri, February 15, 2019 - test data release
  * Thu, February 28, 2019 - papers due (shared task & regular workshop papers)
  * Wed, March 27, 2019 - notification of acceptance
  * Fri, April 5, 2019 - camera-ready papers due
  * Thu, June 6, 2019 - workshop

## Directories

The shared task repository currently comprises the following directories (to be extended as the task progresses):

  * data - individual corpora from various languages and frameworks. 
    * Folders are given names in the scheme `LANG.FRAMEWORK.CORPUS`, e.g. `eng.rst.gum` is the directory for the GUM corpus, which is in English and annotated in the framework of Rhetorical Structure Theory (RST).
    * Note that four corpora (eng.rst.rstdt, eng.pdtb.pdtb, tur.pdtb.tdb, zho.pdtb.cdtb) **do not contain text** and text therefore needs to be reconstructed using `utils/process_underscores.py`.
  * sample - sample data to illustrate formats, provided ahead of the release of training data (this data will be included in training data).
  * utils - scripts for validating, evaluating and generating data formats. The official scorer is `seg_eval.py`.

See the README files in individual data directories for more details on each dataset.

## Surprise language

At the release of the test data, a surprise language dataset was added: Turkish connective data from the Turkish from the Turkish Discourse Bank (TDB). Since the existence of the surprise language was not originally announced, and some systems may not have resources to handle the additional language, evaluation on the Turkish dataset is optional and will be reported separately in the shared task results.

## Statistics

| corpus | lang | framework | train_toks | train_sents | train_docs | dev_toks | dev_sents | dev_docs | test_toks | test_sents | test_docs | total_toks | total_sents | total_docs | seg_style | underscored | SpaceAfter | syntax | has_multitoks |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| deu.rst.pcc | deu | rst | 26,831 | 1,773 | 142 | 3,152 | 207 | 17 | 3,239 | 213 | 17 | 33,222 | 2,193 | 176 | EDU | no | no | UD | no |
| eng.pdtb.pdtb | eng | pdtb | 1,061,222 | 44,563 | 1,992 | 39,768 | 1,703 | 79 | 55,658 | 2,364 | 91 | 1,156,648 | 48,630 | 2,162 | Conn | yes | no | UD (gold) | no |
| eng.rst.gum | eng | rst | 67,098 | 3,600 | 78 | 15,593 | 784 | 18 | 15,924 | 890 | 18 | 98,615 | 5,274 | 114 | EDU | no | yes | UD (gold) | no |
| eng.rst.rstdt | eng | rst | 166,849 | 6,672 | 309 | 17,309 | 717 | 38 | 21,666 | 929 | 38 | 205,824 | 8,318 | 385 | EDU | yes | no | UD (gold) | no |
| eng.sdrt.stac | eng | sdrt | 36,445 | 7,689 | 29 | 4,747 | 981 | 6 | 6,549 | 1,350 | 6 | 47,741 | 10,020 | 41 | EDU | no | no | UD | no |
| eus.rst.ert | eus | rst | 21,122 | 990 | 84 | 7,533 | 350 | 28 | 6,658 | 320 | 28 | 35,313 | 1,660 | 140 | EDU | no | no | other | no |
| fra.sdrt.annodis | fra | sdrt | 22,278 | 880 | 64 | 4,987 | 227 | 11 | 5,146 | 211 | 11 | 32,411 | 1,318 | 86 | EDU | no | no | UD | no |
| nld.rst.nldt | nld | rst | 17,566 | 1,202 | 56 | 3,789 | 257 | 12 | 3,565 | 248 | 12 | 24,920 | 1,707 | 80 | EDU | no | no | UD | no |
| por.rst.cstn | por | rst | 44,808 | 1,595 | 110 | 6,233 | 232 | 14 | 3,615 | 123 | 12 | 54,656 | 1,950 | 136 | EDU | no | yes | UD | yes |
| rus.rst.rrt | rus | rst | 214,484 | 9,859 | 140 | 29,412 | 1,327 | 19 | 28,768 | 1,327 | 19 | 272,664 | 12,513 | 178 | EDU | no | no | UD | no |
| spa.rst.rststb | spa | rst | 43,034 | 1,577 | 203 | 7,531 | 256 | 32 | 8,026 | 303 | 32 | 58,591 | 2,136 | 267 | EDU | no | no | UD | no |
| spa.rst.sctb | spa | rst | 10,249 | 304 | 32 | 2,450 | 74 | 9 | 3,813 | 100 | 9 | 16,512 | 478 | 50 | EDU | no | no | UD | no |
| tur.pdtb.tdb | tur | pdtb | 398,203 | 25,080 | 159 | 50,272 | 3,179 | 19 | 47,880 | 2,937 | 19 | 496,355 | 31,196 | 197 | Conn | yes | yes | UD | yes |
| zho.pdtb.cdtb | zho | pdtb | 52,061 | 2,049 | 125 | 11,178 | 438 | 21 | 10,075 | 404 | 18 | 73,314 | 2,891 | 164 | Conn | yes | no | other (gold) | no |
| zho.rst.sctb | zho | rst | 8,960 | 344 | 32 | 2,102 | 87 | 9 | 3,380 | 132 | 9 | 14,442 | 563 | 50 | EDU | no | no | UD (V1) | no |