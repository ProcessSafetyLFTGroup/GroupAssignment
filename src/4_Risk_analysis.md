# 4 Risicoanalyse

De volgende risicoanalyse beschrijft mogelijke risico's in het LFT-handlingsproces en de bijbehorende mitigeringsstrategieën.

```plantuml
@startuml
title Risicoanalyse voor LFT-handlingsmechanisme

skinparam rectangle {
    BorderColor black
    BackgroundColor LightGray
}

partition "Risico 1: Falen van de Extruder" {
    :Beschrijving: Extruder start niet, waardoor het proces stopt;
    :Waarschijnlijkheid: Gemiddeld;
    :Impact: Hoog;
    :Mitigatie: Regelmatig onderhoud en systeemmonitoring;
}

detach

partition "Risico 2: Sensorstoring" {
    :Beschrijving: Fotocel of Reed-schakelaar detecteert geen materiaal of gereedschapsposities;
    :Waarschijnlijkheid: Laag;
    :Impact: Hoog;
    :Mitigatie: Regelmatige sensorcontroles en redundantie met secundaire sensoren;
}

detach

partition "Risico 3: Pneumatisch Systeem Falen" {
    :Beschrijving: Falen van het pneumatische systeem verhindert de werking van de grijper;
    :Waarschijnlijkheid: Gemiddeld;
    :Impact: Hoog;
    :Mitigatie: Noodstopprocedures en regelmatige inspectie van pneumatische leidingen;
}

detach

partition "Risico 4: Misalignment van Robotarm" {
    :Beschrijving: Robotarm bereikt niet de juiste positie;
    :Waarschijnlijkheid: Laag;
    :Impact: Gemiddeld;
    :Mitigatie: Gebruik van positionele sensoren en herkalibratieprotocollen; 
}

partition "Risico 5: Verstopte gripperneedles" {
    :Beschrijving: Gripper needles vastgeklemd in beplating
    :Waarschijnlijkheid: Gemiddel;
    :Impact: Gemiddeld;
    :Mitigatie: Tool tijdig behandelen met lossingsmiddel.


@enduml
