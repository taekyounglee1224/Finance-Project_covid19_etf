### Model Summary 
##### 기준: decideCnt(확진자 수), deathCnt(사망자 수)

##### [평가 지표] ARIMA: Log Likelihood, ARIMAX: p-value 


- ARIMA와 ARIMAX 중 더 설명력이 좋은 모델을 선정하기 위해 각각의 Log Likelihood를 비교
- ARIMAX 모델에 사용된 COVID-19 외생변수가 종속변수(ETF 종가)를 잘 설명하는지 판단하기 위해 p-value를 관찰


#### ARIMAX
$$\begin{equation}
y_t = \alpha + \sum_{i=1}^{p} \phi_i y_{t-i} + \sum_{i=1}^{q} \theta_i \epsilon_{t-i} + \sum_{i=0}^{r} \beta_i x_{t-i} + \epsilon_t
\end{equation}$$

#### GC-Test
\begin{equation}
y_t = \alpha + \sum_{i=1}^{p} \beta_i y_{t-i} + \sum_{i=1}^{q} \gamma_i x_{t-i} + \epsilon_t
\end{equation}
