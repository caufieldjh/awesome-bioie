# awesome-bioie 

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of resources dedicated to Biomedical Information Extraction (BioIE).

Inspired by [awesome-nlp](https://github.com/keon/awesome-nlp). Please see that list for more resources relevant to Natural Language Processing in general.

Where possible, tools and resource entries include links to corresponding papers. If an open-access version of the paper is not available, this link should be either a PubMed citation entry or a link to another citation database.

_Please read the [contribution guidelines](contributing.md) before contributing. Please add your favourite resource by raising a [pull request](https://github.com/caufieldjh/awesome-bioie/pulls)._

## Contents
* [Research Overviews](#research-overviews)
* [Tutorials](#tutorials)
  * [Guides](#guides)
  * [Video Lectures and Online Courses](#video-lectures-and-online-courses)
  * [Books](#books)
* [Code Libraries](#code-libraries)
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
* [Credits](#credits)
* [License](#license)

## Research Overviews
[Back to Top](#contents)

## Tutorials
[Back to Top](#contents)

### Guides
[Back to Top](#contents)

### Video Lectures and Online Courses
[Back to Top](#contents)

### Books
[Back to Top](#contents)

## Code Libraries
[Back to Top](#contents)

## Tools, Platforms, and Services
[Back to Top](#contents)

### Annotation Tools
[Back to Top](#contents)

## Techniques
[Back to Top](#contents)

### Text Embeddings
[Back to Top](#contents)

#### Word Embeddings
[Back to Top](#contents)

#### Sentence and Language Model Based Word Embeddings
[Back to Top](#contents)

### Question Answering and Knowledge Extraction
[Back to Top](#contents)

## Datasets

Some of the datasets listed below require a [UMLS Terminology Services (UTS) account](https://www.nlm.nih.gov/databases/umls.html#license_request) to access. Please note that the license granted with the UTS account requires users to submit an annual report about their use of UMLS resources. This is less challenging than it sounds.

### Annotated Text Data
* [n2c2 (formerly i2b2) Data](https://portal.dbmi.hms.harvard.edu/projects/n2c2-nlp/) - the Department of Biomedical Informatics (DBMI) at Harvard Medical School manages data for the National NLP Clinical Challenges and the Informatics for Integrating Biology and the Bedside challenges running since 2006. They require registration before access and use. Datasets include a variety of topics. See the [list of data challenges](https://portal.dbmi.hms.harvard.edu/data-challenges/) for individual descriptions.
* [Word Sense Disambiguation (WSD)](https://wsd.nlm.nih.gov/) - [paper](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-12-223) - 203 ambiguous words and 37,888 automatically extracted instances of their use in biomedical research publications. Requires UTS account.

#### Protein-protein Interaction Annotated Corpora
Protein-protein interactions are abbreviated as PPI. The following sets are available in [BioC format](http://bioc.sourceforge.net/) and are available courtesy of the [WBI corpora repository](http://corpora.informatik.hu-berlin.de) and were originally derived from the original sets by a [group at Turku University](http://mars.cs.utu.fi/PPICorpora/).

* [AIMed](http://corpora.informatik.hu-berlin.de/corpora/brat2bioc/aimed_bioc.xml.zip) - [paper](https://www.ncbi.nlm.nih.gov/pubmed/15811782) - 225 MEDLINE abstracts annotated for PPI.
* [BioInfer](http://corpora.informatik.hu-berlin.de/corpora/brat2bioc/bioinfer_bioc.xml.zip) - [paper](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-8-50) - 1,100 sentences from biomedical research abstracts annotated for relationships (including PPI), named entities, and syntactic dependencies. [Additional information and download links are here.](http://mars.cs.utu.fi/BioInfer/)
* [HPRD50](http://corpora.informatik.hu-berlin.de/corpora/brat2bioc/hprd50_bioc.xml.zip) - [paper](https://academic.oup.com/bioinformatics/article/23/3/365/236564) - 50 scientific abstracts referenced by the Human Protein Reference Database, annotated for PPI
* [IEPA](http://corpora.informatik.hu-berlin.de/corpora/brat2bioc/iepa_bioc.xml.zip) - [paper](http://psb.stanford.edu/psb-online/proceedings/psb02/abstracts/p326.html) - 486 sentences from biomedical research abstracts annotated for pairs of co-occurring chemicals, including proteins (hence, PPI annotations).
* [LLL](http://corpora.informatik.hu-berlin.de/corpora/brat2bioc/lll_bioc.xml.zip) - [paper](https://www.semanticscholar.org/paper/Learning-Language-in-Logic-Genic-Interaction-Nedellec/0863a9d71955341b7e1a6a6877d44d4f0bb22671) - 77 sentences from research articles about the bacterium _Bacillus subtilis_, annotated for protein–gene interactions (so, fairly close to PPI annotations). [Additional information is here.](http://genome.jouy.inra.fr/texte/LLLchallenge/#task1)

[Back to Top](#contents)

### Other Datasets
[Back to Top](#contents)

## Ontologies and Controlled Vocabularies

* [RxNorm](https://www.nlm.nih.gov/research/umls/rxnorm/index.html) - [paper](https://academic.oup.com/jamia/article/18/4/441/734170) - Normalized names for clinical drugs and drug packs, with combined ingredients, strengths, and form, and assigned types from the Semantic Network (see below). Released monthly.
* [SPECIALIST Lexicon](https://lexsrv3.nlm.nih.gov/Specialist/Summary/lexicon.html) - [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2247735/) - a general English lexicon that includes many biomedical terms. Updated yearly since 1994 and still updated as of 2019. Part of UMLS but does not require UTS account to download.
* [UMLS Semantic Network](https://semanticnetwork.nlm.nih.gov/) - [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2447396/) - Lists of 133 semantic types and 54 semantic relationships covering biomedical concepts and vocabulary. Is the Metathesaurus too complex for your needs? Try this. Does not require UTS account to download.

[Back to Top](#contents)

## Credits

[Credits](./CREDITS.md) for initial curators and sources.

[Back to Top](#contents)

## License
[Back to Top](#contents)

[License](./LICENSE) - CC0
