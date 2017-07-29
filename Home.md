![Logo](https://img2.picload.org/image/riwprwgr/logo.png)

The Transport-Pipes plugin adds several different pipes into Minecraft. At the moment there are colored pipes, golden pipes, iron pipes, extraction pipes, void pipes and ice pipes. Similar to the BuildCraft mod, these pipes can transport any kind of item. In the following wiki you will learn how to craft and use this pipes and what the difference between those pipe types is. Also some basic information about the plugin's commands and config is described.

## Dependencies
TransportPipes depends only on ProtocolLib. In order for this plugin to work, make sure a recent version of ProtocolLib is installed on your server. You can download ProtocolLib here: <https://www.spigotmc.org/resources/protocollib.1997>

## Features
As explained above, you have to use different pipe types in different situations. Every pipe type and their purpose is listed below:
* **Extraction Pipe**: This pipe is the only one which can extract items from container blocks. Container blocks are blocks which hold inventories: Chests, furnaces, hoppers, shulker boxes and much more. Extraction pipe don't connect to each other but they do connect with every other pipes and with container blocks of course. One extraction pipe only has one extract direction from where it extracts items. This direction is displayed by a different connection texture.
You can change the extract direction as well as the extract condition by right-clicking the pipe with a wrench and choosing the desired option. The extract condition determins when to extract items. There are three extract conditions:
    * **needs redstone**: the pipe only extracts items if it's powered with a redstone signal.
    * **always extract**: the pipe always extracts items regardless of whether it's powered with redstone or not.
    * **never extract**: the pipe never extracts items.
* **Colored Pipe**: This is the simplest pipe. Its only purpose is to transport items. Nevertheless you can color this kind of pipe. Different colored pipes behave the same but don't connect to each other. Therefore you can create complex pipe system without issues of wrong connected pipes.
* **Ice Pipe**: The Ice Pipe transports items as well as any other pipe. The only difference is the transport speed. Ice Pipes transport items four times faster than other pipes.
* **Iron Pipe**: Iron Pipes can also be called "One-Way-Pipe". It's feature is that regardless of from which direction an item comes from, it will always move into the desired output direction. You can change this output direction by right-clicking the pipe with a wrench.
* **Void Pipe**: Void Pipes simply destroy all items moving inside them.
* **Golden Pipe**: A Golden Pipe can sort items. Every output direction on the Golden Pipe has a specific color. By right-clicking this pipe with a wrench, a sorting inventory opens. You can put items in there to determine which items should go where. Every row in this inventory is referring to an output direction of the Golden Pipe. The color indicates which row refers to which output direction. By clicking on a color indicator inside this inventory, you can change the filtering mode for this output direction row. The filtering mode determines which traits to compare when calculating the desired output direction for an incoming item. The following filtering modes exist:  
_In this context, type stands for the material of the item (e.g. the material of any colored wool is still wool). Damage stands for the durability of a tool item and in correlation to "not-tool" items, they determine the "damage" value (e.g. the damage value of wool is the color of the wool and the damage value of wood is the type of wood). Block all mode doesn't check any trait, it blocks the hole direction. Therefore items can only move into the Golden Pipe through a blocked direction but never out this direction_
  
    * filter by type, damage, itemmeta
    * filter by type, damage
    * filter by type, itemmeta
    * filter by type
    * block all

In general, all pipes can put items into container blocks if they are connected to such but only extraction pipes can extract items from container blocks. Also as mentioned some times above, for some pipes you need a wrench. The crafting recipes for the wrench is given below. The wrench can be used simply by right-clicking the desired pipe.

## Crafting Recipes
All crafting recipes can be changed in the config but the default ones are as follows:

### Colored Pipe:
![Colored Pipe](https://img2.picload.org/image/rwrlwwdi/coloredpipe.png)
![Colored PIpe](https://img2.picload.org/image/rwrlwwra/coloredpipes.gif)

### Golden Pipe:
![Golden Pipe](https://img2.picload.org/image/rwrlwwri/goldenpipe.png)

### Iron Pipe:
![Iron Pipe](https://img2.picload.org/image/rwrlwwdr/ironpipe.png)

### Extraction Pipe:
![Extraction Pipe](https://img2.picload.org/image/rwrlwwrl/extractionpipe.png)

### Ice Pipe:
![Ice Pipe](https://img2.picload.org/image/rwrlwwrw/icepipe.png)

### Void Pipe:
![Void Pipe](https://img2.picload.org/image/rwrlwwda/voidpipe.png)

### Wrench:
![Wrench](https://img2.picload.org/image/rwrlwwdl/wrench.png)