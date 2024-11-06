# 1 Introductie
In deze mdBook wordt het project beschreven van het LFT-handlingsmechanisme voor TPAC, dat we uitvoeren in het kader van de minor Industriële Automatisering, zoals beschreven in sectie 1.1. Voor het vak "Proces en Safety" onderzoeken we het proces en analyseren we de bijbehorende risico's. Het mdbook bevat flowcharts van het te doorlopen proces, een hoofdstuk over veiligheid en een uitgebreide risicoanalyse.


# 1.1 Opdrachtomschrijving

```
@startuml
// deegstreeg => hamster noemen
@enduml
```
LFT handling systeem.

TPAC is een onafhankelijk onderzoeks- en innovatiecentrum dat zich specialiseert in thermoplastische composieten en de bijbehorende productieprocessen. TPAC richt zich op praktische toepassingen, ontwikkelt proof-of-concepts voor bedrijven (kleine en middelgrote ondernemingen) en biedt expertise en faciliteiten aan bedrijven die willen innoveren met thermoplastische composieten.

TPAC biedt een open en innovatieve omgeving die gericht is op de ontwikkeling van nieuwe materialen en processen, evenals de verbetering van bestaande processen op een kleine schaal. Projecten worden uitgevoerd voor industriële partners (o.a. GKN Fokker Aerospace, Toray Advanced Composites, Collins Aerospace). 

Betreft dit project, gebruikt TPAC een extruder met lage schuifkracht om composietmateriaal kosteneffectief te recyclen. Momenteel wordt de output van de extruder, een gesmolten en gemengde mix, handmatig overgebracht naar een persvorm. TPAC wil dit proces automatiseren en daarvoor zal een KUKA-robotarm binnen een ENGEL insertcel (gebruikt in dit proces als persvorm) gebruikt worden.
  
De fysieke delen die door de studenten ontworpen zal worden zijn:

    •	De tool aan de robotarm om het materiaal in de persvorm te zetten.
    •	De communicatie tussen extruder, KUKA en Engel
        o	PLC
        o	Sensoren
        o	Etc.
    •	Tussen deze doelen is het voornaamst dat één van deze voltooid zal zijn.

Dit geautomatiseerde proces vereist zo’n klein mogelijk warmteverlies, om efficientie in de ENGEL te waarborgen. 

De volgende documentatie zal worden opgeleverd:

    •	Projectplan
    •	Pakket van Eisen
    •	Technisch Ontwerp
    •	Test- en Analyseverslag

Met deze documenten zal de klant alle relevante informatie hebben wat nodig is voor besturing en correct gebruik van het ontwerp. 


# 1.2 Taakverdeling

```
@startuml
class Taakverdeling {
    || Nummer || Naam || Taak 1 || Taak 2 || Taak 3 ||
    | 1 | Luuk | Algemeen opzet | Test |
    | 2 | Joost | Flowchart Diagram gemaakt | Zelf evaluatie |
    | 3 | Thijs | Risk analysis |
    | 4 | Milan | Diagram |
    | 5 | Jur | Introductie | Taakverdeling | Hoe we omgaan met commits |
}
@enduml
```
# 1.3 Hoe we omgaan met commits
