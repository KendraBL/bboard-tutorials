# NeoPixel Ranges


## Introduction @unplugged

In this tutorial you will learn how to create ranges for NeoPixel Strips. When working with long strips of NeoPixels it can be useful to chunk them into ranges and apply independent colours and animations to them. The range allows to create a new NeoPixel strip instance over a subset of the pixels. 


## Step 1: Connect the NeoPixel Strip to the b.board and Initialize the strip.

Following the steps in the Introduction to NeoPixel's tutorial, connect your strip of NeoPixels to the b.board. Initalize the NeoPixel's by placing the ``||Neopixel: setStrip||`` block in the ``||Basic: onStart||`` block, enter the number of Neopixel's in the strip and select the corresponding RGB format. 

```blocks
let strip: neopixel.Strip = null
strip = neopixel.create(DigitalPin.P2, 30, NeoPixelMode.RGB)
```

## Step 2: Define Neopixel Ranges

To define the Neopixel ranges drag the ``||Neopixel: stripRange||`` block from the Neopixel dashboard and place it under the ``||Neopixel: setStrip||`` block. Rename the variable Range to Head. Define the range of pixels from 0 to 9 (the first 10 neopixels).

```blocks
let range: neopixel.Strip = null
let strip: neopixel.Strip = null
strip = neopixel.create(DigitalPin.P2, 30, NeoPixelMode.RGB)
range = strip.range(0, 4)
```
Repeat two more times. Rename variable Range to Middle and Tail. Define the range of pixels from 10 to 19 (the next 10 neopixels) and 20-29 (the last 10 neopixels) respectively.

```blocks
let Tail: neopixel.Strip = null
let Middle: neopixel.Strip = null
let Head: neopixel.Strip = null
let strip: neopixel.Strip = null
strip = neopixel.create(DigitalPin.P2, 30, NeoPixelMode.RGB)
Head = strip.range(0, 9)
Middle = strip.range(10, 19)
Tail = strip.range(20, 29)
```

## Step 3: Set the Colour of the Ranges

To set the colour within the three ranges, drag the ``||Neopixel: showColor||`` block from the Neopixel dashboard into the ``||Basic: forever||`` block. Change the strip variable name and select a colour. Repeat for each range.

```blocks
basic.forever(function () {
    Head.showColor(neopixel.colors(NeoPixelColors.Purple))
    Middle.showColor(neopixel.colors(NeoPixelColors.Yellow))
    Tail.showColor(neopixel.colors(NeoPixelColors.Green))
})
```

## Step 4: Flash the Microbit with the .hex file

Give the .hex file a name. Click ``|Download|`` to transfer (flash) your code to the Microbit. Disconnect the Microbit from the USB cable once it is done transfering. Click the Microbit into the b.board. Plug in the 4-AA battery pack and turn the b.board on using the power switch. The NeoPixels should now light up in three different colors of 10 neopixels each.


