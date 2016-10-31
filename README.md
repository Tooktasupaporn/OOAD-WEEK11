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
