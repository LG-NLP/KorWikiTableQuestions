# KorWikiTableQuestions
This is the official repo for [Korean-Specific Dataset for Table Question Answering](https://arxiv.org/abs/2201.06223), a menuscript of LREC 2022, that contains Korean-specific datasets for table question answering

## Abstract
Existing question answering systems mainly focus on dealing with text data. However, much of the data produced daily is stored in the form of tables that can be found in documents and relational databases, or on the web. To solve the task of question answering over tables, there exist many datasets for table question answering written in English, but few Korean datasets. In this paper, we demonstrate how we construct Korean-specific datasets for table question answering: Korean tabular dataset is a collection of 1.4M tables with corresponding descriptions for unsupervised pre-training language models. Korean table question answering corpus consists of 70k pairs of questions and answers created by crowd-sourced workers. Subsequently, we then build a pre-trained language model based on Transformer and fine-tune the model for table question answering with these datasets. We then report the evaluation results of our model. We make our datasets publicly available via our GitHub repository and hope that those datasets will help further studies for question answering over tables, and for the transformation of table formats.

## Datasets
We introduce new two datasets: KorWikiTabular contains tables with their descriptions extracted from Korean Wikipedia articles, and KorWikiTQ consists of about 70k pairs of questions and answers over tables, generated according to question difficulty by paid crowdsourced workers.

### KorWikiTabular

### KorWikiTQ



## Citation
Please cite our paper if you use KorWikiTabular or KorWikiTQ dataset for research, :

``` 
@article{jun2022korean,
  title={Korean-Specific Dataset for Table Question Answering},
  author={Jun, Changwook and Choi, Jooyoung and Sim, Myoseop and Kim, Hyun and Jang, Hansol and Min, Kyungkoo},
  journal={arXiv preprint arXiv:2201.06223},
  year={2022}
}
```

## License
Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
