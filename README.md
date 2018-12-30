<p align="center"> <a href="https://github.com/logpai"> <img src="https://github.com/logpai/logpai.github.io/blob/master/img/logpai_logo.jpg" width="500" height="125"/> </a>
</p>


# Logparser  
[![Documentation Status](https://readthedocs.org/projects/logparser/badge/?version=latest)](https://logparser.readthedocs.io/en/latest/?badge=latest)
[![license](https://img.shields.io/badge/license-MIT-green.svg)](./LICENSE.md)

Logparser provides a toolkit and benchmarks for automated log parsing, which is a crucial step towards structured log analytics. By applying logparser, users can automatically learn event templates from unstructured logs and convert raw log messages into a sequence of structured events. In the literature, the process of log parsing is sometimes refered to as message template extraction, log key extraction, or log message clustering.

<p align="center"><img src="./docs/img/example.png" width="502"><br>An illustrative example of log parsing</p>

:point_right: Read the docs: https://logparser.readthedocs.io

:telescope: If you use any of our tools or benchmarks in your research for publication, please kindly cite the following papers.
+ [**ICSE'19**] Jieming Zhu, Shilin He, Jinyang Liu, Pinjia He, Qi Xie, Zibin Zheng, Michael R. Lyu. [Tools and Benchmarks for Automated Log Parsing](https://arxiv.org/pdf/1811.03509.pdf). *To appear in International Conference on Software Engineering (ICSE)*, 2019.
+ [**DSN'16**] Pinjia He, Jieming Zhu, Shilin He, Jian Li, Michael R. Lyu. [An Evaluation Study on Log Parsing and Its Use in Log Mining](https://jiemingzhu.github.io/pub/pjhe_dsn2016.pdf). *IEEE/IFIP International Conference on Dependable Systems and Networks (DSN)*, 2016.



### Log parsers currently available:

| Tools | References |
| :--- | :--- |
| SLCT | [**IPOM'03**] Risto Vaarandi. [A Data Clustering Algorithm for Mining Patterns from Event Logs](http://www.quretec.com/u/vilo/edu/2003-04/DM_seminar_2003_II/ver1/P12/slct-ipom03-web.pdf), 2003 |
| AEL | [**QSIC'08**] Zhen Ming Jiang, Ahmed E. Hassan, Parminder Flora, Gilbert Hamann. [Abstracting Execution Logs to Execution Events for Enterprise Applications](https://www.researchgate.net/publication/4366728_Abstracting_Execution_Logs_to_Execution_Events_for_Enterprise_Applications_Short_Paper), 2008<br> [**JSME'08**] Zhen Ming Jiang, Ahmed E. Hassan, Gilbert Hamann, Parminder Flora. [An Automated Approach for Abstracting Execution Logs to Execution Events](http://www.cse.yorku.ca/~zmjiang/publications/jsme2008.pdf), 2008 |
| IPLoM | [**KDD'09**] Adetokunbo Makanju, A. Nur Zincir-Heywood, Evangelos E. Milios. [Clustering Event Logs Using Iterative Partitioning](https://web.cs.dal.ca/~makanju/publications/paper/kdd09.pdf), 2009<br> [**TKDE'12**] Adetokunbo Makanju, A. Nur Zincir-Heywood, Evangelos E. Milios. [A Lightweight Algorithm for Message Type Extraction in System Application Logs](http://ieeexplore.ieee.org/abstract/document/5936060/), 2012 |
| LKE | [**ICDM'09**] Qiang Fu, Jian-Guang Lou, Yi Wang, Jiang Li. [Execution Anomaly Detection in Distributed Systems through Unstructured Log Analysis](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/DM790-CR.pdf), 2009 |
| LFA | [**MSR'10**] Meiyappan Nagappan, Mladen A. Vouk. [Abstracting Log Lines to Log Event Types for Mining Software System Logs](http://www.se.rit.edu/~mei/publications/pdfs/Abstracting-Log-Lines-to-Log-Event-Types-for-Mining-Software-System-Logs.pdf), 2010|
| LogSig | [**CIKM'11**] Liang Tang, Tao Li, Chang-Shing Perng. [LogSig: Generating System Events from Raw Textual Logs](https://users.cs.fiu.edu/~taoli/pub/liang-cikm2011.pdf), 2011 |
| SHISO | [**SCC'13**] Masayoshi Mizutani. [Incremental Mining of System Log Format](http://ieeexplore.ieee.org/document/6649746/), 2013|
| LogCluster | [**CNSM'15**] Risto Vaarandi, Mauno Pihelgas. [LogCluster - A Data Clustering and Pattern Mining Algorithm for Event Logs](http://dl.ifip.org/db/conf/cnsm/cnsm2015/1570161213.pdf), 2015 |
| LenMa | [**CNSM'15**] Keiichi Shima. [Length Matters: Clustering System Log Messages using Length of Words](https://arxiv.org/pdf/1611.03213.pdf), 2015. |
| LogMine | [**CIKM'16**] Hossein Hamooni, Biplob Debnath, Jianwu Xu, Hui Zhang, Geoff Jiang, Adbullah Mueen. [LogMine: Fast Pattern Recognition for Log Analytics](http://www.cs.unm.edu/~mueen/Papers/LogMine.pdf), 2016 |
| Spell | [**ICDM'16**] Min Du, Feifei Li. [Spell: Streaming Parsing of System Event Logs](https://www.cs.utah.edu/~lifeifei/papers/spell.pdf), 2016 |
| Drain | [**ICWS'17**] Pinjia He, Jieming Zhu, Zibin Zheng, and Michael R. Lyu. [Drain: An Online Log Parsing Approach with Fixed Depth Tree](https://jiemingzhu.github.io/pub/pjhe_icws2017.pdf), 2017 |
| MoLFI | [**ICPC'18**] Salma Messaoudi, Annibale Panichella, Domenico Bianculli, Lionel Briand, Raimondas Sasnauskas. [A Search-based Approach for Accurate Identification of Log Message Formats](http://publications.uni.lu/bitstream/10993/35286/1/ICPC-2018.pdf), 2018 |


### Usage
Please follow the [installation steps](https://logparser.readthedocs.io/en/latest/installation/dependency.html) and [demo](https://logparser.readthedocs.io/en/latest/demo.html) in the docs to get started.


### Data
--------------
In [data](https://github.com/logpai/logparser/tree/dev/data), there are 11 datasets for you to play with. Each dataset contains several text files.
* rawlog.log: The raw log messages with ID. "ID\tword1 word2 word3"
* template[0-9]+: The log messages belong to a certain template.
* templates: The text of templates.


### Quick Start
--------------
***Input***: A raw log file. Each line of the file follows "ID\tword1 word2 word3" <br />
***Output***: Two parts. One is splitted log messages (only contains log ID for simplicity) in different text files. The other is the ***templates*** file which contains all templates. <br />

***Examples***: Before running the examples, please copy the parser source file to the same directory.
* [Example1](https://github.com/logpai/logparser/blob/dev/demo/example1.py): This file is a simple example to demonstrate the usage of Drain. The usage of other log parsers is similar.
* [Example2](https://github.com/logpai/logparser/blob/dev/demo/example2.py): This file is to demonstrate the usage of POP.
* [Example3](https://github.com/logpai/logparser/blob/dev/demo/example3.py): This file is used to evaluate the performance of LogSig. It iterates 10 times and record several important information (e.g., TP, FP, time). To play with your own dataset, you could modify the path and files name in the code. You should also modify the path for ground truth data in [RI_precision](https://github.com/logpai/logparser/blob/dev/demo/RI_precision.py). For the ground truth data format, you can refer to our provided [datasets](https://github.com/logpai/logparser/blob/dev/data/).
* [Evaluation of LogSig](https://github.com/logpai/logparser/tree/dev/demo/LogSigEvaluation): This folder provides a package for you to evaluate the LogSig log parser on 2k HDFS dataset. You could simply run the [evaluateLogSig.py](https://github.com/logpai/logparser/blob/dev/demo/LogSigEvaluation/evaluateLogSig.py) file.

<br /> For SLCT, because it is based on the original C code, the running example is [here](https://github.com/logpai/logparser/blob/dev/logparser/SLCT/demo/SLCT_demo_BGL/precision_10_times.py). This program is platform-dependent because the .so files are only valid in Linux.


### Publications about logparser
+ [**ICSE'19**] Jieming Zhu, Shilin He, Jinyang Liu, Pinjia He, Qi Xie, Zibin Zheng, Michael R. Lyu. [Tools and Benchmarks for Automated Log Parsing](https://arxiv.org/pdf/1811.03509.pdf). To appear in International Conference on Software Engineering (ICSE), 2019.
+ [**TDSC'18**] Pinjia He, Jieming Zhu, Shilin He, Jian Li, Michael R. Lyu. [Towards Automated Log Parsing for Large-Scale Log Data Analysis](https://jiemingzhu.github.io/pub/pjhe_tdsc2017.pdf). IEEE Transactions on Dependable and Secure Computing (TDSC), 2018.
+ [**ICWS'17**] Pinjia He, Jieming Zhu, Zibin Zheng, Michael R. Lyu. [Drain: An Online Log Parsing Approach with Fixed Depth Tree](https://jiemingzhu.github.io/pub/pjhe_icws2017.pdf). IEEE International Conference on Web Services (ICWS), 2017.
+ [**DSN'16**] Pinjia He, Jieming Zhu, Shilin He, Jian Li, Michael R. Lyu. [An Evaluation Study on Log Parsing and Its Use in Log Mining](https://jiemingzhu.github.io/pub/pjhe_dsn2016.pdf). IEEE/IFIP International Conference on Dependable Systems and Networks (DSN), 2016.


### Acknowledgement
Logparser is implemented based on a number of existing open-source projects:
+ [SLCT](http://ristov.github.io/slct/) (C++)
+ [LogCluster](https://github.com/ristov/logcluster) (perl)
+ [LenMa](https://github.com/keiichishima/templateminer) (python 2)
+ [MoLFI](https://github.com/SalmaMessaoudi/MoLFI) (python 3)

### Feedback
For any questions or feedback, please post to [the issue page](https://github.com/logpai/logparser/issues).


### License
--------
[The MIT License (MIT)](https://github.com/logpai/logparser/blob/dev/LICENSE.md)

Copyright © 2018, [LogPAI](https://github.com/logpai), CUHK
