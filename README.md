# FinRL2025
Code for FinRL Contest 2025

The code in this repository, further detailed in the attached paper, aims to develop efficiently engineered prompts to generate DeepSeek-V3-based sentiment signals, integrate them into the FinRL environment, and improve the performance of reinforcement learning trading agents.

The key modifications to the FinRL environment setup, as further detailed in the 'Incorporation of LLM-Generated Signals into FinRL Environment' sub-section of the Methodology section of the paper, are summarized below:

	To integrate LLM-generated sentiment signals into the FinRL-based trading agents, we made the following modifications to the environment setup:
 
Each stock at each time step is represented by its OHLC prices, and the corresponding DeepSeek-V3 generated sentiment score
The sentiment scores were appended directly to the stock feature vector
We extended the FinRL data preprocessing pipeline to merge DeepSeek-V3 sentiment signals with trade data on a per-date and per-stock basis
The RL  agent (PPO agent) observes a richer state containing traditional technical indicators and sentiment-based signals at every time step
No changes were made to the reward function. The change in portfolio value ensures comparability with baseline FinRL agents
