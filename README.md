# Portfolio Selection using Reinforcement Learning 

In this project, I am working on a reinforcement learning algorithm that solves the exploratory mean-variance problem. This algorithm uses accumulative entropy to create exploration in portfolio strategies to achieve a specified target return. The advantage of using such an algorithm over more famous methods such as deep deterministic policy gradient or maximum likelihood estimation is the shorter training time and the lower sensitivity to parameter tuning. This work is inspired by the research paper "Continuous-time mean-variance portfolio selection: A reinforcement learning framework" by Haoran Wang and Xhu Yu Zhou.  


This entire project is based on solving the entropy-regularized mean-variance problem which can be written as the following: 

<img width="714" height="101" alt="emv_portfolio_selection" src="https://github.com/user-attachments/assets/6597d2d2-34b9-49f7-9341-00553e3a9560" />

(details of the notation can be found on the BACHELOR_THESIS_POLYTECHNIQUE.pdf file) 
