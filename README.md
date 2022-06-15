# Debriefing (na eerste gesprek met de opdrachtgever)

# Werking van de vacaturebank
<img width="900" alt="Schermafbeelding 2022-05-25 om 14 39 07" src="https://user-images.githubusercontent.com/74242736/170263847-44fa4538-8262-4d3f-b7a7-07ce532c3e4b.png">

# DISC Test
Vragenlijst om te bepalen binnen welke categorieën van het DISC model een persoon valt.

1.	Ben jij direct of indirect?
-	Direct: Dominant en interactief
-	Indirect: Consciëntieus en stabiel

2.	Ben jij taakgericht of mensgericht?
-	Mensgericht: Stabiel en interactief
-	Taakgericht: Consciëntieus en dominant

3.	Geef aan wat het beste bij jou past
-	Bedachtzaam (blauw)
-	Harmonieus (groen)
-	Direct (rood)
-	Spraakzaam (geel)
 
4.	Geef aan wat het beste bij jou past
-	Analytisch (blauw)
-	Samen (groen)
-	Besluitvaardig (rood)
-	Enthousiast (geel)

5.	Geef aan wat het beste bij jou past
-	Gericht op uitdagingen (rood)
-	Praat graag (geel)
-	Rationeel (blauw)
-	Stabiel (groen)

6.	Geef aan wat het beste bij jou past
-	Inspirerend (geel)
-	Stabiel (groen)
-	Vastbesloten (rood)
-	Perfectie (blauw)

7.	Geef aan wat het beste bij jou past***
-	Levendig (blauw)
-	Gedisciplineerd (groen)
-	Vol zelfvertrouwen (rood)
-	Vriendelijk (geel)

8.	Geef aan wat het beste bij jou past
-	Optimistisch (geel)
-	Wil redenen (blauw)
-	Resultaten (rood)
-	Coöperatief (groen)


9.	Geef aan wat het beste bij jou past
-	Invloed (geel)
-	Dominant (rood)
-	Meegaand en attent (groen)
-	Consciëntieus (blauw)

10.	Geef aan wat het beste bij jou past
-	Helpend en ondersteunend (groen)
-	Feiten (blauw)
-	Gezelligheid (geel)
-	Assertief (rood)


# Proces karaktereigenschappen matchen met vacatures
Het doel is om uiteindelijk a.d.h.v. de persoonlijkheidstest relevante vacatures aan te raden aan gebruikers. Een gebruiker krijgt per DISC categorie punten. Daaruit komen dan karaktereigenschappen die bij de persoon passen. De vacatures moeten gescand worden op kernwoorden, en ook een puntensysteem krijgen waarbij naar voren komt bij welke DISC categorie de vacature het best past. Hierna is het dan de bedoeling om de punten van de gebruiker en vacatures te matchen, en op die manier de meest relevante vacatures aan te bieden op basis van karaktereigenschappen. Omdat dit een uitdagende taak is ben ik begonnen om in stappen verschillende prototypes uit te werken. Hierbij focuste ik op een deel van de eindfunctionaliteit, om op die manier in stappen dichter bij de oplossing te komen.

## Versie 1 'Checken welke eigenschap bij kernwoorden past'
In de eerste versie ben ik aan de slag gegaan om strings uit een array te matchen met een gegeven waarde. Op die manier is het mogelijk om te kijken bij welke categorie van het DISC model de kernwoorden uit de vacatures passen. Dit heb ik gedaan door gebruik te maken van '.includes'. Dit chheckt of een bepaalde waarde in een array voorkomt, en vervolgens daar een counter aan toegevoegd om de waarde te meten. 

<img width="1038" alt="Schermafbeelding 2022-06-14 om 14 02 33" src="https://user-images.githubusercontent.com/74242736/173572482-199eb160-e605-4eb5-bc8f-b2afed24c553.png">

<img width="1038" alt="Schermafbeelding 2022-06-14 om 14 07 13" src="https://user-images.githubusercontent.com/74242736/173573297-2af1595b-3acf-47c2-b6f8-e3595c6f3399.png">


## Versie 2 'Kernwoorden uit vacature halen en matchen met DISC model'
In de tweede versie heb ik de kernwoorden uit een vacature gehaald, als een soort prototype van hoe het moet gaan werken. De vacatures zouden gescraped moeten worden, en vervolgens in een vast format gezet worden. Vervolgens zou je net als ik in deze versie heb gedaan de kernwoorden uit een vacature kunnen halen, en die door de functie halen. Op die manier kan je dan een counter maken die bijhoudt per DISC categorie hoeveel kernwoorden er matchen uit de vacatures. Het probleem wat hier voorkomt is dat ik de kernwoorden los moest selecteren in JS, en er niet automatisch wordt gecheckt op elke vacature. Dit is uiteraard niet handig voor een vacaturebank waarin veel vacatures staan.

<img width="1038" alt="Schermafbeelding 2022-06-14 om 14 03 32" src="https://user-images.githubusercontent.com/74242736/173572699-a83e51c4-cd94-4d6b-aced-1b5cca25b7ff.png">

<img width="800" alt="Schermafbeelding 2022-06-14 om 14 04 41" src="https://user-images.githubusercontent.com/74242736/173572893-f7649133-16c4-4bc0-b678-82efa39c74d3.png">

<img width="800" alt="Schermafbeelding 2022-06-14 om 14 06 30" src="https://user-images.githubusercontent.com/74242736/173573175-f021a6de-5685-4603-a393-694f20f61e6c.png">

## Versie 3 'Alle vacatures automatisch scannen en matchen met DISC model'
In versie 3 zijn de juiste vacatures gebruikt die we hebben gekregen van de opdrachtgever. Ook is er nu een focus aangebracht door de opdrahtgever op de BioTech sector, daar hebben wij de vacatures en stijl op aangepast. In deze versie zit een automatisch JS systeem die per toegevoegde vacature de kernwoorden naloopt en matcht met de DISC categorie. Het probleem wat hier blijft bestaan is echter dat er een algemene counter is die omhoog gaat per matchend kernwoord. Het systeem kijkt niet per 3 kernwoorden van de vacature, en maakt geen eigen variabele aan die per vacature de matchende kernwoorden bijhoudt. Hierdoor is het nog niet gelukt om een sorteer systeem te maken op basis van de DISC categorieën. Daarvoor moet het systeem per vacature van 0 tot max 3 punten geven, en dat bijhouden in een variabele.

<img width="1038" alt="Schermafbeelding 2022-06-15 om 15 03 10" src="https://user-images.githubusercontent.com/74242736/173833525-f2d36be4-17e7-42fa-821a-4f9da36ab317.png">

<img width="1038" alt="Schermafbeelding 2022-06-15 om 15 03 48" src="https://user-images.githubusercontent.com/74242736/173833644-5d56f400-733d-4f5d-a223-fe3fb3114133.png">


## Licentie

![GNU GPL V3](https://www.gnu.org/graphics/gplv3-127x51.png)

This work is licensed under [GNU GPLv3](./LICENSE).

