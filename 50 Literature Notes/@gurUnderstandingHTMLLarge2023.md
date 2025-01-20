---
category: literaturenote
tags: Computer Science - Machine Learning, Computer Science - Artificial Intelligence
citekey: gurUnderstandingHTMLLarge2023
status: unread
dateread:
---

> [!Cite]
> Gur, I., Nachum, O., Miao, Y., Safdari, M., Huang, A., Chowdhery, A., Narang, S., Fiedel, N., & Faust, A. (2023). _Understanding HTML with Large Language Models_ (No. arXiv:2210.03945). arXiv. [https://doi.org/10.48550/arXiv.2210.03945](https://doi.org/10.48550/arXiv.2210.03945)

>[!Synth]
>**Contribution**:: 
>
>**Related**:: 
>

>[!metadata]
> **FirstAuthor**:: Gur, Izzeddin  
> **Author**:: Nachum, Ofir  
> **Author**:: Miao, Yingjie  
> **Author**:: Safdari, Mustafa  
> **Author**:: Huang, Austin  
> **Author**:: Chowdhery, Aakanksha  
> **Author**:: Narang, Sharan  
> **Author**:: Fiedel, Noah  
> **Author**:: Faust, Aleksandra  
~    
> **Title**:: Understanding HTML with Large Language Models  
> **Year**:: 2023   
> **Citekey**:: gurUnderstandingHTMLLarge2023  
> **itemType**:: preprint  
> **DOI**:: 10.48550/arXiv.2210.03945    

> [!LINK] 
>
>  [PDF](file:///home/cbrosch/Zotero/storage/CKUKTVQ2/Gur%20et%20al.%20-%202023%20-%20Understanding%20HTML%20with%20Large%20Language%20Models.pdf).

> [!Abstract]
>
> Large language models (LLMs) have shown exceptional performance on a variety of natural language tasks. Yet, their capabilities for HTML understanding -- i.e., parsing the raw HTML of a webpage, with applications to automation of web-based tasks, crawling, and browser-assisted retrieval -- have not been fully explored. We contribute HTML understanding models (fine-tuned LLMs) and an in-depth analysis of their capabilities under three tasks: (i) Semantic Classification of HTML elements, (ii) Description Generation for HTML inputs, and (iii) Autonomous Web Navigation of HTML pages. While previous work has developed dedicated architectures and training procedures for HTML understanding, we show that LLMs pretrained on standard natural language corpora transfer remarkably well to HTML understanding tasks. For instance, fine-tuned LLMs are 12% more accurate at semantic classification compared to models trained exclusively on the task dataset. Moreover, when fine-tuned on data from the MiniWoB benchmark, LLMs successfully complete 50% more tasks using 192x less data compared to the previous best supervised model. Out of the LLMs we evaluate, we show evidence that T5-based models are ideal due to their bidirectional encoder-decoder architecture. To promote further research on LLMs for HTML understanding, we create and open-source a large-scale HTML dataset distilled and auto-labeled from CommonCrawl.
>> 
# Notes
>.


# Annotations%% begin annotations %%



### Imported: 2025-01-20 1:09 pm



<mark style="background-color: #ffd400">Quote</mark>
> In this paper, we investigate whether LLMs can be applied to HTML understanding to produce better-performing, more sample-efficient HTML understanding models and without the need for custom NN architecture design.

<mark style="background-color: #ffd400">Quote</mark>
> First, we devise Semantic Classification as a task that requires a model to classify a given HTML element into one of a set of categories, such as address, email, password etc., with application to automated form-filling.

<mark style="background-color: #ffd400">Quote</mark>
> Second, we present Description Generation, a label-extraction task where a model is given an HTML snippet and is asked to produce a natural language description.

<mark style="background-color: #ffd400">Quote</mark>
> The third task is Autonomous Web Navigation (Shi et al., 2017). A model is presented with an HTML page paired with a natural language command and must apply appropriate actions on a sequence of HTML pages to satisfy the command.

<mark style="background-color: #ffd400">Quote</mark>
> Our results show that LLMs demonstrate a remarkable level of HTML understanding across all tasks, with up to 192× more sample-efficiency than models trained from scratch, and achieving a new SoTA for supervised learning on the MiniWoB benchmark suite (Shi et al., 2017). The encoder-decoder architectures with bi-directional attention show the best performance across the board even when their pretraining does not include HTML. In addition, we show that the performance scales sub-linearly with the model size.

<mark style="background-color: #2ea8e5">Section</mark>
> PRE-PROCESSING

<mark style="background-color: #f19837">Challange</mark>
> Snippet Extraction. Real HTML pages can grow extremely large, reaching thousands of elements, far beyond the context window of the largest LLM that we studied (1920 tokens in PaLM (Chowdhery et al., 2022)). LLMs typically truncate such long sequences, which can be detrimental to HTML understanding as HTMLs are not linearly structured. We take an element-centric approach and extract HTML snippets (a small portion of HTML code) surrounding a salient element (Figure 5).

<mark style="background-color: #2ea8e5">Section</mark>
> SEMANTIC CLASSIFICATION TASK RESULTS

<mark style="background-color: #ffd400">Quote</mark>
> Accuracy per category. In Figure 3, we present accuracy distribution of the WebC-T5-3B model on the development dataset. The fine-tuned encoder-decoder model performs strongly on a majority of the categories (Figure 3), even on those with very few samples. For instance, the model is 100% accurate on password new which has only 56 training examples, because the class is unambiguous. On the other hand, unsurprisingly, the performance drops when the category is ambiguous, such as in the email category which is frequently mistaken as username.

<mark style="background-color: #ff6666">Conclusion</mark>
> We presented canonical tasks and fine-tuned LLMs for HTML understanding. The comprehensive evaluations and analyses over a range of architectures, dataset sizes, and baselines yields practical findings and highlights current limitations of these models. We find that a) pretraining is critical for the performance and can reduce labeled data requirements, improving sample efficiency up to 200x; b) model architecture is the second-most important factor, and T5 models with bidirectional attention and encoder-decoder architecture perform the best across the board; c) given a choice, model size should be evaluated in the context of the model’s training and inference performance, as the model size sub-linearly correlates with its performance. Finally, the proposed HTML understanding tasks highlight the relatively short context window that limits current LLMs, suggesting possibilities for future research that incorporate or eliminate this constraint.


%% end annotations %%

%% Import Date: 2025-01-20T13:09:30.247+01:00 %%
