# P1: Solve the OpenAI Gym [Taxi V3](https://gym.openai.com/envs/Taxi-v3/) Environment
---

You must meet each of the requirements below to pass the project. The solution has to be submitted as a Jupyter nnotebook. 

## 1: P: for each (state, action), store the (probability, nextstate, reward, done) information based on the topology. Probability is set to 1 since there is a single deterministic nextstate given current state. action_space: id for each action; observation_space: id for each state; isd is intial state distribution and values are equiviprobable. seed(): set random seed; reset(): init the model and pick a random start state; step(): given state and action, get the next state, reward and done status by quering the P table.
Describe the methods and variables in the class DiscreteEnv which is the parent class of the Taxi V3 class.

## 2
Describe the methods and variables in the Taxi V3 class.

## 3
Describe the Taxi V3 environment, its actions, states, reward structure and the rationale behind such a reward structure. 

## 4
Train an algorithm to achieve a 100-episode average reward with a 5th percentile of 7.2 or higher and a 95th percentile of 8.2 or higher on the last 1000 episodes. 

## 5
The algorithm should be able to perform pick-ups and dropoffs with zero penalties over 1000 episodes. 

## 6
Document your solution including all hyper parameters and how those hyperparameters were selected. 
