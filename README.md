# Portfolio Selection using Reinforcement Learning 

In this project, I am working on a reinforcement learning algorithm that solves the exploratory mean-variance problem. This algorithm uses accumulative entropy to create exploration in portfolio strategies to achieve a specified target return. The advantage of using such an algorithm over more famous methods such as deep deterministic policy gradient or maximum likelihood estimation is the shorter training time and the lower sensitivity to parameter tuning. This work is inspired by the research paper "Continuous-time mean-variance portfolio selection: A reinforcement learning framework" by Haoran Wang and Xhu Yu Zhou.  



### Theorem 4 (Policy Improvement Theorem) [Wang and Zhou, 2020]

Let w ∈ ℝ, i ∈ ℕ, and let fᶦ = fᶦ(·; ·, ·, w) be an admissible feedback control.  
Assume the value function J^{fᶦ}(·, ·; w) ∈ C^{1,2}([0,T) × ℝ) ∩ C⁰([0,T] × ℝ)  
and satisfies J_{vv}^{fᶦ}(t,v;w) > 0 for all (t,v) ∈ [0,T) × ℝ.
Define:

```math
\boldsymbol{f}^{i+1}(\theta; t,v,w) = f_{\mathcal{N} \left(-\frac{\gamma}{\sigma} \frac{J^{\boldsymbol{f}^i}_{v}(t, v;w)}{J^{\boldsymbol{f}^i}_{vv}(t, v;w)}, \frac{\lambda}{\sigma^2 J^{\boldsymbol{f}^i}_{vv}(t, v;w)} \right)}(\theta)
