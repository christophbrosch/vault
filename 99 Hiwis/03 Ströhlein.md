## Februar 17

- Logs in eine extra Collection mit Pointer
- nohup solara run --port 7474 --host 0.0.0.0 frontend pages &
- host anpassen auf 0.0.0.0 in der API.py 
- Mehr Except Blöcke?  Flask in Debug Mode?

## März 05

Plots sollten auch alleinstehend sinn machen (X-Achse besser beschriften), vielleicht auch Titel. In den Titel auch das N = Anzahl der Produkte erkennen.

Boxplots die Beschriftung in die x-Achse (Rechte Kante das aktuelle Datum)

Plots anklickbar machen

Run Details Page fehlen noch Einträge, bzw scheint etwas überschrieben zu sein.

![[Pasted image 20250305101555.png]]

Wie bestimmen wir aktuell ob ein Produkt entfernt wurde?

Boxplot über das durchscnittliche Alter (Alter eines Produkts = Datum - Last Visited)
Auch durchschnittliches Alter als Wert

Plots zur Completeness

Häufigkeit der Produktattribute als Tabelle darstellen

## März 12

In Plots deleted nicht beachten  
  
Beide Boxplots trennen mit Multiselect  
  
Tausend Trennzeichen für Graph N  
  
Urls/Logs als eigene Documents?  
  
Beim Run Start urls mit Produkturls vergleichen (welche deleted?)  
Wenn url nicht erreichbar -> deleted  
Ggf. deleted flag wieder entfernen  
  
Completeness Hist in % und zusätzlich Boxplot für Completeness durch Multiselect  
  
Eigene Seite ("Data Quality") mit Attributtabelle mit allen Attributen (dynamisch Attribute holen) (keine Seitenränder)