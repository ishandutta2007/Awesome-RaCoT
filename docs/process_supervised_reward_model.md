# Process-Supervised Reward Model (PRM) Verification

## Overview
Uses a value network to score the correctness of individual reasoning steps, verifying factual claims against knowledge sources.

## Architectural Diagram
```mermaid
flowchart TD
    Step[Reasoning Step Generated] --> PRM[PRM Evaluator]
    PRM --> FactCheck[Fact-check via RAG]
    FactCheck --> Score[Score Step Quality]
    Score --> Dec{Accept Step?}
    Dec -- Yes --> Next[Proceed to Next Step]
    Dec -- No --> Backtrack[Backtrack and Regenerate]
```

## Detailed Explanation
This documentation page provides deeper insights into **Process-Supervised Reward Model (PRM) Verification** under the Retrieval-Augmented Chain-of-Thought (RaCoT) framework. By integrating external reference verification loops directly into active generation cycles, this methodology reduces error rates and stabilizes multi-step reasoning capabilities.

---
[Back to main README](../README.md)
