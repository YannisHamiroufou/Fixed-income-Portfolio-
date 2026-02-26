# Macro-Credit to Portfolio Workflow

This repository contains two Python notebooks built around a simple idea: monitor macro-credit conditions, then use that analysis to think about fixed income allocation.

## Notebooks

### `macro-credit-risk-monitor.ipynb`
This notebook is a monitoring dashboard. It tracks credit spreads, rates volatility, curve dynamics, inflation expectations and some broader market sentiment indicators.

The goal is to better understand the market environment, especially in terms of risk aversion, liquidity stress and spread conditions.

### `fixed-income-allocation-engine.ipynb`
This notebook is an ETF-based fixed income allocation prototype. It uses a simple allocation framework across sovereign bonds, investment-grade credit, inflation-linked bonds and liquidity buffers, with monthly rebalancing and basic performance/risk analysis.

## Investment Logic

The current allocation is mainly focused on the 3–7Y part of the curve. The idea is to benefit from carry and roll-down while staying more cautious on the long end, which looks more exposed to fiscal risk and term premium repricing.

The portfolio also keeps a defensive credit stance. There is no HY exposure for now, because spread compensation versus IG still looks relatively compressed and not especially attractive from a risk-reward perspective.

Part of the research has also extended to Brazil, which I find particularly interesting because of the interaction between inflation, Selic, FX and the local curve.

## Limitations

This project is a prototype, not a production-ready portfolio system. Some important limitations are:
- ETF prices are used as proxies
- rebalancing is simplified
- some price series are forward-filled
- transaction costs are not fully included
- allocation is rule-based, not optimized

## Tools

Python, pandas, numpy, matplotlib, yfinance, FRED API and Excel.

## About

I am a Master's student in Finance at emlyon business school, specializing in Financial Markets, and a CFA Level II candidate.

I am particularly interested in macroeconomics, geopolitics and fixed income. This is one of the reasons why I started building projects like this one: I like the idea of linking market monitoring, macro analysis and portfolio construction.

Alongside my academic curriculum and the CFA Program, I also study independently using Frank Fabozzi’s fixed income handbook, especially in the areas that interest me most: emerging markets debt, distressed credit and convertible bonds.

## Next Steps

Some next improvements would be:
- adding z-scores and percentiles for regime signals
- improving the benchmark
- adding transaction cost assumptions
- making the link between monitoring and allocation more systematic
- exploring more EM and local rates markets
