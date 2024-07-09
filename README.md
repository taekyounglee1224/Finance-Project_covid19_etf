
## Changes in ETF Price in response to COVID-19 Pandemic Situations 📊
- 공동 1 저자: 이태경, 박성수, 신경수, 이수인
- 공동 2 저자: 최인수, 김장호
- 교신저자: 김우창
------------------------------------------------------------------------------------------------
### Analysis on the economic impact of the COVID-19 Pandemic on ETF markets by correlation of COVID exogenous variables with the volatility of ETF stock prices

- Exog: 확진자 수, 사망자 수 <a href = "https://kdx.kr/data/view/25918">출처: KDX 한국 데이터거래소</a>
- Target : KODEX, TIGER, TIGER200 <a href = "https://finance.naver.com/sise/etf.naver">출처: 네이버 증권 ETF</a>
-------------------------------------------------------------------------------------------------------
### Table of Contents

- Introduction
- Environments and Tools
- References

---------------------------------------------------------------------------------------------

### Introduction

Our key goal for the research is to confirm our hypothesis that the Pandemic of the COVID-19 will have economically impacted certain domestic ETF Stocks.
Based on our conclusion, we are looking forward to interpret our results by relating our analysis to social phenomena. We have  

### Environments and Tools:
- Request Tools
- Python 3.9 ~ 3.11
- Models : ARIMA, ARIMAX, Auto Arima

```
  !pip install requests
  !pip install pmdarima
  !pip install statsmodels

  from pmdarima import auto_arima
  from statsmodels.tsa.arima.model import ARIMA
```

-------------------------------------------------------------------------------------------------------
### References
- 남영진, 김재혁, 조하현(2022). 국내주식시장 수익률 변동성 추정 및 변동성 전이효과 : 코로나 19, 메르스, 신종플루 기간을 중심으로. [한국산업경제 저널, 35(3), 421-458]

- 김동현, 백승우, 김수현(2021). 개입 ARIMA 모형을 통한 축산물 가격 예측연구 : 코로나 19 팬데믹 시대의 한우와 수입쇠고기를 중심으로. [식품유통연구, 38(1), 95-111]

- 박준신, 안재준, 오경주(2021.) 코로나 ESG 투자 전략 평가: ESG 인덱스 성과를 중심으로. [지식경영연구, 22(4), 87-101]


