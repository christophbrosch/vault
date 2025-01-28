
![[SmartCrawl - Overview.jpg]]
## Was versuchst du zu tun?   

Einen generischen Wissensgraphen (Produktgraphen) mithilfe von Informationen aus Produktseiten unterschiedlicher Warenbereiche aufzubauen. Das Ganze auf Grundlage von Produkttyp-spezifischen Attributen. Die Daten sollen dabei mithilfe eines generischen Webcrawlers erhoben werden, welcher sich durch die Verwendung generativer KI an das Webseiten-Layout anpasst. Der Wissensgraph wird basierend auf dem RDF-Datenmodell aufgebaut. Dieser stellt anschlieszend eine Plattform fuer weitere Forschungsarbeiten dar und demokratisiert vorhandenes Produktwissen in einer strukturierten und semantischen Form. 

## Formulieren Sie Ihre Ziele ganz ohne Fachjargon.  
    

Das Ziel ist es einen generischen Webcrawler zu entwickeln, welcher mithilfe von generativer KI (ChatGPT) Inhalte aus Webseiten extrahiert. Die zu extrahierende Attribute sind dabei abhängig von dem auf der Produktseite gezeigten Produkt und werden dem GPC-Klassifikation-System entnommen. Generische Attribute wie Preis, Name, Marke, Verfügbarkeit oder Bewertungen sollen dabei immer berücksichtigt werden. Produktseiten müssen erfolgreich einem GPC-Brick zugeordnet werden, um von den Attributen und Werten auf Brick-Ebene Gebrauch machen zu können. Mithilfe der gewonnenen Daten soll ein Wissensgraph gefüllt mit Produktinformationen aus unterschiedlichsten Warensortimenten entstehen. Dieser hat durch die Verwendung manuell angelegter, ergänzender Ontologien (z. B. extrahiert aus dem GS1 Global Product Classification-System) eine klare Semantik. Die Daten innerhalb des Wissensgraphen können dann der Allgemeinheit bereitgestellt werden und ermöglichen die Umsetzung vieler neuer Forschungsarbeiten durch die breitere Forschungsgemeinschaft. 

## Wie wird es heute gemacht und wo liegen die Grenzen der aktuellen Praxis?   
    

Webcrawler und Wissensgraphen werden heutzutage bereits eingesetzt. Dabei werden in aktuellen Crawl-prozessen i. d. R. die zu extrahierende Attribute hartkodiert. Die Crawler sind dadurch an eine, oder vielleicht eine Handvoll Seiten anwendbar. Für das Verarbeiten von Produktseiten müssen für jede Produktkategorie eigene Verfahren manuell erarbeitet werden. Eine Produktkategorie kann dabei z. B. eine GPC-Klasse (n: ~133 (nur Lebensmittel)) sein oder sogar ein GPC-Brick (n: >3,700) sein, da im Klassifikation System jedem Brick (n: >3,700) eigenständige Wertkombinationen (GPC-Attributes) zugeordnet sind.  Um alle Wertkombinationen für die Produkte abhängig ihrer GPC-Brick Klassifikation zu extrahieren könnten potenziell >3,700 -Crawler notwendig sein. 

## Was ist neu an Ihrem Ansatz und warum glauben Sie, dass er erfolgreich sein wird? 
    

Das neue an dem Ansatz: A) Die Klassifikation von Produktseiten auf GPC-Brick-Ebene. B) der generische Ansatz für das Webcrawling der auf generativer KI basiert in Kombination mit der Bestimmung der zu extrahierende Attribute basierend auf GPC (oder ähnlichen CPV (Category – Property – Value)) und C) der entstehende Produktgraph, welcher Wissen aus unterschiedlichen Produktbereichen (Lebensmittel, Elektronik, Möbel etc.) zusammenführet. 

## Wen interessiert das? Welchen Unterschied wird es machen, wenn Sie erfolgreich sind? 
    

Für Interesse sind die Ergebnisse vorrangig für eine Vielzahl von Handelsunternehmen. Der Produktgraph enthält Informationen die z. B. für eine ausgiebige Konkurrenzpreisanalyse genutzt werden kann oder für die das Stammdatenmanagement als Ausgangspunkt für die Produktinformationen genutzt werden können. GS1 arbeitet an einem Global Data Model, welches in Zukunft potenziell von immer mehr Handelsunternehmen eingesetzt wird, um die eigenen Handelsdaten zum Strukturieren. In diesem Fall ist eine enge Bindung an das Klassifikationssystem von GS1 von Vorteil. Des weiteren profitiert auch die Forschungsgemeinschaft daran, dass sie auf einen Produktgraphen zugreifen kann, um weitere Fragestellungen zu erforschen. Dies ist derzeit noch nicht der Fall, nur Unternehmensinterne-Teams von bspw. Amazon, Ebay oder Alibaba haben Zugriff auf genug Daten, um aktiv an dem Themengebiet zu forschen. 

## Was sind die Risiken?   
    

Durch die Abhängigkeiten der Teilschritte B) und C) sind Risiken unter anderem der Misserfolg der vorherigen Teilschritte. Scheitert die Klassifikation der Produktseiten, oder gelingt nur zu einem zu kleinen Präzisionswert (<.95) können durch den  Webcrawler nicht die benötigten Informationen aus der Webseite extrahiert werden. Im besten Fall kann dies automatisiert im Crawl-Prozess erkannt werden, wodurch die Produktseite verworfen wird. Im worst case werden falsche Produktattribute aus der Produktseite entnommen und in den Produktgraphen eingepflegt. Dies bedeutet, dass Fehler aus vorherigen Prozessschritten durchgereicht werden. 

Ein weiteres Risiko ist das fehlende Interesse an der Technologie im deutschsprachigen Raum. Produktgraphen finden vermehrt im eCommerce Einsatz und werden auch von unternehmensinternen Forschungsteam untersucht. Dies Publikationen stammen entsprechend vermehrt von Unternehmen wie Amazon, Alibaba oder Walmart. Nach dem aktuellen Erkenntnisstand sind Produktgraphen im deutschsprachigen Raum noch kein Thema, vermutlich, da die Use-Cases für PGs derzeit keine hohe Relevanz haben. 

## Wie viel wird es kosten?
## Wie lange wird es dauern?
## Was sind die Zwischen- und Abschlussprüfungen, um den Erfolg zu überprüfen?