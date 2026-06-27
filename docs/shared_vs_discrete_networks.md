# 🧠 Shared vs. Discrete Parameter Networks

Architectural choices in neural network design for Actor-Critic models.

## 📌 Concept
- **Shared Network:** The Actor and Critic share early layers (e.g., visual feature extractors), branching out only at the output head.
- **Discrete Network:** Completely separate neural network graphs for the Actor and Critic to prevent gradient interference.

## 📊 Diagram
```mermaid
flowchart TD
    subgraph Shared Network
        Input1[Input] --> Backbone[Shared Backbone Layer]
        Backbone --> ActorHead[Actor Head]
        Backbone --> CriticHead[Critic Head]
    end
    subgraph Discrete Network
        Input2[Input] --> ActorNet[Actor Network]
        Input2 --> CriticNet[Critic Network]
    end
```

[⬅️ Back to Main README](../README.md)
