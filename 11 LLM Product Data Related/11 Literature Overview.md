### [[@brinkmannUsingLLMsExtraction2024]]

The authors use OpenAI's GPT-3.5 and GPT-4 to evaluate the extraction and normalization of Product Attribute Values. Motivated by the use of for product search and comparison.

<mark style="background-color: #ffd400">Quote</mark>
> Product attribute value extraction (PAVE) identifies attribute values in product titles and descriptions. After normalizing the extracted attribute values to attribute-specific scales, they are used for tasks such as faceted product search or product comparison.

They conclude that this approach works very well compared to baseline pre-trained language models, presumably BERT-models. This could be evaluated in an effort to improve the results of Flavio Horbach, who used a transformer based model (FLAIR NER?) with moderate success.

<mark style="background-color: #ff6666">Conclusion</mark>
> This paper investigated the ability of GPT-3.5 and GPT-4 to extract and normalize product attribute values from product offers. We experimented with different prompt templates that use example values and demonstrations for in-context learning. We introduced the WDC-PAVE benchmark, which features manually verified ground truth values for attribute value extraction as well as value normalization. GPT-4 achieves the best F1-score of 91% in the extraction task, surpassing the best PLM baseline by 10%, and shows similar performance for the extraction with normalization task. A compelling avenue for future research is to give LLMs access to scale-specific functions that the model can decide to invoke for normalizing values.
