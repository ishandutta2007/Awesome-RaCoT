# Thought-Tree Search RaCoT (MCTS-RaCoT)

## Overview
Thought-Tree Search combines Tree-of-Thoughts with active retrieval, scoring factuality of branches using MCTS to prune invalid paths.

## Architectural Diagram
```mermaid
flowchart TD
    Root[Initial State] --> Branch1[Thought Branch A]
    Root --> Branch2[Thought Branch B]
    Branch1 --> Eval1[RAG Fact-Check & Grade]
    Branch2 --> Eval2[RAG Fact-Check & Grade]
    Eval1 --> MCTS[MCTS Pruning & Selection]
    Eval2 --> MCTS
```

## Detailed Explanation
This documentation page provides deeper insights into **Thought-Tree Search RaCoT (MCTS-RaCoT)** under the Retrieval-Augmented Chain-of-Thought (RaCoT) framework. By integrating external reference verification loops directly into active generation cycles, this methodology reduces error rates and stabilizes multi-step reasoning capabilities.

---
[Back to main README](../README.md)
