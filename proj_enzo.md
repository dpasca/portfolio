<h3>{{ include.title }}</h3>

A complete trading system for cryptocurrencies. See [www.enzobot.com](https://www.enzobot.com).

![]({{ site.baseurl }}/images/20221017_tsp_with_indicators.png)

#### My work on the project

I developed most of the front-end and trading models in C++. Some of the major tasks are:

- Realized machine-learning driven trading algorithms and indicators
- Live trading on Bybit and Binance exchanges via REST and WebSocket APIs
- Backtesting infrastructure
  - Simulation of exchange orders, including HFT (sub-minute) data
  - Reporting of P&L, Calmar ratio, Sharpe ratio, Monte Carlo validation, etc.
- Risk management (see video [Levels of risk management. Our approach summarized.](https://youtu.be/09yW6IgQkqA))
- Live profit calculation and reporting
- TCP/IP client-server infrastructure to distribute trading signals to customers
- IPC protocol based on BSD sockets
- UI based on Dear ImGui
- Chart and indicators rendering in OpenGL

#### What I learned

- Challanges of building consistently profitable strategies
- Practical meachine-learning application and techniques to reduce curve fitting
- REST API connectivity and crypto exchange protocols
- Risk and portfolio management techniques
- Leverage trading and short selling
- Usage of Dear ImGui for a complex project
- Reliance on multiprocessing for fault-tolerance

