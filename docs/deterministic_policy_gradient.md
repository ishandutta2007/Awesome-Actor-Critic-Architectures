# 🎯 Deterministic Policy Gradient (DDPG / TD3)

Tailoring actor-critic methods to deterministic continuous action spaces.

## 📌 Concept
Introduced in DPG and scaled up in DDPG and TD3, the actor outputs a deterministic action $a = \mu(s)$. The critic evaluates this action, and the policy parameters are updated in the direction of the critic's gradient with respect to the action coordinates.

## 📊 Diagram
```mermaid
flowchart LR
    State[State s] --> Actor[Deterministic Actor]
    Actor -->|Action a| Critic[Action-Value Critic Q(s,a)]
    Critic -->|Chain Rule Gradient w.r.t action| Actor
```

[⬅️ Back to Main README](../README.md)
