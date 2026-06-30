# Error-Conditioned Self-Reflective RaCoT

## Overview
This variant tracks token generation confidence/perplexity. Downward spikes in confidence trigger retrieval steps to resolve factual ambiguities.

## Architectural Diagram
```mermaid
flowchart TD
    Generate[Generate Token Flow] --> Monitor{Token Perplexity High?}
    Monitor -- Yes --> Retrieve[Trigger Retrieval]
    Retrieve --> Correct[Correct Generation Path]
    Monitor -- No --> Continue[Continue Generation]
```

## Detailed Explanation
This documentation page provides deeper insights into **Error-Conditioned Self-Reflective RaCoT** under the Retrieval-Augmented Chain-of-Thought (RaCoT) framework. By integrating external reference verification loops directly into active generation cycles, this methodology reduces error rates and stabilizes multi-step reasoning capabilities.

---
[Back to main README](../README.md)
