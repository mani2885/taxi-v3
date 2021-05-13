# P1: Solve the OpenAI Gym [Taxi V3](https://gym.openai.com/envs/Taxi-v3/) Environment
---

You must meet each of the requirements below to pass the project. The solution has to be submitted as a Jupyter nnotebook. 

## 1: P (reward table): for each (state, action), store the (probability, nextstate, reward, done) information based on the topology. Probability is set to 1 since there is a single deterministic next state given the current state. action_space: id for each action; observation_space: id for each state; isd is intial state distribution and values are equiviprobable. seed(): set random seed; reset(): init the model and pick a random start state; step(): given state and action, get the next state, reward and done status by quering the P table.
Describe the methods and variables in the class DiscreteEnv which is the parent class of the Taxi V3 class.

## 2 init(): primary task is to populate the P table according to the topology - for each state, set the appropriate next state, reward and done status. initial_state_distrib assigns equal probablity to each valid state. The number of states is 500 = 25*5*4: the taxi could be in any of the 25 squares, the passenger could be in any of the 5 locations (4 passenger designated locations + taxi), the destination is any of the 4 passenger designated: each of the three quantites are all independent and can occur in any combination. total actions are 6. encode() gets the state id given the state information (location of taxi, passenger, destination). decode() gives the state information given the state id. render() draws the topology given the state information
Describe the methods and variables in the Taxi V3 class.

## 3 The 6 discrete deterministic actions move N, E, W, S, pickup and drop off. default per-step reward of -1, this is to penalize if taking longer route than necessary. delivering the passenger is +20 as this is the end goal. penalize -10 if pick-up executed at wrong location or drop off at wrong location. But it is not clear to me the rationale to set penality at -10 instead of say -20 or more.
Describe the Taxi V3 environment, its actions, states, reward structure and the rationale behind such a reward structure. 

## 4 Submitted in P1.ipynb
Train an algorithm to achieve a 100-episode average reward with a 5th percentile of 7.2 or higher and a 95th percentile of 8.2 or higher on the last 1000 episodes. 

## 5 
The algorithm should be able to perform pick-ups and dropoffs with zero penalties over 1000 episodes. 

## 6
Document your solution including all hyper parameters and how those hyperparameters were selected. 
