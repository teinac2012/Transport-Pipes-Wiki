## Commands
* **/tpipes tps** - Shows some performance stats, e.g. the ticks per second of the TransportPipes thread or the amount of pipes and items currently ticking.
* **/tpipes settings** - Opens the player specific settings interface. Here you can change the render distance of the pipes and you can switch between Vanilla and Modelled Render System. Vanilla Render System uses Vanilla Minecraft textures and the Modelled Render System uses a custom resourcepack.
* **/tpipes creative** - Opens an inventory where you get access to every pipe without crafting them manually. This only works in creative mode.

## Config
The TransportPipes data folder ("plugins/TransportPipes/") has the following structure:
* **config.yml**: This is the general plugin config file where you can adjust some global properties.
* **lang_[LANG].yml**: These are the language files where all of the localized text is saved. You can directly change "your" language file or create one on your own and set the language option in the config.yml to the suffix of your created file (e.g.: _language: en_ loads the language file _lang_en.yml_).
* **playersettings/**: This directory contains player specific settings files which are bound to the players UUIDs. You may delete one of those files to auto-generate a new one on the next server restart.

The general config file maintains the following properties:
* **max_items_per_pipe** - If the amount of items in one pipe exceeds this value, the pipe explodes in order to prevent lag issues.
* **crafting_enabled** - Disable this option to disable all pipe crafting recipes. (Can be useful if you want to implement different recipes with a custom recipes plugin)
* **anticheat_plugins** - List all AntiCheat plugins running on your server here. If not listed here, some players may not be able to place or break pipes due to AntiCheat prevention.
* **default_render_system** - Can be either "vanilla" or "modelled". The vanilla rendersystem displays pipes without any resourcepack and only with the help of invisible armorstands. The modelled rendersystem uses a custom resourcepack for a much better playing experience (the modelled version also reduces the amount of entities in the world which increases FPS)
* **default_show_items** - Specify the default value for the player-specific option "show items". This option allows you to visually hide all items moving through the pipes.
* **default_render_distance** - Specify the default render distance of ducts. (Can be changed individually by each player).
* **resourcepack_mode** - This option can be one of three values: "default", "server" or "none". The option "default" automatically loads the default resourcepack for TransportPipes. "server" assumes that the resourcepack is handled by the server completely ("server-resourcepack" option in the server.properties). "none" means no resourcepack should be used and therefore the modelled rendersystem is completely disabled. If you already have got a server resourcepack but want to use the TransportPipes resourcepack too, this is where the "server" option comes into play. Just download the TransportPipes resourcepack from [here](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/master/src/main/resources/TransportPipes-ResourcePack.zip), merge it with your own resourcepack put a link to the merged pack into your server-resourcepack option in the server.properties and set the "resourcepack_mode" in TransportPipes to "server".
* **disabled_worlds** - For every world contained in this list, the duct system will be disabled.
* **wrench** - The wrench item. "item" is the Material and "glowing" just makes the item be enchanted without any "enchantment label" on it.
* **language** - Specify the language you want to use. If you change the language here, make sure that the respective lang_[LANG].yml file in the plugins data folder exists (You may create such with your own translations).
* **show_hidden_ducts_time** - When a player shift-clicks with a wrench in his hand, he will get to see all hidden nearby ducts. This property is the time in seconds, how long the ducts are revealed.