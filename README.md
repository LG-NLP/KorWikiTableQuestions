# KorWikiTableQuestions
This is the official repo for [Korean-Specific Dataset for Table Question Answering](https://arxiv.org/abs/2201.06223), a menuscript of LREC 2022, that contains Korean-specific datasets for table question answering

## Abstract
Existing question answering systems mainly focus on dealing with text data. However, much of the data produced daily is stored in the form of tables that can be found in documents and relational databases, or on the web. To solve the task of question answering over tables, there exist many datasets for table question answering written in English, but few Korean datasets. In this paper, we demonstrate how we construct Korean-specific datasets for table question answering: Korean tabular dataset is a collection of 1.4M tables with corresponding descriptions for unsupervised pre-training language models. Korean table question answering corpus consists of 70k pairs of questions and answers created by crowd-sourced workers. Subsequently, we then build a pre-trained language model based on Transformer and fine-tune the model for table question answering with these datasets. We then report the evaluation results of our model. We make our datasets publicly available via our GitHub repository and hope that those datasets will help further studies for question answering over tables, and for the transformation of table formats.

## Datasets
We introduce new two datasets: KorWikiTabular contains tables with their descriptions extracted from Korean Wikipedia articles, and KorWikiTQ consists of about 70k pairs of questions and answers over tables, generated according to question difficulty by paid crowdsourced workers.

### KorWikiTabular
#### Example
|Field|Content|설명|
|T | N서울타워| |
|U | https://ko.wikipedia.org/w/index.php?title=N서울타워| |
|Description | N서울타워의 층수는 P0, P1, P2, EZ, T1, T2, T3, T5로 총 8개 층으로 되어있다. P는 플라자의 약자이며 출입구와 약간의 상가로 구성되어있다. EZ는 익스프레스 존의 약자이며 흰색 기둥부분을 가리킨다. T는 타워의 약자이며 전망대와 스낵코너, 그리고 식당으로 구성되어 있다. 지하 1층에서 지상 5층까지는 서울타워 플라자의 시설이 있고 5층부터 타워 1층에서 타워 5층까지는 N서울타워의 시설이 있다. 남산 케이블카도 유명하다./가 있는 구역은 일반인의 출입이 금지된 구역이다.| |
|Caption | N서울타워_시설| |
|TBL | [["층수", "시설", "비고"], ["타워 7층", "엔그릴/기계실", "양식당 '엔그릴'이며 이곳에서는 개성과 인천의 관측도 가능하다. 특히 이곳은 48분당 한바퀴를 도는 형태로 되어있다."], ["타워 6층", "N칼국수,전망대", "N칼국수식당은 2015년 만들어 주인사업이고, 50인의 고객을 수용할 수 있다. 또한 휴전선까지 관측 가능하다"], ["타워 5층", "전망대, N기프트, N포토, 위니비니", "디지털 전망대와 상행 엘리베이터가 있다."], ["타워 4층", "전망대, N포토 스튜디오, 하늘 화장실, 투썸커피", "아날로그 전망대와 하행 엘리베이터가 있다."], ["타워 3층", "한쿡", "뷔페식 한식당 '한쿡'이다. 이곳에서는 서울 시내까지만 보인다."], ["타워 2층", "루프테라스, 더 플레이스 다이닝", "루프테라스, 더 플레이스 다이닝이 있다."], ["타워 1층", "치켓부스, 푸드오클락, N버거, N테라스, N기프트, 투썸커피, 올리브영, 포토 스토리", "N으로 시작하는 명칭들이 있다."], ["5층", "전망대 가는 길, 헬로키티아일랜드, 썬토이 박물관, 안내데스크, N기프트, N스위트바, 투썸커피, 화장실", "N으로 시작하는 명칭들이 있다."], ["4층", "계절밥상, 게임플라자, 호식이두마리치킨, 아참, 러브터널, 석양존, 스타토토, 스타포토, 포토카드사진기, 유후랜드, 올레드 웨이브, 3D체험관, 화장실", "게임방, 치킨집, 미디어 시설 등이 있다."], ["2층", "본 우리반상, 사랑의서약 사진기, 올레드 서클, 화장실", "본 우리반상, 사랑의서약 사진기, 올레드 서클, 화장실이 있다."], ["1층", "스타벅스, K명품관, 솔나라, 공차, 서울타워 기념품샵, 린린랜드프로포즈 계단, 사랑의서약 사진기, 올레드 터널, 올레드 파노라마, 반월당고로케, 화장실", "커피집, 기념품샵 등이 있어 화장실도 있다."], ["지하 1층 (로비)", "한복문화체험관", "대한민국의 전통인 한복문화를 체험할 수 있다."]]| |

### KorWikiTQ
#### Example
Will be updated soon

## Citation
Please cite our paper if you use KorWikiTabular or KorWikiTQ dataset for research :

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
