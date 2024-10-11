The **Markov Property** states that the future state of the environment depends only on the current state and the action taken, not on the sequence of events that preceded it. In other words, the future is independent of the past, given the present.

### Formal Definition

An MDP is formally defined by the tuple (S,A,T,R,γ)(S, A, T, R, \gamma)(S,A,T,R,γ), where:

- SSS is the set of states,
- AAA is the set of actions,
- TTT is the transition function (or model of the environment),
- RRR is the reward function,
- γ\gammaγ is the discount factor.

### Objective in MDP

The objective in an MDP is to find a policy π\piπ that maximizes the **expected cumulative reward**, also known as the **return**. The return can be defined as:

Gt=Rt+1+γRt+2+γ2Rt+3+…G_t = R_{t+1} + \gamma R_{t+2} + \gamma^2 R_{t+3} + \dotsGt​=Rt+1​+γRt+2​+γ2Rt+3​+…

Where GtG_tGt​ is the return at time step ttt, and RtR_tRt​ is the reward at time ttt.

### Summary of Steps in an MDP

1. **Agent observes the current state** s∈Ss \in Ss∈S.
2. **Agent selects an action** a∈Aa \in Aa∈A, based on its policy π(s)\pi(s)π(s).
3. **Environment transitions** to a new state s′∈Ss' \in Ss′∈S with probability P(s′∣s,a)P(s' | s, a)P(s′∣s,a).
4. **Agent receives a reward** r=R(s,a,s′)r = R(s, a, s')r=R(s,a,s′).
5. The process repeats from step 1, and the agent updates its policy based on the rewards it accumulates.

By interacting with the environment and optimizing its policy, the agent learns to make decisions that maximize the total return in the long run.