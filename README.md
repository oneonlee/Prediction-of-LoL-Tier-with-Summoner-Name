# Prediction-of-LoL-Tier-with-Summoner-Name

RNN(Recurrent Neural Network)을 이용한 (재미로 보는) 리그오브레전드 소환사 이름으로 티어 예측하기

(+부록 : [리그오브레전드 소환사 이름 기반 워드클라우드 분석](/Wordcloud-of-LoL-Summoner-Name/))
<br>

```python
>>> tier_predict('KT way')
('마스터 이상', 0.25377932)

>>> tier_predict('플래티넘 문지기')
('플래티넘', 0.21506898)

>>> tier_predict('아몬드가 죽으면')
('다이아몬드', 0.28879693)

>>> tier_predict('아이언맨')
('아이언', 0.18356498)

>>> tier_predict('정보통신기술협회')
('플래티넘', 0.18466833)
```

## 사용하기

### 모델 훈련

- [Google Colab](https://colab.research.google.com/drive/1xcIGEgBWajNtVOhVXVnF2EUP8beEHbt_?usp=sharing)
- [`.ipynb` file](/Prediction_of_LoL_Tier_with_Summoner_Name.ipynb)
- [`.py` file](/Prediction_of_LoL_Tier_with_Summoner_Name.py)

### 모델 사용

- [Google Colab](https://colab.research.google.com/drive/1ER1-TH3yvx17iiVNZd5aoLnXz7Ks_xzn?usp=sharing)
- [`.ipynb` file](/Using_pre_trained_model_Prediction_of_LoL_Tier_with_Summoner_Name.ipynb)
- [`.py` file](/Using_pre_trained_model_Prediction-of-LoL-Tier-with-Summoner-Name.py)

## 사용 데이터

- 전체 3,718,157건
  - 리그오브레전드 소환사 랭킹
  - 리그오브레전드 소환사 이름
  - 리그오브레전드 티어

| ranking |      nickname |       tier |
| ------: | ------------: | ---------: |
|       1 |       JUGKlNG | challenger |
|       2 |        viper3 | challenger |
|       3 |        KT Way | challenger |
|       4 | SMB heixiaohu | challenger |
|       5 |      냥똥벌레 | challenger |

### 티어 별 분포

![](/image/tier_graph.png)

- Challenger tier : 296건
- Grandmaster tier : 681건
- Master tier : 3,806건
- Diamond tier : 57,195건
- Platinum tier : 404,496건
- Gold tier : 1,020,424건
- Silver tier : 1,272,286건
- Bronze tier : 854,653건
- Iron tier : 104,320건

## 사용한 RNN 모델 별 성능

각 모델 별 뒤에 붙은 숫자는 `embedding_dim`, `hidden_units`, `batch_size` 값을 의미함.

| RNN Models          | **Accuracy** |
| ------------------- | ------------ |
| LSTM-128            | 0.21945      |
| LSTM-64             | 0.21972      |
| BiLSTM-128          | 0.22147      |
| BiLSTM-64           | 0.22132      |
| GRU-128             | 0.22105      |
| GRU-64              | 0.21993      |
| BiGRU-128           | 0.22192      |
| [BiGRU-64](/model/) | **0.22210**  |

---

<div align="center">
2022년 인트아이 여름 해커톤 "그로우업톤" - 인공지능 팀 참가 작품
</div>

<br>

<div align="center">

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Foneonlee%2FPrediction-of-LoL-Tier-with-Summoner-Name%2Fblob%2Fmain%2FREADME.md&count_bg=%232D404F&title_bg=%23CDC5C5&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

</div>
