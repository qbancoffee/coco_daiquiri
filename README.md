# coco_daiquiri
A drop in replacement board for the SC77527P DAC chip found in the Tandy CoCo's




- [How to order from JLCPCB](#Ordering-the-board)

This board replaces the functionality of the SC77527P DAC chip found in the Tandy CoCo's. 
The DAC chip is one of the custom linear integrated circuits used in the Color Computer
2 and 3. As its name implies, it contains a Digital to Analog Converter.
This chip also contains a sound multiplexer and the circuitry necessary to interface the joystick
controllers to the microprocessor.

I designed it using available parts from JLCPCB to reduce assembly time and to bring down the cost.

## Goals
- [x] Generate sound.
- [x] Route sound.
- [x] Read Joysticks.
- [x] Input analog sound.
- [x] Output sound data to save to cassette.

All goals were met!!!<br>
[Video testing the Daiquiri board with NitrOS9 and the Joey-HighRes](https://youtu.be/EgFfznWoyZE)
[Video testing most of the functions of the Daiquiri](https://youtu.be/KFkKGCwIwdY)
[Video saving a BASIC program using the Daiquiri board](https://youtu.be/1Up1ANTkjJg)
[Video testing Rev 1 of the DAC replacement board AKA the Daiquiri ](https://youtu.be/-PZM2CGa1yw)

## Layout
![Layout](images/daiquiri_layout.png?raw=true "Component layout")


## 3D rendering and pictures of it installed
![Top view](images/daiquiri_top.png?raw=true "Top view")
<br>
<br>
![Side view](images/daiquiri_side.png?raw=true "Top view")
<br>
CoCo 3 with Daiquiri chip installed
![Pepper installed](images/daiquiri_installed.jpg?raw=true "Pepper installed")
<br>

## Daiquiri and DAC
![SALT and PEPPER](images/daiquiri_and_dac.jpg?raw=true "SALT and PEPPER")


## Ordering the board
First Thing to do is clone this repository or download the latest release.
- [Download the latest release](place link here)<br>
All the files you'll need are in the gerber folder.

Many PCB manufacturers provide proprietary EDA software with nice and helpful features to help the user decrease the time and difficulty when designing a PCB. Unfortunately sometimes these programs will only allow you to order from that specific manufacturer. This is good for the manufacturer because it increases the odds that the person will order from them again because of the amount of time invested in learning to use that specific EDA program.

There are very nice EDA programs that will allow to design a PCB really quickly with fewer errors when it comes to components and footprints. Some of these programs are free to download and use for a trial period but after finishing your design sometimes you'll find that in order to export your design files so that you can actually order the boards you have to purchase a license. Sometimes you'll also find that there is a total area limit on the size of your design unless you buy a license. Companies use these tactics to make money and I really can't blame them because they have to make a living somehow.

I guess the question you might be asking is "Is there a specific PCB manufacturer I must use for a PCB designed with KiCAD?" The answer is no.
PCB manufacturers will still take your business even if you've elected to use another piece of software for your design so long as you can provide the Gerber files for your design. The Gerber format is an open ASCII vector format for printed circuit board (PCB) designs. It is the de facto standard used by PCB industry software to describe the printed circuit board images: copper layers, solder mask, legend, drill data, etc.

KiCAD has a bit of learning curve to it but once you are familiar with its quirks you'll find that having no limits on size, layers, components ect for your design is really nice and worth your investment in time. Also, being completely free, having no vendor association, and having no licensing issues  means that you can start using right it away without worries and when you're done just create the gerber files.

You can open the PCB design and create the gerber files yourself but I've already done that for the board so all you have to do is download the zip archive and upload it to your PCB manufacturer of choice. Click on the link below to download the gerber files.
<BR>
- [Download the gerber files](https://github.com/qbancoffee/coco_daiquiri/raw/main/gerber/daiquiri_gerber.zip)

There are a ton of PCB manufactures to choose from but recently I've been using [JLPCB](https://jlcpcb.com/) because the quality is good and they are well priced. JLPCB will even provide an automated online quote for pcb manufacturing and assembly. Once ordered they should arrive in the mail.
Obviously you can use any PCB manufacturer you wish.

Some manufacturers also have assembly services with costs varying based on the number of components, packaging and size of the board. 
Surface mount components are difficult to solder onto a board by hand but are perfect for automated PCB assembly making it much cheaper when it comes to using an assembly service. I chose to design these boards using surface mount components from LCSC's inventory so that JLCPCB can mostly assemble them.

To order the components you'll need a Bill Of Materials or a BOM. I've included a BOM for the board in the repo and just like the gerber files, they will be in the repo once you download it. Click on the link below to download the BOM.
<BR>
- [View BOM for the Daiquiri board](https://github.com/qbancoffee/coco_daiquiri/raw/main/color_computer_dac_1.1.0_BOM.csv)

The BOM includes LCSC part numbers so you can order them from JLCPCB, manufacturer part numbers so can search for the parts sold by other vendors, and other nice pieces of information to help you along.

To assemble the board JLCPCB will need to know the part locations and orientations, this information is in the CPL file.
- [View the CPL file](https://github.com/qbancoffee/coco_daiquiri/raw/main/color_computer_dac-all_1.1.0_POS.csv)  

- Go to jlcpcb and create an account if you don't have one.
- Click on "Quote Now" and then click on "Add Gerber File"
- Select "daiquiri_gerber.zip
- Scroll down and select "Free SMT Assembly for your PCB order"
- Select "Assemble Top side" and agree to the terms and conditions.
- Click on "Add BOM" and select "BOM.csv"
- Click on "Add CPL file" and select "salt_replacement-all-pos.csv"
- Click "Next" and go over the components and pricing.
- Click "Next" or "Save to Cart".
  
  If you like the price, order it and you should receive a mostly assembled board.
  
Beacuse they are through hole components you'll have to solder the pin headers yourself. However, I just found out that JLCPCB offers hand soldering services now so you may want to look into that.....
  
  If you don't have 2.54 mm pitch breakaway pin headers laying around you can order from many places.
  - Amazon
  - Digikey
  - Mouser
  
  Here is a set from Adafruit<br>
  [Break away male pin headers .1 inch (2.54mm) pitch](https://www.adafruit.com/product/392)
  
  




