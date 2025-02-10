With the manually labeled data we try to predict brick code based off all possible candidates within the gpc class. We hope that this approach can leverage the LLM's ability to comprehend the extensive natural language descriptions (such as explicit include and exclude relations) provided by gs1. We assume that we can train a smaller model which can accurately classify up to the gpc class level. 

| Model   | Language | URL | Name | Name + Description |
| ------- | -------- | --- | ---- | ------------------ |
| 4o Mini | English  |     |      |                    |
| 4o      | English  |     |      |                    |
| 4o Mini | German   |     |      |                    |
| 4o      | German   |     |      |                    |

### 4o Mini  and 4o with URL
With only the url (e.g. https://www.edeka24.de/Lebensmittel/Kaffee-Tee/Milch-Sahne-Alternativen/Alnatura-Bio-Kaffeesahne-10-Fett-165G.html) the model might overvalue the provided taxonomy. In this case, gpt assumes this product to be an alternative (plant-based) product. Most likely based off the provided classification ***Milch-Sahne-Alternativen***. This is wrong.
### 4o Mini and 4o with URL + Name (German)

Is wrongly classified as ***Milch (leicht verderblich)*** even though it is shelf stable milk as mentioned in the product description: 

>H-Trinkmilch angereichert mit Milchweiweiß, 3,0% Fett, ultrahocherhitzt, homogenisiert

>UHT drinking milk enriched with milk protein, 3.0% fat, ultra-high temperature, homogenised  (translated with deepl)

![[Pasted image 20250203130255.png]]

### 4o Name + Description

Claims this to be ***Schokolade und Mischungen aus Schokolade und Zuckerwaren - Süßwaren***. Probably because ***Kakao*** is mentioned in the description. Correct: ***Bonbons / Zuckerwaren auf Basis Zuckerersatz***.
![[Pasted image 20250203133044.png]]