# Module 1 – LLM Foundations & Prompt Engineering

## References Module 1.2:
+ [LLM API Pricing](https://www.helicone.ai/llm-cost)
+ [Hugging Face — Tokenizers](https://huggingface.co/docs/transformers/tokenizer_summary)
+ [PromptHub - Prompt Engineering](https://www.prompthub.us/blog/the-difference-between-system-messages-and-user-messages-in-prompt-engineering)
+ [Agenta — Manage Context Lengths](https://agenta.ai/blog/top-6-techniques-to-manage-context-length-in-llms)

## Summary Module 1.2:
+ Tokenisation is the process whereby text is broken down into smaller units, with the common approach being Byte Pair Encoding (BPE).
+ When working with LLMs, a few message roles come into play:
    + User – prompts from a human.
    + System – general instructions for the chatbot; shapes its behaviour/style.
    + Assistant – response from the LLM.
+ Context management is key due to the possibility of context being lost; there’s only so much information an LLM can hold (context window). Some of the strategies are:
    + Full History
    + Selective History – a fixed number (n) of texts is stored.
    + Summarisation – a full summary or a summary plus selective history.

## Summary Module 1.3
+ Prompt Engineering:
    + Zero-Shot — basic instructions without examples, “figure it out yourself”.
    + Few-Shot — instructions with examples.
    + Chain-of-Thought (CoT) — thought process outputted enabling user to conduct independent verification.
+ Prompt Chaining — ***To be updated***
+ Structured Outputs — ***To be updated***
+ JSON Validation — ***To be updated***

## Additional Learnings:
In the non-Math example provided by the course material, a simple few-shot prompt like the one below provided a one-word answer.
````
Classify the sentiment of each review as positive, negative, or neutral:
Review: "This phone is amazing! Best purchase I've made all year."
Sentiment: Positive
Review: "The product broke after two days. Complete waste of money."
Sentiment: Negative
Review: "It's okay, nothing special but does what it's supposed to."
Sentiment: Neutral
````
In this example, it appears that Claude is a rather chatty LLM compared to Azure OpenAI and will provide additional justification/reasoning on how it achieved the final outcome. An explicit instruction had to be included to ensure the output matches expectations.
````
Classify the sentiment in {{ question }} as positive, negative, or neutral. Do not include any reasoning, explanation, or extra text.
Review: "This phone is amazing! Best purchase I've made all year."
Sentiment: Positive
Review: "The product broke after two days. Complete waste of money." 
Sentiment: Negative
Review: "It's okay, nothing special but does what it's supposed to." 
Sentiment: Neutral
````
