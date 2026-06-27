# 🎯 Moving Target Instability & Target Networks

Addressing the feedback loop problem during training.

## 📌 Concept
Since both the actor and critic are updated continuously, the targets for the critic keep shifting. This is solved by using Target Networks (Polyak/Exponential Moving Averages or Periodic Updates) to stabilize the target values.

## 📊 Diagram
```mermaid
flowchart LR
    Critic[Online Critic Q] -->|Computes Loss| TargetCritic[Target Critic Q-]
    TargetCritic -->|Provides Stable Target| Critic
    Critic -->|Polyak Average Update| TargetCritic
```

[⬅️ Back to Main README](../README.md)
