<h1 align="center"> 🐾 반려동물 의료 챗봇 서비스 </h1>
<h4 align="center"> 2023-1학기 자기주도 진로설계 프로젝트 </h4>

## Introduction

- 주제: 반려동물 의료 챗봇 서비스 개발
- 목적: 반려동물 관련 질의응답에 특화된 챗봇을 개발하여, 반려인을 위한 비대면 진료 역할을 수행하고자 함
- 분석 기간: 2023.03 ~ 2023.06
- 데이터 출처 및 제공
    - 네이버 지식iN에 등록된 '전문 수의사 답변' 기반 질문-답변 데이터를 크롤링하여 사용
- 참여자
    - [송지빈](https://github.com/jibin86)
    - [정다운](https://github.com/daunJJ)
    - [정재원](https://github.com/havehill)

## Content 
**데이터 수집** 
- [네이버 지식iN 수의사 답변 Crawling](https://github.com/daunJJ/kobert-animal-chatbot/tree/master/crawling)

**데이터 전처리**
- [질문-답변 데이터 전처리](https://github.com/daunJJ/kobert-animal-chatbot/blob/master/preprocess/preprocess.ipynb)
- [데이터 라벨링 (Prompt Engineering)](https://github.com/daunJJ/kobert-animal-chatbot/blob/master/preprocess/labeling.ipynb)

**모델학습**
- [ko-BERT fine-tuning](https://github.com/daunJJ/kobert-animal-chatbot/tree/master/kobert-wellness-chatbot)

**웹 구현** 
- [챗봇 웹 서비스 구현](https://github.com/jibin86/Animal_Medical_Chatbot)
  
    <img src="https://github.com/daunJJ/daunJJ/assets/109944763/9309d2e7-1ed5-415f-a614-b271f9dd1c04" width="400" height= "300"/>

