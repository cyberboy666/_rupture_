# \_rupture\_

### simple analog video glitch circuit - adapted from a karl klomp design

![image](https://user-images.githubusercontent.com/12017938/155052362-16561705-3511-47c2-86ef-be1389ea9c0f.png)

- this circuit is distributed by __UNDERSCORES__ - _an open video hardware label_ : it is available to purchase - as a pcb, kit or assembled unit - at [underscores.shop](https://underscores.shop/_rupture_/)
- the schematic for the circuit can be found [here](/hardware/schematic.pdf)
- the pcb gerber files for the lastest version can be found [here](/hardware/gerber_latest.zip)
- interactive BOM is [here](https://htmlpreview.github.io/?https://github.com/cyberboy666/_rupture_/blob/main/hardware/bom/ibom.html)
- consider [donating](https://opencollective.com/underscores) to the underscores project to help us continue creating for the commons
## description

this circuit takes any composite video signal as input and destroys the signal in many interesting and unpredictable ways - due to the nature of analog video glitches for best results you should output this signal directly to a crt tv.

## demo video

[![image](https://user-images.githubusercontent.com/12017938/156677846-15a28025-9c6a-4628-a28b-1f68a9dce7b4.png)](https://videos.scanlines.xyz/w/6zXGHYLE1xnu9w47Xd3Zn1)

## background

<details><summary>background</summary>
  
this project is an adaption of a video glitch processing circuit created orginally by [Karl Klomp](https://www.karlklomp.nl/) known as __the rupter__. this and many other interesting historic video hardware glitch machines can be seen on [web-archive](https://web.archive.org/web/20150206171254/https://www.karlklomp.nl/) of their site. pictures, schematic and videos of the original circuit are below:
  
[![image](https://user-images.githubusercontent.com/12017938/97462093-add4c000-193e-11eb-9234-b89c1700fb6e.png)](https://vimeo.com/13738566)


![image](https://user-images.githubusercontent.com/12017938/97461494-1b342100-193e-11eb-9746-ab868f613323.png)

![image](https://user-images.githubusercontent.com/12017938/97461894-79610400-193e-11eb-89d4-a3764f4bab7b.png)

![image](https://user-images.githubusercontent.com/12017938/97349019-3ac04080-188f-11eb-9a8b-2f2abbbc492c.png)

my adaption of it started as an exercise in my [_intro to kicad_](https://github.com/cyberboy666/kicad_video_workshop) workshop for VIDICON_2020 - i ended up getting the boards fab'd and found it to be a very useful device in my studio - worthy of sharing futher!
  
</details>

# documentation

this project is fully _open-source hardware_ - all the files required to build it are included in this repo for free. if you have the time and/or skill you can contribute back by collaborating on / testing new designs, improving these docs, making demo videos/other creative content etc. you can also support the project financially by [donating directing](https://opencollective.com/underscores), or purchasing through the [web shop](https://underscores.shop).

depending on whether you are going fully diy or buying an assembled and tested unit, some of the following guides will be relavent to you. the flow would be:

## ordering parts

<details><summary><b>parts sourcing guide (w/ notes on pcb fabracation )</b> - start here if you are building fully from scatch or have purchased a pcb</summary>

i try to source all the parts i can from either:
- [tayda](https://www.taydaelectronics.com/) ; cheaper for common parts like resistors etc, also good for mechanical parts like switches and buttons
- [mouser](https://www.mouser.de/) ; has lots more options, speciality video ic's, can sometimes cost more (free shipping on orders over 50euros)
- other ; ocationally there will be parts which will need to be sourced elsewhere - usaully either aliexpress, ebay or amazon etc...

take a look at the [full_bom](/hardware/bom/full_bom.csv) for this project to see where i am sourcing each part from

## omitting parting
  
if you know you will only power _rupture_ with a 5v supply then the __regulator__ part of the circuit (c7, c8, r1, r2, u1, sw9) can be omitted - just connect the middle and left pins on the sw9 footprint with a resistor leg to permanently select 5v power by-pass.
  
also the values of capicitors on the glitch switches (c1-6) can be customised - i find smaller values are more interesting than larger ones.
  
## import into tayda

- go to the [tayda quick order](https://www.taydaelectronics.com/quick-order/) and in bottom corner choose _add from file_
- select the file [tayda_bom.csv](./hardware/bom/tayda_bom.csv) in the BOM folder (you will have to download it first or clone this repo)
- after importing select _add to cart_
- __NOTE:__ the minimum value for resistors is 10, so you may need to modify these values to add to cart (or if they are already modified here you will need to see the  full_bom for actual part QTY) 

- OPTIONAL: it is a good idea to add some dip-ic sockets and 2.54pin headers/sockets to your tayda order if you dont have them around already
  
## import into mouser

- go to [mouser bom tool](https://nz.mouser.com/Bom/) and click _upload spreadsheet_
- select the file [mouser_bom.csv](./hardware/bom/mouser_bom.csv) in this folder (you will have to download it first or clone this repo), then _upload my spreadsheet_ and _next_
- ensure that __Mouser Part Number__ is selected in the dropdown above the first row, then _next_, _process_
- if everything looks correct can now put _add to basket_

# ordering pcbs

you can support this project by buying individual pcbs from the [shop](https://underscores.shop). if you would rather have pcbs fabricated from gerbers directly the file you need is [here](/hardware/gerber_latest.zip) 

- i get my pcbs fabricated from [jlcpcb](https://cart.jlcpcb.com/quote) - 5 is the minumum order per design
- upload the zip file with the `add gerber file` button
- the default settings are mostly fine - set the __PCB Qty__ and __PCB Color__ settings (you can check that the file looks correct with pcb veiwer)
- it may be best to combine orders with other pcbs you want to have fab'd since the shipping can cost more than the items - also orginising group buys is a good way to distribute the extra pcbs /costs 
  
i often use jlcpcb because they are reliable, cheap and give you an option of colours. remember though that the cheapest Chinese fab houses are not always the most ethical or environmently friendly - if you can afford it consider supporting local companies. 

</details>

## assembly guide

<details><summary><b>assembly guide</b> - start here if you have purchased a diy kit</summary>
  

## interactive BOM for build guiding

follow this link to view the [interactive BOM](https://htmlpreview.github.io/?https://github.com/cyberboy666/_rupture_/blob/main/hardware/bom/ibom.html)

## general solder advices

- remember to heat pad first (2-3seconds), then add solder, then continue to heat (1-2seconds)

- Checkout the web-comic [soldering is easy](https://mightyohm.com/files/soldercomic/FullSolderComic_EN.pdf) for more soldering advice

## general order of assembly

- in general while assembling i start placing resistors and capacitors first. placing 5 - 10 components at a time and then flipping the board to solder them and trim the legs etc.
- next i would do diodes, transistors and ic's - taking care that these are placed in the right direction (using a ic socket can be useful)
- finally i place the interface parts - rca jacks, power jack, pots and switches - make sure these have lots of solder on for structural stablity

## specific assembly advice

- start with the ic if you going for smd part - remember to orient it correctly (follow arrow on silkscreen) - can check connection with multimeter by using the dip pads
- next place resistors and capicators - can also do regulator...
- now place the switches - make sure enough solder is on the outer pins for structural stability
- barrel and rca jacks next
- and finally the pots
  
</details>
  
## operating guide
  
<details><summary><b>operating guide</b> - start here if you have purchased an assembled unit</summary>

![image](https://user-images.githubusercontent.com/12017938/156061444-3c6de3a7-d6e1-41e5-bc37-5e18eaab0bf1.png)

### setup
  
start by connecting a composite video source to the IN rca jack and a composite video display to the OUT rca jack (use a crt tv for best results) - now without the power plugged in you should be able to see your clean video source on the display by changing the ROUTER switches to both UP or both DOWN
  
### router
  
the video input and video output signals can be connected to the effect circuit in 4 different ways - this is because the left router switch will connect the IN signal to the TOP/BOTTOM of the effect circuit, and the right router switch will connect the OUT signal to the TOP/BOTTOM - without power TOP-TOP and BOTTOM-BOTTOM acts as straight signal pass-through. with power these will give different effects.
  
### regulator
  
the REGULATOR switch next to the power jack selects whether the power line is passed through a ~7v voltage regulator -> if you are powering your circuit with 9-12v then you must have this switched on (RIGHT) to avoid damaging your ic. if you are powering with 5v then it can be bypassed by switching to the left, although it wont hurt to still have it on - just changes the effects slightly in some places.
  
### glitch controls
  
the 4 knobs and 6 switches will control the glitch effects when the power is connected. the default position is all knobs rotated anti-clockwise and all glitch switches set to UP. in general i would start by moving the left most knob first and working towards the right most - same with the glitch switches.
  
ROUTER positions UP-UP, DOWN-DOWN and DOWN-UP all produce quite interesting and different glitches on a crt screen. UP-DOWN for the most part does little more than a few abstract lines.
  
</details>

### more info

<details><summary><b>how the circuit works</b></summary>
  
[coming soon]
                                                                                                                             
</details>

<details><summary><b>contributing guide</b></summary>
  
if you would like to contribute back to these projects in some way but dont know how the best thing (for now) would be to reach out to me directly ( tim@cyberboy666.com or @cyberboy666 on scanlines forum) - i will be happy to help
  
</details>


## credits & more info


This circuit is distributed through UNDERSCORES – open video hardware label – visit [underscores.shop](https://underscores.shop) for more info

The pcb was designed using KICAD

Everything from gerbers, cad files, panels and documentation is freely available online and distributed under CC-BY-SA / open-source licenses – help us contribute to the commons !

Ask any questions or start discussions related to this project on the [scanlines.xyz](https://scanlines.xyz) forum – an online community space dedicated to diy av / electronic media art

You can contact me directly at tim (at) cyberboy666 (dot) com 
Please get in touch if you are interested in hosting a workshop !

![image](https://user-images.githubusercontent.com/12017938/156065418-201cd215-828a-4883-a828-2e82401d451e.png)


thanks to Karl Klomp for inpiring me and so many others, to Bastien Lavaud for circuit advice, always. To Ben Caldwell for project advice. To everyone who has or will contribute ♥♥♥

