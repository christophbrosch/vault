---
category: literaturenote
tags: Computer Science - Computation and Language, Computer Science - Artificial Intelligence
citekey: huangAutoScraperProgressiveUnderstanding2024
status: unread
dateread:
---

> [!Cite]
> Huang, W., Gu, Z., Peng, C., Li, Z., Liang, J., Xiao, Y., Wen, L., & Chen, Z. (2024). _AutoScraper: A Progressive Understanding Web Agent for Web Scraper Generation_ (No. arXiv:2404.12753). arXiv. [https://doi.org/10.48550/arXiv.2404.12753](https://doi.org/10.48550/arXiv.2404.12753)

>[!Synth]
>**Contribution**:: 
>
>**Related**:: 
>

>[!metadata]
> **FirstAuthor**:: Huang, Wenhao  
> **Author**:: Gu, Zhouhong  
> **Author**:: Peng, Chenghao  
> **Author**:: Li, Zhixu  
> **Author**:: Liang, Jiaqing  
> **Author**:: Xiao, Yanghua  
> **Author**:: Wen, Liqian  
> **Author**:: Chen, Zulong  
~    
> **Title**:: AutoScraper: A Progressive Understanding Web Agent for Web Scraper Generation  
> **Year**:: 2024   
> **Citekey**:: huangAutoScraperProgressiveUnderstanding2024  
> **itemType**:: preprint  
> **DOI**:: 10.48550/arXiv.2404.12753    

> [!LINK] 
>
>  [Preprint PDF](file:///home/cbrosch/Zotero/storage/9B7KMYDK/Huang%20et%20al.%20-%202024%20-%20AutoScraper%20A%20Progressive%20Understanding%20Web%20Agent%20for%20Web%20Scraper%20Generation.pdf).

> [!Abstract]
>
> Web scraping is a powerful technique that extracts data from websites, enabling automated data collection, enhancing data analysis capabilities, and minimizing manual data entry efforts. Existing methods, wrappers-based methods suffer from limited adaptability and scalability when faced with a new website, while language agents, empowered by large language models (LLMs), exhibit poor reusability in diverse web environments. In this work, we introduce the paradigm of generating web scrapers with LLMs and propose AutoScraper, a two-stage framework that can handle diverse and changing web environments more efficiently. AutoScraper leverages the hierarchical structure of HTML and similarity across different web pages for generating web scrapers. Besides, we propose a new executability metric for better measuring the performance of web scraper generation tasks. We conduct comprehensive experiments with multiple LLMs and demonstrate the effectiveness of our framework. Resources of this paper can be found at \url{https://github.com/EZ-hwh/AutoScraper}
>> 
# Notes
>
>Comment: 19 pages, 4 figures, 18 tables. Accepted to EMNLP 2024.


# Annotations%% begin annotations %%



### Imported: 2025-01-20 10:38 am



<mark style="background-color: #2ea8e5">Section</mark>
> Introduction

<mark style="background-color: #ffd400">Quote</mark>
> Due to the diversity of sources and information on the internet, the construction of a web scraper requires substantial human effort. Consequently, two types of methods for automatic web information acquisition have been proposed, categorized as wrapper-based and language-agent-based

<mark style="background-color: #ffd400">Quote</mark>
> The wrapper-based method entails complex sequences of operations within customized rule-based functions, which are designed to efficiently access and retrieve desired data from websites, which is especially beneficial for structured websites with stable layouts (Kushmerick, 1997; Dalvi et al., 2011; Bronzi et al., 2013).

<mark style="background-color: #ffd400">Quote</mark>
> Conversely, the language-agent-based method leverages powerful natural language processing capabilities of large language models (LLMs) to interpret free-text queries and directly extract data within websites to meet the demand, effectively handling both structured and dynamic web content (Whitehouse et al., 2023; Marco Perini, 2024).

<mark style="background-color: #ffd400">Quote</mark>
> although language-agent-based methods demonstrate superior performance in adapting to new content, their reliance on a limited number of superpowerful API-based LLMs for web scraping incurs considerable time and financial costs.

<mark style="background-color: #5fb236">Thesis</mark>
> To address the shortcomings of the aforementioned two paradigms, the paradigm of generating web scrapers with LLMs would be the optimal solution. On one hand, compared to wrapper-based methods, it fully leverages the reasoning and reflection capacities of LLMs, reducing manual design on new tasks and enhancing scalability. On the other hand, compared to language-agent-based methods, it introduces repeatable extraction procedures, reducing the dependency on LLMs when dealing with similar tasks, and thereby improving efficiency when handling a large number of web tasks.

<mark style="background-color: #f19837">Challange</mark>
> Long HTML document.

<mark style="background-color: #f19837">Challange</mark>
> Reusability.

<mark style="background-color: #f19837">Challange</mark>
> Appropriate evaluation metrics.

<mark style="background-color: #ffd400">Quote</mark>
> AUTOSCRAPER comprises two main components: progressive generation and synthesis. The progressive generation stage leverages the hierarchical structure of HTML for progressive understanding to address the long HTML document. Subsequently, the synthesis module integrates multiple scrapers generated on different web pages to produce a cohesive, website specific scraper that functions universally within that site. Besides, we propose a new evaluation metric for web scraper generation tasks, called the executability metric. Unlike traditional information extraction metrics that measure single web pages, this metric measures multiple web pages within a website, accurately reflecting the reliability and reusability of the scraper.

<mark style="background-color: #ffd400">Quote</mark>
![[image-4-x70-y446.png]]

<mark style="background-color: #ffd400">Quote</mark>
> AUTOSCRAPER comprises two main components: progressive generation and synthesis. The progressive generation stage leverages the hierarchical structure of HTML for progressive understanding to address the long HTML document. Subsequently, the synthesis module integrates multiple scrapers generated on different web pages to produce a cohesive, websitespecific scraper that functions universally within that site. Besides, we propose a new evaluation metric for web scraper generation tasks, called the executability metric. Unlike traditional information extraction metrics that measure single web pages, this metric measures multiple web pages within a website, accurately reflecting the reliability and reusability of the scraper.

<mark style="background-color: #2ea8e5">Section</mark>
> Comparison with LLM Direct Extraction

<mark style="background-color: #ffd400">Quote</mark>
> Table 4 shows that in the direct extraction setting, the extraction performance of all LLMs other than GPT-4-Turbo is superior to that of AUTOSCRAPER. However, as the capability of LLMs improves, the gap between the two settings narrows.

<mark style="background-color: #ffd400">Quote</mark>
> 1. While LLMs like Phi-3-medium can understand webpage content well (i.e., correctly extract the expected content), they still struggle to comprehend webpage structures (i.e., generating XPath using features like DOM tree).

<mark style="background-color: #ffd400">Quote</mark>
> 2. AUTOSCRAPER, combined with the best current LLMs, already achieves superior extraction performance, and the framework is expected to deliver even better and more stable performance as LLMs continue to improve.

<mark style="background-color: #2ea8e5">Section</mark>
> Error Analysis

<mark style="background-color: #f19837">Challange</mark>
> Non-generalizability of webpages

<mark style="background-color: #f19837">Challange</mark>
> Miss in multi-valued

<mark style="background-color: #ff6666">Conclusion</mark>
> In this paper, we introduce the scraper generation task and the paradigm that combines LLMs and scrapers to improve the reusability of the current language-agent-based framework. We then propose AUTOSCRAPER , a two-phase framework including progressive generation and synthesis module to generate a more stable and executable action sequence. Our comprehensive experiments demonstrate that AUTOSCRAPER can outperform the state-of-the-art baseline in the scraper generation task.


%% end annotations %%

%% Import Date: 2025-01-20T11:42:38.295+01:00 %%
