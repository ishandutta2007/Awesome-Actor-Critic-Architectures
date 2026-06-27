# 📉 Q-Actor-Critic (QAC)

A classic actor-critic architecture where the critic directly learns the action-value function.

## 📌 Concept
The Critic estimates the action-value function $Q(s, a)$. The Actor parameterizes the policy and updates its parameters in the direction of the gradient of the estimated $Q$-values.

## 📊 Diagram
```mermaid
flowchart TD
    s[State s] --> Actor[Actor Policy]
    Actor -->|Action a| Critic[Q-Value Critic Q(s,a)]
    Critic -->|Q Gradient| Actor
```

[⬅️ Back to Main README](../README.md)
