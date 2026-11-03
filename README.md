# Hola soy Alonso y esta es mi primera creacion en GitHub para probar como funciona y aprender.
## Esta es mi primera Web, con ayuda de Claude
Esta pagina la he creado con ayuda de Claude para las partes interactivas y diseño, puedo crear la parte del texto, titulos etc. Pero la parte interactiva aun no se hacerla, por eso hago esta prueba, la idea era crear una Web que hablara un poco de mi, sobre lo que estudio y proyectos que he hecho como este, la mayor complicacion fue entender GitHub. Yo queria tener una "pagina web propia" gratuita, que no sea un servicio como Netlify u otras que funcionan con usos limitados. La mayor complicacion fue entender como configurar y usar el GitHub. La primera configuracion fue la seccion Page de Settings, eso fue facil, el problema vino cuando yo queria modificar el index.
## El problema del index.html
Como norma general en cualquier sitio si tu quieres cambiar un archivo por otro que tenga el mismo nombre se remplaza, en GitHub no pasa eso, lo que tienes que hacer es eliminar el archivo anterior y meter el nuevo, es logico pero yo no queria ir perdiendo los cambios que hago para ver los avances y como iba aprendiendo. De esta manera descubri que se pueden añadir los cambios que haces y la descripcion y queda guardado con el dia y hora, pero aun asi no acaba de resolver mi problema, que queria tener los archivos antiguos guardados, asi que me puse a investigar y me di cuenta que puedes crear como una especie de carpetas y dentro de ellas guardar los archivos que quieras, asi arregle el problema.
## Funcionamiento del readme
Lo mas importante al hacer una pagina o simplemente hacer codigo es entender y saber que estas haciendo para saber explicarlo y que otras personas que lo vean sepan usarlo o modificarlo como quieran, el readme aunque sea algo que nadie lea y pasen de el totalmente es algo muy importante, es muy util si quieres explicar un error y como solucionarlo o explicar una linea de codigo que sea complicada, aunque tambien te sirve a ti mismo para saber lo que estas haciendo y como replicarlo. Pues por todo esto y mas cosas me vi en la obligacion de aprender a usar un poco el readme, no es como abrir un Word y ponerte a poner texto como un loco, hay unas pautas y trucos, por ejemplo para separar por titulos se pone "#" para el mas grande y principal y "##" para los subtitulos, asi se puede separar comodamente. Ademas de esto tambien hay que saber que tienes que decir y explicar, aqui solo importa como hiciste las cosas y si se conoce de algun error y su solucion. Yo no le daba importancia a esto hasta que empece a verlo y me di cuenta de que es realmente util.
## Errores 
Hablando de errores, revisando el index.html he visto dos cosas que podria arreglar, la pagina esta pensada para que dependiendo del tamaño de la pantalla y del dispositivo varie, para eso hice la regla: 
* 64:    .consola code {
* 65:    display: block; margin-top: .35rem; min-height: 1.5em;
* 66:    font: 500 1.05rem/1.5 "IBM Plex Mono", ui-monospace, monospace;
  
Pero esta regla ultima regla es pisada por otra que puse justo antes:
* 61:    .consola code { font-size: clamp(1.05rem, 2vw, 1.4rem); }

La solucion fue borrar la linea 61 entera, y si quisiera que aparezca en pantallas grandes cambiar en la linea 66 1.05rem por clamp(1.05.rem, 2vw, 1.4rem) y borrar la 61. Entonces de una u otra quedaria igual

Basicamente lo que hace clamp es adaptar el ancho de la pantalla pero sin pasarse por arriba ni por abajo, por eso lleva 3 valores, el mínimo, el ídeal y el máximo, en este orden. En mi caso el 1.05rem es lo mas pequeño que puede ser (1rem suelen ser 16px), 2vw es el tamaño que intenta tener, el 2% del ancho de la ventana (vw = viewport width), es decir si la ventana son 1000px pone 20px y 1.4re es lo mas grande que puede llegar a ser (unos 22px).

Explicado todo esto ahora al cambiarlo ya se arregla todo, tambien tuve un error que me olvide de cambiar al nombre a una cosa y a veces fallaba pero ya lo modifique y va perfecto. 
