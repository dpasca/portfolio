---
---
This section summarizes the AI and machine-learning work that connects several of the newer projects listed above.

- Financial market forecasting using artificial neural networks
- Vehicle navigation, pathfinding, obstacle avoidance, and autopilot logic
- Custom C++ neural network implementation for inference and training
- Neural networks with PyTorch, Python, and C++/LibTorch
- Genetic algorithms, neuro-evolution, and REINFORCE-ES
- LLM applications with model routing, tool orchestration, memory, search, and agentic workflows
- AI-assisted production pipelines for games, tools, screenshots, localization checks, and release assets

#### Professional Journey

Below are the highlights of my involvement in AI and machine learning at various stages of my career.

##### 1) Simulation and AI

My journey in machine learning started in 2017, when I began designing autopilot logic for the plane and missile airframes in my experimental flight simulator [XPSVR](#xpsvr-experimental-flight-simulator).

Simulation is a key component of machine learning because it forms the basis for training at a **much faster pace and a much reduced cost**, especially when dealing with extremely expensive or dangerous tasks such as flight and weapon delivery.

##### 2) Algorithmic Trading and Neural Networks

In 2018 I started applying ML to **financial market forecasting** for the [ENZO Trading System](#enzo-trading-system).

By early 2023, my focus shifted toward **artificial neural networks**, tackling increasingly complex tasks from autonomous driving experiments to sophisticated time-series prediction models deployed in live trading.

##### 3) LLM-Based Assistants and Agents

Since late 2023, my AI work has increasingly focused on LLM systems: model routing, tool use, memory, search, image generation, and agentic workflows.

That work is now represented most clearly by [AskMei.ai](#askmei-ai), a production AI assistant and multi-instance platform, and by [Little Control Room](#little-control-room), a terminal-first AI development tool for coordinating Codex, OpenCode, Claude Code, and an experimental native agent called LCAgent.

##### 4) AI-Assisted Games and Production Workflows

I also use AI as a production multiplier for games and interactive projects. [Fractal Strike](#fractal-strike) is an example of an AI-first game production workflow, while [RogueLLM](#rogue-llm) explores LLM-generated worlds and game content inside a deterministic roguelike structure.

#### Insights Gained

Building systems from simple cases was essential in grasping the core concepts involved.

In time-series prediction, **Evolution Strategies (ES)** proved effective, particularly with limited computational resources. While backpropagation is generally more efficient and likely a better long-term solution, the evolutionary approach provided a practical balance between exploration and exploitation. This balance is crucial in chaotic environments like financial markets, where the potential for useful predictions is debatable and top-tier research often remains undisclosed due to its financial significance.

In my opinion, time-series prediction can be especially challenging for backpropagation because of the chaotic nature of the task and the loss function, which must be carefully designed to avoid local minima and overfitting.

This research also highlighted the profound effects of training data, network architecture, hyperparameters, and **loss function design**. Crafting a loss function is particularly nuanced in trading, where there is no universal truth: many suitable outcomes exist, some more realistic than others, when it comes to training a model.

Technically, I honed my skills in using **PyTorch** both in Python and C++ (LibTorch), focusing on minimizing CPU-GPU data transfers, which is crucial for CPU-executed evolutionary strategies.

A key optimization was increasing tensor dimensionality, reducing the number of batches needed for each generation's processing. Neuro-evolution's explorative nature demands evaluating numerous models, a process that can be computationally intensive without efficient parallelization.

The more recent LLM work reinforced a different lesson: reliability comes less from a single clever prompt and more from architecture. Clear tool schemas, bounded agent loops, model tiering, memory hygiene, verification, and user control all matter.
