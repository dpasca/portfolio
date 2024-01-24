---
---
- Financial market forecasting using Artificial Neural Networks
- Vehicle navigation: pathfinding and obstacle avoidance
- Custom C++ Neural Networks implementation (inference and training)
- Neural Networks with PyTorch using C++ and Python
- Genetic algorithms, neuro-evolution, REINFORCE-ES

#### Professional Journey

Below are the highlights of my involvement in AI and machine-learning at various stages of my career.

##### 1) Simulation and AI

My journey in machine-learning started in 2017, when I started to design auto-pilot logic for the plane and missiles airframes in my experimental flight simulator [XPSVR](#xpsvr-experimental-flight-simulator).

Simulation is a key component of machine-learning as it forms the basis for training at a **much faster pace and a much reduced cost**, especially when dealing with extremely expensive or dangerous tasks, such as flight and weapon delivery.

##### 2) Algorithmic Trading and Neural Networks

In 2018 I started to apply basic ML to **financial market forecasting** for the [ENZO Trading System](#enzo-trading-system).

By early 2023, my focus shifted towards **Artificial Neural Networks**, tackling increasingly complex tasks from autonomous driving to sophisticated time-series prediction models, now deployed in live trading.

##### 3) LLM-based Virtual Assistants and Agents

In late 2023, I developed [ChatAI](https://github.com/dpasca/ChatAI), a virtual assistant integrating **OpenAI's API** that uses **function-calling** and implements a **multi-agent** architecture to enhance the user's experience in terms of usefulness and reliability.
Function-calling and **prompt-injection** are used to give the assistant a sense of location and time of the user.

Parallel agents are used to **fact-check the conversation** and provide additional information on the subject being discussed. This approach, while requiring additional token budget, **addresses the hallucination issue** that arises from naive use of an LLM. The increase in reliability for the user is ultimately worth the additional cost, as it **saves time** that the user would otherwise have to spend for manual verification or, worse, risk being completely misinformed.

The assistant operates as a web app, leveraging *Flask*, *Bootstrap*, and additional external modules for code syntax highlighting and LaTeX rendering, but at the core it's a Python application that is adaptable to other platforms.

This is an ongoing project used both for deployment and internal research.

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

##### 4) My Open Sourced AI Projects

See the sources of my other [AI projects & experiments](https://github.com/topics/ai?q=user:dpasca) on GitHub.

#### Insights Gained

Building a system from simple cases was essential in grasping the core concepts involved.

In time-series prediction, **Evolution Strategies (ES)** proved effective, particularly with limited computational resources. While backpropagation is generally more efficient and likely a better solution long-term, the evolutionary approach facilitated a better balance between exploration and exploitation. This balance is crucial in chaotic environments like financial markets, where the potential for useful predictions is debatable and top-tier research often remains undisclosed due to its financial significance.

In my opinion, time-series prediction might be more challenging for backpropagation due to the chaotic nature of its task and loss-function, which must be carefully designed to avoid local minima and overfitting.

This research also highlighted the profound effects of training data, network architecture, hyperparameters, and **loss function design**. Crafting a loss function is particularly nuanced in trading, where there isn't an universal truth: many suitable outcomes exist, some more relistic than others, when it comes to training a model.

Technically, I honed my skills in using **PyTorch** both in Python and C++ (LibTorch), focusing on minimizing CPU-GPU data transfers, crucial for CPU-executed evolutionary strategies.

A key optimization was increasing the tensors' dimensionality, reducing the number of batches needed for each generation's processing. Neuro-evolution's explorative nature demands evaluating numerous models, a process that can be computationally intensive without efficient parallelization.