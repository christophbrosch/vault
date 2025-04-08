# Informationsbedarfanalyse

## Ziel

In dem Fachprojekt welches im Sommersemester 2025 zusammen mit Robin Wert und Raffael Schäfer durchgeführt wird soll eine Weboberfläche entwickelt werden, welche es ermöglicht Produkte, dargestellt mit unterschiedlichen Attributen (Produtname, Bild, Beschreibung, URL), auf Brick Level zu klassifizieren. Die Aufgabe der beiden Studenten beschränkt sich hierbei auf die Ausarbeitung der Nutzeroberfläche, aufbauend auf den Technologien React und NextJS.

## Eingabe

Anzudenken sind Eingabefelder wie z. B. Produktname, Produktbeschreibung und Produktbild.

Produktdaten liegen für Handelsunternehmen in unterschiedlichen Konstellationen vor. Die sinnigste Unterscheidung ist hier vermutlich auf Datenquelleebene zu treffen.

- Product Information Management System (PIM-System)
	- Beinhaltet die beschreibenden Attribute eines Produkts, darunter Produktname, Beschreibung, Kategorien, Bilder etc. Einzelhandelsunternehmen definieren ihr Datenmodell i. d. R. selbst. Ein Mitarbeiter eines solchen Unternehmens würde vermutlich Elemente eines Produktfeeds (z. B. als XML-Datei) zur Klassifikation schicken. Entspricht in etwa der Datenlieferung von Globus. Mehr Informationen: https://de.wikipedia.org/wiki/Produktfeed. 
- Webshop
	- Zum testen des Systems möchte eine Nutzer:in vielleicht eine Produktseite klassifizieren. Hierbei ist zu unterscheiden ob die Nutzer:in die Informationen selbst aus der Weboberfläche extrahieren und in entsprechende Eingabefelder überführt, oder ob die Produktseite von uns "geparsed" und Eingabefelder entsprechend vorausgefüllt werden. Hierbei kann das einheitliche JSON-LD Elemente, welches auf den meisten Produktseiten zu finden ist, verwendet werden. Nachfolgend ein Beispiel eines solchen JSON-LD Produkts (sehr gut gepflegt vom Webshop Mytime.de), abgebildet mit dem Schema.org Vokabular.

```json
{
    "@context": "https:\/\/schema.org",
    "@type": "Product",
    "name": "Ferrero Milch-Schnitte",
    "description": "<p>F&uuml;r die kleine Pause im Alltag. Um gut durch den Tag zu kommen, sollte man sich ab und zu eine kleine Pause g&ouml;nnen. Mit der Familienpackung haben Sie immer einen frischen Snack im K&uuml;hlschrank.<\/p>\n<p>Ohne k&uuml;nstliche Farbstoffe, ohne Zusatz von Alkohol und Konservierungsstoffen.<\/p>",
    "sku": "4503060121",
    "gtin": "4008400192024",
    "manufacturer": {
        "@type": "Organization",
        "name": "Ferrero"
    },
    "brand": {
        "@type": "Brand",
        "name": "Ferrero"
    },
    "image": "https:\/\/d2jdyzt6tc17s.cloudfront.net\/products\/images\/4503060121_4008400191423_01.jpg.jpg",
    "offers": {
        "@type": "Offer",
        "availability": "https:\/\/schema.org\/InStock",
        "itemCondition": "https:\/\/schema.org\/NewCondition",
        "priceSpecification": {
            "@type": "UnitPriceSpecification",
            "priceType": "https:\/\/schema.org\/ListPrice",
            "price": "2.99",
            "priceCurrency": "EUR",
            "valueAddedTaxIncluded": true
        }
    },
    "hasMerchantReturnPolicy": {
        "@type": "MerchantReturnPolicy",
        "applicableCountry": "DE",
        "returnPolicyCategory": "https:\/\/schema.org\/MerchantReturnFiniteReturnWindow",
        "merchantReturnDays": 14
    }
}
```

## Ausgabe

- Brick Klassifikation (Top 1, Top 3)
- Ähnliche Produkte im Produktgraphen

## Fragestellungen (Christoph)

- Die Anwendung soll in NextJS implementiert werden und auf unterschiedliche Backend ML Funktionalitäten zugreifen. Diese sind im besten Fall nicht besonders kompliziert in der Ausführung. 
- NextJS verfügt über ein sehr weitreichendes Öko-System, interessant vorallem in Hinblick auf das Thema Authentifizierung (vgl. einfach umzusetzen mit OAuth-Services). Können wir die Authentifizierung in einklang mit einigen Python-Endpunkten (z. B. implementiert mit Flask) bringen? Lösung angelehnt an: https://vercel.com/templates/next.js/nextjs-flask-starter.
- Alles sollte in ein Repository 
- Möglichst KISS
![[Zeichnung 1(6).png]]
- Kann eine Architektur wie die abgebildet erreicht werden, ist diese überhaupt sinnvoll?

## Grafik (Krieger)
![[image001.png]]