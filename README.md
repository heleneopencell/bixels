# bixels
 
This document will show you how to visualize fluorescent proteins. They are widely used in biology as a research aid. In standard bio-labs you would use a transilluminator or platereader to visualize them which are wildly expensive. We will make a simple and very low-cost version of this which can be also used as a 8x8 biodisplay or as a STEAM education kit to get kids excited about biotechnology.  

[More info](https://www.bixels.io/tutorials)

### 1)Electronic parts
### 2)[Cardboard box](https://github.com/heleneopencell/bixels#2cardboard-box-1)
### 3)Assembly
### 4)Software
### 5)Timelapse with webcam
### 6)GFP - Green fluorescent proteins

### Overview Materials  

| Electronic Parts  | Supplier EU  | Supplier US  |
|-------------------|--------------|--------------|
| 1x Neopixel Matrix |[RS Components](https://uk.rs-online.com/web/p/led-evaluation-kits/1245498/) | [Adafruit](https://www.adafruit.com/product/1487) |
| 1x Adafruit Feather 32u4 | [RS Component](http://tiny.cc/xpbmez) | [Adafruit](https://www.adafruit.com/product/2829) |
| 1x USB Micro B-Breakout   | [Amazon](http://tiny.cc/k0bmez) | [Adafruit](https://www.adafruit.com/product/1833) |
| 1x Jumper wire female/female | [RS Components](https://uk.rs-online.com/web/p/breadboard-jumper-wire-kits/7916450/) | [Adafruit](https://www.adafruit.com/product/1951)|
| 1x Jumper wire female/male | [RS Components](https://uk.rs-online.com/web/p/breadboard-jumper-wire-kits/7916454/) | [Adafruit](https://www.adafruit.com/product/1953)|

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
  

##### Overview
A fluorescent protein is a type of fluorescent chemical compound (fluorophore) that can re-emit light upon light excitation. If one colour of light lands on a fluorescent protein, the protein will glow with a different colour.

The story of the extraction, isolation and study of **green fluorescent protein (GFP)** is fascinating. It is also a hugely significant scientific discovery for which the 2008 Nobel Prize in Chemistry was awarded.

In this tutorial we will build a cardboard box to block out any unwanted light and use a set of optical filters. The filters allow the correct light to reach the fluorescent proteins from the LEDs and for the correct light to reach your eye from the fluorescent proteins. The diffuser simply diffuses the light evenly which is not necessary but useful if you want to use Bixels for something else than PCR tubes, for example electrophoresis gels. 

The RGB LED matrix we are using is capable of generating the required light to stimulate fluorescence in many types of fluorescent proteins. The filters described in this tutorial are only suitable for GFP but you can exchange them. [You can learn more here](https://www.biotek.com/assets/tech_resources/Filter%20Combinations.pdf) which filters to use for which fluorescent protein.

The software and app allow you to control each single led and it's individual light color from your phone. 

Proteins can take up to a few hours to get expressed. We therefore added a section how to add a webcam to Bixels which takes every few minutes a picture which will create a timelapse streamed to the web. 

_____________________

### 1)Electronic parts
We will be using off-the-shelf electronics from adafruit for this project. Adafruit is super user friendly, fantastic for quick DIY projects and has a huge community to reach out for help and inspiration.
We will be using their [Adafruit Feather 32u4](https://www.adafruit.com/product/2829) board which is bluetooth enabled to control a [8x8 Neopixel LED matrix](https://www.adafruit.com/product/1487) with our phone. To power bixels we will add a [micro USB breakout](https://www.adafruit.com/product/1833). This enables you to power bixels with a power bank, your laptop or with a wall plug.

![electronic circuit](/picturesreadme/image7.jpg)
  

To start with we have to solder the stacking headers on the Adafruit Feather and Neopixel Matrix. I recommend using the headers rather than soldering the cables directly on the board. The headers will allows you to be much for flexible and enable you to expand your project at a later stage with useful sensors such as humdity and temperature. For the ones that are new to soldering, check out this usefull [guide to excellent soldering](https://learn.adafruit.com/adafruit-guide-excellent-soldering).
 

![soldering bluefruit](/picturesreadme/image11.jpg)

![soldering neopixel](/picturesreadme/image12.jpg)  

To power bixels we will add a micro usb port. Take a black or brown "female to female" jumper wire an cut it in half. Connect the wire end with each other and solder it on the GND pin on the USB Micro B-Breakout board. Now take a red "female to female" jumper wire an cut it in half. Connect the wire end with each other and solder it on the 5V pin on the USB Micro B-Breakout board. We will use one black and one red cable to power the LEDs and one black and one red one to power the board itself.  
  
![soldering microusb](/picturesreadme/image17.png)


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
 
###### Folding the boxes
Bixels is made of 3 parts. The main box for the electronics, the filterbox to turn it into a transilluminator and our PCR matrix to hold your PCR strips in place.

First we have to mount the USB breakout board on the main box with the two M2 screws and nuts. Now let's **fold the main box** for the electronics: The inner box will be used as a platform for your led-display.  
[![fold mainbox](https://uploads-ssl.webflow.com/5beda5244920652be0723efa/5da7201874d4ca4d1c8be2a2_video1.jpg)](https://vimeo.com/259026890)

 
Now let’s **fold the filter box**: Glue the orange filter from on top of the cut-out. We have made two designs for this:  

**Smaller round cut-out:** The benefit here is that less natural light gets in the box which improves the performance. This is particular useful if are planning to use it with a camera. Which I will explain in more detail in [chapter 4](chapter 4).  
[Watch video here](https://vimeo.com/236662100l)


**Larger cut-out:** This works better if you want to turn it into a bio-display. You can do fun things such as building your own bio-gameboy with it. Downside is that it works best in the dark because it lets more natural light in. You can also improve this by using 2 blue flights on top of each other.  
[Watch video here](https://vimeo.com/259029617)

Let's **fold the PCR matrix:**  
The PCR matrix is designed to fit with PCR strips which will place each PCR tube right on top of an LED. Fill the matrix when you are ready to make your experiment to ensure they are sterile.
It is a simple matrix which can be connected without the use of any glue.  
[Watch how here](https://vimeo.com/259033478)

### 3)Assembly
### 4)Software
### 5)Timelapse with webcam
### 6)GFP - Green fluorescent proteins
What is a Fluorescent Protein?




