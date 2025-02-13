For our dataset, consisting of 3.000 Products spread across different GPC Families, we manually confirmed the ground truth values provided to us by globus. Four people were actively involved in this process. Here is what each person noted:

### Christoph

GPC sometimes has very confusing translations for both the brick title, as well as the includes and excludes descriptions. One prominent example for a misleading brick title in german is:  ***Müsli / Müsliriegel***, which makes labelers assume that both grain-based cereals ("Müsli" in german) and grain-based bars are supposed to be in this brick. The description makes it clear that ***only*** bars are mean to be in this brick:

>Umfasst alle Produkte, die als Riegel beschrieben werden können, welche sämtliche oder einige der folgenden Zutaten enthalten: Getreide, Müsli, Weizen, Reis, Kleie, Samen, Obst, Nüsse und Honig.

>Includes all products that can be described as bars containing all or some of the following ingredients: Cereals, muesli, wheat, rice, bran, seeds, fruit, nuts and honey. (translated using deepl)

The english title for this brick is: ***Cereal/Muesli Bars***, which conveys the intended use much clearer.

An example for their mistranslation of descriptions is seen in the brick:
***Fertiggerichte aus mehreren Bestandteilen - verzehrfertig (ohne Kühlung haltbar)*** and 
***Fertiggerichte mit mehreren Bestandteilen - nicht verzehrfertig (ohne Kühlung haltbar)***
where the labeler has to distinguish between what is considered ***verzehrfertig*** (Ready to eat) and ***nicht verzehrfertig*** (Not ready to eat). The first two sentences in both descriptions being:

>Fertiggericht aus mehreren Zutaten oder Mikrowellengerichte sind abgepackte, leicht verderbliche, vollständige Mahlzeiten. Dieses Gericht verlangt keine andere Vorbereitung außer Erwärmung und enthält sämtliche Elemente, [...]

>Multi-ingredient ready meals or microwave meals are packaged, perishable, complete meals. This dish requires no preparation other than heating and contains all the elements, [...] (translated using deepl)

This makes the aforementioned task more difficult than it has to be, since the english version clearly differentiates between ***to warm up*** and ***to cook***:

Ready-Made Combination Meals - Ready to Eat (Shelf Stable):
>Ready-made combination meal or microwave meal is a pre-packaged shelf stable full meal.  The meal requires no preparation, but may be warmed [...]

Ready-Made Combination Meals - Not Ready to Eat (Shelf Stable):
>Ready-made combination meal or microwave meal is a pre-packaged shelf stable full meal.  The meal requires no preparation other than cooking [...]

Globus sorted every ready-made canned meal into ***Fertiggerichte aus mehreren Bestandteilen - verzehrfertig (ohne Kühlung haltbar)***, yet there are more specific bricks available such as  ***Getreidebasierte Produkte/-Gerichte, herzhaft - verzehrbereit (ohne Kühlung haltbar)*** (in a different class). E. g.:

![[Pasted image 20250203113837.png]]

or ***Gemüse- /Kartoffelbasierte Produkte /-Gerichte - verzehrbereit (ohne Kühlung haltbar)*** (in a different class)

![[Pasted image 20250203113730.png]]

Elektrisch???
![[Pasted image 20250211132347.png]]
![[Pasted image 20250211132401.png]]
### Sian
To be added
### Krieger
To be added
### Philipp
To be added