---
title: Pixel Mapping in Photoshop
tags: [resources, art, mapping]
author: foreveryone
toc: true
---

The version of Photoshop used in this tutorial is CC 2019. There may be differences between the user interface in screenshots and the user interface of the version of Photoshop that you are using

### Setting up layers and groups
Create a new .psd file with the dimensions of the outline file. Open the outline file and select and copy its contents (ctrl +a, then ctrl+c). Paste into a new layer in the .psd. Repeat with the biome plan you made in tiled. Finally, create 4 empty layers and place them into a folder called water. With the names and the order matching the image below.

![Pasted image 20210622011544.png](/assets/img/Pasted%20image%2020210622011544.png#center)*How your layer overview should look after following the steps above.*

### Separating the biomes
Using the magic wand tool (settings: 0 tolerance, anti-alias off, and contiguous disabled), select a biome colour. Right click the selection and select layer via cut.

![Pasted image 20210622012114.png](/assets/img/Pasted%20image%2020210622012114.png#center)

Repeat for each biome colour.

![Pasted image 20210622014026.png](/assets/img/Pasted%20image%2020210622014026.png#center)

Control+click the grass layer's preview image in the layer overview, and then click the biomes folder in the layers overview. In the layer menu, select layer mask > reveal selection.

![Pasted image 20210622014823.png](/assets/img/Pasted%20image%2020210622014823.png#center)

![Pasted image 20210622014918.png](/assets/img/Pasted%20image%2020210622014918.png#center)

![Pasted image 20210622015052.png](/assets/img/Pasted%20image%2020210622015052.png#center)

Control + click the outline once again. In the select menu, expand the selection by 2 pixels.

![Pasted image 20210622015848.png](/assets/img/Pasted%20image%2020210622015848.png#center)

Then, select the **water outline** layer and fill with `224E79`.

![[Pasted image 20210622020516.png]]

Expand the selection by another 4 pixels and then select the **shallow water** layer. Fill with black.

Repeat this process for the final time, expanding by 1 pixel and selecting the **final water border** layer before filling with `1d8cbd`.

Select the whole image by pressing control + a, and then fill the water layer with black.

### Importing patterns
Open the presets manager and go to the Patterns preset type. Load `Patterns.pat`, which can be found in the github releases.

![Pasted image 20210622023701.png](/assets/img/Pasted%20image%2020210622023701.png#center).

### Overlaying patterns

Right click the **water** layer and select blending options. Select pattern overlay and then select the water texture.

![Pasted image 20210622025823.png](/assets/img/Pasted%20image%2020210622025823.png#center)

Do the same for the **shallow water** layer, but use the `watercoast` texture.

Use the grass texture for the outline, and the other **base** textures for the corresponding layers you have chosen.

### Drawing accents

Add a layer for each accent you wish to add to a biome, and place them directly above the biome base layer to ease your organisation.

![Pasted image 20210622123401.png](/assets/img/Pasted%20image%2020210622123401.png#center)*The base layers and accents for the example map. Only the `Snowforest` has a pattern overlay applied so far.*

Apply the pattern overlay layer style with the appropriate accent texture. With the accent layer active, select the pencil tool. Increase the pencil size to dimensions you're comfortable working with, and 'paint' the accent over the base layer.

Use the eraser tool set to pencil mode to clean up any edges and incomplete patterns.

![Pasted image 20210622132503.png](/assets/img/Pasted%20image%2020210622132503.png#center) *The accent layer has been painted, but cleaning has not been performed yet.*

Repeat the process for each of the accent layers you use.

[![photoshopexport.png](/assets/img/photoshopexport.png#center)](/assets/img/photoshopexport.png#center)

### Adding map ornaments

Create a new folder called map ornaments. Ornaments such as roads, towns, and large mountains will be added to this folder.

#### Adding large mountains
Open `mapdecoration/mountain/mountainbig.png` in Photoshop and select its contents. Paste the large mountain onto an area with space for the mountain. Selectively erase parts of the mountain sprite or the mountain asset layer to get them to line up properly.

#### Adding cities
I recommend not including every town on your map, instead limiting yourself to only the largest cities. Make use of the limited colour palette and space to include only the essentials for making a town distinct: a handful of buildings in a style unique for the nation.

The colour used for the background of towns and roads in the example map is `e3cec0`. The github release also contains some example buildings in various flavours which can be used.

Open the .png building sheets in photoshop, and select the building you want to import. Then, paste into the map .psd. Repeat to build towns. 

Select all layers that contain buildings and towns that belong to the same nation and merge them, for organizational ease.

### Adding labels
There are countless pixel-fonts available for free on [fontstruct](https://fontstruct.com/gallery/tag/9/Pixel).

For this map, I have chosen to use the [Metal Slug](https://fontstruct.com/fontstructions/show/833151/metal_slug_6) font.

Due to peculiarities with photoshop's font rendering, I instead write my text in paint on a `227, 206, 192` background at font size 5.

![Pasted image 20210623175737.png](/assets/img/Pasted%20image%2020210623175737.png#center)

I then select the text and paste it into Photoshop.

I add town labels **after** exporting the map by opening the export in a new .psd file and pasting the labels. Otherwise town labels can become overly large and draw too much attention.

### Exporting the map
When you are satisfied with the map you can export it. I prefer exporting my maps at double resolution, to emphasis their 'pixel appearance'

The save for web option with nearest neighbour scaling doesn't blur the output, which makes it ideal for pixel art maps. If you decide to multiply the resolution of your map, do so at percentages that are multiples of 100% to ensure there are no scaling artifacts.

![Pasted image 20210623150556.png](/assets/img/Pasted%20image%2020210623150556.png#center)

[![mapexportphotoshop.png](/assets/img/mapexportphotoshop.png#center)](/assets/img/mapexportphotoshop.png#center)*The final result.*