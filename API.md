If you're a developer and you want to create your custom pipe system from another plugin, you can use the following PipeAPI:

```java
//Builds a pipe at the given location. Additionally you can determine which type and which color the pipe should have.
//The PipeColor is ignored if PipeType is not COLORED.
PipeAPI.buildPipe(Location blockLoc, PipeType pipeType, PipeColor pipeColor);

//Detroys the pipe at the given location.
PipeAPI.destroyDuct(Location blockLoc);

//Returns the current ticks per second of the TransportPipes thread.
PipeAPI.getTPS();

//Returns the max tps of the TransportPipes thread.
//If this value is reached with the real tps, the thread is running fine.
PipeAPI.getMaxTPS();

//Returns the amount of pipes in all worlds.
PipeAPI.getDuctCount();

//Returns the amount of pipes in the given world.
PipeAPI.getDuctCount(World world);

//Checks whether at the given location is a pipe (just set ductType to DuctType.PIPE).
PipeAPI.isDuct(Location blockLoc, DuctType ductType);

//Returns the pipe object at the given location or null if there is no pipe.
PipeAPI.getPipeAtLocation(Location blockLoc);

//Destroys all pipes in this world.
PipeAPI.destroyDucts(World world);

//Puts "item" into the given pipe with a moving direction of "itemDirection".
PipeAPI.putItemInPipe(Pipe pipe, ItemStack item, WrappedDirection itemDirection);

//Registers a custom container block at the given location. Every pipe around this block will try to extract/insert items from/into this container.
//Create your own implementation of the TransportPipesContainer interface in order to specify which items to extract and where inserted items should go.
PipeAPI.registerTransportPipesContainer(Location blockLoc, TransportPipesContainer container);

//Unregisters a custom container block. See PipeAPI.registerTransportPipesContainer(Location blockLoc, TransportPipesContainer container).
PipeAPI.unregisterTransportPipesContainer(Location blockLoc);
```

In addition to this methods, there are several events you can use to get notified about important things:
* **PlayerPlaceDuctEvent** - when a player places a duct (you have to check for DuctType.PIPE).
* **PlayerDestroyDuctEvent** - when a player destroys a duct (you have to check for DuctType.PIPE).
* **DuctConnectionsChangeEvent** - gets called when a duct changes its connections amount. For example when a container block or another duct is placed next to it (you have to check for DuctType.PIPE).
* **DuctRegistrationEvent** - abstract level of PlayerPlaceDuctEvent. This event also gets called when another plugin registers a duct or a duct gets loaded from the save file.
* **DuctUnregistrationEvent** - abstract level of PlayerDestroyDuctEvent. This event also gets called when another plugin unregisters a duct.