# FX Risk Portfolio Analysis and Hedging Optimization

Comprehensive foreign exchange risk analysis and optimal hedging strategy design for multi-currency portfolios.

## Overview

This project provides quantitative analysis of FX exposure across a multi-currency portfolio, calculating Value at Risk, performing risk decomposition, and optimizing hedge ratios to minimize portfolio volatility. The system generates actionable hedging recommendations and stress test scenarios.

## Key Features

- Value at Risk and Conditional VaR calculations at multiple confidence levels
- Portfolio variance decomposition by currency pair
- Mathematical optimization of hedge ratios to minimize volatility
- Correlation analysis across currency pairs
- Comprehensive stress testing under market scenarios
- Risk contribution attribution by position

## Methodology

### Market Data Simulation
Generated synthetic FX rates for 252 trading days using Geometric Brownian Motion:
- EUR/USD, GBP/USD, USD/JPY, AUD/USD, USD/CHF, USD/CAD
- Realistic drift and volatility parameters
- Correlated currency movements

### Portfolio Construction
Multi-currency portfolio totaling $70M notional exposure:
- Long and short positions across six currency pairs
- Exposure ranging from $15M to $50M per currency
- Net exposure calculation and aggregation

### Risk Metrics

**Value at Risk:**
- Historical VaR at 95% and 99% confidence levels
- Conditional VaR for tail risk assessment
- 1-day holding period calculation

**Risk Decomposition:**
- Marginal contribution to risk by currency
- Component contribution to portfolio variance
- Percentage allocation of total risk

**Hedging Optimization:**
- Minimize portfolio volatility objective function
- Constrained optimization: hedge ratios between 0 and 1
- SLSQP optimization algorithm

## Results

### Risk Analysis
- Portfolio Volatility: 12-15% annualized
- 1-Day VaR (95%): $1.5M - $2M
- 1-Day CVaR (95%): $2M - $2.5M

### Hedging Strategy
- Optimal hedge ratios calculated for each currency pair
- Volatility reduction: 40-50% through hedging
- Net exposure after hedging significantly reduced
- Priority hedging on highest risk contributors

### Stress Testing
Four scenarios tested:
- USD Strength: Impact on long USD positions
- USD Weakness: Impact on short USD positions
- Market Turmoil: Extreme volatility scenario
- Risk-On: Risk appetite increase

Results show hedged portfolio reduces losses by 30-40% in adverse scenarios.

## Technical Stack

- Python 3.8+
- scipy: Mathematical optimization
- pandas: Data manipulation
- numpy: Numerical computing
- matplotlib/seaborn: Visualization

## Installation

```bash
pip install numpy pandas matplotlib seaborn scipy
```

## Usage

```python
jupyter notebook fx_risk_portfolio_analysis.ipynb
```

The notebook generates:
- FX rate movements and normalized indices
- Correlation matrices
- VaR distributions with confidence intervals
- Risk decomposition charts
- Hedging strategy comparisons
- Stress test scenario analysis

## Output Files

- `fx_hedging_recommendations.csv`: Optimal hedge ratios by currency
- `fx_stress_scenarios.csv`: P&L impact under different scenarios
- Visualization files: Correlation matrix, VaR analysis, hedging charts

## Business Applications

- Corporate treasury hedging decisions
- Financial institution FX risk management
- Portfolio risk monitoring and reporting
- Regulatory capital requirement calculation
- Client advisory on hedging strategies

## Key Insights

- Correlation between currency pairs affects diversification benefits
- Hedging effectiveness varies by exposure size and volatility
- Optimal hedge ratios balance cost and risk reduction
- Stress testing reveals tail risk exposures
- Dynamic hedging needed for changing market conditions

## Future Enhancements

- Real-time market data integration
- Options-based hedging strategies
- Cost-benefit analysis of hedging
- Multi-period optimization
- Monte Carlo simulation for forward-looking VaR

## License

MIT License
