###Section1 : 다음 분기 제작 게임 출시

1. 데이터 셋 

코드스테이츠에서 제공한 데이터셋 데이터로

데이터 구성은 게임의 이름(Name), 게임이 지원되는 플랫폼의 이름(Platform), 게임이 출시된 연도(Year), 게임의 장르(Genre), 게임을 제작한 회사 (Publisher), 북미 지역에서의 출고량(Na_Sales),  유럽지역에서의 출고량(EU_Sales), 일본지역에서의 출고량(JP_Sales), 기타지역에서의 출고량(Other_Sales)로 구성되어 있습니다. 


2. 프로젝트에서 풀고자 하는 문제 (문제인식, 문제 정의, 가설)

가설 1.  지역에 따라서 선호하는 게임 장르가 다를까? 

가설 2. 연도별 게임의 트렌드가 있을까?

 

3. 프로젝트 진행과정  

빈 데이터는 0으로 대체하고 Unnamed: 0'의 컬럼을 삭제하였습니다.

북미지역 출고량, 유럽지역 출고량, 일본지역 출고량의 데이터 타입을 float형으로 통일시켜주었습니다. 

장르를 기준으로 지역별 출고량을 합쳐주었습니다. 

장르명 중에서도 0으로 나오는 것을 삭제하였습니다. 


4. 문제상황 해결과정(분석기법, 모델 등)

귀무가설: 지역에 따라서 선호하는 게임 장르가 다르다 

대안가설: 지역에 따라서 선호하는 게임 장르가 다르지 않다.

t-test를 이용하여 P-values: 0.0002로 P-values 값이 유의수준인 0.05보다 작아 지역마다 장르에 따른 판매량의 차이가 있다고 볼 수 있다.

귀무가설: 지역마다 장르에 따른 판매량의 차이가 없다.

대립가설: 지역마다 장르에 따른 판매량의 차이가 있다. 

t-test를 이용해 P-values: 0.0002로 ,P-values 값이 유의수준인 0.05보다 작아 지역마다 장르에 따른 판매량의 차이가 있다고 볼 수 있다.

5. 결과정리

 

장르에 따라 출고량이 높은 게임은 지역에 따라 선호하는 게임 장르가 다를까라는 질문에서 했던 답과 같이

북미지역에서는 엑션, 스포츠, shooter

<img width="{80}" src="{https://user-images.githubusercontent.com/102473586/236314925-39228af7-4f80-483a-867e-a8a59ee16516.png}"/>

유럽지역에서는 액션,스포츠, shooter

![download.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ff59117f-d758-4349-b7ea-8189a1c5bafc/download.png)

일본지역에서는 Role-playing, 액션, 스포츠

![download.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4d67e8e3-4efc-4237-b607-0d3cc022c690/download.png)

기타지역에서는 액션, 스포츠, shooter 순으로 나타났다는것을 알 수 있었습니다.

![download.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5fc2b452-2646-43ee-b5cd-3bdc5d314bc8/download.png)

지역들에서 공통적으로 좋아하는 게임은 액션,스포츠라는 것을 알 수 있습니다.

---

Total_Sales 총 매출로 보면 Wii Sports인 Sports장르가 82.74로 많이 팔렸음을 알 수 있다.

하지만 지역별 타겟팅으로 가게된다면 1번의 답과 같이 연결하여서 결론을 지어진다면? 액션,스포츠장르를 낸다고 한다면

북미 -X360, PS2,/ Wii

![download.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7f0953d1-c7d2-47e7-b8b9-54bbbb7d17de/download.png)

유럽 -PS3, PS2,/ X360

![download.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7b0563a0-e636-4cfd-8494-8b4aacc9ec6c/download.png)

일본 -DS /PS PS2

![download.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d9ac9582-e86e-403e-93ca-5c2ee912cd24/download.png)

기타지역 -PS2, PS3, X360, wii

![download.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/f25e17a2-382e-4707-8af9-4ea5ad2a9c5a/download.png)

플랫폼 top3의 상위권에 항상 속해있는 PS2 플랫폼을 이용하여 게임을 출시해야한다.

---

---

총 결론:

전 지역 타겟팅을 한다면 sport 장르, PS2북미 Action장르 ,X360플랫폼 이용

유럽 Action장르, PS3플랫폼 이용

기타 Action장르, PS2

일본 Role-playing, DS

6. 한계점 및 해결방안  

먼저, 프로젝트를 앞서 데이터셋에 집중하느라 데이터만 보고 프로젝트를 진행했던 점이 문제였고 그래프를 시이적절하게 사용하지 못하였고, 그래프 실력이 미숙했다 

→ 다음 프로젝트 전에는 자료조사를 우선적으로 하고 필요한 그래프의 특징을 미리 공부해야함을 깨달았습니다. 
