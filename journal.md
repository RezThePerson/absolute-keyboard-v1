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

## Schematic (keyboard switches) - 10rd Jun 2026 (3hrs)

i dont know why but finding a "hotswap mx 5pin switch" took so long :'(. but i finally found the MX_V2 lib!! 

<details>
    <summary>
        switch matrix wired
    </summary>
      
  ![](https://cdn.hackclub.com/019eb38e-cd5f-7ae5-8ad0-a0b6d85c2c10/image.png)
</details>

## Schematic (Neopixels) - 10rd Jun 2026 (3hrs)

I had to reasurch a few things...




seccond was that will they take a 3.3v, if not then what... turns out they need a 5v but if it goes above they will go boom boom

<details>
    <summary>
        so i added this capacitor, to stablize the voltage and not boom boom the neopixel
    </summary>
      
  ![](https://cdn.hackclub.com/019eb38e-cd5f-7ae5-8ad0-a0b6d85c2c10/image.png)
</details>

last was can i chain 68 of them! turns out i can..

<details>
    <summary>
        so i added the chain in the schematic and wired it all!
    </summary>
      
  ![](eee)
</details>