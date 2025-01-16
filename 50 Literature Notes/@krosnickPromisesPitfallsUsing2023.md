---
category: literaturenote
tags: 
citekey: krosnickPromisesPitfallsUsing2023
status: unread
dateread:
---

> [!Cite]
> Krosnick, R., & Oney, S. (2023). _Promises and Pitfalls of Using LLMs for Scraping Web UIs_.

>[!Synth]
>**Contribution**:: 
>
>**Related**:: 
>

>[!metadata]
> **FirstAuthor**:: Krosnick, Rebecca  
> **Author**:: Oney, Steve  
~    
> **Title**:: Promises and Pitfalls of Using LLMs for Scraping Web UIs  
> **Year**:: 2023   
> **Citekey**:: krosnickPromisesPitfallsUsing2023  
> **itemType**:: journalArticle  
> **Journal**:: **    

> [!LINK] 
>
>  [Krosnick and Oney - 2023 - Promises and Pitfalls of Using LLMs for Scraping W.pdf](file:///home/cbrosch/Zotero/storage/VA2NZXVA/Krosnick%20and%20Oney%20-%202023%20-%20Promises%20and%20Pitfalls%20of%20Using%20LLMs%20for%20Scraping%20W.pdf).

> [!Abstract]
>
> ChatGPT and other publicly available large language models (LLMs) put AI into the hands of everyday computer users, offering the possibility of automating computer tasks. One candidate task is web scraping. We informally experimented with ChatGPT to explore the potential promises and pitfalls of using it for scraping data from web user interfaces. We share our observations and considerations for future human-LLM web scraping systems.
>.
> 
# Notes
>.


# Annotations%% begin annotations %%



### Imported: 2025-01-16 11:42 am



<mark style="background-color: #ffd400">Thesis</mark>
> Web scraping may be a good candidate task for LLMs, since one way of looking at web scraping is as a text extraction task, and LLMs are good at generating text. LLMs such as ChatGPT have the potential to address the above two challenges with web scraping specific tools: 1) ChatGPT is currently (at the time of this writing) readily available to the public and widely known, and 2) given their generative nature may be able to produce a web scraping answer for a broader set of scenarios, albeit possibly at a lower quality than their domain-specific counterparts.

<mark style="background-color: #ffd400">Quote</mark>
> For many pages, ChatGPT often scraped the exact right data, especially when given the website’s text rather than HTML.

<mark style="background-color: #ffd400">Quote</mark>
> When given the website’s HTML and asked to write code for scraping, ChatGPT seemed to mostly generate correct code logic and CSS selectors [2] if the elements to be scraped have salient selectors


<mark style="background-color: #2ea8e5">Section</mark>
> Asking ChatGPT to scrape and return an answer

<mark style="background-color: #ffd400">Quote</mark>
> There were a few kinds of mistakes we saw ChatGPT make. Sometimes it produced nearly the correct output data except it would be missing a small number of entries.

<mark style="background-color: #ffd400">Quote</mark>
> ChatGPT seemed to make more mistakes when we gave it the page’s HTML rather than text. ChatGPT would frequently prematurely end its scraping.

<mark style="background-color: #ffd400">Quote</mark>
> In one especially interesting case where we gave ChatGPT the HTML for the CODA movie page, it returned 11 actor and character pairs, only 3 of which were correct. ChatGPT hallucinated some character names, some of which matched patterns in real character names (e.g., “Gina” Rossi –> not a real character, but other characters in the movie have the same last name “Rossi”; Ms. “Han” –> not a real character, but another character in the movie has the same title,“Ms.” Simon).

<mark style="background-color: #2ea8e5">Section</mark>
> Asking ChatGPT to write code for scraping

<mark style="background-color: #ffd400">Quote</mark>
> This needs to be explored further, but we observed ChatGPT make mistakes in the code it generated when the items to be scraped did not have salient CSS classes or attributes. For example, the Citi Open tennis tournament (Table 1, website #4) website has minimal styling, so ChatGPT did not have meaningful CSS classes to latch on to.

<mark style="background-color: #ffd400">Quote</mark>
> It should also be further explored how accurate and robust CSS selectors and element selection logic LLMs can generate.

<mark style="background-color: #ff6666">Conclusion</mark>
> ChatGPT has some promise right out of the box for web scraping, but it has many dangers as well. Given how often ChatGPT can be right or close to right for web scraping, people may not check its results closely and instead just trust it. Any future LLM-powered web scraping tool needs to provide users tools to check its work, e.g.,  by contextualizing results visually with the web page, by providing links to sources. Future work may also explore ways to leverage LLMs more effectively for web scraping, perhaps by combining demonstration, web UI specific models, and LLM-based approaches.


%% end annotations %%

%% Import Date: 2025-01-16T11:56:28.033+01:00 %%
