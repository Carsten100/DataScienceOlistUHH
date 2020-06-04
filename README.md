# Brazilian E-Commerce Public Dataset by Olist
## OweysBranch

Dein Notizbuch

*Muss noch gemacht werden:*
* Datenset analysieren und visualisieren.

*Momentan bearbeitetes Notebook:
```csharp
Datavisualization.pynb
- Wie viele Bestellungen pro monat?

- Wie viele Kunden pro Monat?

- Beliebteste Verkäufer und deren Verkäufe
1.) ueber OrderItemSet
2.) seller_id aufrufen. Wie oft wurde seller_id aufgerufen? //haeufigkeit des Sellers
3.) ueber Order_id den durschnitt des review_scores des verkaeufers bestimmen.
---> Problem: in einer Order_id wurden manchmal mehrere Produkte vereint bewertet. Das heißt es kann
sein, dass ein verkaeufer fuer sein produkt besser bzw schlechter bewertet wird, wegen eines 
anderen Produktes innerhalb der Order_id.
Idee: es sind mehr einzelprodukte pro bestellungen. Wir nehmen die Abweichung in kauf. (bitte vorher
anmerken)
--> Balkendiagram für Bestellungsanzahl
.....
```

Jeder hat erstmal sein eigenes Notebook. Beim Masterbranch werden Ideen Commited die von mindestens einer weiteren Person 
akzeptiert werden. Also erstmal an eigenem Branch arbeiten und dann einen Request anfragen. 
