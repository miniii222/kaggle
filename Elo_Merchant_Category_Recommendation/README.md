# https://www.kaggle.com/c/elo-merchant-category-recommendation

- [2019-01-17] 주제 선정 및 회의
- [2019-01-22] [EDA](https://github.com/miniii222/kaggle/tree/master/Elo_Merchant_Category_Recommendation/eda) train,test, transaction data
- [2019-01-23] EDA transaction, merchant data
- [2019-01-28] EDA data간 관계 살피기. base_line model RMSE(Elastic_net : 3.928 lightGBM : 3.905)
- [2019-01-31] NA처리 및 oulier
- [2019-02-05] New Feature -> RMSE(Elastic_net : 3.866 lightGBM : 3.811)
- [2019-02-06] New Feature -> RMSE(Elastic_net : 3.866 lightGBM : 3.771)
- [2019-02-10] merchant 데이터로 feature 생성
- [2019-02-17] target outlier (-33... 값 잡으려 했으나 실패...)
- [2019-02-18] feature 더 뽑아보자!
- [2019-02-20] 각자의 feature 다 합치기
- [2019-02-23] spline으로 lightgbm, catboost, xgboost 모델링
- [2019-02-25] 모델 블렌딩
- [2019-02-26] 최종 모델 선택 및 제출.
- [2019-02-27] 끝!!!



## historical_transactions+new_merchant_transactions -> sorted_history (card_id, purchase_date로 sorting)
- category3가 B = installments 가 다 1
- installments -999 -> category3 C (역은 성립 x), 승인 난 경우도 있음
#### category3 과 installments의 관계
- category3 = A : installments = 0 (할부 x - 체크카드든 뭐든..)
- category3 = B : installments = 1 (할부 x)
- category3 = C : installments = 2,3,...999 (할부 ㅇ)
- category3 = NA : installmenst = -1(NA)

### new feature
1. authorized : 승인 수
2. not_authorized : 비승인 수
3. authorized_rate : 승인/ 비승인
4. merchant_visit : 같은 가게 다른 날 여러 번 방문 횟수 -> "sum", "mean", "min", "max",'nunique','size',mode
5. merchant_try : 같은 가게 같은 날 여러 번 결제 시도 ->  "mean", "std", "min", "max",'nunique','size',mode
6. Ref_Date : 2017-01-01로부터 결제일 며칠 -> "mean", "std", "min", "max",'nunique','size',mode
7. 위치 관련 변수들 mode로 생성 ('city_id','state_id','subsector_id','category_2')
8. category3 으로 만든 변수 망함!
9. 총 산 물건 양 / 들른 가게 

## historical_transactions
- merchant_id 가 key인데 왜 여러개가 존재하냐 
- transaction merchant_id가 merchant에 있는 merchant_id보다 
- category_2와 지역간의 관계 [link](https://www.kaggle.com/c/elo-merchant-category-recommendation/discussion/76579)
### new data
#### history_inner - installments = -999인 card_id, merchant_id 만 뽑아서 
#### category2_null : category2 가 null인 데이터

