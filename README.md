# B.eata 
https://shaded-chip-9ff.notion.site/B-eata-1e1b4a688e294510bac7bc16440c2054?pvs=4
## 1. 프로덕트 및 프로젝트 개요

### 1-1. 주제

<aside>
💡 ***식품 트렌드 인텔리전스(Food Trend Intelligence)***
식품 인기검색어 트렌드를 기반으로 상품 정보 및 상품평 분석 결과를 제공하는 데이터 프로덕트 개발

</aside>

### 1-2. 프로젝트 진행(24.06.03 → 24.06.27)

<aside>
💡 **Agile/Scrum Team**
매일 09:00 데일리스크럼 진행 / 개인별 포커스타임 지정해 한달간 진행

각 스프린트 종료 시 회고 및 미팅, 시작 미팅 진행


</aside>

### 1-3. 활용한 라이브러리 등 기술적 요소

| ✔ numpy | ✔ selenium | ✔ figma | ✔ Tableau Public |
| --- | --- | --- | --- |
| ✔ pandas | ✔ BeautifulSoup | ✔ AWS | ✔ Hugging Face |
| ✔ matplotlib | ✔ chardet | ✔ Amplify Studio | ✔ KcELECTRA |
| ✔ seaborn | ✔ collections | ✔ sklearn | ✔ BERT |
| ✔ konlpy | ✔ wordcloud | ✔ pytorch | ✔ SQL |
| ✔ transformer | ✔ stopwords | ✔ dynamoDB | ✔ undetected_chromedriver |

## 2. MVP(Minimum Viable Product)

### 2-1. 데이터 및 사용자 플로우 서비스 기획



### 2-2. UI/UX 기획 및 디자인



### 2-3. 프로토타입 웹사이트



### 2-4. 프로젝트 시연영상(QR)
![image](https://github.com/user-attachments/assets/2ecbd21c-9465-46ba-8d9c-867adee7c3f6)


---

## 3. 팀원 소개 및 역할

<aside>
💛 **남진아**

- Product Owner
- 서비스 기획 및 개발
- UI/UX 디자인 지원
- 인프라 구축 및 관리 (AWS)
- 데이터베이스 구성 및 데이터 관리
- 상품평 데이터 수집
- 키워드트렌드 데이터 모델링
- 키워드트렌드 인사이트 도출
- 상품정보비교 인사이트 도출
- 발표자료 제작 및 발표
</aside>

<aside>
💚 **이건**

- 서비스 기획
- 상품검색결과 상품평 데이터 수집
- 상품검색결과 상품평 데이터 전처리
- 상품정보비교 상품평 요약 모델링
- 키워드트렌드 인사이트 도출
- 프로젝트 인사이트 도출
- 컨텐츠 기획 및 작성

</aside>

<aside>
💙 **이재만** a.k.a 아뱅💡

- 서비스 기획
- UI/UX, 컨텐츠 기획 서브
- 키워드트렌드 데이터 수집 및 전처리
- 키워드트렌드 데이터 분석 및 모델링
- 키워드트렌드 인사이트 도출
- 상품정보비교 상품평 데이터 전처리 및 2,3차 감정분석 모델링
- 상품정보비교 감정분석 모델 파인튜닝 기획 및 진행
- 상품정보비교 감정분석 모델 결과분석 및 성능비교
</aside>

<aside>
🩷 **전세현**

- 서비스 기획 리드
- UI/UX 기획 리드
- 디자인 리드
- 키워드트렌드 이상치 제거
- 상품정보비교 상품평 데이터 전처리 및 1차 감정분석 모델링
- 키워드트렌드 인사이트 도출
- 상품정보비교 인사이트 도출
- 자료 취합 및 문서화
- 발표자료 제작
</aside>

---

## 4. 담당업무 - 프로젝트 수행 절차 및 방법

### 4-1. 사용 데이터

- 네이버 데이터랩
    - 2024년 상반기 전체 **‘식품’ 카테고리 인기검색어 데이터** 수집
    

- 쿠팡, 마켓컬리, 네이버쇼핑
    - 인기검색어를 해당 플랫폼에 검색 시 **정렬되는 랭킹상품**, **해당상품의 상품평 데이터** 수집
    
- 데이터 기본 정보
    - 데이터 수집 기간
        - 2024 상반기 (240101~240615)기간 반기(H1),분기(Q1,Q2),월별(M1~M6),일별(0601~06xx) 데이터
    - 전체 데이터에 대한 정보 (데이터 크기)
        - 인기검색어 `(11250309, 6)`
            
            
            ![기본정보](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/b9741fac-47a3-4dcb-ac30-f6085433b2c6/Untitled.png)
            
            기본정보
            
            ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/ba8e247a-38e8-42c4-a0b2-cdfc35c739f8/Untitled.png)
            
            ![결측치](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/2812e521-a3c6-4c0c-8bcd-c2fff1776b8a/Untitled.png)
            
            결측치
            
            ![기본통계량](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/2168357d-8ceb-4b57-a4a5-fd59e7cede45/Untitled.png)
            
            기본통계량
            
        - 상품검색결과 `(4988, 9)`
            
            
            ![기본정보](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/e796c6ac-a9b7-4b17-9fdf-0768657efd19/Untitled.png)
            
            기본정보
            
            ![결측치 확인](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/29325c97-b04e-47f4-bb84-0198d755b020/Untitled.png)
            
            결측치 확인
            
            ![기본통계량](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/9507579a-1e41-4618-b81a-990267db06b6/Untitled.png)
            
            기본통계량
            
        - 상품평 `(13482, 6)`
            
            
            ![기본정보](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/6b941967-e600-4c0d-9096-8b0f4ee579cd/Untitled.png)
            
            기본정보
            
            ![결측치 확인](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/f4613fd7-5b46-422d-a764-63618f880110/Untitled.png)
            
            결측치 확인
            
            ![기본 통계량](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/d113167f-807a-4e32-bbcc-26ced264885f/Untitled.png)
            
            기본 통계량
            
- Feature
    
    
    - 인기검색어
        
        
        | date | 랭크 날짜 |
        | --- | --- |
        | category | 카테고리 |
        | gender | 검색자 성별 기준 |
        | age | 검색자 연령대 기준 |
        | rank | 검색어 랭크 순위 |
        | keyword | 검색어 |
    - 상품평
        
        
        | url | 상품 구매 링크 |
        | --- | --- |
        | review, review_text | 상품평 |
        | review_date | 상품평 업로드 날짜 |
        | rate | 리뷰 별점 |
        | date | 상품 랭크 날짜 |
        | time | 작성 시간 |
    
    - 상품검색결과
        
        
        | keyword | 검색어 |
        | --- | --- |
        | sorting | 나열 기준(추천순, …) |
        | url | 상품 구매 링크 |
        | name | 상품명 |
        | price | 가격(원) |
        | ref | 판매플랫폼명(쿠팡, 컬리, …) |
        | date | 랭크 날짜 |
        | time | 랭크 시간 |
        | rank | 플랫폼 내 랭크 순위 |
        

### 4-2. 프로젝트 수행 방식/절차

- 데이터 수집
    - 인기검색어, 상품검색결과, 상품평
- 데이터 전처리
- 데이터 시각화  및 모델링
    - 키워드트렌드, 상품정보비교

- UI/UX 디자인 (Figma)
- 프론트 개발 (Amplify Studio)
- 개발 환경 구축 (AWS)
- 데이터 파이프라인 (S3, DynamoDB)

## 5. 담당업무 - 데이터 전처리

### 5-1. 이상치, 결측치 처리

- 이상치, 결측치 확인 후 처리
    - 네이버 데이터랩 결측치(TOP100)
        - 성별, 연령별, 카테고리별 등 세분화된 인기검색어를 크롤링 했을때 일부 검색어의 경우 TOP100까지 검색기록이 없는 날이 있는 것을 확인
        - 이를 처리하기 위해 월별 TOP100 데이터를 크롤링 하거나, TOP10 데일리 데이터를 크롤링해서 해결함
            
            ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/0aeaff1b-467c-4862-9f47-c6a8022823b9/Untitled.png)
            
            ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/116ffde5-d793-4c94-8a27-6cf24ea21a08/Untitled.png)
            
    - 쿠팡 상품평 데이터 별점 이상치
        - 상품평 별점이 인기검색어 특성상 높은 별점에 몰려있음
        
        ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/35bc6bfe-5b2e-4a83-a3b2-42c7472d300c/Untitled.png)
        
- 형태소 분석기
    - Okt, Mecab 적용했으나 **최종모델은** 원본 텍스트를 그대로 사용하는데 최적화 되어있어 **형태소분석기 미사용**
- 불용어 제거
    - 최초 조사 등 13개의 불용어 적용
    `stopwords = set(["그", "이", "저", "것", "들", "의", "에", "를", "가", "은", "는", "이다", "하다"])`
    - 이후 ranks.nl의 한국어 불용어 리스트 총 675개를 적용했으나 **최종 모델은** 원본 텍스트를 그대로 사용하는데 최적화 되어있어 **불용어 제거 미적용**

### 5-2. 데이터 수집 및 전처리

- 인기검색어 데이터 수집
- 상품 검색결과 및 상품평 데이터 수집
    - 인기 검색어 키워드를 불러와 해당 키워드에 대하여 각 플랫폼에 해당키워드 상품을 크롤링 후 저장
    - **Selenium** : 동적 조작 필요
    - **undetected chromedriver 와 options**를 통한 여러 옵션
    : 사이트마다 크롤링을 막기위해 다양한 장치 사용 - 이를 회피하면서 정보를 가져오기 위해
    - **close_driver**  함수 : 브라우저를 띄우게 될 시 컴퓨터 리소스 확보
- 마켓컬리 상품 검색결과 및 상품평 데이터 수집
    - 컬리는 쿠팡과 거의 동일 다만 사이트에서 상품에대해 제공하는 정보가 동일하지 않기 때문에 수집과정에서 긁어오는 정보의 차이는 존재 이외에는 **엘리먼트만 선택해서 바꿔주면 되는 것으로 해결**
    - 다만 상품평의 경우 하나의 상품당 10개의 상품평을 긁어오기로한 기준에 따라 컬리는 쿠팡과 달리 한페이지에 10개의 상품평을 노출하기에 따로 페이지를 넘기는 코드는 필요하지 않았음.
- 네이버 상품 검색결과 및 상품평 데이터 수집
    - 네이버의 경우 상품검색결과에서 긁어온 url이 각자의 판매처로 연결되기 때문에 상품평을 긁어오는 프로세스는 기간내 해당 프로젝트에서 완성시키지 못함. (각 판매 사이트에서 제공하는 리뷰의 구조가 다 다르기때문)
    - 네이버의 경우 크롤링이 가장 하기 힘든구조
        - 상품정보가 페이지를 스크롤해서 내려야 로딩됨.
        - 긁어온 url이 홈페이지로  리다이렉션됨
        - 보안정책상인지 불분명하나 중간에 크롤링 데이터가 끊김(못가져옴)
    - 이를 해결하기 위해 쿠팡과 컬리와 달리 **점진적 스크롤 코드삽입**과 실제 url을 가져오기위해 1차적으로 url을 가져오고 **브라우저를 한번 더 열어 해당 url에 접속**한다음에  url을가져오는식으로 해결
- 데이터 파이프라인에 맞게 코드 추가
- 상품검색결과 데이터 컬럼 및 파일명 통일 / 필요컬럼 추가 및 불필요컬럼 삭제

### 5-3. 데이터 클리닝 및 정제 코드

- 인기검색어, 상품검색결과 데이터 (감정분석 X) 전처리  
상품평 데이터(감정분석 O / 불용어 처리, 형태소분석기) 전처리
    
    https://colab.research.google.com/drive/1AxVNq4ex5p6_xz5F3k2pKD0PZ1stuO7u 텍스트전처리 및 형태소분석(불용어제거포함).ipynb
    
- 감정분석 전 토큰화, 라벨범위 맞춤, 학습데이터 분리
    
    https://colab.research.google.com/drive/1x13WJrQUEZj2MRbga8CrtGyCmr833uDl 쿠팡컬리_감정분석_KcBERT파인튜닝.ipynb
    

## 6. 담당업무 - 데이터 분석, 감정분석 모델링

### 6-1. 최초 데이터 EDA

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/598ffe2d-e98c-44d1-b267-555ff9e32679/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/f93680a9-3ab2-4e5c-8495-fd64f68a9bf3/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/ff44e953-f62c-4c9e-9075-955aac252ae6/Untitled.png)

![Screenshot_2024-06-26_at_4.24.55_PM.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/201f686f-a758-4ba6-a112-cca1baa47abf/Screenshot_2024-06-26_at_4.24.55_PM.png)

![Screenshot_2024-06-26_at_4.25.31_PM.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/0b5656a7-6105-4fa4-9f96-7c6d290164f7/498efd28-3cc9-4613-8327-2e3846a08c76.png)

### 6-2. 감정분석 모델링

**6-2-1. 1차 감정분석**

> 감정분석에 주로 활용되는 모델을 사용
> 
- 선택 모델
    
    <aside>
    1️⃣ Hugging Face의 `bert-base-multilingual-uncased-sentiment` 모델을 이용한 감정분석 모델링
    
    - **Pre-trained 모델 선정 이유**
        - 최초 CNN, LSTM으로 모델을 직접 학습시켜 만들고자 했으나
        - **수집된 리뷰 데이터셋이 적은편으로** 학습시간과 자원을 절약 할 수 있고 높은 모델성능이 검증된 **사전 학습 모델을 1차 진행으로 선정**
        - 이후 수집한 데이터셋으로 파인튜닝을 통한 모델 최적화를 고려 함
    
    ### 모델 특징
    
    - **다국어 지원**
    이 모델은 영어, 프랑스어, 독일어, 스페인어, 이탈리아어, 네덜란드어 등 다양한 언어를 지원
    → 이는 글로벌 시장을 타겟으로 하는 서비스에서 유리
    - **BERT 기반**
    BERT(Transformer)의 다국어 버전으로, 트랜스포머 아키텍처를 기반으로 하여 높은 성능의 자연어 처리 작업 수행 가능
    - **미세 조정 가능**
    모델은 사전 학습된 상태에서 다양한 감정 분석 작업에 쉽게 미세 조정(fine-tuning) 가능
    
    ### 모델 사용 의도
    
    - **다국어 리뷰 분석**
    이 모델은 다양한 언어로 작성된 리뷰를 처리할 수 있으며, 특히 한국어와 같은 비영어권 언어도 잘 지원됨 → 추후 글로벌 시장 진출 시 타 언어 분석 고려하여 선정
    - **사전 학습된 성능**
    대규모 데이터셋으로 사전 학습되어 있는 모델 → 감정 분석 작업에 대한 높은 정확도 기대
    - **고성능 감정 분석**
    BERT 기반 모델의 높은 성능과 정확도를 활용하여, 리뷰 텍스트의 긍정적, 중립적, 부정적 감정을 효과적으로 분석하고자 선정
    - **빠른 프로토타이핑**
    Hugging Face의 라이브러리를 통해 모델을 손쉽게 적용할 수 있어, 빠른 프로토타이핑과 초기 결과 도출 가능
    
    ### 결과 데이터 상위 5개 column과 시각화 결과
    
    ![전처리 결과 clean_review 칼럼 생성 → 
    clean_review 칼럼 데이터를 바탕으로 감정분석 결과인 sentiment 행 생성](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/bd985c0c-0576-497f-9cee-b2c221ca8f38/Untitled.png)
    
    전처리 결과 clean_review 칼럼 생성 → 
    clean_review 칼럼 데이터를 바탕으로 감정분석 결과인 sentiment 행 생성
    
    ![Sentiment Distribution - 모든 날짜, 기간에서 대체로 이런 추이의 차트가 나왔다.](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/73b398ce-32d3-420b-8119-0127724eb4e4/Untitled.png)
    
    Sentiment Distribution - 모든 날짜, 기간에서 대체로 이런 추이의 차트가 나왔다.
    
    ![미스매치 레이블별 카운트](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/84c8dc3b-e608-42a0-ae32-928b8dc41cda/Untitled.png)
    
    미스매치 레이블별 카운트
    
    </aside>
    

**6-2-2. 2차 감정분석**

> 데이터 불균형에 대한 문제 해결 + 다국어 모델 대신 한국어 특화 모델으로 변경
상품평텍스트에 최적화 시키기 위해 **구어체**에 특화된 모델이 필요하여 파인튜닝 진행
> 

<aside>
1️⃣ 파인튜닝 시 과적합 문제점을 고려한 솔루션

- 오버샘플링
    - 학습시킬 리뷰 데이터의 수가 상대적으로 작고 레이블분포가 불균형 하기 때문에 레이블 기준 오버샘플링을 진행해 적은 데이터 양과 불균형을 해결
    - **랜덤 오버샘플링**(Random Oversampling) 방식을 적용하고 random_state를 설정해 **재현성 보장**
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/6073e58e-6bf4-41f1-8b80-cfccbbd63705/Untitled.png)
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/eec02383-50c8-4285-a31e-c452607d7d47/Untitled.png)
    
</aside>

<aside>
2️⃣ 불용어처리, 형태소분석기 적용

- 675개의 불용어(출처 : [stopwords(불용어)](https://www.ranks.nl/stopwords/korean))처리, 형태소 분석기를 적용한 모델을 적용하려 했으나 너무 오랜시간이 걸리고 KcELECTRA모델이 형태소분석기, 불용어 처리 없이 더 적은 자원으로 더 정확한 결과를 얻을 수 있는 것을 확인해 2차 감정분석 종료
- 별점레이블이 있는 쿠팡데이터로 지도학습을, 지도학습된 모델을 통해 정답레이블이 없는 컬리데이터를 활용해 비지도학습을 진행해 파인튜닝 하려했으나 시간이 오래걸리고 파인튜닝을 컬리데이터로 하는것은 비효율적인것으로 확인해 쿠팡데이터로 지도학습을 통한 파인튜닝을 진행
</aside>

<aside>
💻 Hugging Face의 `KcBERT`를 이용한 모델링

https://colab.research.google.com/drive/1x13WJrQUEZj2MRbga8CrtGyCmr833uDl 쿠팡컬리_감정분석_KcBERT파인튜닝.ipynb

</aside>

**6-2-3. 3차 감정분석**

> BERT기반 모델보다 성능이 뛰어나고 더 많은 데이터셋을 학습했으며 형태소분석기와 
불용어처리를 적용하지 않아도 높은 성능을 보여주는 ELECTRA기반 모델로 변경
> 

<aside>
1️⃣ **모델 변경을 고려한 이유**

- bert-base 모델은 실제 별점레이블과 상이한결과가 많음
- 특정 레이블에 몰린 불균형한 분포결과를 확인했고 팀자체적으로 예측한 별점레이블과 차이가 났기 때문에 정확성에 의문을 가짐
- **기존의 감정분석모델 성능에 의문이 생겨 새로운 모델을 선별**
    
    <aside>
    📑 bert-base 모델 감정분석 결과
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/e84aed69-c01a-4e33-a3f5-c7c2e8768917/Untitled.png)
    
    - 별점 2점에 몰려있음
        
        ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/01a7affc-1b85-443d-917e-7f5816c9e00f/9da88553-65b4-4151-b489-3f3c55ea799d.png)
        
    - 실제 레이블과 예측 레이블이 다른 경우가 많음
    </aside>
    
</aside>

<aside>
2️⃣ ELECTRA기반 모델을 채택한 이유

- 결정적으로 ELECTRA는 BERT보다 컴퓨팅자원을 더 적게 소모하기 때문에 선택
- **효율적인 학습 구조**: 제너레이터-디스크리미네이터 구조를 사용하여, 적은 자원으로 높은 성능을 달성한 모델(BERT는 마스크드언어모델 MLM을 사용)
    
    ![참고논문 : ELECTRA: PRE-TRAINING TEXT ENCODERS AS DISCRIMINATORS RATHER THAN GENERATORS](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/73f2e033-071d-423a-b21d-18c2b9c79e7d/Untitled.png)
    
    참고논문 : ELECTRA: PRE-TRAINING TEXT ENCODERS AS DISCRIMINATORS RATHER THAN GENERATORS
    
    - 이 구조는 전체 입력 문장에서 원래의 토큰과 교체된 토큰을 구별하는 방법으로 학습해서 더 적은 계산 자원으로 학습이 가능
- **높은 평균 성능**: ELECTRA는 다양한 태스크에서 가장 높은 평균 성능을 기록한 모델
    
    ![참고논문 : ELECTRA: PRE-TRAINING TEXT ENCODERS AS DISCRIMINATORS RATHER THAN GENERATORS](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/fd79a0e6-65e9-4271-ad75-baacf3e11dbf/Untitled.png)
    
    참고논문 : ELECTRA: PRE-TRAINING TEXT ENCODERS AS DISCRIMINATORS RATHER THAN GENERATORS
    
    ![https://github.com/Beomi/KcELECTRA](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/c741b76f-6e77-4661-a4b4-8d79f1f861c4/%EB%AA%A8%EB%8D%B8%ED%8F%89%EA%B0%80.png)
    
    https://github.com/Beomi/KcELECTRA
    
- 일관된 성능 향상: ELECTRA는 모든 태스크에서 일관되게 높은 성능을 발휘하고, 균형 잡힌 성능을 제공
</aside>

<aside>
3️⃣ 형태소분석기 및 불용어처리를 진행하지 않은 이유

- **사전 학습된 모델 성능 고려** : KcELECTRA 모델은 문맥을 이해하고 단어 간의 관계를 파악하는 데 문제가 없고 파인튜닝시 형태소 분석과 불용어 처리 없이 진행하는것을 예시로 두고 있어 해당 전처리는 미적용
- 텍스트의 자연스러움 유지 : 의미와 문장구조를 보존하기 위해 원본 텍스트 데이터를 사용
- 실험적 결과 : 사전실험결과를 고려, 전처리 없이도 높은 성능을 달성 한 것을 확인 함
</aside>

<aside>
4️⃣ 새로운 데이터셋 예측은 colab T4 gpu 시스템RAM 사용량 고려 배치처리 적용

- 배경 : 새로운 데이터셋 예측시 배치처리를 하지 않으면 시스템RAM 사용량이 초과되어 세션이 종료되는 문제가 있어 배치처리로 해결 
성능 : GPU RAM 15.0 GB / 시스템 RAM 12.7 GB
- 배치사이즈 32 : 평균 3.1GB / 피크 3.5GB
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/d1d4e090-af2b-4406-b676-1be08998e728/2f52a608-c60d-4442-9b1d-d45553f659ed.png)
    
- 배치사이즈 256 : 평균  9GB / 피크 11.1GB
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/01f51035-5970-4a86-9b4c-8ac48f6712f5/Untitled.png)
    
</aside>

<aside>
💻 Hugging Face의 KcELECTRA을 이용한 모델링 
https://colab.research.google.com/drive/1j4wJVD7FMoCcWlDvb_lFZ2ub7fvkkVRX 쿠팡오버샘플링기반_파인튜닝_감정분석모델.ipynb

</aside>

## **6-3.** 상품평 데이터 모델링 결과 분석

> 모델성능 비교 : 평가지표 및 그래프 등 활용
> 

<aside>
📑 **파인튜닝 결과**

![모델3 평가데이터셋 평가지표 결과](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/822f1f0f-7e9a-4f23-985d-097a80475133/%EB%AA%A8%EB%8D%B8_%ED%8F%89%EA%B0%80%EB%A7%89%EB%8C%80%EA%B7%B8%EB%9E%98%ED%94%84.png)

모델3 평가데이터셋 평가지표 결과

- **eval_loss**: 0.0032
- **eval_accuracy**: 0.9996
- **eval_precision**: 0.9996
- **eval_recall**: 0.9996
- **eval_f1**: 0.9996

**모든 평가지표가 높음**

정확도, 정밀도, 재현율, F1 점수가 모두 1에 가까운 우수한 성능을 보임

![실제 리뷰 레이블과 예측 레이블 비교](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/34c0154d-f116-451d-9436-80a18a67b17e/Untitled_(6).png)

실제 리뷰 레이블과 예측 레이블 비교

**새로운 데이터셋 예측 결과(기존 모델과 성능비교)**

![모델1 vs 모델3 미스매치 레이블별 카운트 바그래프](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/4acd43f7-032a-4f21-a02a-05cee4d333f3/13%EB%AA%A8%EB%8D%B8_%EB%AF%B8%EC%8A%A4%EB%A7%A4%EC%B9%98_%EC%B9%B4%EC%9A%B4%ED%8C%85.png)

모델1 vs 모델3 미스매치 레이블별 카운트 바그래프

![모델1 vs 모델3 컨퓨젼매트릭스 : 오차부분 상당 수 개선](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/1d6b3b2f-c1fb-4b57-8165-625d9e36f81d/Untitled.png)

모델1 vs 모델3 컨퓨젼매트릭스 : 오차부분 상당 수 개선

![모델1 vs 모델3 평가지표 비교 : MAE는 매우 낮아지고 정확도는 크게 상승](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/78592667-cef4-4c57-8bbe-56c084aa8ef9/Untitled.png)

모델1 vs 모델3 평가지표 비교 : MAE는 매우 낮아지고 정확도는 크게 상승

**이커머스상품평을 최종 모델로 감정분석한 결과 라벨별 이모지로 제공**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/4b3ae153-b653-4172-8caa-b38416bcb5f7/Untitled.png)

</aside>

## 7. 부록

### 7-1. 참고자료

https://huggingface.co/beomi/KcELECTRA-base-v2022

https://huggingface.co/nlptown/bert-base-multilingual-uncased-sentiment

https://huggingface.co/ainize/kobart-news
https://jin-na.tistory.com/entry/Figma의-인터랙티브-컴포넌트-기능-이해하기

https://github.com/Beomi/KcELECTRA?tab=readme-ov-file

https://www.ranks.nl/stopwords/korean

[[2024년 제 1호] 2024 식품외식산업 7대 이슈.pdf](https://prod-files-secure.s3.us-west-2.amazonaws.com/13c7ec80-34cc-459c-a734-470b4537d2d1/3a042581-9a6c-4804-83d2-13a0f29a94bb/2024%EB%85%84_%EC%A0%9C_1%ED%98%B8_2024_%EC%8B%9D%ED%92%88%EC%99%B8%EC%8B%9D%EC%82%B0%EC%97%85_7%EB%8C%80_%EC%9D%B4%EC%8A%88.pdf)

https://wikidocs.net/94600

https://huggingface.co/

https://www.figma.com/community

https://www.tableau.com/

https://drive.google.com/drive/folders/10-3H6CWre-a_n_2rJjS8oqMUV2xUnnTu?usp=drive_link /RAISE 공유드라이브
