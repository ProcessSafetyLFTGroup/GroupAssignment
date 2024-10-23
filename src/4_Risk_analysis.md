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

detach

partition "Risico 5: Verstopte gripperneedles" {
    :Beschrijving: Gripper needles vastgeklemd in beplating
    :Waarschijnlijkheid: Gemiddel;
    :Impact: Gemiddeld;
    :Mitigatie: Tool tijdig behandelen met lossingsmiddel.;
}

detach

partition "Risico 6: Warmte" {
    :Beschrijving: De extruder geeft warmte af en staat niet in het hekwerk
    :Waarschijnlijkheid: Gemiddel;
    :Impact: Gemiddeld;
    :Mitigatie: Afstand houden en waarschuwenbord dat het heet is.;
}

detach

partition "Risico 7: Materiaal te koud" {
    :Beschrijving: Materiaal teveel afgekoeld, waardoor oppakken niet meer mogelijk is.;
    :Waarschijnlijkheid: Gemiddeld;
    :Impact: Gemiddeld;
    :Mitigatie: Extruder stopzetten na het cutten, tot de pers klaar is.;
}

partition "Risico 8: Materiaal te koud" {
    :Beschrijving: Materiaal teveel afgekoeld, waardoor oppakken niet meer mogelijk is.;
    :Waarschijnlijkheid: Gemiddeld;
    :Impact: Hoog;
    :Mitigatie: Extruder stopzetten na het cutten, tot de pers klaar is.;
}

@enduml
