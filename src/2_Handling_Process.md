In dit hoofdstuk worden twee diagrammen weergeven:

Interface diagram (hoofdstuk 2.1): In dit diagram worden de volgorde van de verschillende systemen weergeven. Daarnaast word ook weergeven hoe alle losse systemen comminuceren.

Flow chart (hoofdstuk 2.2): In de flowchart wordt het volledige proces gedetaileerd stap voor stap weergeven.


# 2.1 LFT Interface diagram

```plantuml
@startuml interface Diagram
skinparam rectangle {
    BackgroundColor white
    BorderColor black
    FontSize 12
}


rectangle "gerecycled Materiaal" as GerecycledMateriaal
rectangle "Extruder" as Extruder
rectangle "Cutting Tool" as CuttingTool
rectangle "Output Materiaal" as OutputMateriaal
rectangle "Robot Arm (KUKA)" as KUKA
rectangle "Mal (ENGEL)" as Mal
rectangle "Product" as Product


GerecycledMateriaal -right-> Extruder 
Extruder -right-> CuttingTool 
CuttingTool -right-> OutputMateriaal
OutputMateriaal -right-> KUKA
KUKA -right-> Mal
Mal -right-> Product 

Extruder <..> communication: "communication"
CuttingTool <..> communication: "communication"
KUKA <..> communication: "communication"
Mal <..> communication: "communication"


KUKA-up-> Grijper 
KUKA -up-> Beweging

@enduml
```

# 2.2 LFT proces flowchart

```plantuml
@startuml Proces diagram
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
