---
title: Pixel Art Mapping
state: publish
tags: [resources, art, mapping]
author: foreveryone
toc: true
---

 <iframe src="https://foreveryone1.github.io/map/#-173.5,368,1z" style="height:300px;width:100%;" title="Pixel Map Example"></iframe>*An example of the type of map one can make with pixel art.*

There are many ways of presenting your campaign's world, from realistic terrain  maps to more diegetically plausible painterly maps.

A pixel art map is decidedly on the 'stylised' side of the spectrum, which comes with certains benefits and drawbacks: the art style implicitly communicates that the map is an incomplete representation of the world, rather than an end-all be-all map of the environ. This gives the DM leeway to deviate from the visuals of the map.

In addition, the simplified vibrant symbols on a pixel art map's tiles quickly communicate the various environments, making them very player-legible.

Because of the conscious decision to restrict the colour palette, pixel art maps compress well: the 6912 pixel by 5040 pixel map in the example above is less than a megabyte as a png, and half that as a webp. This makes pixel art maps accessible even for slower internet connections, in contrast to a high-resolution map in a more graphically intensive style.

A pixel art map, by virtue of naturally being pixellated, scales well. What would be displeasing visual artifacts on other maps are quirks that enhance the charm of the stylisation of a pixel map.

### Choosing a scale
The first part of mapping is choosing a scale for your map. In this example  we'll choose a scale of 2 pixels for every mile. Depending on the resolution, this scale is suited to portraying anything from a regional to a continental scale.

When choosing the dimensions of your map, it is best to ensure it is a multiple of 8 if you are using the included textures and tools.

A resolution of 1280 by 800 means the map will cover an area of 640 by 400 miles upon completion.

### Creating a land outline

Using an image editing program of your preference, draw the outline of your landmass. Tracing distorted / composited real world maps or maps from [Azgaar's Fantasy Map Generator](https://azgaar.github.io/Fantasy-Map-Generator/) can be done to ease your workload. 

![Map outline](/assets/img/outline.webp) *An example outline, generated on Azgaar's Fantasy Map Generator.*

### Downloading the asset pack

[The Github releases page](https://github.com/5egeneral/compendium/releases/tag/map.1) contains three zip files, one for mapping with [Krita](#open-source-krita), one for mapping with [Photoshop](#paid-software-photoshop), and one containing the project files.

### Planning regions using Tiled
[Tiled](https://thorbjorn.itch.io/tiled) is a free and open source tile-based image editor which we shall use to plan the patterns of every region.

We'll start by creating a map with the same dimensions as the outline we just drew.

![Pasted image 20210621025234.png](/assets/img/Pasted%20image%2020210621025234.png#center)

After that has been done, open the 'tiledset' in Tiled. Next, add an object layer.


![Pasted image 20210621025604.png](/assets/img/Pasted%20image%2020210621025604.png#center)

Drag your outline from your file explorer into your tilesets overview. 

![Pasted image 20210621030408.png](/assets/img/Pasted%20image%2020210621030408.png#center) *Drag and drop the outline into this area to create a new 'tile'.*

When prompted, select a tile height and width equal to the resolution of your outline.

![Pasted image 20210621030620.png](/assets/img/Pasted%20image%2020210621030620.png#center)

In the layer overview, select the Object layer you just created and place the Outline 'tile' onto your map using the insert tile tool (t).

![Pasted image 20210621030859.png](/assets/img/Pasted%20image%2020210621030859.png#center)

Adjust the opacity of the object layer so you can see the background beneath it.

![Pasted image 20210621031201.png](/assets/img/Pasted%20image%2020210621031201.png#center)

Now, select the tile layer, and begin planning environments. The tiles in the 'tiledset' are intentionally simply just 8x8 squares with bright colours and rounded corners, we'll add the pixel patterns to them afterwards.

Each base texture has at least one accent, although some have several. The base textures and accents beyond the base texture are listed in the table below.

**Table: Base textures and accents.**

| Base Texture  | Additional Accent |
| ------------- | :-----------------: |
| Forest        | Pines, Rainy      |
| Savannah      | /                 |
| Desert        | /                 |
| Snowy Forest  | Mountains         |
| Mountains     | /                 |
| Gloomy Forest | /                 |
| Hills         | /                 | 

There are more colours in the 'tiledset' than there are biome base textures, in case you want to create your own textures or experiment with other textures in the future.

Adorn your landmass using the tile brush(b) and shape fill tool (p), keeping in mind that each colour corresponds with one biome. You don't have to colour neatly within the lines nor do you have to fill in the whole landmass, as unadorned areas will be filled with grass.

There are rounded corners if you wish to use them, but they are by no means obligatory. 

If your biomes intersect, which they most likely will when planning the hills and mountains biomes, it is best if you work in several tile layers to make your work easier.

![Pasted image 20210621040000.png](/assets/img/Pasted%20image%2020210621040000.png#center) *Most of the biomes can fit on the same layer, but the mountain biome needs to be placed on another layer as it has been placed on top of the hill layer.*

Once you are satisfied with the arrangement of the biomes, hide the object layer by clicking on the eye in the layer overview.

![Pasted image 20210621173818.png](/assets/img/Pasted%20image%2020210621173818.png#center)

Export the map as an image with the settings below.

![Pasted image 20210621174147.png](/assets/img/Pasted%20image%2020210621174147.png#center)

### Texturing the map

Once the biome planning has been completed, we can turn broad splotches of colour and an outline into an actual map.

#### Open source: Krita
Krita is a free and open source painting program which supports non-destructive editing, unlike GIMP, the other premier open source image editor, which is why it has my preference.

[Get Krita here.](https://krita.org/en/download/krita-desktop/)

[[Pixel Mapping in Krita]]

#### Paid software: Photoshop
The version of Photoshop used in this tutorial is CC 2019. There may be differences between the user interface in screenshots and the user interface of the version of Photoshop that you are using.

[[Pixel Mapping in Photoshop]]