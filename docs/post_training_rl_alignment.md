# ✍️ Post-Training RL Alignment for Large Reasoning Models

Applying RL to fine-tune large language models and reasoning agents.

## 📌 Concept
RLHF (Reinforcement Learning from Human Feedback) or RLAIF (from AI Feedback) uses an actor (the LLM generating tokens/reasoning chains) and a critic (reward model or process supervisor) to guide the language model output.

## 📊 Diagram
```mermaid
flowchart LR
    Prompt[User Prompt] --> LLM[LLM Actor]
    LLM -->|Response / Reason Step| PRM[Process Reward Model Critic]
    PRM -->|Dense Step-wise Reward| LLM
```

[⬅️ Back to Main README](../README.md)
