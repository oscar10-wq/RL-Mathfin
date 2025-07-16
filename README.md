# Portfolio Selection using Reinforcement Learning 

In this project, I am working on a reinforcement learning algorithm that solves the exploratory mean-variance problem. This algorithm uses accumulative entropy to create exploration in portfolio strategies to achieve a specified target return. The advantage of using such an algorithm over more famous methods such as deep deterministic policy gradient or maximum likelihood estimation is the shorter training time and the lower sensitivity to parameter tuning. This work is inspired by the research paper "Continuous-time mean-variance portfolio selection: A reinforcement learning framework" by Haoran Wang and Xhu Yu Zhou.  


This entire project is based on two important results which are the following: 




### **Theorem 4.0** (Policy Improvement Theorem) [Wang & Zhou, 2020]

Let `w ∈ ℝ`, `i ∈ ℕ`, and let `fⁱ = fⁱ(·; ·, ·, w)` be an admissible feedback control.  
Assume the corresponding value function `J^{fⁱ}(·, ·; w)` lies in  
`C^{1,2}([0,T) × ℝ) ∩ C⁰([0,T] × ℝ)`  
and satisfies `J_{vv}^{fⁱ}(t, v; w) > 0` for all `(t, v) ∈ [0, T) × ℝ`.

Suppose the feedback control `fⁱ⁺¹` is defined by:

```
fⁱ⁺¹(θ; t, v, w) = f_{𝒩(μ, σ²)}(θ)

where:
  μ   = - (γ / σ) * (J_v^{fⁱ}(t, v; w)) / (J_{vv}^{fⁱ}(t, v; w))
  σ²  = λ / (σ² * J_{vv}^{fⁱ}(t, v; w))
```

and `fⁱ⁺¹` is admissible. Then the value function improves (or remains the same):

```
J^{fⁱ⁺¹}(t, v; w) ≤ J^{fⁱ}(t, v; w)   for all (t, v) ∈ [0, T] × ℝ
```
