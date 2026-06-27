# ⚖️ Advantage Actor-Critic (A2C/A3C)

Using Advantage baselines to stabilize policy gradients.

## 📌 Concept
Instead of using raw action-values $Q(s, a)$, the advantage function $A(s, a) = Q(s, a) - V(s)$ evaluates actions based on whether they perform better or worse than the average expected outcome.

## 📊 Diagram
```mermaid
flowchart TD
    State[State s] --> Actor[Actor Policy]
    State --> Critic[Critic Value V(s)]
    Actor -->|Action a| Env[Environment]
    Env -->|Reward r| TD[TD Target: r + V(s')]
    TD & Critic --> Advantage[Advantage: TD - V(s)]
    Advantage -->|Update| Actor
```

[⬅️ Back to Main README](../README.md)
