---
---
- Financial market forecasting using Artificial Neural Networks
- Vehicle navigation: pathfinding and obstacle avoidance
- Custom C++ Neural Networks implementation (inference and training)
- Neural Networks with PyTorch using C++ and Python
- Genetic algorithms, neuro-evolution, REINFORCE-ES

#### Professional Journey

My journey in machine-learning started in 2017, when I started to design auto-pilot logic for the plane and missiles airframes in my experimental flight simulator [XPSVR](#xpsvr-experimental-flight-simulator).

In 2018 I started to apply basic ML to **financial market forecasting** for the [ENZO Trading System](#enzo-trading-system).

By early 2023, my focus shifted towards **Artificial Neural Networks**, tackling increasingly complex tasks from autonomous driving to sophisticated time-series prediction models, now deployed in live trading.

In late 2023, I developed [ChatAI](https://github.com/dpasca/ChatAI), a virtual assistant integrating **OpenAI's API**. This chatbot enhances the experience for the user using function-calling and prompt injection to have a better sense of the user's time and location.

The assistant operates as a web app, leveraging *Flask*, *Bootstrap*, and additional external modules for code syntax highlighting and LaTeX rendering.

<div style="display: flex;">
  <div style="height: 350px; overflow: hidden; width: 50%; margin-right: 5px;">
    <img src="https://raw.githubusercontent.com/dpasca/ChatAI/master/docs/chatai_sshot_01.webp"
      style="position: relative; top: 0px; width: 100%;" />
  </div>
  <div style="height: 350px; overflow: hidden; width: 50%;">
    <img src="https://raw.githubusercontent.com/dpasca/ChatAI/master/docs/chatai_sshot_01.webp"
      style="position: relative; top: -350px; width: 100%;" />
  </div>
</div>
<br/>

#### Insights Gained

Building a system from simple cases was essential in grasping the core concepts involved.

In time-series prediction, **Evolution Strategies (ES)** proved effective, particularly with limited computational resources. While backpropagation is generally more efficient and likely a better solution long-term, the evolutionary approach facilitated a better balance between exploration and exploitation. This balance is crucial in chaotic environments like financial markets, where the potential for useful predictions is debatable and top-tier research often remains undisclosed due to its financial significance.

In my opinion, time-series prediction might be more challenging for backpropagation due to the chaotic nature of its task and loss-function, which must be carefully designed to avoid local minima and overfitting.

This research also highlighted the profound effects of training data, network architecture, hyperparameters, and **loss function design**. Crafting a loss function is particularly nuanced in trading, where there isn't an universal truth: many suitable outcomes exist, some more relistic than others, when it comes to training a model.

Technically, I honed my skills in using **PyTorch** both in Python and C++ (LibTorch), focusing on minimizing CPU-GPU data transfers, crucial for CPU-executed evolutionary strategies.

A key optimization was increasing the tensors' dimensionality, reducing the number of batches needed for each generation's processing. Neuro-evolution's explorative nature demands evaluating numerous models, a process that can be computationally intensive without efficient parallelization.