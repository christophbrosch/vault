---
category: literaturenote
tags: 
citekey: openai_2024
status: unread
dateread:
---

> [!Cite]
> Openai. (2024). _Prompt Caching in the API_. [https://openai.com/index/api-prompt-caching/](https://openai.com/index/api-prompt-caching/)

>[!Synth]
>**Contribution**:: 
>
>**Related**:: 
>

>[!metadata]
> **FirstAuthor**:: Openai,   
~    
> **Title**:: Prompt Caching in the API  
> **Year**:: 2024   
> **Citekey**:: openai_2024  
> **itemType**:: webpage    

> [!LINK] 
>.

> [!Abstract]
>
> Offering automatic discounts on inputs that the model has recently seen
>> 
# Notes
>.


# Annotations%% begin annotations %%



### Imported: 2025-01-27 10:38 am



<mark style="background-color: #ffd400">Quote</mark>
> Many developers use the same context repeatedly across multiple API calls when building AI applications, like when making edits to a codebase or having long, multi-turn conversations with a chatbot. Today, we’re introducing Prompt Caching, allowing developers to reduce costs and latency. By reusing recently seen input tokens, developers can get a 50% discount and faster prompt processing times.

<mark style="background-color: #ffd400">Quote</mark>
> API calls to supported models will automatically benefit from Prompt Caching on prompts longer than 1,024 tokens. The API caches the longest prefix of a prompt that has been previously computed, starting at 1,024 tokens and increasing in 128-token increments. If you reuse prompts with common prefixes, we will automatically apply the Prompt Caching discount without requiring you to make any changes to your API integration.


%% end annotations %%

%% Import Date: 2025-01-27T10:38:26.671+01:00 %%
