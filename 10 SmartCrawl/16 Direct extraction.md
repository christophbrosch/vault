Initial findings with 4o-mini:

- globus 0.7134285714285736 
- edeka24 0.8688571428571462 
- supermarkt24h 0.5622857142857116

Two things were noticed:

- Mini calculated the daily_value_intake_percentage correctly based off the European recommended daily intake: ![[Screenshot from 2025-03-04 16-01-25.png]]
- Mini removed Prefixes in the Ingredient statement such as "Zutaten:".
- If no ingredient_statement is present, mini assumes Allergenes to be ingredients:
	- "Fischerzeugnisse und andere Spurenelemente" -> Ingredients even though it is allergens