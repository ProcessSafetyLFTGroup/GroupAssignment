# 1 Introductie
In deze mdBook wordt het project beschreven van het LFT-handlingsmechanisme voor TPAC, dat we uitvoeren in het kader van de minor Industriële Automatisering, zoals beschreven in sectie 1.1. Voor het vak "Proces en Safety" onderzoeken we het proces en analyseren we de bijbehorende risico's. Het mdbook bevat flowcharts van het te doorlopen proces, een hoofdstuk over veiligheid en een uitgebreide risicoanalyse.


## 1.1 Opdrachtomschrijving

LFT handling systeem.

TPAC is een onafhankelijk onderzoeks- en innovatiecentrum dat zich specialiseert in thermoplastische composieten en de bijbehorende productieprocessen. TPAC richt zich op praktische toepassingen, ontwikkelt proof-of-concepts voor bedrijven (kleine en middelgrote ondernemingen) en biedt expertise en faciliteiten aan bedrijven die willen innoveren met thermoplastische composieten.

TPAC biedt een open en innovatieve omgeving die gericht is op de ontwikkeling van nieuwe materialen en processen, evenals de verbetering van bestaande processen op een kleine schaal. Projecten worden uitgevoerd voor industriële partners (o.a. GKN Fokker Aerospace, Toray Advanced Composites, Collins Aerospace). 

Betreft dit project, gebruikt TPAC een extruder met lage schuifkracht om composietmateriaal kosteneffectief te recyclen. Momenteel wordt de output van de extruder, een gesmolten en gemengde mix (Ook wel hamster genoemd), handmatig overgebracht naar een persvorm. TPAC wil dit proces automatiseren en daarvoor zal een KUKA-robotarm binnen een ENGEL insertcel (gebruikt in dit proces als persvorm) gebruikt worden.
  
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


## 1.2 Taakverdeling

```
@startuml
class Taakverdeling {
    || Nummer || Naam || Taak 1 || Taak 2 || Taak 3 ||
    | 1 | Luuk | Algemeen opzet | Handeling proces analyzed | |
    | 2 | Joost | Handeling Flowchart Diagram | Zelf evaluatie | |
    | 3 | Thijs | Risk analysis | | |
    | 4 | Milan | Diagram | Handeling introductie| Handeling interface|
    | 5 | Jur | Introductie | Taakverdeling | Samenwerking in GitHub commits |
}
@enduml
```



## 1.3 Samenwerking in GitHub


Voor onze groepssamenwerking hebben we een workflow opgesteld in GitHub die ons helpt om overzichtelijk en efficiënt te werken. Hierbij verdelen we taken en zorgen we voor een gecontroleerde versiebeheeromgeving. Hieronder beschrijven we de aanpak voor commits, pull requests, merges en algemene samenwerking.


### 1.3.1 Commits Structureren


We hanteren een gestructureerde aanpak voor commits om de geschiedenis overzichtelijk en leesbaar te houden:

• Frequentie van commits: We commiten na elke afgeronde taak of logische wijziging, en niet voor elke kleine aanpassing, zoals een enkele zin. Dit zorgt voor een overzichtelijke commitgeschiedenis.

• Commit-berichten: We gebruiken beschrijvende commit-berichten om duidelijk aan te geven wat de commit inhoudt.

    
### 1.3.2 Pull Requests


Onze aanpak voor pull requests en het reviewproces is als volgt:

• Commit in onze fork: Tussen door de dag doen wij een commit per onderdeel om zo duidelijk mogelijk te hebben wat er aangepast is. Dit doen we omdat het dan duidelijk is wat er aangepast is

• Pull requests (PRs): Aan het einde van een werkdag of na het voltooien van een taak maken we een pull request naar de Github organistatie. Hiermee voorkomen we te veel kleine pull requests en houden we het overzicht.
    

### 1.3.3 Mergen en Merge-commits


Onze merge-strategie helpt ons om de projectgeschiedenis overzichtelijk te houden:
    
• Code reviews en dubbele controle: Een teamlid die de taak niet zelf heeft geschreven, reviewt de pull request. Dit zorgt voor een dubbele controle van de wijzigingen, wat de kwaliteit en veiligheid verhoogt.

• Checklist voor reviews: Tijdens de review controleren we op duidelijke structuur, afwezigheid van syntax- of veiligheidsfouten, en duidelijke commit-boodschappen.

• Feedback: De reviewer kan suggesties geven of kleine aanpassingen maken, zodat de PR zo snel mogelijk kan worden afgerond.
    

### 1.3.4 Regelmatige Communicatie en Planning

Voor een transparante en efficiënte samenwerking hebben we dagelijkse overlegmomenten ingepland. Tijdens deze check-ins bespreken we de voortgang en verdelen we nieuwe taken. Alle taken en issues worden bijgehouden in GitHub en gekoppeld aan de relevante pull requests, waardoor iedereen inzicht heeft in de planning en voortgang.