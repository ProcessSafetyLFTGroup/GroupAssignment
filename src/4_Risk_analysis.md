# 4 Risk analysis

De volgende risicoanalyse beschrijft mogelijke risico's in het LFT-handlingsproces en de bijbehorende mitigeringsstrategieën.

```plantuml
@startuml
title Risicoanalyse voor LFT-handlingsmechanisme

skinparam rectangle {
    BorderColor black
    BackgroundColor LightGray
}

rectangle "Risico 1: Falen van de Extruder" as R1 {
    :Beschrijving: Extruder start niet, waardoor het proces stopt;
    :Waarschijnlijkheid: Gemiddeld;
    :Impact: Hoog;
    :Mitigatie: Regelmatig onderhoud en systeemmonitoring;
}

rectangle "Risico 2: Sensorstoring" as R2 {
    :Beschrijving: Fotocel of Reed-schakelaar detecteert geen materiaal of gereedschapsposities;
    :Waarschijnlijkheid: Laag;
    :Impact: Hoog;
    :Mitigatie: Regelmatige sensorcontroles en redundantie met secundaire sensoren;
}

rectangle "Risico 3: Pneumatisch Systeem Falen" as R3 {
    :Beschrijving: Falen van het pneumatische systeem verhindert de werking van de snijtool of grijper;
    :Waarschijnlijkheid: Gemiddeld;
    :Impact: Hoog;
    :Mitigatie: Noodstopprocedures en regelmatige inspectie van pneumatische leidingen;
}

rectangle "Risico 4: Misalignment van Robotarm" as R4 {
    :Beschrijving: Robotarm bereikt niet de juiste positie;
    :Waarschijnlijkheid: Laag;
    :Impact: Gemiddeld;
    :Mitigatie: Gebruik van positionele sensoren en herkalibratieprotocollen;
}

R1 --> R2 : Afhankelijkheden
R2 --> R3 : Potentiële kettingreactie
R3 --> R4 : Impact op robotoperaties
@enduml

