If your a developer and you want to create your custom pipe system from another plugin, you can use the following PipeAPI:

```java
//Simply build a pipe
PipeAPI.buildPipe(Location, PipeType, PipeColor);

//Simply destroy a pipe
PipeAPI.destroyPipe(Location);

//Returns the ticks per second of the TransportPipes thread
PipeAPI.getTPS();

//Returns the amount of pipes registered in all worlds
PipeAPI.getPipeCount();

//Returns the amount of pipes registered in the given world
PipeAPI.getPipeCount(World);

//Whether there is a pipe at the given location
PipeAPI.isPipe(Location);

//Returns a pipe object at the given location or null if there is no pipe
PipeAPI.getPipeAtLocation(Location);

//Simply destroys all pipes in the given world
PipeAPI.destroyPipes(World);

//puts any item (with an amount of 1) into the given pipe object with a moving direction of "itemDirection"
PipeAPI.putItemInPipe(Pipe, ItemData, PipeDirection);

//register a custom container block at a specific location.
//Every pipe around this block will try to extract/insert items from/into this container.
//Create your own implementation of the TransportPipesContainer interface in order to specify
//which items to extract and where inserted items should go.
PipeAPI.registerTransportPipesContainer(Location, TransportPipesContainer);

//unregisters a custom container block
PipeAPI.unregisterTransportPipesContainer(Location);
```

In addition to this methods, there are several events you can use to get notified about important things:
* **PipeExplodeEvent** - gets called when a pipe explodes due to too many items inside it. This event is not called when a pipe explodes because of a natural explosion.
* **PlayerPlacePipeEvent** - when a player places a pipe.
* **PlayerDestroyPipeEvent** - when a player destroys a pipes.
* **PipeConnectionsChangeEvent** - gets called when a pipe changes its connections count. For example when a container block or another pipe is placed next to it.