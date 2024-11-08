# 1 Introductie
In deze mdBook wordt het project beschreven van het LFT-handlingsmechanisme voor TPAC, dat we uitvoeren in het kader van de minor Industriële Automatisering, zoals beschreven in sectie 1.2. Voor het vak "Proces en Safety" onderzoeken we het proces en analyseren we de bijbehorende risico's. Het mdbook bevat flowcharts van het te doorlopen proces.

## 1.1 Groepleden

| Naam             | Opleiding         | Studentnummer |
|------------------|-------------------|---------------|
| Thijs ten Heggeler| Werktuigbouwkunde | 523908        |
| Milan Wichink    | Werktuigbouwkunde | 518044        |
| Luuk Vulkers     | Elektrotechniek   | 523822        |
| Joost Peters     | Mechatronica       | 514165        |
| Jur Otten        | Mechatronica       | 514476        |


## 1.2 Opdrachtomschrijving

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


## 1.3 Taakverdeling

| Nummer | Naam  | Taak 1                    | Taak 2                        | Taak 3                        |
|--------|-------|---------------------------|-------------------------------|-------------------------------|
| 1      | Luuk  | Algemeen opzet            | Handeling proces analyzed     |                               |
| 2      | Joost | Handeling Flowchart Diagram| Zelf evaluatie               |                               |
| 3      | Thijs | Risico analisyse          |                               |                               |
| 4      | Milan | Handeling diagram         | Risico analisyse ondersteunen | Handeling interface           |
| 5      | Jur   | Introductie               | Taakverdeling                 | Samenwerking in GitHub commits|




## 1.4 Samenwerking in GitHub


Voor onze groepssamenwerking gebruiken we GitHub om overzichtelijk en efficiënt te werken. We verdelen de taken, zorgen voor versiebeheer en volgen een duidelijke werkwijze voor commits, pull requests, merges en communicatie.


### 1.4.1 Commits Structureren


We zorgen ervoor dat commits duidelijk en overzichtelijk zijn:

    • Frequentie van commits: We maken een commit na elke afgeronde taak of belangrijke wijziging, niet bij elke kleine aanpassing, zodat de commitgeschiedenis helder blijft.
    
    • Commit-berichten: We schrijven beschrijvende berichten bij elke commit, zodat het duidelijk is wat er is veranderd.

    
### 1.4.2 Pull Requests


Onze aanpak voor pull requests is als volgt:

    • Commits in onze fork: Gedurende de dag maken we commits voor elk onderdeel, zodat we precies kunnen zien wat er is aangepast.
    
    • Pull requests (PR's): Aan het einde van de werkdag of na een voltooide taak, maken we een pull request naar de hoofdrepository. Dit voorkomt teveel kleine pull requests en houdt het overzichtelijk.
    

### 1.4.3 Mergen en Merge-commits


Voor het mergen van code hanteren we de volgende werkwijze:

    • Code reviews en dubbele controle: Iemand anders dan de auteur van de taak reviewt de pull request. Dit zorgt voor extra controle en verhoogt de kwaliteit.
    
    • Checklist voor reviews: Tijdens de review controleren we op een duidelijke structuur, geen syntax- of veiligheidsfouten, en duidelijke commit-berichten.
    
    • Feedback: De reviewer kan suggesties geven of kleine wijzigingen voorstellen om de PR snel af te ronden.
    

### 1.4.4 Regelmatige Communicatie en Planning

We plannen op zijn tijd een overleggen in om de voortgang te bespreken en nieuwe taken te verdelen. Alle taken en issues worden in GitHub bijgehouden en gekoppeld aan de relevante pull requests, zodat iedereen altijd op de hoogte is van de voortgang.