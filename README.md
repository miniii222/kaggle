# kaggle

## 1. [Elo Merchant Category Recommendation Competition](https://github.com/miniii222/kaggle/tree/master/Elo_Merchant_Category_Recommendation)

브라질의 최대 결제 결제 브랜드 중 하나인 Elo 카드 회원 데이터를 이용하여 회사의 추천도에 대한 고객들의 만족도를 score화하여 예측하는 competition :[Competition Link](https://www.kaggle.com/c/elo-merchant-category-recommendation/)

## 결과
#### 상위 5% 은메달!
![](https://github.com/miniii222/kaggle_competition/blob/master/Elo_Merchant_Category_Recommendation/ranking.JPG "elo")


## 2. [Santander Customer Transaction Prediction]
- [Competition Link](https://www.kaggle.com/c/santander-customer-transaction-prediction)
- Can you identify who will make a transaction?
- identify which customers will make a specific transaction in the future, irrespective of the amount of money transacted
- The data provided for this competition has the same structure as the real data we have available to solve this problem.
#### 평가기준
- AUC (Area under the ROC curve)

## 3. [2nd_Kaggle_kr_Competition]
#### [Competition Link](https://www.kaggle.com/c/2019-2nd-ml-month-with-kakr)
#### Competition background
내 집 마련의 꿈은 누구나 가지고 있습니다. 하지만 집의 가격은 누구나 알고 있지는 않죠. 집의 가격은 주거 공간의 면적, 위치, 경관, 건물의 연식 등 여러 가지 복잡한 요인의 조합에 의해 결정됩니다. 이번에 분석하실 데이터는 20개의 변수를 가지고 있으며, 어떤 조건을 가진 집의 가격이 높고 낮은지를 예측하는 모델을 만드는 것을 목표로 합니다.
#### Data fields
- ID : 집을 구분하는 번호
- date : 집을 구매한 날짜
- price : 집의 가격(Target variable)
- bedrooms : 침실의 수
- bathrooms : 침실 개수 당 화장실의 수(화장실의 수 / 침실의 수 )
- sqft_living : 주거 공간의 평방 피트(면적)
- sqft_lot : 부지의 평방 피트(면적)
- floors : 집의 층 수
- waterfront : 집의 전방에 강이 흐르는지 유무 (a.k.a. 리버뷰)
- view : 집이 얼마나 좋아 보이는지의 정도
- condition : 집의 전반적인 상태
- grade : King County grading 시스템 기준으로 매긴 집의 등급
- sqft_above : 지하실을 제외한 평방 피트(면적)
- sqft_basement : 지하실의 평방 피트(면적)
- yr_built : 지어진 년도
- yr_renovated : 집을 재건축한 년도
- zipcode : 우편번호
- lat : 위도
- long : 경도
- sqft_living15 : 2015년 기준 주거 공간의 평방 피트(면적, 집을 재건축했다면, 변화가 있을 수 있음)
- sqft_lot15 : 2015년 기준 부지의 평방 피트(면적, 집을 재건축했다면, 변화가 있을 수 있음)
#### Evaluation : RMSE


## 4. [Predict Future Sales]
- [Competition Link](https://www.kaggle.com/c/competitive-data-science-predict-future-sales/kernels)
- In this competition you will work with a challenging time-series dataset consisting of daily sales data, kindly provided by one of the largest Russian software firms
#### 평가기준
- RMSE
