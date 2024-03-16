<h1 align="center"> 🐾 반려동물 의료 챗봇 서비스 </h1>
<h4 align="center"> 2023-1학기 자기주도 진로설계 프로젝트 </h4>

## Introduction

- 주제: 반려동물 의료 챗봇 서비스 개발 
- 분석 기간: 2023.03 ~ 2023.06
- 데이터 출처 및 제공
    - 네이버 지식iN에 등록된 '전문 수의사 답변' 기반 질문-답변 데이터를 크롤링하여 사용
- 참여자
    - [송지빈](https://github.com/jibin86)
    - [정다운](https://github.com/daunJJ)
    - [정재원](https://github.com/havehill)

<br>

## 데이터 전처리 
### 데이터 전처리
- 네이버 지식iN에서 질문자가 ‘제목’과 ‘내용’을 따로 작성
    
    → ‘제목’에 질문의 내용을 적는 경우가 많아 ‘제목’과 ‘내용’을 하나의 질문으로 통합
    
- 하나의 ‘질문’에 2개 이상의 ‘답변’이 달린 경우
    
    → ‘답변’을 분리해 2개의 질문-답변 쌍으로 구성
    
- ‘답변’에 삽입된 수의사 인사말 삭제

### 데이터 라벨링 
- GPT-3.5 turbo API를 이용하여 질문 데이터에 대해 라벨링 진행
  
- 대분류(동물 구분), 중분류(진료과)를 통해 총 125개의 카테고리로 분류

- 모델 적합을 위해 데이터를 3가지의 파일로 구분
  - label-숫자 쌍 파일 / label-Answer쌍 파일 / label-Question쌍 파일
  
## 모델 학습
### Ko-BERT 
- 사용 목적: 질문에 대한 적절한 라벨을 예측하여 매핑 후 수의사의 답변 제공 
- 학습 방법: pre-trained ko-BERT를 분류 task에 맞게 fine-tuning

   <img src="https://github.com/daunJJ/daunJJ/assets/109944763/98ed14dc-2e2d-4035-bc67-33f96b145150" width="350" height= "300"/>

## 웹 구현
- 챗봇 화면을 디자인한 후 HTML, CSC, javascript를 작성하여 웹 서비스 화면을 구현
- flask의 ngrok을 사용하여 API를 개방
  
  <img src="https://github.com/daunJJ/daunJJ/assets/109944763/9309d2e7-1ed5-415f-a614-b271f9dd1c04" width="400" height= "300"/>

