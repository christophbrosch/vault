[@wang_2022][@] [@zhouSimplifiedDOMTrees2021] look at ways to Transform the HTML source code to improve information extraction. Not necessarily related to LLM-based extraction but maybe worth looking into for deeper understanding of related work. Authored by researchers associated with @google and @meta.

### [[@gurUnderstandingHTMLLarge2023]]

The authors give a broad overview over the topic and evaluate fine-tuning pre-trained LLMs on HTML data. 

<mark style="background-color: #ffd400">Quote</mark>
> Our results show that LLMs demonstrate a remarkable level of HTML understanding across all tasks, with up to 192× more sample-efficiency than models trained from scratch, and achieving a new SoTA for supervised learning on the MiniWoB benchmark suite (Shi et al., 2017). The encoder-decoder architectures with bi-directional attention show the best performance across the board even when their pretraining does not include HTML. In addition, we show that the performance scales sub-linearly with the model size.

Their work goes into more technical depth than for our use-case currently necessary regarding the architecture and model size. One interesting idea from their work is the concept of semantic classification with LLMs:

<mark style="background-color: #ffd400">Quote</mark>
> First, we devise Semantic Classification as a task that requires a model to classify a given HTML element into one of a set of categories, such as address, email, password etc., with application to automated form-filling.

We could maybe apply an similar approach to classifying the regions of a product page.  Jonas Scheffler started defining the common areas in a product webpage:

![[Pasted image 20250120132258.png]]
### [[@krosnickPromisesPitfallsUsing2023]]

In their short paper (4 pages), the authors evaluated gpt-3.5 for direct extraction. Indirect extraction using automatically generated was looked at, but not in detail.

<mark style="background-color: #ffd400">Thesis</mark>
> Web scraping may be a good candidate task for LLMs, since one way of looking at web scraping is as a text extraction task, and LLMs are good at generating text. LLMs such as ChatGPT have the potential to address the above two challenges with web scraping specific tools: 1) ChatGPT is currently (at the time of this writing) readily available to the public and widely known, and 2) given their generative nature may be able to produce a web scraping answer for a broader set of scenarios, albeit possibly at a lower quality than their domain-specific counterparts.

<mark style="background-color: #ff6666">Conclusion</mark>
> ChatGPT has some promise right out of the box for web scraping, but it has many dangers as well. Given how often ChatGPT can be right or close to right for web scraping, people may not check its results closely and instead just trust it. Any future LLM-powered web scraping tool needs to provide users tools to check its work, e.g.,  by contextualizing results visually with the web page, by providing links to sources. Future work may also explore ways to leverage LLMs more effectively for web scraping, perhaps by combining demonstration, web UI specific models, and LLM-based approaches.

### [[@huangAutoScraperProgressiveUnderstanding2024]]

[[@huangAutoScraperProgressiveUnderstanding2024]] implemented AutoScraper, a tool which generates XPath-based Action Sequences for extracting information from websites. They first generate different Action Sequences based on seed websites for a given domain (n = 3). After which they run the remaining websites through these generated Action Sequences, always choosing the result from the best performing Action Sequence. They evaluated their methods on three datasets (SWD, SWDE and DS1). As of writing their source code has 445 stars.

![[image-4-x70-y446.png]]

<mark style="background-color: #5fb236">Thesis</mark>
> To address the shortcomings of the aforementioned two paradigms, the paradigm of generating web scrapers with LLMs would be the optimal solution. On one hand, compared to wrapper-based methods, it fully leverages the reasoning and reflection capacities of LLMs, reducing manual design on new tasks and enhancing scalability. On the other hand, compared to language-agent-based methods, it introduces repeatable extraction procedures, reducing the dependency on LLMs when dealing with similar tasks, and thereby improving efficiency when handling a large number of web tasks.

<mark style="background-color: #ff6666">Conclusion</mark>
> In this paper, we introduce the scraper generation task and the paradigm that combines LLMs and scrapers to improve the reusability of the current language-agent-based framework. We then propose AUTOSCRAPER , a two-phase framework including progressive generation and synthesis module to generate a more stable and executable action sequence. Our comprehensive experiments demonstrate that AUTOSCRAPER can outperform the state-of-the-art baseline in the scraper generation task.

The authors compare their results with supervised baselines and come to the conclusion that their zero-shot learning approach leveraging LLMs can surpass these baselines.


