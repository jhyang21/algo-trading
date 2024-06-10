# Bitcoin Trading Algorithm Combining Artificial Neural Network (ANN) and Drift Diffusion Model (DDM)

## Overview
This project implements an algorithmic trading strategy using an ANN to produce the drift parameter for a DDM. The ANN is trained on historical market data to predict the drift rate, which is then used in the DDM to make trading decisions. The strategy is backtested against historical data to evaluate its performance against buy and hold strategy.

## Rationale: Why combine ANN and DDM?
My hypothesis is that by combining ANN and DDM, we would be able to combine the benefits of both algorithmic trading, the objectiveness, and human trading, the carefulness. DDM is a sequential sampling model that attempts to simulate the noisy human decision-making process based on information accrued over time. Instead of making decision on the spot based on the output layer of the ANN, the output layer then passes through the DDM, a noisy process, which I believe could simulate the charateristics of carefulness and reduce the downside risk. However, this strategy could backfire and only introduce the human indecisiveness, losing the strengths of algorithmic trading and rendering the strategy useless.

## Next Steps
- A benchmark should be created with ANN only to isolate the benefit of combining DDM.
- The neural network architecture should be further refined. 
- I'm interested in testing the strategy with LSTM or xLSTM instead of ANN.

## Version History
Version 1.0: Created the initial version combining ANN and DDM
