TransportPipes provides a lightweight API for duct creation / destruction, putting items inside them and so on.
Let me know if you need any API extensions.

```java
//Builds a duct at the given location. Pass "pipe" as baseDuctTypeName and one of "white", "blue", "red", "yellow", "green", "black", "golden", "iron", "ice", "void", "extraction" or "crafting as ductTypeName.
//The rest should be self-explanatory.
TransportPipesAPI.getInstance()#buildDuct(String baseDuctTypeName, String ductTypeName, BlockLocation blockLocation, World world, Chunk chunk)

//Detroys the duct at the given location.
TransportPipesAPI.getInstance()#destroyDuct(BlockLocation blockLocation, World world)

//Returns the current ticks per second of the TransportPipes thread.
TransportPipesAPI.getInstance()#getTPS()

//Returns the preferred tps of the TransportPipes thread.
//If this value is equal to the real tps, the thread is running fine.
TransportPipesAPI.getInstance()#getPreferredTPS()

//Returns the amount of ducts in the given world.
TransportPipesAPI.getInstance()#getDuctCount(World world)

//Returns the duct object at the given location or null if there is no duct.
TransportPipesAPI.getInstance()#getDuct(BlockLocation blockLoc, World world)

//Puts "item" into the given pipe with a moving direction of "itemDirection".
TransportPipesAPI.getInstance()#putItemInPipe(Pipe pipe, ItemStack item, TPDirection itemDirection)

//Registers a custom container block at the given location. Every pipe around this block will try to extract/insert items from/into this container.
//Create your own implementation of the TransportPipesContainer interface in order to specify which items to extract and where inserted items should go.
TransportPipesAPI.getInstance()#registerTransportPipesContainer(TransportPipesContainer container, BlockLocation blockLocation, World world)

//Unregisters a custom container block. See TransportPipesAPI.getInstance()#registerTransportPipesContainer(TransportPipesContainer container, BlockLocation blockLocation, World world).
TransportPipesAPI.getInstance()#unregisterTransportPipesContainer(BlockLocation blockLocation, World world)

//Whenever a vanilla container block such as a normal chest, furnace or something like that is placed or destroyed programmatically such that TransportPipes does not know about this block change,
//call this method to update the internal TransportPipes container set. "placed" just says if the block was placed or destroyed.
TransportPipesAPI.getInstance()#updateVanillaContainerBlock(Block block, boolean placed)
```