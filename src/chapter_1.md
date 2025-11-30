# Chapter 1: Making coffee process
```plantuml
@startuml
    [*] --> Idle
    Idle --> Start Coffee : Get off bed
    Start Coffee --> Heating Water : Press hot water
    Heating Water --> Water Hot : Wait 5s
    Water Hot --> Grinding : Press Grinding
    Grinding --> Grind Done : Wait 5s
    Grind Done --> Brewing : Press Brewing
    Brewing --> Done : wait 5s
    Brewing --> Error : LowWaterLevel
    Error --> Idle : Reset
    Done --> [*]
@enduml
```