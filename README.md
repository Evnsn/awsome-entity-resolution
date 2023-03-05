# (_working progress_) Awesome Entity Resolution [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

> A collection of awesome resources regarding Entity Resolution.

# Table of Contents

<!-- * What is Record Linkage? -->

- [Books](#books)
- [Papers](#papers)
- Frameworks
<!-- * Datasets -->
- Projects
- Miscellaneous

## :point_right: What's Record Linkage?

...

## :books: Books

1. [Data Matching: Concepts and Techniques for Record Linkage, Entity Resolution, and Duplicate Detection](https://link.springer.com/book/10.1007/978-3-642-31164-2) by Peter Christen (2012)
2. [Data Quality and Record Linkage Techniques](https://link.springer.com/book/10.1007/0-387-69505-2) by Thomas N. Herzog, Fritz J. Scheuren & William E. Winkler (2007)

## :page_with_curl: Papers

### Surveys

- 2020 | An Overview of End-to-End Entity Resolution for Big Data | Vassilis Christophides, et al. | [`pdf`](https://arxiv.org/pdf/1905.06397.pdf)
- 2012 | A Survey of Indexing Techniques for Scalable Record Linkage and Deduplication | Peter Christen | [`pdf`](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=5887335)

### Entity Matching Management Systems

- 2016 | Magellan: Toward Building Entity Matching Management Systems | Pradap Konda, et al. | [`pdf`](http://www.vldb.org/pvldb/vol9/p1197-pkonda.pdf) | [`git`](https://github.com/anhaidgroup/py_entitymatching)

### Indexing

- [Corleone: Hands-Off Crowdsourcing for Entity Matching](https://pages.cs.wisc.edu/~anhai/papers/corleone-sigmod14.pdf), 2009

#### Debugging of blocking

- [MatchCatcher: A Debugger for Blocking in Entity Matching](https://pages.cs.wisc.edu/~anhai/papers1/matchcatcher-edbt18.pdf), 2018

### Pair compairinson

...

### Miscellaneous (impactful papers?)

- 1969 | A Theory for Record Linkage | Fellegi, I.P., Sunter, A.B. | [`pdf`](https://courses.cs.washington.edu/courses/cse590q/04au/papers/Felligi69.pdf)

### Classification

#### Supervised

...

#### Unsupervised

- 2019 | Using a Probabilistic Model to Assist Merging of Large-Scale Administrative Records | T. Enamorado, et al. | [`pdf`](https://imai.fas.harvard.edu/research/files/linkage.pdf) | [`GiT`](https://github.com/kosukeimai/fastLink)

### Clustering /

- 2020 | Entity Matching in the Wild: A Consistent and Versatile Framework to Unify Data in Industrial Applications | Yan Yan, et al. | [`pdf`](https://dl.acm.org/doi/pdf/10.1145/3318464.3386143)

## :hammer: Frameworks
Table 1 is a composition of tools presented in [(2020, V. Christophides)](https://arxiv.org/pdf/1905.06397.pdf), [(2015, P. Konda)](http://www.vldb.org/pvldb/vol9/p1197-pkonda.pdf) and [J535D165/data-matching-software](https://github.com/J535D165/data-matching-software).

<!-- TODO:
* Move 
  * 'scaling column', right of 'language' 
* Move Paper?
 -->

**<ins>Table 1:</ins>** 
***Blocking:** Attribute equivalence (AE), Blocking index (BI), Canopy clustering (CC), Canopy index (CI), Clustering (C), Expectation maximization (EM), Full index (FI), Hash-based (HB), Hybrid (H), Induction (I), Predicate-based (PB), Probabilistic (P), Relational clustering (RC), Rule-based (RB), Sorted neighborhood (SN) Sorting index (SoI), Stringmap index (StI), Suffixarray index (SuI). 
**Matching:** Agglomerative hierarchical clustering-based (AHC), Decision trees (DT), Farthest First (FF), Fellegi-Sunter (FS), k-Nearest-neighbour (KNN), Logistic regression (LR), Optimal threshold (OT), Support vector machine (SVM) TwoStep (TS).*

| Tools |Blocking|Matching|Clustering|  | UI | Scaling | Language | OSS | GiT/Inst | Paper |
|:--|:--|:--|:--|:--| :--|:--|:--|:--|:--|:--
| Active Atlas  |HB|DT|---|  | GUI, CMD |:x:|Java|:x:|---|---|
|Atyimo|---|---|---||---|---|Python|---|[`git`](https://github.com/pierrepita/atyimo)|---|
| BigMatch      |AE, RB|:x:|---|  | CMD |:heavy_check_mark:|C|:x:|---| [(2002, W. E. Yancey)](https://www.census.gov/content/dam/Census/library/working-papers/2002/adrm/rrc2002-01.pdf)     
| D-Dupe        |AE|RC|---|  | GUI, CMD |:x:|C#|:x:|---|[(2006, M. Bilgic)](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4035746)|    
| Dedoop |AE, SN| DT, LR, SVM, etc| --- |  | GUI | Hadoop | Java|:x:|[`install`](https://dbs.uni-leipzig.de/howto_dedoop)| [(2012, L Kolb)](https://dbs.uni-leipzig.de/file/Dedoop.pdf)|
| Dedupe |CC, PB| AHC | :x: |  | API, CMD | :heavy_check_mark:| Python | :heavy_check_mark:| [`git`](https://github.com/dedupeio/dedupe)|[(2003, M. Bilenko)](https://www.cs.utexas.edu/~ml/papers/marlin-kdd-03.pdf), [(2006, M. Bilenko)](https://www.cs.utexas.edu/~ml/papers/marlin-dissertation-06.pdf)|
| DuDe    | SN | RB |:x:|  |CMD|:x:|Java|:heavy_check_mark:|[`install`](https://hpi.de/en/naumann/projects/data-quality-and-cleansing/dude-duplicate-detection.html)|[(2010, U. Draisbach)](https://www.comp.nus.edu.sg/~vldb2010/proceedings/files/vldb_2010_workshop/QDB_2010/Paper5_Draisbach_Naumann.pdf)
|Duke|:heavy_check_mark:|:heavy_check_mark:|---||CMD|:x:|Java|---|[`git`](https://github.com/larsga/Duke)|Blog: [(2011, L. Marius)](https://www.garshol.priv.no/blog/217.html)|
| FAMER |:x:|:x:|:heavy_check_mark:|  |---|Apache Flink|---|---|[`gitlab`](https://git.informatik.uni-leipzig.de/dbs/FAMER/) |[(2018, A Saeedi)](https://dbs.uni-leipzig.de/file/FAMER-2407-8454-1-SM.pdf)|
| fastLink|:x:|---|---|  |API|:heavy_check_mark:|R|:heavy_check_mark:|[`git`](https://github.com/kosukeimai/fastLink)|[(2017, T. Enamorado)](https://imai.fas.harvard.edu/research/files/linkage.pdf)|
| Febrl |BI, CI, FI, SoI, StI, SuI, Q-gram|FS, OT, K-means, FF, SVM, TS|:x:|  |GUI|:grey_question:|Python|:heavy_check_mark:|[`install`](https://sourceforge.net/projects/febrl/)|[(2013, P. Christen)](https://unstats.un.org/unsd/demographic/meetings/wshops/Ethiopia_14_Sept_09/Manuals/Peter.christen-febrl-demo.pdf)|
| FRIL |AE, SN|EM|:x:|  |GUI|:grey_question:|Java|:heavy_check_mark:|[`install`](https://fril.sourceforge.net/download.html)|[(2008, P Jurczyk)](https://onlinelibrary.wiley.com/doi/full/10.1002/bdra.20521)|
| JedAI|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:||GUI|Apache Spark|Java|:heavy_check_mark:|[`git`](https://github.com/scify/JedAIToolkit)|[(2020, G. Papadakis)](https://openproceedings.org/2020/conf/edbt/paper_273.pdf)|
| KnoFuss|:heavy_check_mark:|:heavy_check_mark:|---||---|:x:|Java|---|---|[(2008, A. Nikolov)](http://oro.open.ac.uk/28010/5/27994.pdf)|
| LIMES|---|---|---||GUI|:x:|Java|:heavy_check_mark:|[`git`](https://github.com/dice-group/LIMES)|[(2011, A. C. N. Ngomo)](https://www.ijcai.org/Proceedings/11/Papers/385.pdf)|
| Magellan|:heavy_check_mark:|:heavy_check_mark:|:x:| |API, GUI|Apache Spark|Python|:heavy_check_mark:|[`git`](https://github.com/anhaidgroup/py_entitymatching)|[(2016, P. Konda)](https://arxiv.org/pdf/1905.06397.pdf)
| MARLIN|CC|DT, SVM|---|  |:x:|---|---|---|---|[(2004, M. Bilenko)](https://www.cs.utexas.edu/~ml/papers/marlin-aaaidc-04.pdf)|
| Merge Toolbox |AE, CC|P, EM|---|  |GUI|:x:|Java|:x:|[`install`](https://www.record-linkage.de/software/index.html)|[(2004, R. Schnell)](https://d-nb.info/1191659240/34)|
| MinoanER|:heavy_check_mark:|:heavy_check_mark:|:x:||GUI|Apache Spark|Java|:heavy_check_mark:|---| [(2019, V. Efthymiou)](https://arxiv.org/pdf/1905.06170.pdf)|
| NADEEF |---|RB|---|  |GUI|:x:|Java|:x:|---|[(2013, M. Dallachiesa)](https://cs.uwaterloo.ca/~ilyas/papers/NADEEFSigmod2013.pdf)|
| OYSTER|AE|RB|---|  |CMD|:x:|Java|:heavy_check_mark:|[`install`](https://sourceforge.net/projects/oysterer/)|[(2011, E. D. Nelson)](http://worldcomp-proceedings.com/proc/p2011/IKE5074.pdf)|
| PRIL|---|---|---||GUI|---|C#|---|[`git`](https://github.com/LSHTM-ALPHAnetwork/PIRL_RecordLinkageSoftware)|[(2018, C. T. Rentsch)](https://gatesopenresearch.org/articles/1-8/v1)|
| pydedupe|AE|KNN, K-means, RB|---||CMD|:x:|Python|:heavy_check_mark:|[`git`](https://github.com/gpoulter/pydedupe)|---|
| Reclin2|---|---|---||API|---|R|---|[`git`](https://github.com/djvanderlaan/reclin2)|---|
| RELAIS|---|---|---||GUI|---|R/Java|---|[`install`](https://www.istat.it/en/methods-and-tools/methods-and-it-tools/process/processing-tools/relais)| [(2006, M. Fortini)](https://www.istat.it/it/files/2011/03/FSTT_IQIS06_CR.pdf)|
|RLTK|---|---|---| |API|---|Python|:heavy_check_mark:|[`git`](https://github.com/usc-isi-i2/rltk)|---|
| Record Linkage (R)|AE|ML-based|---|  |CMD|:x:|R|:heavy_check_mark:|[`cran`](https://cran.r-project.org/web/packages/RecordLinkage/index.html)|[(2011, M Sariyar)](https://www.sciencedirect.com/science/article/pii/S1532046411000372)|
| Record Linkage (Python) |FI, BI, SN|DC, LR, SVM, K-means, EM|---| |API|:x:|Python|:heavy_check_mark:|[`git`](https://github.com/J535D165/recordlinkage)|2015, inspired by *FEBRL*|
| SERIMI|:heavy_check_mark:|:heavy_check_mark:|---||---|---|Ruby|---|[`git`](https://github.com/samuraraujo/SERIMI-RDF-Interlinking)|[(2015, S Araujo)](https://ieeexplore.ieee.org/document/6940278)|
| SERF|---|R-swoosh|---||CMD|:x:|Java|:x:|[`git`](https://github.com/trevorprater/serf)|[(2009, O. Benjelloun)](http://infolab.stanford.edu/serf/swoosh_vldbj.pdf)|
| Splink |:heavy_check_mark:|EM, etc?|:heavy_check_mark:| |API, GUI|Apache Spark|Python|:heavy_check_mark:|[`git`](https://github.com/moj-analytical-services/splink)|2019, same as *fastLink*|
| Silk|---|RB|---||GUI|Hadoop|Scala|:heavy_check_mark:|[`git`](https://github.com/silk-framework/silk), [`install`](http://silkframework.org/download)|[(2009, J. Volz)](http://events.linkeddata.org/ldow2009/papers/ldow2009_paper13.pdf)|
| TAILOR|AE, SN|P, C, H, I|---||GUI|:x:|Java|:x:|---|[(2002, M. G. Elfeky)](https://www.cs.purdue.edu/homes/ake/pub/TAILOR_ICDE2002.pdf)|
|WHIRL|---|---|---||CMD|:x:|C++|:x:|[`install`](https://www.cs.cmu.edu/~wcohen/whirl/)|[(2000, W.W Cohen)](https://www.sciencedirect.com/science/article/pii/S0004370299001022)|

## :pushpin: Miscellaneous
- List of [blog posts](https://www.robinlinacre.com/probabilistic_linkage/) on "Probabilistic Record Linkage" by Robin Linacre (Lead developer of Splink).
- TWD series
- GiT: [Data Matching software](https://github.com/J535D165/data-matching-software)
- Documentation: [FAst Multi-source Entity Resolution system (FAMER)](https://dbs.uni-leipzig.de/research/projects/object_matching/famer)
- *SERF* - Standford Entity Resolution Framework: [Homepage](http://infolab.stanford.edu/serf/)
- *Silk* - related [publications](http://silkframework.org/publications).
- *Magellan* - rlated [material](https://sites.google.com/site/anhaidgroup/current-projects/magellan).