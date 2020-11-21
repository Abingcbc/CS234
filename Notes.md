# Notes

## L1: Introduction

1. One sentence: Learn to make good sequences of decisions
2. Components
   * Optimization
   * Delayed consequences
   * Exploration
   * Generalization

3. Markov Assumption: Future is independent of past given present

4. Type of Sequential Decision Process:
   * Bandits: actions have no influence on next observations
   * MDPs & POMDPs: actions influence future observations

5. RL Algorithm:
   * Model: Representation of how the world changes in response to agent's action
   * Policy: function mapping agents's states to action
   * Value function: future rewards from being in a state and/or action when following a particular policy

6. Exploration: find more information about environment

   Exploitation: get more benefit using known information

7. 3 Kinds:
   * Value-based: optimize value function
   * Policy-based: optimize policy
   * Model-based: model environment

## L2: Tabular MDP planning

1. Markov Process

   <img src="img/截屏2020-11-11 下午9.11.11.png" alt="截屏2020-11-11 下午9.11.11" style="zoom:50%;" />

2. Discount Factor

   <img src="img/截屏2020-11-11 下午9.12.13.png" alt="截屏2020-11-11 下午9.12.13" style="zoom:50%;" />

3. Markov Decision Process

   <img src="img/截屏2020-11-12 下午2.49.44.png" alt="截屏2020-11-12 下午2.49.44" style="zoom:50%;" />

4. MDP + Policy = MRP

   A Policy is a map from a state to an action.

   ### Policy based

5. MDP Policy Evaluation

   <img src="img/截屏2020-11-14 下午7.46.59.png" alt="截屏2020-11-14 下午7.46.59" style="zoom:50%;" />

6. The optimal value function is unique, but there may be multiple policy to get the value.

   The space size is $|A|^{|S|}$

7. State-Action Value Function: Q

   <img src="img/截屏2020-11-14 下午8.07.36.png" alt="截屏2020-11-14 下午8.07.36" style="zoom:50%;" />

   **This function suppose that we follow $\pi_{i+1}$  only one step and then follow $\pi_i$ forever. **

   $R(s, a)$ is the innermediate reward and the rest part is the future reward following $\pi_{i+1}$

8. <img src="img/截屏2020-11-14 下午8.33.54.png" alt="截屏2020-11-14 下午8.33.54" style="zoom:50%;" />

   **Provement**

   <img src="img/截屏2020-11-14 下午8.34.29.png" alt="截屏2020-11-14 下午8.34.29" style="zoom:50%;" />

   ### Value based

9. <img src="./img/截屏2020-11-14 下午8.40.29.png" alt="截屏2020-11-14 下午8.40.29" style="zoom:50%;" />

10. <img src="img/截屏2020-11-14 下午8.46.14.png" alt="截屏2020-11-14 下午8.46.14" style="zoom:50%;" />

11. Bellman backup operator is a contraction operator.

    Provement

    <img src="img/截屏2020-11-14 下午8.58.40.png" alt="截屏2020-11-14 下午8.58.40" style="zoom:50%;" />

## L3: Model-Free Policy Evaluation

1. Policy search can be considered as searching on a tree

   <img src="img/截屏2020-11-14 下午10.26.19.png" alt="截屏2020-11-14 下午10.26.19" style="zoom:50%;" />

2. Dynamic Programming

   <img src="img/截屏2020-11-14 下午10.25.02.png" alt="截屏2020-11-14 下午10.25.02" style="zoom:50%;" />

   <img src="img/截屏2020-11-14 下午10.30.42.png" alt="截屏2020-11-14 下午10.30.42" style="zoom:50%;" />

3. Monte Carlo

   <img src="img/截屏2020-11-14 下午10.49.52.png" alt="截屏2020-11-14 下午10.49.52" style="zoom:50%;" />

   * First-Visit

     <img src="img/截屏2020-11-14 下午10.51.09.png" alt="截屏2020-11-14 下午10.51.09" style="zoom:50%;" />

   * Every-Visit

   <img src="img/截屏2020-11-14 下午10.56.28.png" alt="截屏2020-11-14 下午10.56.28" style="zoom:50%;" />

   * Incremental-Visit

   <img src="img/截屏2020-11-14 下午11.03.19.png" alt="截屏2020-11-14 下午11.03.19" style="zoom:50%;" />

4. Temporal Difference

   <img src="img/截屏2020-11-14 下午11.43.58.png" alt="截屏2020-11-14 下午11.43.58" style="zoom:50%;" />

   <img src="img/截屏2020-11-14 下午11.44.40.png" alt="截屏2020-11-14 下午11.44.40" style="zoom:50%;" />

   <img src="img/截屏2020-11-14 下午11.45.01.png" alt="截屏2020-11-14 下午11.45.01" style="zoom:50%;" />

5. Difference

   <img src="img/截屏2020-11-14 下午11.48.24.png" alt="截屏2020-11-14 下午11.48.24" style="zoom:50%;" />

   Consistency means infinite dataset, bias means finite dataset.

   First-Visit MC is unbiased and Every-Visit MC is biased.

6. MC vs TD

   <img src="img/截屏2020-11-15 上午12.26.07.png" alt="截屏2020-11-15 上午12.26.07" style="zoom:50%;" />

   <img src="img/截屏2020-11-15 上午12.25.11.png" alt="截屏2020-11-15 上午12.25.11" style="zoom:50%;" />

































