
# Generation of Parallel Corpora in PubAnnotationfor the WMT Biomedical Task

Machine translation (MT) of the biomedical literature can support researchers in various tasks. In the current COVID-19 pandemic, the translation into English of scientific publications only available in other languages, i.e. [Chinese](https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(20)30375-5/fulltext), can contribute to widen the availability of data on an emerging disease.
Thus, bringing novel information for researchers and health professionals who could not read those documents otherwise.

With this aim, we have been organizing the [WMT Biomedical task](http://www.statmt.org/wmt20/biomedical-translation-task.html) since 2016. 
In the most recent edition of the shared task, we addressed seven languages pairs for 
%the MEDLINE 
the biomedical literature test sets, namely: English to and from Chinese, French, German, Italian, Portuguese, Russian, and Spanish.

MEDLINE contains many parallel abstracts, i.e., abstracts which are available in more than one language, for instance, the article referenced with the PubMed identifier (PMID) [32074817](https://pubmed.ncbi.nlm.nih.gov/32074817/) is available in Chinese, with title and abstract both in Chinese and English.
Because our test sets are derived from MEDLINE, participants are asked to not download the database by themselves and instead, consider using the MEDLINE training data that we [release](https://github.com/biomedical-translation-corpora/corpora). Currently, we release the training data for some of the languages in a zip file format in the task shared folder. 
Since new parallel abstracts are available every year, this means releasing new zip files every year, or creating a new joint single zip file.

As alternative to this, we propose to use [PubAnnotation](http://www.pubannotation.org/) for creating a collection of the parallel abstracts that we consider for our training data.
PubAnnotation offers many interesting features:
(a) the possibility of adding new PMID collections at any time;
(b) a newly implemented feature to specify which language data should be downloaded;
(c) no need to release the documents, since they are available in PubAnnotation.

We plan to create one project in PubAnnotation for each language in each language pair.
For instance, for the language pair Chinese-English, we would have one project in Chinese and one in English, both containing the same number of documents and the same PMIDs. 
%We created one pilot project to illustrate this approach.
During the hackathon, we plan to generate the various projects, 14 of them in total, one for each language direction for all seven language pairs. 
Further, we plan to use the newly created resources for downloading the abstracts and 
%applying them for 
training our baseline systems.

We also plan to assess the impact using PubAnnotation for building these resources, in particular from the perspective of reproducibility. 
%We also plan to assess the impact of the problems that might occur when using PubAnnotation for building these resources.
For instance, if we chose to have just one repository for each language of the language pairs, which would evolve (increase) every year, this means that we could not have different versions of the training data associated to each edition of the challenge.
This could be problematic if researchers plan to reproduce a particular system that was based only on training data available for a particular year. One solution to this issue could be to record a log of the PMIDs used in each edition of the campaign, to be included in the repository metadata. 
Further, previously, we have aligned the parallel abstracts in both language, i.e., specifying the one or more sentences in one language that correspond to one or more sentence in the other language.
However, as far as we know, annotations across documents, and across projects, are not allowed in PubAnnotation.
Finally, we need to check whether the PubAnnotation format for the textual files is a format that could be well accepted by the MT community.
