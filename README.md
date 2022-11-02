# Tuberias-Yayicraft-Wiki
![Logo](https://github.com/teinac2012/Transport-Pipes-Wiki/raw/master/nuevo_cartel_comunidad.png))

El complemento YayiTuberias agrega varias tuberías diferentes a Minecraft. Actualmente hay tubos de colores, tubos dorados, tubos de hierro, tubos de extracción, tubos vacíos, tubos de hielo y tubos de artesanía. Al igual que el mod BuildCraft, estas tuberías pueden transportar cualquier tipo de artículo. En el siguiente wiki, aprenderá cómo crear y usar estas tuberías y cuál es la diferencia entre esos tipos de tuberías. También se describe información básica sobre los comandos y la configuración del complemento.


## Funciones
Como se explicó anteriormente, debe usar diferentes tipos de tuberías en diferentes situaciones. Cada tipo de tubería y su propósito se enumeran a continuación:
* **Tubo de extracción**: Este tubo es el único que puede extraer elementos de los bloques de contenedores. Los bloques de contenedores son bloques que contienen inventarios: cofres, hornos, tolvas, cajas de shulker, etc. Las tuberías de extracción no se conectan entre sí, pero sí se conectan con todas las demás tuberías y, por supuesto, con bloques de contenedores. Una tubería de extracción solo tiene una dirección de extracción de donde extrae elementos. Esta dirección se muestra mediante una textura de conexión diferente. Puede cambiar la dirección del extracto, así como la condición del extracto, haciendo clic con el botón derecho en la tubería con una llave inglesa y eligiendo la opción deseada. La opción extraer cantidad le permite extraer varios elementos en un solo tick. Puede filtrar qué elementos se extraen utilizando la interfaz de filtro (explicada en detalle en la sección Tubería dorada). Por último, pero no menos importante, la condición de extracción determina cuándo extraer elementos. Hay tres condiciones de extracción:
    * **Necesita Redstone**: La tubería solo extrae elementos si está alimentada con una señal Redstone..
    * **Extraer siempre**: La tubería siempre extrae elementos independientemente de si está alimentada con Redstone o no.
    * **Nunca extraer**: la tubería nunca extrae elementos.
* **Tubo de color**:  Este es el tubo más simple. Su único propósito es transportar artículos. Sin embargo, puedes teñir este tipo de pipa. Las tuberías de diferentes colores se comportan de la misma manera, pero no se conectan entre sí. Por lo tanto, puede crear un sistema de tuberías complejo sin tener que preocuparse por dejar suficiente espacio entre las tuberías. La tubería de color blanco tiene un papel especial: es la tubería predeterminada y, por lo tanto, se conecta a cualquier otra tubería vecina.
* **Tubería de hielo**: La tubería de hielo transporta artículos de la misma manera que cualquier otra tubería. La única diferencia es la velocidad de transporte. Las tuberías de hielo transportan artículos cuatro veces más rápido que otras tuberías.
* **Tubería de hierro**: Las tuberías de hierro son básicamente "tuberías unidireccionales". Independientemente de la dirección de la que provenga un elemento, siempre se moverá en la dirección de salida deseada. Puede cambiar esta dirección de salida haciendo clic con el botón derecho en la tubería con una llave inglesa. Esta dirección de salida está marcada por una textura amarilla.
* **Void Pipe**: Void Pipes simplemente destruye todos los elementos que se mueven dentro de ellos.
* **Crafting Pipe**: El Crafting Pipe te da la posibilidad de automatizar los procesos de elaboración. Después de especificar una receta de elaboración, todos los elementos que ingresan a esta tubería se almacenarán en caché y el elemento resultante se elaborará tan pronto como se almacenen suficientes ingredientes en su interior. Al hacer clic con el botón derecho en esta tubería con una llave inglesa, primero puede definir la dirección de salida en la que irán los elementos elaborados, en segundo lugar, puede ver los elementos almacenados en caché, utilizados para crear el elemento de resultado y, por último, pero no menos importante, puede definir la receta de elaboración.
* **Tubo de oro**:  El tubo de oro puede ordenar artículos. Cada dirección de salida en la tubería dorada tiene un color específico. Al hacer clic con el botón derecho en esta tubería con una llave inglesa, se abre un inventario de clasificación. Puede colocar elementos allí para determinar qué elementos deben ir a dónde. Cada fila de este inventario se refiere a una dirección de salida de la Tubería Dorada. El color indica qué fila se refiere a qué dirección de salida. Al hacer clic en un indicador de color (bloque de lana) dentro de este inventario, puede cambiar el modo de filtro y el rigor del filtro para esta dirección de salida. El rigor del filtro determina qué tan estricto es comparar elementos al calcular la dirección de salida deseada para un elemento entrante y el modo de filtro proporciona información sobre cómo se debe aplicar este filtro.

Existen los siguientes modos de filtro:
  * **Normal**: el modo de filtro predeterminado. Solo acepta un elemento si encaja con al menos un elemento de filtro dentro de esta fila
  * **Invertido**: compara los elementos de la misma manera que el modo de filtro normal, pero invierte el resultado, lo que bloqueará todos los elementos excepto los que están dentro de esta fila de filtro
  * **Bloquear todo**: simplemente bloquea todos los elementos

Existen las siguientes opciones de rigor del filtro:
  * **Material del artículo**: solo comprueba si el material del artículo encaja con el elemento de comparación de filtros (ignora los metadatos)
  * **Material y metadatos del artículo**: comprueba si el elemento de comparación es exactamente el mismo que el elemento comprobado

En general, todas las tuberías pueden colocar elementos en bloques de contenedores si están conectados a ellos, pero solo las tuberías de extracción pueden extraer elementos de los bloques de contenedores. También como se mencionó muchas veces anteriormente, para configurar tuberías necesita una llave inglesa. La receta de elaboración de la llave inglesa se da a continuación. La llave se puede utilizar simplemente haciendo clic con el botón derecho en la tubería deseada.

Cada tubería se puede ofuscar con un bloque sólido simplemente haciendo clic derecho en la tubería con un bloque en la mano. Esto colocará el bloque en la ubicación de las tuberías y, por lo tanto, lo ofuscará. Aunque una tubería ofuscada no será visible en este estado, todavía funciona normalmente. Por lo tanto, esta característica de ofuscación se puede utilizar para aumentar FPS en un sistema de tuberías complejo. Simplemente rompa el bloque como de costumbre para deshacer la ofuscación. Para revelar simplemente tuberías ofuscadas durante un par de segundos sin deshabilitar la ofuscación, simplemente haga clic con la llave inglesa en la mano.

## Elaboración de recetas
La elaboración de recetas se puede deshabilitar en el archivo de configuración, lo que le permite usar cualquier complemento externo de "recetas personalizadas" para implementar diferentes recetas. Sin embargo, las siguientes recetas son las predeterminadas:

### Tubo de color:
![White Pipe](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/master/src/main/resources/wiki/recipes/white.png)
![Colored Pipes](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/master/src/main/resources/wiki/recipes/colors.gif)

### Golden Pipe:
![Golden Pipe](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/master/src/main/resources/wiki/recipes/gold.png)

### Iron Pipe:
![Iron Pipe](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/master/src/main/resources/wiki/recipes/iron.png)

### Extraction Pipe:
![Extraction Pipe](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/master/src/main/resources/wiki/recipes/extraction.png)

### Ice Pipe:
![Ice Pipe](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/master/src/main/resources/wiki/recipes/ice.png)

### Void Pipe:
![Void Pipe](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/master/src/main/resources/wiki/recipes/void.png)

### Crafting Pipe:
![Crafting Pipe](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/master/src/main/resources/wiki/recipes/crafting.png)

### Wrench:
![Wrench](https://raw.githubusercontent.com/RoboTricker/Transport-Pipes/master/src/main/resources/wiki/recipes/wrench.png)
