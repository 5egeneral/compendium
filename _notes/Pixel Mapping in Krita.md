---
title: Pixel Mapping in Krita
tags: [resources, art, mapping]
author: foreveryone
toc: true
---

Krita is a free and open source painting program which supports non-destructive editing, unlike GIMP, the other premier open source image editor, which is why it has my preference.

[Get Krita here.](https://krita.org/en/download/krita-desktop/)

### Getting familiar with Krita
Krita is set up to be fairly familiar for most users who have prior image editor software experience, barring a few idiosyncrasies.

You zoom in and out by simply using the scroll wheel, and you pan the image with the middle mouse button.

The advanced color selector doesn't have a field to enter the hex code of a color. Instead, click the color selector on the top bar to enter a hex code.

![Pasted image 20210624155006.png](/assets/img/Pasted%20image%2020210624155006.png#center)

Pixel or raster layers are called paint layers. One can add new layers using this button in the layer overview panel.

![Pasted image 20210624155315.png](/assets/img/Pasted%20image%2020210624155315.png#center)

Select one or more layers and select the group option after right clicking them to group them. Alternatively, press ctrl+g after selecting the layers.

![Pasted image 20210624155533.png](/assets/img/Pasted%20image%2020210624155533.png#center)

A brush's size can include decimals. To type a brush's size, right click the size selector and input a number.

![Pasted image 20210624160433.png](/assets/img/Pasted%20image%2020210624160433.png#center)

### Setting up layers and groups
Create a new .kra file with the dimensions of the outline file. Drag and drop the outline file into the .kra file. When prompted, select `Insert as new layer`. 

Repeat with the biome plan you made in tiled. The biome plan may not align properly, if this is the case, select the move tool and zoom in on the top left corner. Adjust until the corner of the biome plan matches with the image's top left corner.

![Pasted image 20210624162600.png](/assets/img/Pasted%20image%2020210624162600.png#center)

Place the  biome plan into a group called biomes. 

Select the biome group and the outline, and then create another group called land.

Finally, create 4 empty layers and place them into a group called water. With the names and the order matching the image below.

![Pasted image 20210624161708.png](/assets/img/Pasted%20image%2020210624161708.png#center)*How your layer overview should look after following the steps above.*

### Separating the biomes
Select the biome layer. Using the similar color selection tool (settings: 0 tolerance, anti-alias off, and contiguous disabled), select a biome colour.

![Pasted image 20210624161858.png](/assets/img/Pasted%20image%2020210624161858.png#center)

![Pasted image 20210624162049.png](/assets/img/Pasted%20image%2020210624162049.png#center)

Right click the selection and select layer via cut.

![Pasted image 20210624162207.png](/assets/img/Pasted%20image%2020210624162207.png#center)

Repeat for each biome colour.

![Pasted image 20210624163707.png](/assets/img/Pasted%20image%2020210624163707.png#center)

Click the inherit alpha button on the biomes group to only display biomes on areas where land is visible.

![Pasted image 20210624164605.png](/assets/img/Pasted%20image%2020210624164605.png#center)

Control + click the outline layer's preview image. In the select menu, grow the selection by 2 pixels.

![Pasted image 20210624164915.png](/assets/img/Pasted%20image%2020210624164915.png#center)


Click the colour picker and set your foreground colour to `224E79`.

![Pasted image 20210624165429.png](/assets/img/Pasted%20image%2020210624165429.png#center)

Then, select the **water outline** layer and fill with the foreground colour.

![Pasted image 20210624165536.png](/assets/img/Pasted%20image%2020210624165536.png#center)

Grow the selection by another 4 pixels and then select the **shallow water** layer. Fill with the foreground colour again.

Change the foreground colour to `1d8cbd`. Grow the selection by 1 pixel and select the **final water border** layer. Fill with the foreground colour.

Select the whole image by pressing control + a, and then fill the water layer with the foreground colour.

### Importing patterns
Open the Manage Resources dialogue box import patterns. Select all the images in the textures folder, which can be found in the github releases. You can select more than one file at a time by pressing control + a while you have opened the textures folder.

![Pasted image 20210624171934.png](/assets/img/Pasted%20image%2020210624171934.png#center)

After importing the patterns, save and exit Krita, and then reopen your project, to make sure the texture have been saved.

### Overlaying patterns

Right click the **water** layer and select layer styles. Select pattern overlay and then select the water texture.

Change the blend mode to normal and increase the opacity to 100%. Finally increase the scale to 100%.

![Pasted image 20210624172322.png](/assets/img/Pasted%20image%2020210624172322.png)

Do the same for the **shallow water** layer, but use the `watercoast` texture.

Due to a peculiarity in how Krita lays out tiles, land textures need to be overlayed in a different way to match seamlessly.

Select a 'base layer' and then click the 'add other layer type' button. Select fill layer, and then select the appropriate base texture.

If you have selected the wrong texture, right click the fill layer and select **Properties**, and select the correct pattern.

![Pasted image 20210624192327.png](/assets/img/Pasted%20image%2020210624192327.png#center)

Rename the newly created layer to `texture fill`, and toggle its alpha inheritance. Then group the fill layer and the base layer together.

Repeat the process for each biome's base layer.

After a group has been made, you can collapse it to conserve space.

![Pasted image 20210624192508.png](/assets/img/Pasted%20image%2020210624192508.png#center) *The fill layer is above the base layer and has alpha inheritance toggled.*



### Drawing accents

Add a paint layer above the *group* of the base layer. Add a fill layer on top of that. Group them together.

![Pasted image 20210625004342.png](/assets/img/Pasted%20image%2020210625004342.png#center)*The Hills Accent group is placed directly above the HillsBase group. The HillsAccentFill layer has alpha inheritance toggled.*

Select the accent **paint layer** and select the paint brush tool (hotkey b). In the Brush Presets pane, select the pixel art group and select the first brush.

![Pasted image 20210625004639.png](/assets/img/Pasted%20image%2020210625004639.png#center)

I prefer working with an 8px square brush rather than a round brush, so I edit the brush to be square in the settings.

![Pasted image 20210625004911.png](/assets/img/Pasted%20image%2020210625004911.png#center)

Paint the accent, while toggling the eraser (hotkey e) on and off to correct mistakes.

Repeat the process for each of the accents you wish to use use.

![Pasted image 20210625023816.png](/assets/img/Pasted%20image%2020210625023816.png#center)


### Adding map ornaments

Create a new group called map ornaments. Ornaments such as roads, towns, and large mountains will be added to this folder.

#### Adding large mountains
Drag and drop `mapdecoration/mountain/mountainbig.png` into Krita. When prompted, select `insert as new layer`. Selectively erase parts of the mountain sprite or the mountain asset layer to get them to line up properly.

#### Adding cities
I recommend not including every town on your map, instead limiting yourself to only the largest cities. Make use of the limited colour palette and space to include only the essentials for making a town distinct: a handful of buildings in a style unique for the nation.

The colour used for the background of towns and roads in the example map is `e3cec0`. The github release also contains some example buildings in various flavours which can be used.

Drag and drop buildings from the `buildings/krita` folder into Krita. When prompted, select `insert as new layer`. Repeat to build towns. 

Select all layers that contain buildings and towns that belong to the same nation and merge them, for organizational ease.

### Adding labels
There are countless pixel-fonts available for free on [fontstruct](https://fontstruct.com/gallery/tag/9/Pixel).

For this map, I have chosen to use the [Metal Slug](https://fontstruct.com/fontstructions/show/833151/metal_slug_6) font.

Due to peculiarities with Krita's font rendering, I instead write my text in paint on a `227, 206, 192` background at font size 5.

![Pasted image 20210623175737.png](/assets/img/Pasted%20image%2020210623175737.png#center)

I then select the text and paste it into Krita.

I add town labels **after** exporting the map by opening the export in a new .kra file and pasting the labels. Otherwise town labels can become overly large and draw too much attention.

### Exporting the map
When you are satisfied with the map you can export it. I prefer exporting my maps at double resolution, to emphasis their 'pixel appearance'.

Go to `layer > flatten image` and then go to `image > scale image to new size`. Make sure to choose nearest neighbour as the scaling filter to maintain sharpness.

![Pasted image 20210625025420.png](/assets/img/Pasted%20image%2020210625025420.png#center)

The final result:

[![mapexportkrita.png](/assets/img/mapexportkrita.png#center)](/assets/img/mapexportkrita.png#center)

This means that, using [the scale we determined in the previous segment](https://5eg-compendium.netlify.app/notes/20210627-pixel-art-mapping#choosing-a-scale), the ratio of pixels to miles is now 4 to 1.