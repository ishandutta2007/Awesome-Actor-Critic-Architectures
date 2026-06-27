# 🔮 Off-Policy Maximum Entropy (SAC)

The modern gold standard for continuous control and robotics tasks.

## 📌 Concept
Soft Actor-Critic (SAC) incorporates an entropy regularization term into the RL objective. The objective encourages exploration by maximizing the policy's expected reward and its entropy simultaneously.

## 📊 Diagram
```mermaid
flowchart TD
    State[State s] --> Actor[Stochastic Actor]
    Actor -->|Action a| Env[Environment]
    Env -->|Reward r + Entropy| RewardCalc[Augmented Reward]
    RewardCalc --> Critic[Soft Q-Critic]
    Critic -->|Soft Q-Values| Actor
```

[⬅️ Back to Main README](../README.md)
