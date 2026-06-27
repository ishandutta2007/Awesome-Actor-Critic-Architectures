# 🚀 Deep Distributed Era (A2C & A3C)

Merging Deep Learning with distributed environments to solve complex Reinforcement Learning tasks.

## 📌 Concept
Popularized by Mnih et al. in 2016, this era utilized parallel execution threads to sample decorrelated transitions. 
- **A3C (Asynchronous Advantage Actor-Critic):** Independent CPU threads update a global network asynchronously.
- **A2C (Advantage Actor-Critic):** Synchronous version optimizing GPU utilization.

## 📊 Diagram
```mermaid
flowchart LR
    subgraph Global
        G_AC[Global Actor-Critic Network]
     color:red
    end
    subgraph Worker1 [Worker Thread 1]
        W1[Local Network] --> Env1[Env Clone 1]
    end
    subgraph Worker2 [Worker Thread 2]
        W2[Local Network] --> Env2[Env Clone 2]
    end
    Env1 -->|Gradients| G_AC
    Env2 -->|Gradients| G_AC
    G_AC -->|Pull weights| W1
    G_AC -->|Pull weights| W2
```

[⬅️ Back to Main README](../README.md)
