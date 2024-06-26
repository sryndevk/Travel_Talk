# 실시간 대화 요약 & 컨텐츠 추천 봇: TravelTalk


## 1. Introduction

![image](https://user-images.githubusercontent.com/28976334/217152562-3f970d1e-6b69-460e-8cd1-01c0c1409c1a.png)


### Members

|팀원1|팀원2|팀원3|Lynxzdevk (ME)|팀원5|
|:---:|:---:|:---:|:---:|:---:|
| <img src='https://avatars.githubusercontent.com/u/97166760?v=4' height=80 width=80px></img> | <img src='https://avatars.githubusercontent.com/u/33012030?v=4' height=80 width=80px></img> | <img src='https://avatars.githubusercontent.com/u/87929279?v=4' height=80 width=80px></img> | <img src='https://avatars.githubusercontent.com/u/28976334?v=4' height=80 width=80px></img> | <img src='https://avatars.githubusercontent.com/u/49403520?v=4' height=80 width=80px></img> |
| [![Git Badge](http://img.shields.io/badge/-Github-black?style=flat-square&logo=github)](https://github.com/khs0415p) | [![Git Badge](http://img.shields.io/badge/-Github-black?style=flat-square&logo=github)](https://github.com/papari1123) | [![Git Badge](http://img.shields.io/badge/-Github-black?style=flat-square&logo=github)](https://github.com/coderJoon) | [![Git Badge](http://img.shields.io/badge/-Github-black?style=flat-square&logo=github)](https://github.com/lynxzdevk) | [![Git Badge](http://img.shields.io/badge/-Github-black?style=flat-square&logo=github)](https://github.com/iknocho) |

### Contribution

- [`팀원1`](https://github.com/khs0415p) &nbsp; Front/Back-end 구현 • ElasticSearch 구현
- [`팀원2`](https://github.com/papari1123) &nbsp; Product Manager(PM) • Dialogue summarization 고도화
- [`팀원3`](https://github.com/coderJoon) &nbsp; Dense retriever baseline 학습 및 평가 • ICT 응용기법 학습 및 평가 데이터 제작
- [`Lynxzdevk (ME)`](https://github.com/siryuon) &nbsp; Front/Back-end 구현 • Dialogue summarization 및 metric 구현
- [`팀원5`](https://github.com/iknocho) &nbsp; Data crawling scheduler 구현 • MongoDB 적용 • Retriever model 구현

### Project Tree

```
|-- app
|   |-- assets
|   |-- src
|   |   |-- elastic
|   |   └-- models
|   |-- templates
|   |-- app.py
|   |-- config.py
|   └-- mongodb.py
|-- train
|   |-- summary
|   └-- retriever
└-- monstache
    └-- mongo-elastic.toml
```

## 2. Model

### KoBART
![image](https://user-images.githubusercontent.com/28976334/217154805-074a1273-57d5-4a8b-a5ec-7a5bf6d0f78e.png)
#### Result
![image](https://user-images.githubusercontent.com/28976334/217692822-873a5243-a78b-4d94-8ba8-75e3465a6147.png)

### ColBERT
![image](https://user-images.githubusercontent.com/28976334/217154876-e0783607-28ef-489c-903b-841923acb695.png)
#### Result
![image](https://user-images.githubusercontent.com/28976334/217692905-5b401b6a-a82a-4359-b55f-adbe1a0b6b5c.png)

## 3. Flow Chart

### System Architecture

![image](https://user-images.githubusercontent.com/28976334/217692565-47e03ab8-0eb9-4187-ad1f-bbd61a274c59.png)

### Pipeline

![image](https://user-images.githubusercontent.com/28976334/217154026-2a9beaa8-0863-4df4-b3aa-8e57ef452e9f.png)

## 4. How to Use

### Install Requirements

```bash
pip install -r requirements.txt
```

### Getting Started

- Summary model train
```python
python ./train/summary/train.py
```

- Retriever model train
```python
python ./train/retriever/train.py
```

- Run chat app with model server
```python
python ./app.py
python ./src/models/summary_model.py
python ./src/models/retriever_model.py
```


## 5. Demo 
![image](https://user-images.githubusercontent.com/28976334/217154127-3c9c578d-63d2-486d-8ecf-fce637c39e29.png)
- Video Link: [YouTube](https://youtu.be/byFroRoArCY)

## 6. Reference
- [Dense Passage Retrieval for Open-Domain Question Answering](https://arxiv.org/pdf/2004.04906.pdf)
- [Latent Retrieval for Weakly Supervised Open Domain Question Answering](https://arxiv.org/pdf/1906.00300.pdf)
- [ColBERT: Efficient and Effective Passage Search via Contextualized Late Interaction over BERT](https://arxiv.org/pdf/2004.12832.pdf)
- [네이버 ColBERT 사용방법](https://tv.naver.com/v/23650668)
- [Reference and Document Aware Semantic Evaluation Methods for Korean Language Summarization](https://arxiv.org/pdf/2005.03510.pdf)
- [Better Fine-Tuning by Reducing Representational Collapse](https://arxiv.org/pdf/2008.03156.pdf)
- [Momentum Calibration for Text Generation](https://arxiv.org/pdf/2212.04257v1.pdf)
- 요약 관련 Survey 자료 : https://github.com/uoneway/Text-Summarization-Repo
- 요약 모델 (KoBART) baseline : https://github.com/seujung/KoBART-summarization
- 요약 모델 성능 개선 방법 (Scatterlab) : https://tech.scatterlab.co.kr/alaggung-dlaggung-dialog-summary/ 

