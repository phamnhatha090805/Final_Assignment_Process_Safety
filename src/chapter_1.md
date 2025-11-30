# Chapter 1: Making coffee process
```plantuml
@startuml
    [*] --> Idle
    Idle --> StartCoffee : Get off bed
    StartCoffee --> HeatingWater : Press hot water
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