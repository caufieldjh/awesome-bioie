# Awesome Biomedical Information Extraction (BioIE)

[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)

A curated list of resources dedicated to Biomedical Information Extraction (BioIE).

![Awesome BioIE Logo](/images/abie_head.png)

What is BioIE? It includes any effort to extract structured information from _unstructured_ (or, at least inconsistently structured) biological, clinical, or other biomedical data. The data source is often some collection of text documents written in technical language. If the resulting information is verifiable and consistent across sources, we may then consider it _knowledge_. Extracting information and producing knowledge from bio data requires adaptations upon methods developed for other types of unstructured data.

Inspired by [awesome-nlp](https://github.com/keon/awesome-nlp). Please see that list for more resources relevant to Natural Language Processing in general. See also [awesome-biology](https://github.com/raivivek/awesome-biology) and [Awesome-Bioinformatics](https://github.com/danielecook/Awesome-Bioinformatics).

Resources included here should preferentially be available at no monetary cost and limited license requirements (i.e., few commercial platforms should be listed). Also omitted: methods without publicly accessible code, datasets without public means of access, tools without documentation, and older versions of existing platforms.

Where possible, tools and resource entries include links to corresponding papers. If an open-access version of the paper is not available, this link should be either a PubMed citation entry or a link to another citation database.

_Please read the [contribution guidelines](contributing.md) before contributing. Please add your favourite resource by raising a [pull request](https://github.com/caufieldjh/awesome-bioie/pulls)._

## Contents
* [Research Overviews](#research-overviews)
* [Groups Active in the Field](#groups-active-in-the-field)
* [Tutorials](#tutorials)
  * [Guides](#guides)
  * [Video Lectures and Online Courses](#video-lectures-and-online-courses)
  * [Books](#books)
* [Code Libraries](#code-libraries)
  * [Repos for Specific Datasets](#repos-for-specific-datasets)
* [Tools, Platforms, and Services](#tools-platforms-and-services)
  * [Annotation Tools](#annotation-tools)
* [Techniques](#techniques)
  * [Text Embeddings](#text-embeddings)
    * [Word Embeddings](#word-embeddings)
    * [Sentence and Language Model Based Word Embeddings](#sentence-and-language-model-based-word-embeddings)
 * [Question Answering and Knowledge Extraction](#question-answering-and-knowledge-extraction)
* [Datasets](#datasets)
  * [Annotated Text Data](#annotated-text-data)
    * [Protein-protein Interaction Annotated Corpora](#Protein-protein-interaction-annotated-corpora)
  * [Other Datasets](#other-datasets)
* [Ontologies and Controlled Vocabularies](#ontologies-and-controlled-vocabularies)
* [Data Models](#data-models)
* [Credits](#credits)
* [License](#license)

## Research Overviews

* [Literature Based Discovery: Models, methods, and trends](https://www.sciencedirect.com/science/article/pii/S1532046417301909) - a review of Literature Based Discovery (LBD), or the philosophy that meaningful connections may be found between seemingly unrelated scientific literature. 
  * For some historical context on LBD, see papers by University of Chicago's Don Swanson and Neil Smalheiser, including [_Undiscovered Public Knowledge_](https://www.jstor.org/stable/4307965) (paywalled) and [_Rediscovering Don Swanson: the Past, Present and Future of Literature-Based Discovery_](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5771422/).
* [Mining Electronic Health Records (EHRs): A Survey](https://arxiv.org/abs/1702.03222) - a review of the methods and philosophy behind mining electronic health records, including using them for adverse event detection. See Table 2 for a list of relevant papers as of mid-2017.

[Back to Top](#contents)

## Groups Active in the Field
Biomedical IE, text mining, natural language processing, and data management is an active field of research and development with a rich history. Some research groups have roots in medical libraries and are primarily concerned with how to best organize biomedical literature and data. Others approach biomedical questions from a computer science perspective. Still other groups are based in biology and medicine, but have found that computational strategies for learning from large datasets are informative and useful. Because of the interdisciplinary nature of much of this work, it may be described in a variety of terms, including _(bio)medical informatics_, _computational biology_, or _bioinformatics_ (though the last of these generally concerns structured data such as DNA or protein sequences). The following groups have not been separated on the basis of their perspectives (as with all other sections, this list is vastly incomplete).

* [Boston Children's Hospital Natural Language Processing Laboratory](http://www.childrenshospital.org/research/labs/natural-language-processing-laboratory) - Led by Dr. Guergana Savova, formerly at Mayo Clinic and the Apache cTAKES project.

* [BD2K](https://commonfund.nih.gov/bd2k) - the U.S. National Institutes of Health (NIH) funded 13 Centers of Excellence through their Big Data to Knowledge (BD2K) program, several of which developed tools and resources for BioIE.
  * [HeartBD2K](http://www.heartbd2k.org/) - based at University of California, Los Angeles (UCLA). Led by Dr. Peipei Ping.
  * [KnowEng](https://knoweng.org/about/people/) - based an University of Illinois at Urbana-Champaign (UIUC). Led by Dr. Jiawei Han.
  * [Mobilize](http://mobilize.stanford.edu/) - based at Stanford. Led by Dr. Scott Delp.

* [BioNLP group at NCBI](https://www.ncbi.nlm.nih.gov/research/bionlp/) - based at the National Center for Biotechnology Information (NCBI) of the National Library of Medicine (NLM) in the U.S. National Institutes of Health (NIH). Develops improvements to biomedical literature search and curation (e.g., through PubMed). Led by Dr. Zhiyong Lu.   

* [Center for Computational Pharmacology NLP Group](http://compbio.ucdenver.edu/Hunter_lab/CCP_website/index.html) - based at University of Colorado, Denver. Led by Larry Hunter. [See their GitHub repos here.](https://github.com/UCDenver-ccp)

* [National Centre for Text Mining (NaCTeM)](http://www.nactem.ac.uk/) - based at the University of Manchester, NaCTeM is concerned with text mining in general but has a particular focus on biomedical applications. Its director is Prof. Sophia Ananiadou.

* [Mayo Clinic's clinical natural language processing program](https://www.mayo.edu/research/departments-divisions/department-health-sciences-research/medical-informatics/projects) - Several groups at Mayo Clinic have made major contributions to BioIE over the past 20 years. The Apace cTAKES platform was developed here. The program is led by Dr. Hongfang Liu.

* [TurkuNLP](https://turkunlp.org/) - based at the University of Turku. Concerned with NLP in general with a focus on BioNLP and clinical applications.

* [VCU Natural Language Processing Lab](https://nlp.cs.vcu.edu/) - based at Virginia Commonwealth University. Led by Dr. Bridget McInnes.

[Back to Top](#contents)

## Tutorials

The field changes rapidly enough that tutorials any older than a few years are missing crucial details. A few more recent educational resources are listed below. A good foundational understanding of text mining techniques is very helpful, as is some basic experience with the Python and or R languages. Starting with the [NLTK tutorials](https://www.nltk.org/book/) and then trying out the tutorials for the [Flair framework](https://github.com/zalandoresearch/flair) will provide excellent examples of natural language processing, text mining, and modern machine learning-driven methods, all in Python. Most of the examples don't include anything biomedical, however, so the best option may be to learn by doing.

### Guides

* [Getting Started in Text Mining]() - a brief introduction to bio-text mining from Cohen and Hunter. More than ten years old but still quite relevant. See also an [earlier paper by the same authors](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1702322/).

### Video Lectures and Online Courses
* [Coursera - Foundations of mining non-structured medical data](https://www.coursera.org/learn/mining-medical-data) - About three hours worth of video lectures on working with medical data of various types and structures, including text and image data. Appears fairly high-level and intended for beginners.

[Back to Top](#contents)

## Code Libraries

* [medaCy](https://github.com/NLPatVCU/medaCy) - a system for building predictive medical natural language processing models. Built on the [spaCy](https://spacy.io/) framework. 
* [ScispaCy](https://github.com/allenai/SciSpaCy) - [paper](https://arxiv.org/abs/1902.07669) - A version of the [spaCy](https://spacy.io/) framework for scientific and biomedical documents.

### Repos for Specific Datasets

* [mimic-code](https://github.com/MIT-LCP/mimic-code) - Code associated with the MIMIC-III dataset (see below). Includes some helpful [tutorials](https://github.com/MIT-LCP/mimic-code/tree/master/tutorials).

[Back to Top](#contents)

## Tools, Platforms, and Services

* [CLAMP](https://clamp.uth.edu/) - [paper](https://academic.oup.com/jamia/article/25/3/331/4657212) - a natural language processing toolkit intended for use with the text in clinical reports. Check out their [live demo](https://clamp.uth.edu/clampdemo.php) first to see what it does. Usable at no cost for academic research.
* [PubTator Central](https://www.ncbi.nlm.nih.gov/research/pubtator/) - [paper](https://academic.oup.com/nar/article/47/W1/W587/5494727) - a web platform that identifies five different types of biomedical concepts in PubMed articles and PubMed Central full texts. The full annotation sets are downloadable (see [Annotated Text Data](#annotated-text-data) below).

### Annotation Tools

* [brat](https://brat.nlplab.org/) - [paper](https://www.aclweb.org/anthology/E12-2021/) - [code](https://github.com/nlplab/brat) - the brat rapid annotation tool. Supports producing text annotations visually, through the browser. Not subject specific; appropriate for many annotation projects. Visualization is based on that of the [_stav_ tool](https://github.com/nlplab/stav/). 

[Back to Top](#contents)

## Techniques

### Text Embeddings

[This paper from Hongfang Liu's group at Mayo Clinic](https://www.sciencedirect.com/science/article/pii/S1532046418301825) demonstrates how text embeddings trained on biomedical or clinical text can, but don't always, perform better on biomedical natural language processing tasks. That being said, pre-trained embeddings may be appropriate for your needs, especially as training domain-specific embeddings can be computationally intensive.

#### Word Embeddings

* [BioASQword2vec](http://bioasq.org/news/bioasq-releases-continuous-space-word-vectors-obtained-applying-word2vec-pubmed-abstracts) - [paper](http://bioasq.lip6.fr/info/BioASQword2vec/) - word embeddings derived from biomedical text (>10 million PubMed abstracts) using the popular [word2vec](https://code.google.com/archive/p/word2vec/) tool.
* [BioWordVec](https://figshare.com/articles/Improving_Biomedical_Word_Embeddings_with_Subword_Information_and_MeSH_Ontology/6882647) - [paper](https://www.nature.com/articles/s41597-019-0055-0) - [code](https://github.com/ncbi-nlp/BioWordVec) - word embeddings derived from biomedical text (>27 million PubMed titles and abstracts), including subword embedding model based on MeSH.

#### Sentence and Language Model Based Word Embeddings

* [BioBERT](https://github.com/naver/biobert-pretrained) - [paper](https://arxiv.org/abs/1901.08746) - [code](https://github.com/dmis-lab/biobert) - a PubMed and PubMed Central-trained version of the [BERT language model](https://arxiv.org/abs/1810.04805).

[Back to Top](#contents)

## Datasets

Some of the datasets listed below require a [UMLS Terminology Services (UTS) account](https://www.nlm.nih.gov/databases/umls.html#license_request) to access. Please note that the license granted with the UTS account requires users to submit an annual report about their use of UMLS resources. This is less challenging than it sounds.

### Biomedical Text Sources

The following resources contain indexed text documents in the biomedical sciences.
* [OHSUMED](http://davis.wpi.edu/xmdv/datasets/ohsumed.html) - [paper](https://dl.acm.org/citation.cfm?id=188557) - 348,566 MEDLINE entries (title and sometimes abstract) from between 1987 and 1991. Includes MeSH labels. Primarily of historical significance.
* [PubMed Central Open Access Subset](https://www.ncbi.nlm.nih.gov/pmc/tools/openftlist/) - a set of PubMed Central articles usable under licenses other than traditional copyright, though the exact licenses vary by publication and source. Articles are available as PDF and XML.

### Annotated Text Data

* [BioCreAtIvE]() corpora:
  * [BioCreAtIvE 1](https://sourceforge.net/projects/biocreative/files/) - [paper](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-6-S1-S1) - 15,000 sentences (10,000 training and 5,000 test) annotated for protein and gene names. 1,000 full text biomedical research articles annotated with protein names and Gene Ontology terms.
  * [BioCreAtIvE 2](https://sourceforge.net/projects/biocreative/files/) - [paper](https://genomebiology.biomedcentral.com/articles/10.1186/gb-2008-9-s2-s1) - 15,000 sentences (10,000 training and 5,000 test, different from the first corpus) annotated for protein and gene names. 542 abstracts linked to EntrezGene identifiers. A variety of research articles annotated for features of protein–protein interactions.
  * [BioCreAtIvE V CDR Task Corpus (BC5CDR)](https://biocreative.bioinformatics.udel.edu/accounts/login/?next=/resources/corpora/biocreative-v-cdr-corpus/) - [paper](https://academic.oup.com/database/article/doi/10.1093/database/baw068/2630414) - 1,500 articles (title and abstract) published in 2014 or later, annotated for 4,409 chemicals, 5,818 diseases and 3116 chemical–disease interactions. Requires registration.
  * [BioCreative VI CHEMPROT Corpus](https://biocreative.bioinformatics.udel.edu/resources/corpora/chemprot-corpus-biocreative-vi/#chemprot-corpus-biocreative-vi:downloads) - [paper](https://pdfs.semanticscholar.org/eed7/81f498b563df5a9e8a241c67d63dd1d92ad5.pdf) - >2,400 articles annotated with chemical-protein interactions of a variety of relation types. Requires registration.
* [CRAFT](https://github.com/UCDenver-ccp/CRAFT) - [paper](https://link.springer.com/chapter/10.1007/978-94-024-0881-2_53) - 67 full-text biomedical articles annotated in a variety of ways, including for concepts and coreferences. Now on version 3.
* [n2c2 (formerly i2b2) Data](https://portal.dbmi.hms.harvard.edu/projects/n2c2-nlp/) - the Department of Biomedical Informatics (DBMI) at Harvard Medical School manages data for the National NLP Clinical Challenges and the Informatics for Integrating Biology and the Bedside challenges running since 2006. They require registration before access and use. Datasets include a variety of topics. See the [list of data challenges](https://portal.dbmi.hms.harvard.edu/data-challenges/) for individual descriptions.
* [NCBI Disease Corpus](https://www.ncbi.nlm.nih.gov/CBBresearch/Dogan/DISEASE/) - [paper](https://www.sciencedirect.com/science/article/pii/S1532046413001974) - a corpus of 793 biomedical abstracts annotated with names of diseases and related concepts from MeSH and [OMIM](https://omim.org/).
* [PubTator Central datasets](https://www.ncbi.nlm.nih.gov/research/pubtator/) - [paper](https://academic.oup.com/nar/article/47/W1/W587/5494727) - accessible through a RESTful API or FTP download. Includes annotations for >29 million abstracts and ∼3 million full text documents.
* [Word Sense Disambiguation (WSD)](https://wsd.nlm.nih.gov/) - [paper](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-12-223) - 203 ambiguous words and 37,888 automatically extracted instances of their use in biomedical research publications. Requires UTS account.

#### Protein-protein Interaction Annotated Corpora
Protein-protein interactions are abbreviated as PPI. The following sets are available in [BioC format](http://bioc.sourceforge.net/). The older sets (AIMed, BioInfer, HPRD50, IEPA, and LLL) are available courtesy of the [WBI corpora repository](http://corpora.informatik.hu-berlin.de) and were originally derived from the original sets by a [group at Turku University](http://mars.cs.utu.fi/PPICorpora/).

* [AIMed](http://corpora.informatik.hu-berlin.de/corpora/brat2bioc/aimed_bioc.xml.zip) - [paper](https://www.ncbi.nlm.nih.gov/pubmed/15811782) - 225 MEDLINE abstracts annotated for PPI.
* [BioC-BioGRID](http://bioc.sourceforge.net/BioC-BioGRID.html) - [paper](https://academic.oup.com/database/article/doi/10.1093/database/baw147/2884890) - 120 full text articles annotated for PPI and genetic interactions. Used in the BioCreative V BioC task.
* [BioInfer](http://corpora.informatik.hu-berlin.de/corpora/brat2bioc/bioinfer_bioc.xml.zip) - [paper](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-8-50) - 1,100 sentences from biomedical research abstracts annotated for relationships (including PPI), named entities, and syntactic dependencies. [Additional information and download links are here.](http://mars.cs.utu.fi/BioInfer/)
* [HPRD50](http://corpora.informatik.hu-berlin.de/corpora/brat2bioc/hprd50_bioc.xml.zip) - [paper](https://academic.oup.com/bioinformatics/article/23/3/365/236564) - 50 scientific abstracts referenced by the Human Protein Reference Database, annotated for PPI
* [IEPA](http://corpora.informatik.hu-berlin.de/corpora/brat2bioc/iepa_bioc.xml.zip) - [paper](http://psb.stanford.edu/psb-online/proceedings/psb02/abstracts/p326.html) - 486 sentences from biomedical research abstracts annotated for pairs of co-occurring chemicals, including proteins (hence, PPI annotations).
* [LLL](http://corpora.informatik.hu-berlin.de/corpora/brat2bioc/lll_bioc.xml.zip) - [paper](https://www.semanticscholar.org/paper/Learning-Language-in-Logic-Genic-Interaction-Nedellec/0863a9d71955341b7e1a6a6877d44d4f0bb22671) - 77 sentences from research articles about the bacterium _Bacillus subtilis_, annotated for protein–gene interactions (so, fairly close to PPI annotations). [Additional information is here.](http://genome.jouy.inra.fr/texte/LLLchallenge/#task1)

### Other Datasets

* [MIMIC-III](https://mimic.physionet.org/) - [paper](https://www.nature.com/articles/sdata201635) - deidentified health data from ~60,000 intensive care unit admissions. Requires completion of an online training course (CITI training) and acceptance of a data use agreement prior to use.

[Back to Top](#contents)

## Ontologies and Controlled Vocabularies

* [Disease Ontology](http://www.disease-ontology.org/) - [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4383880/) - an ontology of human diseases. Has cross-links to MeSH, ICD, NCI Thesaurus, SNOMED, and OMIM. Public domain. Available on [GitHub](https://github.com/DiseaseOntology/HumanDiseaseOntology) and on the [OBO Foundry](http://www.obofoundry.org/ontology/doid.html).
* [RxNorm](https://www.nlm.nih.gov/research/umls/rxnorm/index.html) - [paper](https://academic.oup.com/jamia/article/18/4/441/734170) - Normalized names for clinical drugs and drug packs, with combined ingredients, strengths, and form, and assigned types from the Semantic Network (see below). Released monthly.
* [SPECIALIST Lexicon](https://lexsrv3.nlm.nih.gov/Specialist/Summary/lexicon.html) - [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2247735/) - a general English lexicon that includes many biomedical terms. Updated yearly since 1994 and still updated as of 2019. Part of UMLS but does not require UTS account to download.
* [UMLS Metathesaurus](https://www.nlm.nih.gov/research/umls/knowledge_sources/metathesaurus/index.html) - [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC308795/) - Mappings between >3.8 million concepts, 14 million concept names, and >200 sources of biomedical vocabulary and identifiers. It's big. It may help to prepare a subset of the Metathesaurus with the [MetamorphoSys installation tool](https://www.nlm.nih.gov/research/umls/implementation_resources/metamorphosys/help.html) but we're still talking about ~30 Gb of disk space required for the 2019 release. [See the manual here](https://www.ncbi.nlm.nih.gov/books/NBK9684/). Requires UTS account.
* [UMLS Semantic Network](https://semanticnetwork.nlm.nih.gov/) - [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2447396/) - Lists of 133 semantic types and 54 semantic relationships covering biomedical concepts and vocabulary. Is the Metathesaurus too complex for your needs? Try this. Does not require UTS account to download.

[Back to Top](#contents)

## Data Models

Do you need a [data model](https://en.wikipedia.org/wiki/Data_model)? If you are working with biomedical data, then the answer is probably "Yes".

* [Biolink](https://biolink.github.io/biolink-model/) - [code](https://github.com/biolink/biolink-model) - a data model of biological entities. Provided as a [YAML](https://yaml.org/) file.

[Back to Top](#contents)

## Credits

[Credits](./CREDITS.md) for initial curators and sources.

## License

[License](./LICENSE) - CC0
