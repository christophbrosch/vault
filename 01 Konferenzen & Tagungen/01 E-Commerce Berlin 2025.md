I visited the yearly scheduled fair regarding innovative e-commerce solutions in February of 2025. The fair took place in Berlin and and aims to connect sellers, market places and solution providers. My personal goal was to get a broad overview of what current topics are in e-commerce and ask around if knowledge graphs is a technology which is known, and if so, is of current interest. 

Long story short, from my conversations with various company representatives, only a few knew what a knowledge graph is. Only company is actively using a knowledge graph as an integral part of their tech stack. Most companies only had non-technical staff present (marketing), who might not be aware of their own tech stack, therefore this is not definitive. The company that does use a knowledge with their own ontology is https://zoovu.com/de.

>Mithilfe der KI-Discovery-Plattform von Zoovu wandelt Microsoft technische Spezifikationen in bedarfsorientierte Sprache um, um damit kundenzentrierte digitale Einkaufserlebnisse in der Form digitaler Kaufberater und visuellen Konfiguratoren umzusetzen. Diese informieren, beraten und ermöglichen Kunden die einfache Anpassung und Bündelung von Produkten.
>Source: https://zoovu.com/de/customers/microsoft

Zoovu is a startup which follows a current trend in e-commerce: using generative AI agents for product discovery. In their showcase, the representatives showed me how their tool can be used to make the selection for the right laptop easier (or bikes as shown below).

![[Screencast+from+2025-03-03+10-44-09.webm]]

### Memorable companies I talked to:
- Base.com
	- Provides a SAAS Product to manage your products in different marketplaces / webshops in one user interface. The representative told me that in his opinion descriptive product information is becoming more important in general.
- Luigi's Box
	- Provides a SAAS Product for product search and recommendation for your webshop. I've talked with Michal Barla a Co-Founder about the future of generative AI for product search. He was a very technical person aware of the technologies we use and shared an interesting opinion in which the biggest benefit of schema.org is the unified description of product data on the web which is being somewhat enforced upon sellers by google and similar search engines as implementing the json-ld data into your website directly improves SEO. In the future Michal predicts that more and more customers will be lead to products by chat agents such as ChatGPT (we called this shopping experience "headless shopping", a reference to "headless cms" where the frontend is completly seperate from the backend). In this future, a new Ontology might be required for chat agents to comprehend provided product data in the best possible way. For this, one of the big players, e.g. OpenAI has to provide an uniform ontology. The conversation was overall very insightful.
- GS1 
	- I had the pleasure to talk to Thorsten Dietrich from GS1 Germany. We discussed GPC and other standards which are being used by us. He told me that feedback from users is always appreciated. I told him about knowledge graphs, of which their usage inside GS1, he is not aware of, but he told me that they are open to cooperate in the future. We concluded our conversation with the desire to setup an initial online meeting to showcase our work and discuss if we could cooperate in the future. I also asked if we could potentially visit them in Cologne. To which he was open.
- Shopware
	- I asked their co-CEO Sebastian Harmann if he is aware of knowledge graphs / and their usage inside his company. He told me to ask him again on LinkedIn so he can ask his technical employees. As of writing i have not received a response on LinkedIn.

### Current trends:
 - SAAS solutions which base their product on a product feed. Usually provided as an XML file by the retailer. Similar to what Globus gave to us. https://de.wikipedia.org/wiki/Produktfeed , https://support.google.com/merchants/answer/12631822?hl=en
- Guided E-Commerce Solutions provided by companies such as ZOOVU and Neocom. Later told me that in the case of Miele 7% of all customers use their guided track and that there's an >50% higher conversion rate from those customers. [Example Customer Journey from Neocom (Miele)](https://production.neocomapp.com/?wizard&clientOrigin=https%3A%2F%2Fwww.miele.de&clientUrl=https%3A%2F%2Fwww.miele.de%2Fc%2Fstaubsaugen-54.htm&referrer=https%3A%2F%2Fwww.miele.de%2Fc%2Fmiele-experience-center-in-deutschland-699.htm&id=7483ca74-0de8-4703-948d-0e1a24daf27e&autoStart=true&isDraft=false&integrationType=INLINE#s:2e1435e4-2ab7-4551-96a7-96af156973b0,conversationId:d1e137ec-0098-4e31-821e-5eb89f93fdb6,cookieConsent:UNKNOWN)
- Multiple companies provide product recommendations / search based off the product feed. SAAS companies typically keep a "clone" of the data on their own servers and customers can then call an API to receive the most relevant products. ( e.g. FactFinder, NetCore UNXD)
- It appears more European market places (similar to amazon) are being promoted. E.g. Kaufland Market Place.

Overall the fair was very insightful and worthwhile. I would not visit for two days again. All relevant booths could be visited in one day.