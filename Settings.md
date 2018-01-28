## Commands
* **/tpipes tps** - Shows some performance stats, e.g. the ticks per second of the TransportPipes thread or the amount of pipes and items currently ticking.
* **/tpipes settings** - Opens the player specific settings interface. Here you can change the render distance of the pipes and you can switch between Vanilla and Modelled Render System. Vanilla Render System uses Vanilla Minecraft textures and the Modelled Render System uses a custom resourcepack.
* **/tpipes reload \<config | pipes\>** - Reloads either the config files or destroys and recreates all pipes in all worlds.
* **/tpipes delete \<radius\>** - Destroys all pipes around you in the desired radius.
* **/tpipes save** - Saves all pipes in all worlds. Actually on every world save, the pipes get saved automatically but with this command you can save them manually.
* **/tpipes creative** - Opens an inventory where you get access to every pipe without crafting them manually. This only works in creative mode.
* **/tpipes update** - Updates the plugin to a more recent version automatically (if possible). The updated version will be available after the next restart.

## Config
There are three config files managed by the plugin. You can find them here: TransportPipes/config.yml, TransportPipes/localization.yml and TransportPipes/recipes.yml. Inside the localization.yml file you can change every text displayed to your desired language. The config.yml file has several different options:
* **max_items_per_pipe** - If the amount of items in one pipe exceeds this value, the pipe explodes in order to prevent lag issues.
* **crafting_enabled** - Disable this option to disable all pipe crafting recipes.
* **check_updates** - Enable to allow for automatic update check.
* **destroy_pipe_on_explosion** - Whether to destroy pipes if a natural (TNT, Creeper) explosion occurs nearby.
* **anticheat_plugins** - List all AntiCheat plugins running on your server here. If not listed here, some players may not be able to place or break pipes due to AntiCheat prevention.
* **default_rendersystemId** - Specify which RenderSystem (Vanilla = 0, Modelled = 1) to use as default for new players.
* **default_renderdistance** - Specify the default render distance of pipes. (Can be changed individually by each player).
* **default_showitems** - Specify the default value for the player-specific option "show items". This option allows you to visually hide all items flowing through the pipes.
* **force_default_rendersystem** - By enabling this option you can force all players to use the render system given at _default_renderdistance_.
* **resourcepack** - This option can be one of four values: "default", "server", "none" or a custom URL. The option "default" automatically loads the default resourcepack for TransportPipes. "server" assumes that the resourcepack is handled by the server completely ("server-resourcepack" option in the server.properties). "none" means the resourcepack is disabled and therefore only the vanilla rendersystem can be used. Last but not least, by providing a custom (direct) URL to a resourcepack, you can replace the default one with your own resourcepack. You can download the TransportPipes resourcepack [here](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/master/src/main/resources/TransportPipes-ResourcePack.zip).
* **disabled_worlds** - For every world contained in this list, the pipe system will be disabled.

By adjusting the recipes.yml, you can change the crafting recipes for all pipes and the wrench item.
A recipe is specified by the following keys:
* **type** - The recipe type: Either shaped or shapeless.
* **amount** - The amount of the crafted result item.
* **shape** - Only if type is shaped. Every entry in this list describes a row in the crafting table. Every char describes an item.
* **ingredients** - if type is shaped: For every char you have to specify the item to use. (\<itemID\>:\<itemDamage\>)
if type is shapeless: Just list all items (\<itemID\>:\<itemDamage\>) that are needed to craft the desired item. Just write "pipe" instead of \<itemID\>:\<itemDamage\> to use a pipe item.