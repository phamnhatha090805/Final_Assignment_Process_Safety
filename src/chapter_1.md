# Chapter 1: Making coffee process
```plantuml
@startuml
    [*] --> Idle
    Idle --> HeatingWater : Get off bed and Start making coffee
    HeatingWater --> WaterHot : Wait 5s
    WaterHot --> Grinding : Press Grinding
    Grinding --> GrindDone : Wait 5s
    GrindDone --> Brewing : Press Brewing
    Brewing --> Done : wait 5s
    Brewing --> Error : LowWaterLevel
    Error --> Idle : Reset
    Done --> [*]
@enduml
```