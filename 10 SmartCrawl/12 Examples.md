https://www.fissler.com/de/p/adamant-premium-pfanne-26-cm/



## Bratpfanne | Brick 10002144

>    Ideal für knuspriges Anbraten von Fleisch, Rösten von Gemüse und schonendem Braten von empfindlichen Speisen, die leicht anhaften
	Besonders kratzfeste, wasserbasierte Fissler Adamant®-Beschichtung mit sehr gutem Antihaft-Effekt
	Fissler Premium Pfannenkörper aus robustem Edelstahl 18/10 mit abgerundeter Form und extra breitem Schüttrand für einfaches, präzises und kleckerfreies Aus- und Umgießen von Flüssigkeiten
	Exklusiver, energieeffizienter Fissler Cookstar® Boden für optimale Wärmeverteilung
	Geeignet für alle Herdarten einschließlich Induktion
	Premium Qualität - Made in Germany
	Gewicht	1.420 kg
	Höhe	65 mm
	Produkttyp	Rund
	Kapazität	2.5 l
	Material	Edelstahl 18/10
	Serie	Adamant® Premium
	Bodendurchmesser	20 cm
	Durchmesser oben	26 cm
	Produkttyp	Stielpfanne
	Material des Griffs	Kunststoff
	Oberfläche innen	Antihaftversiegelung (PTFE)
	Oberfläche außen	poliert
	Marke	Fissler
	Garantie	5
	Dimensionen	280 mm 465 mm 105 mm
	

```python

from enum import Enum

from pydantic import BaseModel

  
  

class ArtDerAntihaftbeschichtung(Enum):

"""

Attribute Description if provided:

NICHTIDENTIFIZIERBAR (str): Dieser Begriff wird zur Beschreibung der Produktattribute verwendet, die aufgrund vorhandener oder verfügbarer Produktinformationen nicht identifizierbar sind.

NICHTKLASSIFIZIERT (str): Dieser Begriff wird zur Beschreibung von solchen Attributen verwendet, bei denen es nicht möglich ist, sie innerhalb ihres speziellen Marktes / Wirtschafsraumes zu klassifizieren. Ein Beispiel für solche Produkte ist Ziegenkäse: Ziegenkäse wird oft generisch / der Gattung zugeordnet und kann nicht weiter klassifiziert werden.

"""

  

EMAILLE_GLASUR = "Emaille_Glasur"

KERAMIK = "Keramik"

POLYTETRAFLOURETHYLEN_PTFE = "Polytetraflourethylen_PTFE"

NICHTIDENTIFIZIERBAR = "NichtIdentifizierbar"

NICHTKLASSIFIZIERT = "NichtKlassifiziert"

OHNE = "Ohne"

  
  

class ArtVonBratgeschirr_Pfanne_Woks_Kokotten(Enum):

"""

Attribute Description if provided:

NICHTIDENTIFIZIERBAR (str): Dieser Begriff wird zur Beschreibung der Produktattribute verwendet, die aufgrund vorhandener oder verfügbarer Produktinformationen nicht identifizierbar sind.

NICHTKLASSIFIZIERT (str): Dieser Begriff wird zur Beschreibung von solchen Attributen verwendet, bei denen es nicht möglich ist, sie innerhalb ihres speziellen Marktes / Wirtschafsraumes zu klassifizieren. Ein Beispiel für solche Produkte ist Ziegenkäse: Ziegenkäse wird oft generisch / der Gattung zugeordnet und kann nicht weiter klassifiziert werden.

"""

  

BLINIPFANNE = "Blinipfanne"

BRATPFANNE = "Bratpfanne"

BRATPFANNE_GERADE_UND_KONISCH = "Bratpfanne Gerade und Konisch"

COUSCOUSSIER_DAMPFGARER = "Couscoussier/Dampfgarer"

CREPE_PFANNE = "Crepe-Pfanne"

DAMPFDRUCKTOPF_NICHT_ELEKTRISCH = "Dampfdrucktopf (nicht elektrisch)"

DAMPFGARER = "Dampfgarer"

FISCHKESSEL = "Fischkessel"

FISCHPFANNE = "Fischpfanne"

GUSSEISERNE_BRATPFANNE_ECKIG = "Gusseiserne Bratpfanne (eckig)"

KOCHTOPF_KASSEROLLE = "Kochtopf / Kasserolle"

KORB_FUER_PASTAKOCHER = "Korb für Pastakocher"

NICHT_IDENTIFIZIERBAR = "Nicht identifizierbar"

NICHT_KLASSIFIZIERT = "Nicht klassifiziert"

PAELLAPFANNE = "Paellapfanne"

PASTAKOCHER_SET = "Pastakocher - Set"

PASTATOPF = "Pastatopf"

POCHIERPFANNE_FUER_EIER = "Pochierpfanne (für Eier)"

SAUCIER = "Saucier"

SPARGEL_DAMPFGARER = "Spargel-Dampfgarer"

TIEFER_TOPF = "Tiefer Topf"

WASSERBAD = "Wasserbad"

WOK_NICHT_ELEKTRISCH = "Wok (nicht elektrisch)"

  
  

class FallsMitAbnehmbaremGriff(Enum):

JA = "Ja"

NEIN = "Nein"

NICHT_IDENTIFIZIERBAR = "Nicht identifizierbar"

  
  

class Materialart(Enum):

"""

Zeigt, in Bezug auf das Product Branding, die Kennzeichnung oder die Verpackung, den beschreibenden Begriff, der vom Hersteller des Produktes verwendet wird, um die Art des Materials zu bestimmen, aus dem die Produkte bestehen.

  

Attribute Description if provided:

NICHTIDENTIFIZIERBAR (str): Dieser Begriff wird zur Beschreibung der Produktattribute verwendet, die aufgrund vorhandener oder verfügbarer Produktinformationen nicht identifizierbar sind.

NICHTKLASSIFIZIERT (str): Dieser Begriff wird zur Beschreibung von solchen Attributen verwendet, bei denen es nicht möglich ist, sie innerhalb ihres speziellen Marktes / Wirtschafsraumes zu klassifizieren. Ein Beispiel für solche Produkte ist Ziegenkäse: Ziegenkäse wird oft generisch / der Gattung zugeordnet und kann nicht weiter klassifiziert werden.

"""

  

ALUMIUM = "Aluminium"

ALUMINIUMGUSS = "Aluminiumguss"

EDELSTAHL = "Edelstahl"

EISENGUSS = "Eisenguss"

EMAILLE_GLASUR = "Emaille / Glasur"

GLAS = "Glas"

IRON = "Iron"

KERAMIKGLAS = "Keramikglas"

KUPFER = "Kupfer"

MEHRLAGIG = "Mehrlagig"

MISCHUNG = "Mischung"

NICHT_IDENTIFIZIERBAR = "Nicht identifizierbar"

NICHT_KLASSIFIZIERT = "Nicht klassifiziert"

STEINGUT = "Steingut"

TONWARE = "Tonware"

  
  

class Verschlussart(Enum):

"""

Attribute Description if provided:

NICHTIDENTIFIZIERBAR (str): Dieser Begriff wird zur Beschreibung der Produktattribute verwendet, die aufgrund vorhandener oder verfügbarer Produktinformationen nicht identifizierbar sind.

NICHTKLASSIFIZIERT (str): Dieser Begriff wird zur Beschreibung von solchen Attributen verwendet, bei denen es nicht möglich ist, sie innerhalb ihres speziellen Marktes / Wirtschafsraumes zu klassifizieren. Ein Beispiel für solche Produkte ist Ziegenkäse: Ziegenkäse wird oft generisch / der Gattung zugeordnet und kann nicht weiter klassifiziert werden.

"""

  

BAJONETTVERSCHLUSS = "Bajonettverschluss"

BUEGELVERSCHLUSS = "Bügelverschluss"

DRUCKKNOPFVERSCHLUSS = "Druckknopfverschluss"

EINSPRINGENDE_DECKELVERRIEGELUNG = "Einspringende Deckelverriegelung"

NICHT_IDENTIFIZIERBAR = "Nicht identifizierbar"

NICHT_KLASSIFIZIERT = "Nicht klassifiziert"

OHNE = "Ohne"

  
  

class ToepfeFuerBratgeschirr_Pfannen_Woks_Koketten(BaseModel):

"""

Definition: Umfasst alle Produkte, die als nicht elektrische Behälter beschrieben werden können, welche zum Kochen, Dampfgaren, Braten und anderen Kochmethoden auf dem Herd verwendet werden. Beinhaltet Produkte wie beispielsweise nicht elektrische Kasserolle, Woks und Schnellkochtöpfe.

Definition Excludes: Ausgenommen sind insbesondere elektrische Kochtöpfe, Pfannen, Woks und Dampfgarer. Ausgenommen sind Produkte wie beispielsweise Backformen, feuerfeste Formen, Grillzubehör, Camping-Kochgeschirr und Einweg-Kochgeschirr.

"""

  

art_der_antihaftbeschichtung: ArtDerAntihaftbeschichtung

art_von_bratgeschirr_pfanne_woks_kokotten: ArtVonBratgeschirr_Pfanne_Woks_Kokotten

falls_mit_abnehmbarem_griff: FallsMitAbnehmbaremGriff

materialart: Materialart

verschlussart: Verschlussart

```

```json

{
  "art_der_antihaftbeschichtung": "<ArtDerAntihaftbeschichtung.POLYTETRAFLOURETHYLEN_PTFE: 'Polytetraflourethylen_PTFE'>",
  "art_von_bratgeschirr_pfanne_woks_kokotten": "<ArtVonBratgeschirr_Pfanne_Woks_Kokotten.BRATPFANNE: 'Bratpfanne'>",
  "falls_mit_abnehmbarem_griff": "<FallsMitAbnehmbaremGriff.NEIN: 'Nein'>",
  "materialart": "<Materialart.EDELSTAHL: 'Edelstahl'>",
  "verschlussart": "<Verschlussart.NICHT_IDENTIFIZIERBAR: 'Nicht identifizierbar'>"
}

{
  "text_tokens": 279,
  "completion_tokens": 68,
  "prompt_tokens": 1704,
  "total_tokens": 1772,
  "cached": 1536
}
```
