# Interleaved Step-by-Step Retrieval (IRCoT)

## Overview
IRCoT generates one step at a time, using the newly generated sentence as a search query to pull fresh documents recursively.

## Architectural Diagram
```mermaid
flowchart TD
    Input[Input Question] --> Step[Generate Next Step]
    Step --> Ret[Retrieve Info using Step]
    Ret --> Update[Update Prompt Context]
    Update --> Check{Loop Done?}
    Check -- No --> Step
    Check -- Yes --> FinalAnswer[Final Answer]
```

## Detailed Explanation
This documentation page provides deeper insights into **Interleaved Step-by-Step Retrieval (IRCoT)** under the Retrieval-Augmented Chain-of-Thought (RaCoT) framework. By integrating external reference verification loops directly into active generation cycles, this methodology reduces error rates and stabilizes multi-step reasoning capabilities.

---
[Back to main README](../README.md)
