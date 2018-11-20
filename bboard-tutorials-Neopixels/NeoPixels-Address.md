# Addressing Individual NeoPixels

## Introduction @unplugged

In this tutorial you will learn how address individual Neopixels to show a specific colour on a specific Neopixel. Once you are done coding, don't forget to run your code in the simulator or the b.board.

## Step 1: Connect the NeoPixel Strip to the b.board and Initialize the strip.

Following the steps in the Introduction to NeoPixel's tutorial, connect your strip of NeoPixels to the b.board. Initalize the NeoPixel's by placing the ``||Neopixel: setStrip||`` block in the ``||Basic.onStart||`` block, enter the number of Neopixel's in the strip and select the corresponding RGB format. 

```blocks
let strip: neopixel.Strip = null
strip = neopixel.create(DigitalPin.P2, 30, NeoPixelMode.RGB)
```

Set the colour of the Neopixel strip. 

```blocks
basic.forever(function(){
    strip.showColor(neopixel.colors(NeoPixelColors.Purple))
})
```

## Step 2: Code the NeoPixel Strip

In this example, we will code the NeoPixel strip to display the colour purple as a primary colour and will individually address six Neopixels to display orange every five pixels. 

Code the NeoPixel Strip on the b.board to display a singular colour from the drop down menu. 
Select the ``||Neopixel: setColor||``from the NeoPixel dashboard and place it in the ``||basic.forever||`` block and set the colour to purple.

```blocks
basic.forever(function(){
    strip.showColor(neopixel.colors(NeoPixelColors.Purple))
})
```
## Step 3: Code the NeoPixel Strip to Display Individually Addressed Colours

To address individual NeoPixels it is important to note that their address (or location) beings at 0. If you have a strip of 30 Neopixels, the addresses will range between 0-29. 

To code individual Neopixels, select the ``||Neopixel: setPixelColor||`` from the Neopixel dashboard and place it in the ``||Basic.forever||`` block under the ``||Neopixel: showColor||`` block. Set the first Neopixel address to 4 and colour to orange. Repeat six times. 

```blocks
basic.forever(function () {
    strip.showColor(neopixel.colors(NeoPixelColors.Purple))
    strip.setPixelColor(4, neopixel.colors(NeoPixelColors.Orange))
    strip.setPixelColor(9, neopixel.colors(NeoPixelColors.Orange))
    strip.setPixelColor(14, neopixel.colors(NeoPixelColors.Orange))
    strip.setPixelColor(19, neopixel.colors(NeoPixelColors.Orange))
    strip.setPixelColor(24, neopixel.colors(NeoPixelColors.Orange))
    strip.setPixelColor(29, neopixel.colors(NeoPixelColors.Orange))
    strip.show()
})
```

Once you have added the blocks addressing the six individual Neopixels, we need to tell the Neopixel strip to show the colours. Select the ``||Neopixel: stripShow||`` block from the Neopixel dashboard and place it at the end of the code block inside the ``||Basic.forever||`` block. 

## Step 4: Flash the Microbit with the .hex file

Give the .hex file a name. Click ``|Download|`` to transfer (flash) your code to the Microbit. Disconnect the Microbit from the USB cable once it is done transfering. Click the Microbit into the b.board. Plug in the 4-AA battery pack and turn the b.board on using the power switch. The NeoPixels should now light up in your chosen colour and pattern.

## Challenge

Can you create your own pattern on the Neopixel strip by individually addressing NeoPixels?


## 
Excellent, you're ready to continue onto the next NeoPixel tutorial!
