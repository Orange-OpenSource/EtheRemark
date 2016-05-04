EtheRemark
==========

This project is an adaptation of the project [EtherPlant](http://github.com/Orange-OpenSource/EtherPlant) to view etherpad as slides made with [remark.js](https://github.com/gnab/remark)

No more Powerpoint (or (Libre|Open)Office Impress) file to make slides, just use Remark! Add collaborative work (ideal for a debriefing) with Etherpad and you have the best way to make cool slides with EtheRemark.

### Use

You can test it here:

http://orange-opensource.github.io/EtheRemark/src/index.html

Add "?" and a link to a pad in the end of the url, like:

http://orange-opensource.github.io/EtheRemark/src/index.html?https://pad.okfn.org/p/etheremark

#### Install

Just serve the files in the folder **src** via an HTTP server.

### Some tricks with the remark viewer

I had some features on the remark viewer:
- Image resize : you can force image width with classes .width-200, .width-190 ... .width-100, .width-90 ... .width-10
```
.width-10[.center[![test](http://www.plantuml.com/plantuml/png/SyfFKj2rKt3CoKnELR1Io4ZDoSa70000)]]
```
- Auto scale image : you can use the class .autoScale fit a image on a slide :
```
.autoScale[.center[![test](http://www.plantuml.com/plantuml/png/LO_D2i8m48JlUOfXJohqeC6VKr_1WzwAXw0R3DGApIhuzcxIqZPB84lcczt9QhD6LTK87dHvlnXNZaAG9tV684cDz1--WTnTmZV83rjIGK-oZ2IqTCZCM8ABS5OLRYDd8F5dnNl8l0EvgfQz50FsbAN9dACizCEeTu_WpNoRR4Z1wyOxxPV1TpduW1fdft-tBagPgTnr93FcA9vFDCpw0m00)]]
```
- Include PlantUML diagrams : you can add diagrams in your slide by insert PlantUML code between @startuml....@enduml tags :
```
@startuml
Alice -> Bob: Authentication Request

alt successful case

    Bob -> Alice: Authentication Accepted
    
else some kind of failure

    Bob -> Alice: Authentication Failure
    group My own label
            Alice -> Log : Log attack start
        loop 1000 times
            Alice -> Bob: DNS Attack
        end
            Alice -> Log : Log attack end
    end
    
else Another type of failure

   Bob -> Alice: Please repeat
   
end
@enduml
```

#### Warning

The code is not big, but was made in a few hours, so it's not good to look at... Feel free to submit patches.

