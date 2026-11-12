<!-- 
[MD Tips](https://commonmark.org/help/tutorial/) 
<ins>***To be updated***</ins>
-->

# Module 2 – Retrieval Augmented Generation

<ins>***To be updated***</ins>

## References Module 2.1
+ [Helicone — LLM API Pricing](https://www.helicone.ai/llm-cost)

## Summary Module 2.1
+ When working with LLMs, a few message roles come into play:
    + User – prompts from a human.

```mermaid
graph LR
    A[Documents] -->|1. Encoding| C(Embedding Model)
    B[User Query] -->|3. Encoding| C
    C -->|2. Indexing| D[(Vector Database)]
    C -->|4. Similarity Search| D
    D -->|5. Retrieval| E[User Query + Docs]
    E -->|6. Prompt| F(LLM)
    F -->|7. Generation| G[Response]
```
