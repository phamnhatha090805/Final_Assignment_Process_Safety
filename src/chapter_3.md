# Chapter 3: Task communication

```plantuml
@startuml
participant CoffeeMaking
participant GVL
participant ToastMaking

CoffeeMaking -> GVL: CoffeeState = HeatingWater
GVL -> ToastMaking: CoffeeState = 1
ToastMaking -> GVL: ToastState = LoadingBread
ToastMaking -> GVL: ToastState = LeverDown

GVL -> CoffeeMaking: ToastState = 1 or 2

CoffeeMaking -> GVL: WaterHot = true
CoffeeMaking -> GVL: GrindingDone = true
CoffeeMaking -> GVL: BrewingDone = true
ToastMaking -> GVL: ToastState = ToastReady
CoffeeMaking -> GVL: CoffeeState = CoffeeReady
@enduml
```