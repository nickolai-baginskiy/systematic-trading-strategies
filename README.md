# Empirical Study of Systematic Trading Strategies

---

## Overview
This repository presents an empirical study of systematic trading strategies across financial markets.  
The goal is to evaluate how different trading rules behave under realistic conditions and to assess their robustness, stability, and economic significance.

---

## Research Question
- Do simple systematic strategies generate persistent returns after accounting for trading costs?
- How sensitive are results to market conditions and parameter choices?
- Which types of strategies (trend-following, mean-reversion, etc.) show more stable performance?

---

## Methodology

### Data
- Market data: prices, macro data, and trading data  
- Frequency: 15m / 1H / 4H  

### Strategy Classes
- Trend-following strategies  
- Mean-reversion strategies  
- Indicator-based strategies  

### Evaluation Framework
- Walk-forward validation  
- Transaction costs included  
- Performance metrics: return, Sharpe ratio, drawdown, hit rate  

---

## Discussion

The results suggest that:

- Many commonly used trading strategies are not profitable after accounting for costs  
- Robust evaluation often reduces or eliminates apparent profitability  
- Simple strategies can capture structure in the data, but are insufficient as standalone trading solutions and are better treated as supplementary signals  
- Monte Carlo simulations help assess the stability and reliability of strategy performance  
- Machine learning may improve performance, but often introduces additional risk and instability, especially for weak strategies  

---

## Conclusion

This study highlights the importance of rigorous empirical evaluation and robustness testing in systematic trading.  
Future work will focus on improving stability, reducing turnover, and identifying economically meaningful signals.

This study highlights the importance of empirical testing and robustness analysis in systematic trading.  
Future work will focus on improving stability and reducing turnover.


