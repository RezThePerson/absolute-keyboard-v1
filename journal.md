# Journal (total: 33Hrs)

## Schematic (devboard) - 3rd Jun 2026 (1hr)

Im using the [macondo](https://macondo.hackclub.com/docs/build-a-devboard) guide for help on this!

<details>
    <summary>
        Added rp2040 and the capacitors
    </summary>
      
  ![](https://cdn.hackclub.com/019e8eaa-bff0-7f3e-a80d-8cf23a6ba875/image.png)
</details>

## Schematic (devboard) - 9rd Jun 2026 (2hrs)

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

## Schematic (keyboard switches) - 9rd Jun 2026 (2hrs)

i dont know why but finding a "hotswap mx 5pin switch" took so long :'(. but i finally found the MX_V2 lib!!

<details>
    <summary>
        switch matrix wired
    </summary>
      
  ![](https://cdn.hackclub.com/019eb38e-cd5f-7ae5-8ad0-a0b6d85c2c10/image.png)
</details>

## Schematic (Neopixels) - 9rd Jun 2026 (3hrs)

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

## PCB (placing them in the layout) - 10rd Jun 2026 (3hrs)

so first i placed like about 10 of the 68 manualy using a grid, but then i realized there has to be a better way. and ofc there was

<details>
    <summary>
        i installed the [Keyboard footprints placer](https://github.com/adamws/kicad-kbplacer) plugin. and used this (image given) configuration, with a 65% preset from [KLE](https://www.keyboard-layout-editor.com/#/)
    </summary>
      
  ![](https://cdn.hackclub.com/019eb8cf-d16d-72c7-b3fa-f84c9bb938e7/image.png)
</details>

## PCB (wiring) - 11rd Jun 2026 (6hr)

so i placed the components and started wiring...

<details>
    <summary>
        this is how it turned out..
    </summary>
      
  ![](https://cdn.hackclub.com/019eb8cf-6d5d-7b10-a2c7-6559f9c10aa0/image.png)
</details>

<details>
    <summary>
        but the actualy devboard part was too messy for me.. i simply could not manage to understand how i should wire it....
    </summary>
      
  ![](https://cdn.hackclub.com/019eb8d1-85cc-7c21-8d9e-41e7b5f038a3/image.png)
</details>

so i had to restart on the devboard...

## PCB (doing it again) - 12rd Jun 2026 (6hr)

<details>
    <summary>
        omg this is soo soo much cleaner its so much better, took me so long tho!
    </summary>
      
  ![](https://cdn.hackclub.com/019ecda1-77cc-79be-9d3c-2dc040427c48/image.png)
</details>

finaly the whole devboard is done!!

## PCB (fixing filled zones) - 15rd Jun 2026 (3hr)

turns out filled zones are not so easy... and they dont allaways fully connect. so i need to place a lot of vias and connect them.

<details>
    <summary>
        and i have soo many of them i need to fix..
    </summary>
      
  ![](https://cdn.hackclub.com/019ecda1-77cc-79be-9d3c-2dc040427c48/image.png)
</details>

<details>
    <summary>
        why is it so hard to find these.. ??
    </summary>
      
  ![](https://cdn.hackclub.com/019ed13c-9855-796e-85a3-5e037315081c/image.png)
</details>

ok finaly im doneee!!!!

## PCB (oopsie + branding) - 16rd Jun 2026 (2hr)

https://cdn.hackclub.com/019ed176-bd90-7930-8662-b6996dfa222f/image.png

<details>
    <summary>
        so turns out i forgot to add the spacebar stablizer... and now that i do it it is ontop of the parts
    </summary>
      
  ![](https://cdn.hackclub.com/019ed176-bd90-7930-8662-b6996dfa222f/image.png)
</details>

witch means tiime to move a lot of parts and rewire a shit ton

aghh some more filled zone issue + DRC hole overlaps

finaly done

<details>
    <summary>
        and to wrap things up, added a little text to say i made it.
    </summary>
      
  ![](https://cdn.hackclub.com/019ed176-bd90-7930-8662-b6996dfa222f/image.png)
</details>

## case (disinging) - 17rd Jun 2026 (1hr)

so i wanted this to be simple compact case so i googled around and got inspiraration from [this](https://www.myminifactory.com/object/3d-print-65-keyboard-case-100884) case.

i tryed to follow the hackpad guide for freecad (fusion wont work on linux) but i coldnt.

<details>
    <summary>
        so i simply pulled up tinker cad and made this simple thingy!
    </summary>
      
  ![](https://cdn.hackclub.com/019ed676-f46c-734c-ad67-4c9da6510bea/image.png)
</details>

## firmware (coding) - 17rd Jun 2026 (1hr)

used the help of gemini to understand how qmk works and wrote it. thats it lol.

it also helped me do proper mappings