![Logo](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/recode/src/main/resources/wiki/logo.png)

The Transport-Pipes plugin adds several different pipes into Minecraft. At the moment there are colored pipes, golden pipes, iron pipes, extraction pipes, void pipes, ice pipes and crafting pipes. Similar to the BuildCraft mod, these pipes can transport any kind of item. In the following wiki you will learn how to craft and use this pipes and what the difference between those pipe types is. Also some basic information about the plugin's commands and config is described.

## Dependencies
TransportPipes depends on ProtocolLib. In order for this plugin to work, make sure a recent version of ProtocolLib is installed on your server. You can download ProtocolLib here: <https://www.spigotmc.org/resources/protocollib.1997>

## Features
As explained above, you have to use different pipe types in different situations. Every pipe type and it's purpose is listed below:
* **Extraction Pipe**: This pipe is the only one which can extract items from container blocks. Container blocks are blocks which hold inventories: Chests, furnaces, hoppers, shulker boxes and so on. Extraction pipes don't connect to each other but they do connect with every other pipe and with container blocks of course. One extraction pipe only has one extract direction from where it extracts items. This direction is displayed by a different connection texture.
You can change the extract direction as well as the extract condition by right-clicking the pipe with a wrench and choosing the desired option. The extract amount option allows you to extract multiple items in a single tick. You can filter which items get extracted by using the filter interface (explained in detail at the Golden Pipe section). Last but not least, the extract condition determines when to extract items. There are three extract conditions:
    * **needs redstone**: the pipe only extracts items if it's powered with a redstone signal.
    * **always extract**: the pipe always extracts items regardless of whether it's powered with redstone or not.
    * **never extract**: the pipe never extracts items.
* **Colored Pipe**: This is the simplest pipe. Its only purpose is to transport items. Nevertheless you can dye this kind of pipe. Different colored pipes behave the same but don't connect to each other. Therefore you can create complex pipe system without having to worry about leaving enough space between pipes. The white colored pipe has a special role: It is the default pipe and therefore connects to any other neighboring pipe.
* **Ice Pipe**: The Ice Pipe transports items in the same way as every other pipe does. The only difference is the transport speed. Ice Pipes transport items four times faster than other pipes.
* **Iron Pipe**: Iron Pipes are basically "One-Way-Pipes". Regardless of the direction an item comes from, it will always move into the desired output direction. You can change this output direction by right-clicking the pipe with a wrench. This output direction is marked by a yellow texture.
* **Void Pipe**: Void Pipes simply destroy all items which are moving inside them.
* **Crafting Pipe**: The Crafting Pipe gives you the possibility to automate crafting processes. After specifying a crafting recipe, all items going into this Pipe will be cached and the result item is going to be crafted as soon as enough ingredients are stored inside. By right-clicking this Pipe with a wrench, first you can define the output direction in which the crafted items will go, second you can see the cached items, used to craft the result item and last but not least you can define the crafting recipe.
* **Golden Pipe**: A Golden Pipe can sort items. Every output direction on the Golden Pipe has a specific color. By right-clicking this pipe with a wrench, a sorting inventory opens. You can put items in there to determine which items should go where. Every row in this inventory refers to an output direction of the Golden Pipe. The color indicates which row refers to which output direction. By clicking a color indicator (wool block) inside this inventory, you can change the filter mode and the filter strictness for this output direction. The filter strictness determines how strict to compare items when calculating the desired output direction for an incoming item and the filter mode gives information about how this filter should be applied.

There are the following filter modes:
  * **Normal**: the default filter mode. It only accepts an item if it fits with at least one filter item inside this row
  * **Inverted**: compares items the same way as Normal filter mode but inverts the result which will block all items except the ones inside this filter row
  * **Block all**: simply blocks all items

There are the following filter strictness options:
  * **Item material**: only checks if the Material of the item fits with the filter comparison item (ignores metadata)
  * **Item material and metadata**: checks if the comparison item is exactly the same as the the checked item

In general, all pipes can put items into container blocks if they are connected to such but only extraction pipes can extract items from container blocks. Also as mentioned many times above, to configure pipes you need a wrench. The crafting recipe for the wrench is given below. The wrench can be used simply by right-clicking the desired pipe.

## Crafting Recipes
Crafting recipes can be disabled in the config file which allows you to use any external "custom recipes" plugin to implement different recipes. Nevertheless the following recipes are the default ones:

### Colored Pipe:
![White Pipe](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/recode/src/main/resources/wiki/recipes/white.png)
![Colored Pipes](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/recode/src/main/resources/wiki/recipes/colors.gif)

### Golden Pipe:
![Golden Pipe](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/recode/src/main/resources/wiki/recipes/gold.png)

### Iron Pipe:
![Iron Pipe](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/recode/src/main/resources/wiki/recipes/iron.png)

### Extraction Pipe:
![Extraction Pipe](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/recode/src/main/resources/wiki/recipes/extraction.png)

### Ice Pipe:
![Ice Pipe](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/recode/src/main/resources/wiki/recipes/ice.png)

### Void Pipe:
![Void Pipe](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/recode/src/main/resources/wiki/recipes/void.png)

### Crafting Pipe:
![Crafting Pipe](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/recode/src/main/resources/wiki/recipes/crafting.png)

### Wrench:
![Wrench](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/recode/src/main/resources/wiki/recipes/wrench.png)