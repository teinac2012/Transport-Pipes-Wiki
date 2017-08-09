If you're a developer and you want to create your custom pipe system from another plugin, you can use the following PipeAPI:

```java
//Builds a pipe at the given location. Additionally you can determine which type and which color the pipe should have.
//The PipeColor is ignored if PipeType is not COLORED.
PipeAPI.buildPipe(Location, PipeType, PipeColor);

//Detroys the pipe at the given location.
PipeAPI.destroyPipe(Location);

//Returns the current ticks per second of the TransportPipes thread.
PipeAPI.getTPS();

//Returns the max tps of the TransportPipes thread.
//If this value is reached with the real tps, the thread is running fine.
PipeAPI.getMaxTPS();

//Returns the amount of pipes in all worlds.
PipeAPI.getPipeCount();

//Returns the amount of pipes in the given world.
PipeAPI.getPipeCount(World);

//Checks whether at the given location is a pipe.
PipeAPI.isPipe(Location);

//Returns the pipe object at the given location or null if there is no pipe.
PipeAPI.getPipeAtLocation(Location);

//Destroys all pipes in this world.
PipeAPI.destroyPipes(World);

//Puts any item into the given pipe object with a moving direction of "itemDirection".
PipeAPI.putItemInPipe(Pipe, ItemData, PipeDirection);

//Registers a custom container block at the given location. Every pipe around this block will try to extract/insert items from/into this container.
//Create your own implementation of the TransportPipesContainer interface in order to specify which items to extract and where inserted items should go.
PipeAPI.registerTransportPipesContainer(Location, TransportPipesContainer);

//Unregisters a custom container block. See PipeAPI.registerTransportPipesContainer(Location, TransportPipesContainer).
PipeAPI.unregisterTransportPipesContainer(Location);
```

In addition to this methods, there are several events you can use to get notified about important things:
* **PipeExplodeEvent** - gets called when a pipe explodes due to too many items inside it. This event is not called when a pipe explodes due to a natural explosion.
* **PlayerPlacePipeEvent** - when a player places a pipe.
* **PlayerDestroyPipeEvent** - when a player destroys a pipes.
* **PipeConnectionsChangeEvent** - gets called when a pipe changes its connections amount. For example when a container block or another pipe is placed next to it.