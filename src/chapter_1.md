# Chapter 1: Making coffee process
```plantuml
@startuml
    [*] --> Idle
    Idle --> HeatingWater : Get off bed
    HeatingWater --> Grinding : WaterHot
    Grinding --> Brewing : BeansGround
    Brewing --> Done : BrewComplete
    Brewing --> Error : LowWaterLevel
    Error --> Idle : Reset
    Done --> [*]
@enduml
```