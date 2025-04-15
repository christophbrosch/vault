# Information Needs Analysis

## Objective

The aim of the project, to be conducted in the summer semester of 2025 alongside Robin Werth and Raffael Schäfer, is to develop a web interface that allows products to be classified at the Brick Level. These products will be represented with various attributes such as product name, image, description, and URL. The students' task will focus on developing the user interface using React and NextJS.

## Input

Consideration should be given to input fields such as product name, product description, and product image. The students suggested multiple different solutions, such as a "data bubble" where the user can insert as little or as much data as they want.

Product data exists in various configurations for retail companies. The most logical distinction is likely at the data source level:

**Product Information Management System (PIM System)**
- Contains descriptive attributes of a product, including product name, description, categories, images, etc. Retail companies usually define their own data models. An employee from such a company would likely send elements of a product feed (e.g., as an XML file) for classification. This aligns with data delivery from companies like Globus. More information: [Product Feed](https://de.wikipedia.org/wiki/Produktfeed).

**Webshop**
- To test the system, a user might want to classify a product page. It’s important to differentiate whether the user extracts the information manually from the web interface and inputs it into fields, or if the product page is "parsed" by us and input fields are pre-filled accordingly. The standardized JSON-LD element, commonly found on product pages, can be used here. Below is an example of such JSON-LD product data (well-maintained by the webshop Mytime.de), using the Schema.org vocabulary.

```json
{
   "@context":"https://schema.org",
   "@type":"Product",
   "name":"Ferrero Milch-Schnitte",
   "description":"<p>For a small break during the day. To get through the day well, you should occasionally take a small break. With the family pack, you always have a fresh snack in the fridge.</p>\n<p>No artificial colors, no added alcohol or preservatives.</p>",
   "sku":"4503060121",
   "gtin":"4008400192024",
   "manufacturer":{
      "@type":"Organization",
      "name":"Ferrero"
   },
   "brand":{
      "@type":"Brand",
      "name":"Ferrero"
   },
   "image":"https://d2jdyzt6tc17s.cloudfront.net/products/images/4503060121_4008400191423_01.jpg.jpg",
   "offers":{
      "@type":"Offer",
      "availability":"https://schema.org/InStock",
      "itemCondition":"https://schema.org/NewCondition",
      "priceSpecification":{
         "@type":"UnitPriceSpecification",
         "priceType":"https://schema.org/ListPrice",
         "price":"2.99",
         "priceCurrency":"EUR",
         "valueAddedTaxIncluded":true
      }
   },
   "hasMerchantReturnPolicy":{
      "@type":"MerchantReturnPolicy",
      "applicableCountry":"DE",
      "returnPolicyCategory":"https://schema.org/MerchantReturnFiniteReturnWindow",
      "merchantReturnDays":14
   }
}
```

## Output

- Brick Classification (Top 1, Top 3)

- Similar products in the product graph

## Questions (Christoph)
![[Zeichnung 1(6).png]]
- The application should be implemented in NextJS and access various backend ML functionalities, ideally with simplicity.

- NextJS offers an extensive ecosystem, which is particularly interesting in terms of authentication (e.g., easy implementation with OAuth services). Can we integrate authentication with Python endpoints (e.g., implemented with Flask)? Suggested approach: [Next.js Flask Starter](https://vercel.com/templates/next.js/nextjs-flask-starter). Raffi suggested JWTs.

- Everything should be organized in one repository. Because bullet point below.

- Aim for KISS (Keep It Simple, Stupid).

- Is the illustrated architecture achievable and sensible?

## Graphic (Krieger)
![[image001.png]]
## Visualization

The hierarchy could potentially be displayed as a dendrogram:
https://d3-graph-gallery.com/graph/dendrogram_basic.html