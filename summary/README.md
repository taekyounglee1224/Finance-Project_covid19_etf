## Methodology
##### 기준: decideCnt(확진자 수), deathCnt(사망자 수)
##### Target : ETF(KODEX, TIGER, TIGER200)

##### [평가 지표] ARIMA: Log Likelihood, ARIMAX: p-value, GC-Test : No. of efficient lags


- ARIMA와 ARIMAX 중 더 설명력이 좋은 모델을 선정하기 위해 각각의 Log Likelihood를 비교
- ARIMAX 모델에 사용된 COVID-19 외생변수가 종속변수(ETF 종가)를 잘 설명하는지 판단하기 위해 p-value를 관찰
- GC Test를 통해 ARIMAX 모델의 검정결과에 인과성을 더해서 뒷받침
- Clustering을 통해 ARIMAX와 GC-Test에서의 COVID-19 외생변수와 ETF종목 간의 설명력 결과 비교


## Models
### ARIMAX
$$\begin{equation}
y_t = \alpha + \sum_{i=1}^{p} \phi_i y_{t-i} + \sum_{i=1}^{q} \theta_i \epsilon_{t-i} + \sum_{i=0}^{r} \beta_i x_{t-i} + \epsilon_t
\end{equation}$$

- $y_t$ : Dependent variable at time $t$
- $\alpha$ : Intercept term
- $\phi_i$ : Coefficients for the AR terms (autoregressive part)
- $\theta_i$ : Coefficients for the MA terms (moving average part)
- $\beta_i$ : Coefficients for the exogenous variable $x_t$
- $p$ : Order of the AR part
- $q$ : Order of the MA part
- $r$ : Lag order of the exogenous variable
- $\epsilon_t$ : Error term at time $t$ 

#### GC-Test
$$\begin{equation}
y_t = \alpha + \sum_{i=1}^{p} \beta_i y_{t-i} + \sum_{i=1}^{q} \gamma_i x_{t-i} + \epsilon_t
\end{equation}$$

- $y_t$ : Dependent variable
- $x_t$: Independent variable (Granger-causality test variable)
- $\alpha$ : Constant term
- $\beta_i$ : Coefficients of the lagged values of $y_t$
- $\gamma_i$ : Coefficients of the lagged values of $x_t$  (if these are all 0, then $x_t$ does not Granger-cause $y_t$ )
- $p$, $q$ : The number of lags of $y_t$ and $x_t$, respectively
- $\epsilon_t$ : Error term at time $t$ 
