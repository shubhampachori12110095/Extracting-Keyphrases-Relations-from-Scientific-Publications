# semeval2017-ScienceIE

Scripts for SemEval 2017 ScienceIE task (Task 10).
Please contact the task organisers on the ScienceIE mailing list (scienceie@googlegroups.com) if there are any problems with using the scripts

Scripts contained are eval.py, for evaluating performance on the task, and util.py, for reading parsing ScienceDirect .xml files

##Requirements:
* Python 3
* sklearn
* xml.sax

## Script usage:
* eval.py: evaluation script. Usage: ```python eval.py <gold folder> <pred folder> <remove rel>```
    * gold folder (optional): (default: "data/dev/") folder containing the gold standard files distributed by the SemEval 2017 Task 10 organisers, in .ann format.
    * pred folder (optional): (default: "data_pred/dev/") folder containing the prediction files, which should be in the same format as the gold files. Note that the evaluation script ignores IDs and surface forms and only judges based on the provided character offsets.
    * remove rel (optional): "rel" or "" (default). This is for removing relation annotations if you want to test performance for keyphrase boundary identification and keyphrase classification only.
* util.py: script containing utilities for parsing the original ScienceDirect .xml files to obtain text only and for parsing .ann files and looking up spans in corresponding .txt files
    
## References:
* SemEval task: https://scienceie.github.io/
* .ann format: http://brat.nlplab.org/standoff.html
* sklearn: http://scikit-learn.org/
* ScienceDirect: http://www.sciencedirect.com/