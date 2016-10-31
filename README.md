# OOAD-WEEK11
State Diagram

![] (http://www.plantuml.com/plantuml/img/SoWkIImgAStDuOhMYbNGBTArKqZEpoqeBKajKh1IA2ajoilFuuABWENByukoC_FIkQ2qWYvG3AJPIg4uexH48IM_F8-Boo4rBmLeAW00)

@startuml
[*] -r-> computer : turnon
computer -r-> working
working --> [*] : shut down

@enduml

![](http://www.plantuml.com/plantuml/img/SoWkIImgAStDuOhMYbNGBTArKqXEp4vLu0AH46v-VdPcNhg2bGAGB4fDoKpDAodcWedg0bM0T5ef5ASMbQLoSJcavgK0ZGC0)

@startuml
[*] -r-> cake 
cake-r-> cooking : ingredients
cooking --> [*] : serve

@enduml

![](http://www.plantuml.com/plantuml/img/SoWkIImgAStDuUAArefLq2tIjLCepym3YfQaAbWfvAMMAwGdvgPomSJ02dBoYujXAe3iL2w4W6uEgW509h8iK19aZLLgNWhOM2u780jeEm00)

@startuml

[*] -r-> winstate : new game
winstate-r-> lossstate : lose
lossstate -l-> winstate : win
lossstate --> [*] :endgame

@enduml

![](http://www.plantuml.com/plantuml/img/POun2WCn30HxlK9rm1z8STm_GWeZBOc9ppva-I2_ZsCuKgHRsDbbrkRHl6-Pw7QvSx2miCNKe7nb50szmNYtAe0szihoXBngTpgvkPc4QYgFFRut51_pCoayfjmCWdH0wH-U5nAB8EVnIByOHl4L8rg7pV3y0000)

@startuml

[*] -r-> raised : end-user proceeds to checkout
 raised -r-> proceddingpayment : payment detailsreceived
 proceddingpayment-r-> cancelled 
cancelled --> [*] 

@enduml

![](http://www.plantuml.com/plantuml/img/PP312eCm44Jl-nLxwg4WtdieGli1WiVIGvgic1Ap4ZS8VdtJM0lgTMVcpJBLA2f8x1s85KUekMs9i5Uwivu07kSd5bUK6FplnXuHONkueE6o8oKuAQ402wLcKpkboIpw4BWV15iE-0equMXdsd6mCAbiduQllKdkXXnfMNdAlEEO6mDob24AdZBvK9-fUqYctj9BZeGIySwbDOwEPV_qQjucYwIcbG0gyYOD-G40)

@startuml
title coffee machine

[*] -> turnmachineon   
turnmachineon : do/heat water
coffeePodPlaced : do/prompt for brew size
turnmachineon  -d-> coffeePodPlaced 
brewSizeSelected : do/adjust watr output & brew
coffeePodPlaced -d-> brewSizeSelected
brewComplete : Do/idle
brewSizeSelected -d-> brewComplete
brewComplete --> [*]

@enduml

activity diagram

![](http://www.plantuml.com/plantuml/img/SoWkIImgAStDuTBGqbJGrRLJKChCAqujAb58pi_CK-82YaH7vfSg92VcAIHdv1UdAgGKPUPbboUMf1R5AYWLP2Pd8uc0rIi0JU9oICrB0PeA0000)

@startuml
(*) --> "insert coin"
-->[You can chose drinkwater] "pick drinkwater"
--> (*)
@enduml

![](http://www.plantuml.com/plantuml/img/FOr12iCm30JlUiMYKrl85q8kVKN8mRHIOd2KOCl_hmAXfrrsM6PgdghtlT3ZzSGmZE2IzfE9ie8jhvipV1CZN7JsscK1Uw-6mvYaDBdGE6kA-aUgV3_Uzissugp7HrfR41wIs9IcY33_0000)

@startuml
(*) --> "lamp"

if "night" then
  -->[true] "turn on"
else
  ->[false] "turn off"
  -->[Ending process] (*)
endif
@enduml

![](http://www.plantuml.com/plantuml/img/NOvB2iCm34JtEeNGfX_85K8sFKN8mjXoQuZj82aDlNqLkkjgXk4nl4ajYErrXUlzXiCm8WMh150oqXPKZou9YsBi8XoDq5xS04zqDjbvGVATovknziOV0bwLJs2SS_3gGEhjOlY7_IuUBPNsn4rwPDK5tGBOjmoJXtjz0G00)

@startuml
(*) --> "atm"

if "password is correct" then
  -->[true] "receive money"
else
  ->[false] "don't receive money"
  -->[Ending process] (*)
endif
@enduml

![](http://www.plantuml.com/plantuml/img/JOvB2iCm34JtEiMWJJ-GAuHiUegGXKdaDjIrZEMqrwzCDrsD6DuJCraBjHslHEVh1SCmWZVLUZAOl2L3KWycsYEuI3ND-8JqH0dMm6WFoOGkpgqUie2rkEOr-XycIIOT6ESO_7HWJMhoH_piMzxsV4UfkehP0fz3ubsaoSC7VW40)
@startuml
(*) --> "door's seven eleven"

if "person walk past " then
  -->[true] "open the door"
else
  ->[false] "close the door"
  -->[Ending process] (*)
endif
@enduml

![](http://www.plantuml.com/plantuml/img/NOun3eCm34Ltd-BBIsabhe1OUWgK8GA7HgAXSapFNwTiJBRUV_hsM2sg7U-DkiSTVJ-0vwXCb1Fudo722HZsaa9epcHwI00lch-vhAV195kL9WnJYhw6LbLkXejsLZpBqjX7zrbg3V3p9CuIZJxyeHy0)

@startuml
(*) --> "car"

if "start a car " then
  -->[true] "driving a car"
else
  ->[false] "can't driving a car"
  -->[Ending process] (*)
endif
@enduml
