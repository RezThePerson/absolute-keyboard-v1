# Journal (total: xHrs)

## Schematic (devboard) - 3rd Jun 2026 (1hr)

Im using the [macondo](https://macondo.hackclub.com/docs/build-a-devboard) guide for help on this!

<details>
    <summary>
        Added rp2040 and the capacitors
    </summary>
      
  ![](https://cdn.hackclub.com/019e8eaa-bff0-7f3e-a80d-8cf23a6ba875/image.png)
</details>

## Schematic (devboard) - 10rd Jun 2026 (2hrs)

<details>
    <summary>
        Added usb-c port
    </summary>
      
  ![](https://cdn.hackclub.com/019eace0-659f-78f1-918e-8d966a7a0fc2/image.png)
</details>

<details>
    <summary>
        Added crystal oscillator
    </summary>
      
  ![](https://cdn.hackclub.com/019eb271-5214-70a4-abe7-3dcdbc45795b/image.png)
</details>

i could not for the life of me find that exact crystal footprint. turns out they changed it and now pins 2 and 4 are the same in the newer one.... aghhh

<details>
    <summary>
        Added flash storage
    </summary>
      
  ![](https://cdn.hackclub.com/019eb2d3-cdc0-7a80-9b66-1a7db9a79f02/image.png)
</details>

completed (hopefully) the devboard; also did some reranging of the layout of the parts

## Schematic (keyboard switches) - 10rd Jun 2026 (2hrs)

i dont know why but finding a "hotswap mx 5pin switch" took so long :'(. but i finally found the MX_V2 lib!!

<details>
    <summary>
        switch matrix wired
    </summary>
      
  ![](https://cdn.hackclub.com/019eb38e-cd5f-7ae5-8ad0-a0b6d85c2c10/image.png)
</details>

## Schematic (Neopixels) - 10rd Jun 2026 (3hrs)

I had to research 2 things...

first was that will they take a 3.3v, if not then what... turns out they need a 5v but if it goes above they will go boom boom

<details>
    <summary>
        so i added this capacitor, and directly connect it to vbus. and to stabilize the voltage and not boom boom the neopixel
    </summary>
      
  ![](https://cdn.hackclub.com/019eb38e-cabd-7105-87c8-ec83e72aa6a9/image.png)
</details>

second was can i chain 68 of them! turns out i can..

<details>
    <summary>
        so i added the chain in the schematic and wired it all!
    </summary>
      
  ![](https://cdn.hackclub.com/019eb3fc-ca44-744e-b813-d766b4795b67/image.png)
</details>

oh and also i found out that i can add themes :p

## Schematic (Thinking about making it wireless) - 10rd Jun 2026 (2hrs)

i though about making it wireless...

so i started googling and resurching, i would need to parts to this. making it bluetooth and adding a battery

the battery is the easyier part of things, add a lithium ion battery, a charging chip/controller and connect it to the vbus and gnd.

but most batterires only output 3.7v... but the leds need 5v to run :/ so if i use a battery i would need to give that up

bluetooth was harder. i could add another chip but that would be much more complected and i cant just use the base qmk software i would need to cook somthing up

or i could change the rp2040 chip entirely for a nRF52840. that would solve the bluetooth issue.. but i would then need to also remaake its devboard and i dont think i trust myself to do that and expect it to work.

so i eventualy decided that its fine if its not wireless, it would reduce some weight and it would be relitivly thiner!

## Schematic (final stuff) - 10rd Jun 2026 (1hrs)

added footprints

fixed minor issues here and there, hopefully there are no more :p

## PCB (placing them in the layout) - 10rd Jun 2026 (1hrs)

so first i placed like about 10 of the 68 manualy using a grid, but then i realized there has to be a better way. and ofc there was

<details>
    <summary>
        i installed the [Keyboard footprints placer](https://github.com/adamws/kicad-kbplacer) plugin. and used this (image given) configuration, with a 65% preset from [KLE](https://www.keyboard-layout-editor.com/#/)
    </summary>
      
  ![](https://cdn.hackclub.com/019eb4fb-f313-7638-a226-63ec3ea9d9f1/image.png)
</details>


