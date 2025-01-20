---
category: literaturenote
tags: Computer Science - Computation and Language
citekey: brinkmannUsingLLMsExtraction2024
status: unread
dateread:
---

> [!Cite]
> Brinkmann, A., Baumann, N., & Bizer, C. (2024). _Using LLMs for the Extraction and Normalization of Product Attribute Values_ (Vol. 14918, pp. 217–230). [https://doi.org/10.1007/978-3-031-70626-4_15](https://doi.org/10.1007/978-3-031-70626-4_15)

>[!Synth]
>**Contribution**:: 
>
>**Related**:: 
>

>[!metadata]
> **FirstAuthor**:: Brinkmann, Alexander  
> **Author**:: Baumann, Nick  
> **Author**:: Bizer, Christian  
~    
> **Title**:: Using LLMs for the Extraction and Normalization of Product Attribute Values  
> **Year**:: 2024   
> **Citekey**:: brinkmannUsingLLMsExtraction2024  
> **itemType**:: bookSection  
> **Volume**:: 14918  
> **Book**::    
> **Pages**:: 217-230    

> [!LINK] 
>
>  [PDF](file:///home/cbrosch/Zotero/storage/MCVH6DHA/Brinkmann%20et%20al.%20-%202024%20-%20Using%20LLMs%20for%20the%20Extraction%20and%20Normalization%20of%20Product%20Attribute%20Values.pdf).

> [!Abstract]
>
> Product offers on e-commerce websites often consist of a product title and a textual product description. In order to enable features such as faceted product search or to generate product comparison tables, it is necessary to extract structured attribute-value pairs from the unstructured product titles and descriptions and to normalize the extracted values to a single, unified scale for each attribute. This paper explores the potential of using large language models (LLMs), such as GPT-3.5 and GPT-4, to extract and normalize attribute values from product titles and descriptions. We experiment with different zero-shot and few-shot prompt templates for instructing LLMs to extract and normalize attribute-value pairs. We introduce the Web Data Commons - Product Attribute Value Extraction (WDC-PAVE) benchmark dataset for our experiments. WDC-PAVE consists of product offers from 59 different websites which provide schema.org annotations. The offers belong to five different product categories, each with a specific set of attributes. The dataset provides manually verified attribute-value pairs in two forms: (i) directly extracted values and (ii) normalized attribute values. The normalization of the attribute values requires systems to perform the following types of operations: name expansion, generalization, unit of measurement conversion, and string wrangling. Our experiments demonstrate that GPT-4 outperforms the PLM-based extraction methods SU-OpenTag, AVEQA, and MAVEQA by 10%, achieving an F1-score of 91%. For the extraction and normalization of product attribute values, GPT-4 achieves a similar performance to the extraction scenario, while being particularly strong at string wrangling and name expansion.
>> 
# Notes
>
>Comment: The paper has been accepted at ADBIS2024.


# Annotations%% begin annotations %%



### Imported: 2025-01-20 2:16 pm



<mark style="background-color: #ffd400">Quote</mark>
> Product attribute value extraction (PAVE) identifies attribute values in product titles and descriptions. After normalizing the extracted attribute values to attribute-specific scales, they are used for tasks such as faceted product search or product comparison.

<mark style="background-color: #ffd400">Quote</mark>
> this paper explores the potential of LLMs for the following PAVE tasks: (i) direct extraction, (ii) extraction with normalization, and (iii) normalization.

<mark style="background-color: #ff6666">Conclusion</mark>
> This paper investigated the ability of GPT-3.5 and GPT-4 to extract and normalize product attribute values from product offers. We experimented with different prompt templates that use example values and demonstrations for in-context learning. We introduced the WDC-PAVE benchmark, which features manually verified ground truth values for attribute value extraction as well as value normalization. GPT-4 achieves the best F1-score of 91% in the extraction task, surpassing the best PLM baseline by 10%, and shows similar performance for the extraction with normalization task. A compelling avenue for future research is to give LLMs access to scale-specific functions that the model can decide to invoke for normalizing values.


%% end annotations %%

%% Import Date: 2025-01-20T14:16:30.831+01:00 %%
