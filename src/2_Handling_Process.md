# 2 LFT Afhandelingsproces

## 2.1 Flowchart
Deze flowchart biedt een overzicht van het geautomatiseerde productieproces waarin een PLC, extruder, snijtool en KUKA-robot samenwerken. Stap voor stap toont de flowchart hoe deze onderdelen via signalen en sensoren met elkaar communiceren om de hamster door de productiecyclus te begeleiden. De PLC stuurt elk onderdeel aan en zorgt dat het materiaal wordt bewerkt, verplaatst en uiteindelijk in de pers wordt gevormd.

Zo geeft het schema een helder beeld van de samenwerking tussen de machineonderdelen door alle processtappen heen.

```plantuml
@startuml
start

:Start_Signaal>
if (Extruder gestart?) then (Ja)
    :Start_Output>
else (Nee)
    stop
endif

repeat
    :Fotocel_Materiaal_Aanwezig>
    repeat while (Fotocel == True?) is (Nee) not (Ja)
        :Pneumatisch Uit;
        :Cutting Tool sluit en snijdt deegstreng;
repeat
    :Reedcontact_Cutting_Tool>
    repeat while (Reedcontact == True?) is (Nee) not (Ja)
        :Pneumatisch In;
        :Start Lopende Band;
        :Start Kuka Robot;
repeat
    :Robot_Op_Positie_Cutting_Tool>
    repeat while (Robot_Op_Positie_Cutting_Tool == True?) is (Nee) not (Ja)
        :Pneumatisch Uit Grijper Tool;
        :Grijper Tool sluit en pakt deegstreng vast;
repeat
    :Fotocel_Deegstreng_Aanwezig>
    repeat while (Fotocel == True?) is (Nee) not (Ja)
        :Robot arm naar matrijs;
repeat
    :Robot_Op_Positie_Matrijs>
    repeat while (Robot_Op_Positie_Matrijs == True?) is (Nee) not (Ja)
        :Pneumatisch In Grijper Tool;
        :Grijper Tool opent en laat deegstreng los;
repeat
    :Fotocel_Deegstreng_Afwezig>
    repeat while (Fotocel == False?) is (Nee) not (Ja)
        :Robot arm naar home positie;
repeat
    :Robot_Op_Positie_Home>
    repeat while (Robot_Op_Positie_Home == True?) is (Nee) not (Ja)
        :Matrijs sluiten;
stop
@enduml
```