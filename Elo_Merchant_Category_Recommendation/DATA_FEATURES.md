# https://www.kaggle.com/c/elo-merchant-category-recommendation

## historical_transactions -> sorted_history (card_id, purchase_date로 sorting)
- category3가 B = installments 가 다 1
- installments -999 -> category3 C (역은 성립 x)

### new feature
1. authorized : 승인 수
2. not_authorized : 비승인 수
3. authorized_rate : 승인/ 비승인

### new data
#### history_inner - installments = -999인 card_id, merchant_id 만 뽑아서 
#### category2_null : category2 가 null인 데이터

