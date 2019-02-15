# Turkish Discourse Bank 1.0

## Introduction  

Turkish Discourse Bank 1.0 is a 400,000-word corpus funded by TÜBİTAK (The Scientific and Technological Research Council of Turkey) annotated in the PDTB style. For more information regarding TDB, please visit: http://medid.ii.metu.edu.tr/theCorpus.html. TDB 1.0 contains explicit discourse connectives as well phrasal expressions based on postpositions, i.e: 

-conjunctions such as 've' (and), 'ama' (but), etc. 
-adverbials such as 'aksine' (to the contrary),
-postpositions such as için 'for' (conveying the purpose or reason sense), 
-phrasal expressions such as 'bunun için' (for this reason).

Postpositions are single word connectives and they always appear after the verb of the syntactically dependent argument. The phrasal expressions annotated in TDB 1.0 are derived from postpositions and mostly contain a deictic element such as 'bu' (this), 'o' (that). Phrasal expressions are a sub-type of alternative lexicalizations.   

As in the PDTB, in TDB,

-explicit connectives may be continuous or discontinuous, as in 've' (and), 'hem ... hem' (both ... and), 
-explicit connectives may be pre-modified as in 'tam aksine' (just to the contrary); they may also be post-modified as in 'sanki ... gibi' (as if)
-phrasal expressions may be pre-modified, as in 'ancak bundan sonra' (only after this), or they may be post-modified by a focus particle, as in 'bu amaçla da' (for this reason - focus particle). 

## DISRPT 2019 shared task information

The data was automatically parsed using the UDPipe Turkish model (https://github.com/jwijffels/udpipe.models.ud.2.0/blob/master/inst/udpipe-ud-2.0-170801/turkish-ud-2.0-170801.udpipe). 

### Obtaining the text

Since the underlying texts cannot be placed openly online, the shared task data has replaced token information with underscores. To reconstruct the data, users must obtain the raw texts by filling in the user agreement form (`tdb_shared_task_user_agreement.docx`) which they email to `corpora@metu.edu.tr` 
and run the Python script utils/process_files.py. For more details, run python utils/process_files.py -h.

## Notes

A list of all explicit connectives and phrasal expressions annotated in TDB 1.0 can be found in Demirşahin and Zeyrek (2017). 

An introduction to TDB can be found in Zeyrek and Webber (2008)

The full tag set of TDB can be found in Zeyrek et al. (2013)

The list of all modifiers can be found in Çakmak (2015). 

References: 

Çakmak, Deniz Hande. (2015). The Role of Modifiers in Turkish Discourse Bank. Unpublished MS Thesis. Middle East Technical University, Cognitive Science Department. 

Demirşahin, I., & Zeyrek, D. (2017). Pair annotation as a novel annotation procedure: The case of Turkish Discourse Bank. In Handbook of Linguistic Annotation (pp. 1219-1240). Springer, Dordrecht.

Zeyrek, D., Demirşahin, I., Sevdik-Çallı, A. B., & Çakıcı, R. (2013). Turkish Discourse Bank: Porting a discourse annotation style to a morphologically rich language. D&D, 4(2), 174-184.

Zeyrek, D., & Webber, B. (2008). A discourse resource for Turkish: Annotating discourse connectives in the METU corpus. In Proceedings of the 6th workshop on Asian language resources.




