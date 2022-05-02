# KorWikiTableQuestions
This is the official repo for [Korean-Specific Dataset for Table Question Answering](https://arxiv.org/abs/2201.06223), a menuscript of LREC 2022, that contains Korean-specific datasets for table question answering

## Abstract
Existing question answering systems mainly focus on dealing with text data. However, much of the data produced daily is stored in the form of tables that can be found in documents and relational databases, or on the web. To solve the task of question answering over tables, there exist many datasets for table question answering written in English, but few Korean datasets. In this paper, we demonstrate how we construct Korean-specific datasets for table question answering: Korean tabular dataset is a collection of 1.4M tables with corresponding descriptions for unsupervised pre-training language models. Korean table question answering corpus consists of 70k pairs of questions and answers created by crowd-sourced workers. Subsequently, we then build a pre-trained language model based on Transformer and fine-tune the model for table question answering with these datasets. We then report the evaluation results of our model. We make our datasets publicly available via our GitHub repository and hope that those datasets will help further studies for question answering over tables, and for the transformation of table formats.

## Datasets
We introduce new two datasets: KorWikiTabular contains tables with their descriptions extracted from Korean Wikipedia articles, and KorWikiTQ consists of about 70k pairs of questions and answers over tables, generated according to question difficulty by paid crowdsourced workers.

### KorWikiTabular
#### Example
|Field|Content|Note|
|---|---|---|
|T | N서울타워| Title|
|U | https://ko.wikipedia.org/w/index.php?title=N서울타워| Url|
|Description | N서울타워의 층수는 P0, P1, P2, EZ, T1, T2, T3, T5로 총 8개 층으로 되어있다. P는 플라자의 약자이며 출입구와 약간의 상가로 구성되어있다. EZ는 익스프레스 존의 약자이며 흰색 기둥부분을 가리킨다. T는 타워의 약자이며 전망대와 스낵코너, 그리고 식당으로 구성되어 있다. 지하 1층에서 지상 5층까지는 서울타워 플라자의 시설이 있고 5층부터 타워 1층에서 타워 5층까지는 N서울타워의 시설이 있다. 남산 케이블카도 유명하다./가 있는 구역은 일반인의 출입이 금지된 구역이다.| Description about table|
|Caption | N서울타워_시설| Headings if not exist table caption|
|TBL | [["층수", "시설", "비고"], <br>["타워 7층", "엔그릴/기계실", "양식당 '엔그릴'이며 이곳에서는 개성과 인천의 관측도 가능하다..."],<br> ["타워 6층", "N칼국수,전망대", "... 휴전선까지 관측 가능하다"],<br> ["타워 5층", "전망대, N기프트, N포토, 위니비니", "디지털 전망대와 상행 엘리베이터가 있다."],<br> ["타워 4층", "전망대, N포토 스튜디오, 하늘 화장실, 투썸커피", "아날로그 전망대와 하행 엘리베이터가 있다."],<br> ["타워 3층", "한쿡", "이곳에서는 서울 시내까지만 보인다."],<br> ["타워 2층", "루프테라스, 더 플레이스 다이닝", "루프테라스, 더 플레이스 다이닝이 있다."],<br>...]| Flattened table of 2D list|

### KorWikiTQ
#### Dataset Overview
||Total|Train|Dev|
|---|---|---|---|
|Example counts| 69,992|58,221 | 11,771|

#### Example
|Field|Content|Note|
|---|---|---|
|T | 축구 팀 코리아 은퇴식   2002년 11월부터 70경기 이상 대한민국 축구 국가대표팀 경기를 치룬 선수들에게 은퇴식을 거행하고 있다. 박지성은 2014년 7월 K리그 올스타전에서 은퇴경기를 했다.황선홍은 폴란드전 인터뷰에서 이번경기를 마지막 경기로 삼겠다라고 발켰다.이후 홍명보와 은퇴식을 했다.| Title with description|
|U | https://ko.wikipedia.org/w/index.php?title=축구_팀_코리아| Url|
|QAS | "qid": "22638_1", <br> "question": "2010년 8월 11일 대한민국 축구 국가대표팀 은퇴식을 거행한 선수는 누구인가요?",<br>"answer": "이운재" |Question-answering set |
|TBL | [["거행일","이름","포지션","등번호","경기","활동 기간","장소"],<br>["2002년 11월 20일","황선홍","공격수","18","103","1988–2002","서울월드컵경기장"],<br>["2002년 11월 20일","홍명보","수비수","20","136","1990–2002","서울월드컵경기장"],<br>["2010년 8월 11일","이운재","골키퍼","1","133","1994–2010","수원월드컵경기장"],<br>...]| Flattened table of 2D list|

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
