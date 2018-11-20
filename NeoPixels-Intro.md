# Introduction to NeoPixels

## Introduction @unplugged

In this tutorial you will learn how to connect a NeoPixel strip with alligator clips to the b.board and program it to display a solid colour. Once you are done coding, don't forget to run your code in the simulator or the @boardname@.

## Step 1: Connect the NeoPixel Strip to the b.board

Using the alligator clips on your NeoPixel Strip, connect each clip to the corresponding gator gripper on the b.board. For NeoPixels, you can use the 3V power, pin, and ground gator gripper P5 or P2 to power the NeoPixel Strip . Connect the Red alligator clip to the 3V gripper, the Black alligator clip to the ground gripper and the While alligator clip to the centre pin gripper.


## Step 2: Initialize the NeoPixel Strip

To program the NeoPixels we need to initialize the light strip on start. Remember to select the correct Pin (P2 or P5) that the NeoPixels are connected to. Select the ''||let strip: neopixel.Strip = null||'' block from the NeoPixels dashboard. Enter the number of NeoPixels on the Strip. Select the corresponding RGB format according to your NeoPixel Strip specifications. In this example, the NeoPixel strip is on P2, with 30 NeoPixels, in RGB (GRB) format.  

'''blocks
let strip: neopixel.Strip = null
strip = neopixel.create(DigitalPin.P2, 30, NeoPixelMode.RGB)
'''

## Step 3: Code the NeoPixel Strip

Code the NeoPixel Strip on the b.board to display a singular colour from the drop down menu. 
Select the ''||strip.showColor(neopixel.colors(NeoPixelColours.Red))||'' from the NeoPixel dashboard and place it in the ''||basic.forever||'' block.

In this example, the NeoPixel strip will display the colour purple on each NeoPixel.

'''blocks
basic.forever(function(){
    strip.showColor(neopixel.colors(NeoPixelColors.Purple))
})
'''

## Step 4: Flash the Microbit with the .hex file

Give the .hex file a name. Click ''|Download|'' to transfer (flash) your code to the Microbit. Disconnect the Microbit from the USB cable once it is done transfering. Click the Microbit into the b.board. Plug in the 4-AA battery pack and turn the b.board on using the power switch. The NeoPixels should now light up in your chosen colour. 

## 
Excellent, you're ready to continue onto the next NeoPixel tutorial!
