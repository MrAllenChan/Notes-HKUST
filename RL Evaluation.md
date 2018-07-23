**Evaluation of Reinforcement Learning**
横向：比较两个算法—累计奖励曲线，三个统计指标
纵向：
1. performance-informative? p909这篇论文重点在可视化，把历史和当前performance反馈给human，而不是在衡量evaluating state-action value functions

2. marivate：Expected return、MFMC、Distance from optimal values等

我们的工作重点，在于可视化，影响人类，还是用算法来衡量并提升模型？
q-learning中的π，我们做的决策，argmax Q(s,a)？

**Evaluating Reinforcement Learning Algorithms**
We can judge a reinforcement learning algorithm by how good a policy it finds and how much reward it receives while acting in the world. Which is more important depends on how the agent will be deployed. If there is sufficient time for the agent to learn safely before it is deployed, the final policy may be the most important. If the agent has to learn while being deployed, it may never get to the stage where it has learned the optimal policy, and the reward it receives while learning may be what the agent wants to maximize.
One way to show the performance of a reinforcement learning algorithm is to plot the cumulative reward (the sum of all rewards received so far) as a function of the number of steps. One algorithm dominates another if its plot is consistently above the other.

There are three statistics of this plot that are important:
* The asymptotic slope shows how good the policy is after the algorithm has stabilized.
* The minimum of the curve shows how much reward must be sacrificed before it starts to improve.
* The zero crossing shows how long it takes until the algorithm has recouped its cost of learning.
The last two statistics are applicable when both positive and negative rewards are available and having these balanced is reasonable behavior. For other cases, the cumulative reward should be compared with reasonable behavior that is appropriate for the domain; 

One thing that should be noted about the cumulative reward plot is that it measures total reward, yet the algorithms optimize discounted reward at each step. In general, you should optimize for, and evaluate your algorithm using, the optimality criterion that is most appropriate for the domain.

Reference: 
Poole D L, Mackworth A K. Artificial Intelligence: Foundations of Computational Agents[M]. Cambridge University Press, 2010.
link: 
https://artint.info/html/ArtInt_267.html


**Paper:Using Informative Behavior to Increase Engagement in the TAMER Framework**
核心思想：investigating how the agent’s non-task behavior can elicit human feedback of higher quality and quantity 
主要方法：two new training interfaces to increase active involvement in the training process and thereby improve the agent’s task performance. 
1. One provides information on the agent’s uncertainty — uncertainty-informative interface, the agent informs the human of its uncertainty about the actions it selects, in the hope that this motivates the human to reduce that uncertainty by focusing feedback on the most needed areas 
2. the other on its performance.  performance- informative interface, the agent informs the human about its current performance in the task relative to its earlier performance, which we expect will motivate the human to give the feedback needed to further improve this performance 

几种比较：
Learning from Demonstration — 重点在于match or mimic teacher’s motion, 这个过程中agent是被动的，不能主动的收集数据来影响学习过程，只能模仿行为，很大程度上受到了老师的skill level的限制

Learning from Human Feedback  — 重点在于human provide feedback signals that evaluate the quality of the agent’s actions and state transitions ，这种方法requires less task expertise and places less cognitive load on the trainer 
TAMAR->RL->RL+TAMER：the agent learns from both human and environmental feedback, which can lead to better performance than learning from either alone. 

Agent Behavior that Influences the Trainer: how to improve training through the interface design
















