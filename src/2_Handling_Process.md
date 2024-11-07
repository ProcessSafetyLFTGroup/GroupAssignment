# 2 LFT Afhandelingsproces

# 2.1 Flowchart
Deze flowchart biedt een overzicht van het geautomatiseerde productieproces waarin een PLC, extruder, snijtool en KUKA-robot samenwerken. Stap voor stap toont de flowchart hoe deze onderdelen via signalen en sensoren met elkaar communiceren om de hamster door de productiecyclus te begeleiden. De PLC stuurt elk onderdeel aan en zorgt dat het materiaal wordt bewerkt, verplaatst en uiteindelijk in de pers wordt gevormd.

Zo geeft het schema een helder beeld van de samenwerking tussen de machineonderdelen door alle processtappen heen.

```plantuml
@startuml
start

:PLC stuurt Start Signaal naar Extruder;
if (Extruder gestart?) then (Ja)
    :PLC ontvangt 'Start' output;
else (Nee)
    stop
endif

repeat
    :PLC wacht op fotocel van materiaal aanwezig;
    repeat while (Fotocel is True?) is (Nee) not (Ja)
        :PLC stuurt 'Pneumatisch Uit' naar Cutting Tool;
        :Cutting Tool sluit en snijdt deegstreng;
repeat
    :PLC wacht op Reedcontact van de Cutting Tool;
    repeat while (Reedcontact is True?) is (Nee) not (Ja)
        :PLC stuurt 'Pneumatisch In' naar Cutting Tool;
        :PLC stuurt 'Start' naar Lopende Band;
        :PLC stuurt 'Start' naar Kuka Robot;
repeat
    :PLC wacht op Robot arm op positie bij Cutting Tool;
    repeat while (Robot arm op positie bij Cutting Tool?) is (Nee) not (Ja)
        :PLC stuurt 'Pneumatisch Uit' naar Grijper Tool;
        :Grijper Tool sluit en pakt de deegstreng vast;
 repeat
    :PLC wacht op fotocel van deegstreng aanwezig;
    repeat while (Fotocel is True?) is (Nee) not (Ja)
        :PLC stuurt 'Robot arm naar matrijs' naar Kuka Robot;       
repeat
    :PLC wacht op Robot arm op positie in matrijs;
repeat while (Robot arm op positie in matrijs?) is (Nee) not (Ja)
        :PLC stuurt 'Pneumatisch IN' naar Grijper Tool;
        :Grijper Tool opent en laat de deegstreng los;
 repeat
    :PLC wacht op fotocel van deegstreng afwezig;
    repeat while (Fotocel is False?) is (Nee) not (Ja)
        :PLC stuurt 'Robot arm naar home positie' naar Kuka Robot;   
 repeat
    :PLC wacht op Robot arm op home positie;
    repeat while (Robot arm op home positie?) is (Nee) not (Ja)
        :PLC stuurt 'Matrijs sluiten' naar Engel Pers; 
stop
@enduml
```
