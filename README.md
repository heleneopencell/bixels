# bixels
 
This document will show you how to visualize fluorescent proteins with a simple DIT transilluminator / plate reader. Fluorescent proteins are widely used in biology as a research aid. In standard bio-labs you would use a transilluminator or platereader to visualize them which are wildly expensive. We will make a simple and very low-cost version of this which can be also used as a 8x8 biodisplay or as a STEAM education kit to get kids excited about biotechnology.  

[More info](https://www.bixels.io/tutorials)

### 1)[Electronic parts](https://github.com/heleneopencell/bixels#1electronic-parts-1)
### 2)[Cardboard box](https://github.com/heleneopencell/bixels#2cardboard-box-1)
### 3)[Assembly](https://github.com/heleneopencell/bixels#3assembly-1)
### 4)[Software](https://github.com/heleneopencell/bixels#4software-1)
### 5)[GFP - Green fluorescent proteins](https://github.com/heleneopencell/bixels#6gfp---green-fluorescent-proteins-1)
### 6)[Run an experiment]()
### 7)[Timelapse with webcam](https://github.com/heleneopencell/bixels#5timelapse-with-webcam-1)
### 8)[Design Ideas]()
### 9)[Material list](https://github.com/heleneopencell/bixels#overview-materials)
  
  ![final project](/picturesreadme/image21.jpg)


##### Overview
A fluorescent protein is a type of fluorescent chemical compound (fluorophore) that can re-emit light upon light excitation. If one colour of light lands on a fluorescent protein, the protein will glow with a different colour.

The story of the extraction, isolation and study of **green fluorescent protein (GFP)** is fascinating. It is also a hugely significant scientific discovery for which the 2008 Nobel Prize in Chemistry was awarded.

In this tutorial we will show you how to visualize fluorescent proteinswe. We will build a cardboard box to block out any unwanted light and use a set of optical filters. The filters allow the correct light to reach the fluorescent proteins from the LEDs and for the correct light to reach your eye from the fluorescent proteins. The diffuser simply diffuses the light evenly which is not necessary but useful if you want to use Bixels for something else than PCR tubes, for example electrophoresis gels. 

The RGB LED matrix we are using is capable of generating the required light to stimulate fluorescence in many types of fluorescent proteins.  
The filters described in this tutorial are only suitable for GFP but you can exchange them.[You can learn more here](https://www.biotek.com/assets/tech_resources/Filter%20Combinations.pdf) which filters to use for which fluorescent protein.  

The software and app we will use will allow you to control each single led and it's individual light color from your phone.  

Proteins can take up to a few hours to get expressed. We therefore added a section how to add a webcam to Bixels which takes every few minutes a picture which will create a timelapse streamed to the web. 

_____________________

### 1)Electronic parts
We will be using off-the-shelf electronics from adafruit for this project. Adafruit is super user friendly, fantastic for quick DIY projects and has a huge community to reach out for help and inspiration.
We will be using their [Adafruit Feather 32u4](https://www.adafruit.com/product/2829) board which is bluetooth enabled to control a [8x8 Neopixel LED matrix](https://www.adafruit.com/product/1487) with our phone. To power bixels we will add a [micro USB breakout](https://www.adafruit.com/product/1833). This enables you to power bixels with a power bank, your laptop or with a wall plug.

![electronic circuit](/picturesreadme/image7.jpg)
  

To start with we have to solder the stacking headers on the Adafruit Feather and Neopixel Matrix. I recommend using the headers rather than soldering the cables directly on the board. The headers will allows you to be much for flexible and enable you to expand your project at a later stage with useful sensors such as humdity and temperature. For the ones that are new to soldering, check out this usefull [guide to excellent soldering](https://learn.adafruit.com/adafruit-guide-excellent-soldering).
 

![soldering bluefruit](/picturesreadme/image11.jpg)

![soldering neopixel](/picturesreadme/image12.jpg)  

To power bixels we will add a micro usb port. Take two black or brown "female to female" jumper wires and cut one end off. Connect the wire end with each other and solder it on the GND pin on the USB Micro B-Breakout board. Now take two red "female to female" jumper wire wires and cut one end off. Connect the wire end with each other and solder it on the 5V pin on the USB Micro B-Breakout board. We will use one black and one red cable to power the LEDs and one black and one red one to power the board itself.  

Note: You can also make your own wires with femaler headers but I do it the lazy way...
  
![soldering microusb](/picturesreadme/image13.jpg)


### 2)Cardboard box
Let's get started with the cover for bixels which is a simple cardboard box. I have chosen cardboard because it allows you to quickly iterate and customize the design without the need of any equipment such as a 3D printer. 

You can either lasercut your parts or print the PDF on a A3 sheet and cut it out by hand. Use a non see-through cardboard! Test it out beforehand and hold it against the light. No light should be able to get through. I use [Mountboard from Daler Rowney](https://www.amazon.co.uk/Daler-Rowney-Black-Graduate-Mountboard/dp/B00GKCF0VG/ref=sr_1_4?keywords=mount+board+black&qid=1571151582&sr=8-4) because it allows you to make neat hinges. You can also add a layer of black thin cardboard on each side if your cardboard let's any light through, use sprayglue for laminating it on top.
 
###### For the lasercut
[Download](https://github.com/heleneopencell/bixels/tree/master/lasercut) the file here. The yellow lines are for engraving the cardboard to easier fold it. The red lines are cuts. We suggest to test your two settings in a small corner beforehand.  
 
###### For cutting it by hand
[Download](https://github.com/heleneopencell/bixels/tree/master/printfiles) the files here. Print it on an A3 paper and mount it on a thicker cardboard. You don’t want anything moving. I suggest to use (removable) spray-mount for it. For the PCR matrix and it is best to use a lasercutter but it is possible to cut it by hand - a holepuncher is useful. (Just a bit fiddly)  

Note: We have made two designs for the filterbox:  

**Smaller round cut-out:** The benefit here is that less natural light gets in the box which improves the performance. This is particular useful if are planning to use it with a camera. Which I will explain in more detail in [chapter 4](chapter 4).  
**Larger cut-out:** This works better if you want to turn it into a bio-display. You can do fun things such as building your own bio-gameboy with it. Downside is that it works best in the dark because it lets more natural light in. You can also improve this by using 2 blue flights on top of each other.
![lasercut box](/picturesreadme/image15.jpg)  
  
### 3)Assembly
 
###### Folding the boxes
Bixels is made of 3 parts. The main box for the electronics, the filterbox to turn it into a transilluminator and our PCR matrix to hold your PCR strips in place.

First we have to mount the USB breakout board on the main box with the two M2 screws and nuts. Now let's **fold the main box** for the electronics: The inner box will be used as a platform for your led-display.  
  
[![fold mainbox](https://uploads-ssl.webflow.com/5beda5244920652be0723efa/5da72131bc6da772398e5004_video1.jpg)](https://vimeo.com/259026890)

 
Now let’s **fold the filter box**: Glue the orange filter from on top of the cut-out. We have made two designs for this:  

**Smaller round cut-out:** The benefit here is that less natural light gets in the box which improves the performance. This is particular useful if are planning to use it with a camera. Which I will explain in more detail in [chapter 4](chapter 4).  

**Larger cut-out:** This works better if you want to turn it into a bio-display. You can do fun things such as building your own bio-gameboy with it. Downside is that it works best in the dark because it lets more natural light in. You can also improve this by using 2 blue flights on top of each other.  
  

[![fold filterbox](https://uploads-ssl.webflow.com/5beda5244920652be0723efa/5da724359c9af571acbb3807_video2.jpg)](https://vimeo.com/259029617)

Let's **fold the PCR matrix:**  
The PCR matrix is designed to fit with PCR strips which will place each PCR tube right on top of an LED. Fill the matrix when you are ready to make your experiment to ensure they are sterile.
It is a simple matrix which can be connected without the use of any glue.  
  

[![pcr matrix](https://uploads-ssl.webflow.com/5beda5244920652be0723efa/5da724c821fdc55333798553_video3.jpg)](https://vimeo.com/259033478)  

Next let's connect all electronics. Connect one of the **red wires** from the micro usb breakout board to the **5V pin** on the Neopixel matrix and one red wire to the **USB pin** on Bluefruit feather board.
Now connect one of the **black wires** from the micro usb breakout board to the **GND pin** on the Neopixel matrix and one black wire to the **GND pin** on Bluefruit feather board. Next grab one of the female/female **jumper wires** and connect the **DIN pin** on the Neopixel matrix with **Pin6** on the Bluefruit feather board. Hide carefully the board in the little compartment and place the LED matrix on top. Connect the usb cable and we are ready to go.
  
[![assembly](https://uploads-ssl.webflow.com/5beda5244920652be0723efa/5da729025e45da16caef2aed_video4.jpg)](https://vimeo.com/259130358)  


### 4)Software  

###### Arduino set-up for Adafruit Feather 32u4 
If you haven’t done it already, download the newest [Arduino IDE version](https://www.arduino.cc/en/main/software). Next we have to set up our Bluefruit Feather Board for Arduino as described [here](https://learn.adafruit.com/adafruit-feather-32u4-bluefruit-le/setup) and install the board with the Board Manager and install the adafruit driver as described [here](https://learn.adafruit.com/adafruit-feather-32u4-bluefruit-le/setup).  

###### Uploading Arduino sketch 
Before uploading our sketch you need to install the BLE library as described [here](https://learn.adafruit.com/adafruit-feather-32u4-bluefruit-le/installing-ble-library). 
Now download the [bixel.zip](/bixel.zip), extract or unpack it and open the file bixel.ino which is inside the folder.

It’s time to upload your code onto your device. Connect the USB from your bixel to your computer and choose the correct port inside your Arduino window. Now click upload and wait till it got successfully uploaded. It should look something like this.

![choose port](/picturesreadme/image26.png)  
![upload](/picturesreadme/image27.png)  
  
###### App to control the LED's
Now let’s get started with controlling the LEDs. First download the Adafruit Bluefruit LE Connect App on your phone. The app is available for [iOS](https://apps.apple.com/gb/app/adafruit-bluefruit-le-connect/id830125974) and [Android](https://play.google.com/store/apps/details?id=com.adafruit.bluefruit.le.connect&hl=en_GB).
 
Open the app and connect to your device Adafruit Bluefruit LE.
Choose the NeoPixel icon in the bottom line and press OK when it gives you a notice.
Next we have to choose the correct matrix layout. Click the settings button at the top, next to the word ‘NeoPixel’ and choose ‘8x8’.
Press ‘Connect’ and your LED’s should turn on. Now you are ready to control your individual LEDs. 

[![assembly](https://uploads-ssl.webflow.com/5beda5244920652be0723efa/5da882917086594acd830965_appvideo.jpg)](https://vimeo.com/259016118)  

### 5)GFP - Green fluorescent proteins
We need a fluorescent protein to be able to test if our transilluminator is working! So how do we make them?

In most cases we talk and share how to programme with 0's and 1's on this platform but here we would like to share how to programme with DNA, with C G T and A's.  
At the cellular level organisms are complex. A key process is the creation of proteins based on the specific instructions contained in the base pairings of deoxyribonucleic acid (DNA). Base-pairs are composed of either cytosine (C) and guanine (G) or tyrosine (T) and adenine (A). These base pair instructions can be long, the genome of a human is ~ 3 billion base pairs (3gbp), the genome of wheat is even longer at 10 gbp. The length of DNA which encodes green fluorescent protein (a single protein, and the topic of this tutorial) is about 700 bp.  

![DNAprogramme](/picturesreadme/image3.jpg)  

A selection of DNA is transcribed when a type of protein called RNA polymerase attaches to a circuit element called a promoter (initiator of transcription), this creates a piece of RNA of length determined by the location of a terminator (stops transcription). This piece of RNA contains a ribosome-binding site to which an organelle called a ribosome adheres and begins the process of translation, where amino acid sequences are joined to form proteins. 

A piece of **DNA gives these instructions** through encoding specific operations:
![DNAprogramme](/picturesreadme/image4.png)  


* Promoter -  Facilitates RNA polymerase binding to initiate transcription
* Ribosome-binding site (RBS) - Initiation site for translation
* Gene - The part of the DNA code that is converted to the protein of interest
* Terminator - Halts transcription

###### How to Engineer Biology

Synthetic biology is an interdisciplinary branch of biology and engineering. It establishes the tools and techniques to build artificial biological systems for various applications. Some of the best materials to work with in this field are the simplest and most common - like DNA.

In order to understand DNA you can use a visualiser and a great service to use for this is [Benchling](https://www.benchling.com/). To get even more hands on and do it yourself you can review two sites that have everything you could ever need in terms of DNA parts. The first is Addgene, a non-profit set up with the goal of providing a facility for maintaining and storing DNA parts. They have a [dedicated site about fluorescent proteins](https://www.addgene.org/fluorescent-proteins/).  It is roughly £60 for an individual part. Secondly you could go to the [IGEM registry](http://parts.igem.org/Protein_coding_sequences/Reporters#Fluorescent_proteins) where a whole range of parts or “biobricks” are stored and can be requested (although you may need to be part of an IGEM team).

For Bixels we want to produce green fluorescent proteins, these  will glow with a different colour when one colour of light hits them. A wide range of coloured proteins (fluorophores) can be produced from DNA. This allows you to get creative with your combinations.   
  
![different colors](/picturesreadme/image5.png)  

Note: Bear in mind that different coloured proteins need to get excited with a different colour of light, which means you also have to adapt your filters. [Here](https://www.biotek.com/assets/tech_resources/11596/table1.jpg) a useful document about the different excitation wavelenghts for different proteins.
But first let's find out how to even make proteins. We will outline two ways here:

1) **By bacteria transformation**
This involves inserting a plasma into a chassi, for example E.Coli (bacteria) which will express proteins based on the plasmid incerted.
If you are new to genetic engineering we highly recommend you to get the [Zero to genetic engineering hero book](https://amino.bio/products/learn-genetic-engineering-the-genetic-engineering-hero-book) from Amino Labs. It will make teach you every step needed to make your own transformations. With the book you can get kits that will provide you with all materials needed to make your own fluorescent proteins. I recommend the [RGB kit](https://amino.bio/collections/everything/products/rgb-kit-activate-cells-with-light)!

2) **By using Cell-Free systems**
Which allows you to use and work with outside of the research lab. This involves removing the transcription and translation machinery from a cell. It allows you to make proteins without having to grow or work with live cells. Since Cell-Free expression liberates you from the requirements of a bio-lab you can begin to experiment to make your projects more tangible. You can get your cell-free kit to make your own fluorescent proteins at [minipcr.com](https://www.minipcr.com/product/biobits-central-dogma/).

### 6)[Run an experiment]()
Let's make your proteins shine. 

I love that the colors of the app are similar to different protein you can express. In our case we will excite a green fluorescent protein with blue light.
So let's turn your bixel into a transilluminator. The kit includes 3 filters. An amber filter, blue filter and and a diffuser.
We already mounted our amber filter into our filter box. To turn the main box into a transilluminator, layer the blue filter and diffuser on top of the LED matrix and place your PCR matrix (with GFP in 1 or more tubes) on top. Slide the filter box on top of the main box and turn the LEDs to blue. You can either excite single tubes or excite all in once.  

[![assembly](https://uploads-ssl.webflow.com/5beda5244920652be0723efa/5da8938bfdbcf63be43f4198_video8.jpg)](https://vimeo.com/236662582)  

If you look now through the orange filter you will only see your fluorescent proteins glow! I love to use either my phone to capture it or for timelapses a simple web-cam. Below a protocol ‘How to build a timelapse with a web-cam’.  

![transilluminator](/picturesreadme/image30.png)  


### 7)Timelapse with webcam
I like to use electronics and programming not only to be creative, it allows me to be lazy.
My colleague Tom wrote a tutorial how to make a cheap timelapse and webstream with a Raspberry Pi and a webcam.
The design fits great with the bixels project. [Follow the steps here.](http://designbio.co.uk/blog/raspi-timelapse)

### 8)Design Ideas
Now it's time to get creative. We have used bixels for some fun applications so far:

1) As an educational tool to teach biotechnology to non scientists
[![https://uploads-ssl.webflow.com/5beda5244920652be0723efa/5da896fe82e67520d79d7631_video6.jpg)](https://vimeo.com/212755100)  

2) Making a gameboy which has a biopixel display
![gameboy](/picturesreadme/image19.png)  

3) Playing tetris with fluorescent proteins
![gameboy](/picturesreadme/image25.gif)  

4) Test your biology experiment
![lab](/picturesreadme/image23.jpg)  



If you have any ideas you want to share please drop me a line at helene.steiner@rca.ac.uk
  

### Overview Materials  

| Electronic Parts  | Supplier EU  | Supplier US  |
|-------------------|--------------|--------------|
| 1x Neopixel Matrix |[RS Components](https://uk.rs-online.com/web/p/led-evaluation-kits/1245498/) | [Adafruit](https://www.adafruit.com/product/1487) |
| 1x Adafruit Feather 32u4 | [RS Component](http://tiny.cc/xpbmez) | [Adafruit](https://www.adafruit.com/product/2829) |
| 1x USB Micro B-Breakout   | [Amazon](http://tiny.cc/k0bmez) | [Adafruit](https://www.adafruit.com/product/1833) |
| 1x Jumper wire female/female | [RS Components](https://uk.rs-online.com/web/p/breadboard-jumper-wire-kits/7916450/) | [Adafruit](https://www.adafruit.com/product/1951)|
| 1x Micro USB Cable | [RS Components](https://uk.rs-online.com/web/p/usb-cables/8762403/) | [Adafruit](https://www.adafruit.com/product/1995)|


_____________________
  
| Filters | Supplier EU | Supplier US  |
|-------------------|--------------|--------------|
| 1x Diffuser Paper 72mm x 72mm |[Amazon](http://tiny.cc/7ecmez) | [Amazon](https://www.adafruit.com/product/1487) |
| 1x Translucent Amber Filter 72mm x 72mm | [Plastic People](https://www.theplasticpeople.co.uk/coloured-acrylic-perspex/) | [Acrylite](https://www.mcmaster.com/85635k461) |
| 1x Translucent Blue Filter 72mm x 72mm | [Plastic People](https://www.theplasticpeople.co.uk/coloured-acrylic-perspex/) | [Acrylite](https://www.mcmaster.com/85635k461) |
_____________________
  
| Cover / Box | Supplier EU  | Supplier US  |
|-------------------|--------------|--------------|
| 1x Cardboard |[Amazon](http://tiny.cc/vwdmez) | [Amazon](http://tiny.cc/xzdmez) |
| 1x Double sided tape| [Amazon](http://tiny.cc/fqdmez) | [Amazon](http://tiny.cc/jtdmez) |
| 1x Superglue | [Amazon](http://tiny.cc/9odmez) | [Amazon](http://tiny.cc/nndmez)|
| 2x M2 Hex Nut | [RS Compnent](https://uk.rs-online.com/web/p/hex-nuts/0560271/) | [Amazon](http://tiny.cc/nndmez)|
| 2x M2 Hex Screw | [RS Compnent](https://uk.rs-online.com/web/p/connector-screws-nuts/1665038/) | [Amazon](http://tiny.cc/nndmez)|

_____________________
  
| Equipment | Supplier EU  | Supplier US  |
|-------------------|--------------|--------------|
| Lasercutter or | local makerlab | local makerlab |
| Cutter | [Amazon](https://www.amazon.co.uk/Silverline-789397-Zinc-Alloy-Snap-Off-Utility/dp/B003TNYHHW/ref=sr_1_5?keywords=cutter&qid=1571219430&sr=8-5) | [Amazon](http://tiny.cc/6gdmez) |
| Mobile phone | Android or | iOS |
_____________________
  
| Software | Supplier EU  | Supplier US  |
|-------------------|--------------|--------------|
| Arduino |[Windows](https://www.arduino.cc/en/guide/windows) | [OS X](https://www.arduino.cc/en/guide/macOSX) |
| Bluefruit LE Connect | [Android](https://play.google.com/store/apps/details?id=com.adafruit.bluefruit.le.connect&hl=en_GB) | [iOS](https://apps.apple.com/gb/app/adafruit-bluefruit-le-connect/id830125974) |
_____________________
  
| Biological Parts | Supplier EU  | Supplier US  |
|-------------------|--------------|--------------|
| Fluorescent Protein Kit (RGB) |[Amino Labs](https://amino.bio/collections/everything/products/rgb-kit-activate-cells-with-light) | [Amino Labs](https://amino.bio/collections/everything/products/rgb-kit-activate-cells-with-light) |
| Mini Lab: BioExplorer™  | [Amino Labs](https://amino.bio/collections/everything/products/bioproduction-lab?variant=40528228676) | [Amino Labs](https://amino.bio/collections/everything/products/bioproduction-lab?variant=40528228676) |
_____________________





