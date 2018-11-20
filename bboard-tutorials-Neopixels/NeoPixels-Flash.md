# Flashing NeoPixels

## Introduction @unplugged

In this tutorial you will learn how to make a strip of NeoPixels flash, or blink, on and off.

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

## Step 2: Programming the Neopixel Strip to Flash 

To make the Neopixels flash we will add  four more blocks to create the flash cycle. First, add the ``||Basic.pause||`` block and set the time interval to 1000ms. Then add the ``||Neopixel.clear||`` and ``||Neopixel.show||`` blocks. Last add in another ``||Basic.pause||`` block and set the interval to 1000ms. 

```blocks
basic.forever(function(){
    strip.showColor(neopixel.colors(NeoPixelColors.Purple))
    basic.pause(1000)
    strip.clear()
    strip.show()
    basic.pause(1000)
})
```

This will program the Neopixels to flash on and off in a 1 second (1000ms) interval.

## Step 3: Flash the Microbit with the .hex file

Give the .hex file a name. Click ``|Download|`` to transfer (flash) your code to the Microbit. Disconnect the Microbit from the USB cable once it is done transfering. Click the Microbit into the b.board. Plug in the 4-AA battery pack and turn the b.board on using the power switch. The NeoPixels should now light up in your chosen colour and flash on and off.

## Step 4: Changing the Flash Rate

To change the flash rate, experiment with different time intervals in the ``||Basic.pause||`` block.

## Challenge

Can you make the NeoPixel strip flash between two different colours?

## Challenge Solution (Example)

To make the NeoPixel strip flash different colours we need to adjust the code in Step 2 slightly. 

```blocks
basic.forever(function(){
    strip.showColor(neopixel.colors(NeoPixelColors.Purple))
    basic.pause(1000)
    strip.showColor(neppixel.colors(NeoPixelColors.Yellow))
    strip.show()
    basic.pause(1000)
})
```
## 
Excellent, you're ready to continue onto the next NeoPixel tutorial!
