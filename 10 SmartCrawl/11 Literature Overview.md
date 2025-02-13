### Transforming HTML

[@wang_2022][@] [@zhouSimplifiedDOMTrees2021] look at ways to Transform the HTML source code to improve information extraction. Not necessarily related to LLM-based extraction but maybe worth looking into for deeper understanding of related work. Authored by researchers associated with @google and @meta.
### Code Generation for Universal Information Extraction

[@li_2024] present a framework for extracting Entities, Relations and Events from natural language. For extraction, they require a user defined schema. This schema consists of a set of python classes which inherit from the base classes Entity, Relation and Event. They then task the LLM to generate code, in which instances are instantiated based off the provided schema given the input text. This approach has since been somewhat integrated into the default OpenAI API via the structured output methodology. Which requires a schema defined using pydantic v2 (classes) and returns instances of these classes with built-in validation and re prompting.

>![[image-4-x63-y576.png]]

The authors then went ahead, contributed further by generating a python class based schema from the wikidata rdfs schema.

<mark style="background-color: #e56eee">Contribution</mark>
> To solve these restrictions, in this paper, we propose a kind of code-style schema representation method, with which various types of knowledge are generally defined as Python classes.

After which they train their KnowCoder for its different phases.

<mark style="background-color: #ffd400">Quote</mark>
> Thus, as shown in Figure 2, the proposed learning framework contains two phases, i.e., the schema understanding phase and the schema following phase. In the schema understanding phase, KnowCoder undergoes code pretraining to understand each concept in two manners: 1) Go through the class definition code of each concept. 2) Go through the instance codes of each concept. In the schema following phase, KnowCoder is finetuned using instruction tuning code, where multiple task-demanded concepts are given in the schemas, enhancing KnowCoder’s ability to follow schemas and generate instantiating code accordingly.

<mark style="background-color: #ff6666">Conclusion</mark>
> In this paper, we introduced KnowCoder for UIE leveraging Large Language Models. KnowCoder is based on a code-style schema representation method and an effective two-phase learning framework. The code-style schema representation method uniformly transforms different schemas into Python classes, with which the UIE task can be converted to a code generation process. Based on the schema representation method, we constructed a comprehensive code-style schema library covering over 30, 000 types of knowledge. To let LLMs understand and follow these schemas, we further proposed a two-phase learning framework that first enhances the schema comprehension ability and then boosts its schema following ability. After training on billions of automatically annotated data and refining with human-annotated IE datasets, KnowCoder demonstrates remarkable performance improvements on different IE tasks under the various evalution settings.

Very interesting contribution as it somewhat represents what our vision of smartcrawling would be for natural language. We might assume that the Schema is based off gs1 web voc instead of wikidata, but in general they have very similar input - output assumptions. Text + Schema -> Instances of Schema based off Text. We might have HTML + Schema / Attributes -> Instances of GS1 Web Voc which can be translated to JSON-LD for knowledge graph construction. Their approach for Fine-Tuning could be looked at in more detail.

[[@guo_2025]] in a later publication the (probably) same work group evaluated retrieval-augmented code generation.  They embedded examples consisting of schema + text + instantiation code and, during runtime, retrieve the n closest text examples to be handed over to the LLM for code generation.    

>![[image-4-x63-y572.png]]
### LLMs for Information Extraction from HTML Pages
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

The authors compare their results with supervised learning baselines and come to the conclusion that their zero-shot learning approach leveraging LLMs can surpass them.


## LLM4Schema

[@dang_2024] published work regarding the automated extraction of schema.org objects from webpages. They used GPT-3.5 and GPT-4 for their tests. To evaluated their findings, they checked the extracted values for validity, factuality and compliance. Comparing the results with manually extracted objects. These objects are extracted from webpages curated from CommonCrawl by [@brinkmann_2023a]. 

![[image-5-x58-y281.png]]

<mark style="background-color: #ff6666">Conclusion</mark>
> Thanks to LLM4Schema.org, we can sample web pages from the CommonCrawl and evaluate whether LLMs produce better Schema.org markup than humans. Our findings indicate that LLMs should not be used out-of-thebox for generating Schema.org markups, as they often produce invalid, unfactual, or non-compliant markups. For instance, with our best-performing LLM, GPT-4, over 40% of the generated markup is incorrect. However, after filtering the incorrect markup by LLM4Schema.org agents, filtered markup generated with GPT-4 can surpass human performance, achieving a MeMR score of 0.70 compared to 0.568 for humans. In contrast, GPT-3.5 does not outperform humans even after filtering with a MeMR score of 0.585 compared to 0.687 for humans. Additionally, we observed that GPT-3.5 and GPT-4 can enhance web pages by improving poorly filled types or utilizing less popular types, providing added value in specific contexts