Este es el registro de lo aprendido durante un curso de codo a codo 4.0. En este readme escribiré algunos conceptos/información que me parece importante tener a mano para poder recurrir a ellos si los olvido. 

Clase 3 
HTML- Title-Meta-Favaicon-Rutas absolutas y relativas-Iframe 

En la carpeta img se guardan las imagenes;
Debemos tener el orden en la pc: saber en donde guardamos las cosas en el disco;

RUTAS ABSOLUTAS Y RELATIVAS:

Las **rutas absolutas**: Son rutas que se generan desde la particion de mi disco. Desde la raiz del disco. Ej: C:\Users\Nadia\Desktop\Codo-a-codo\Mi-primera-web\img\pizza.webp
Es importante no usarlas, porque no van a funcionar en las maquinas de los clientes. Solo funcionan en mi máquina.

Las **rutas relativas**: Son las direcciones de mi pc, pero es algo que depende de otro recurso. Es relativa a un archivo. Dentro del archivo index.html, tengo que tomar ese archivo como punto de partida para recorrer. En el caso de la imagen de la piza deberia subir: img/pizza.webp
Puedo *acceder* a la ruta desde el index, haciendo ctrl + espacio.
Sirven para levantar videos, audios, documentos locales de tu computadora. El contenido se referencia en src de manera relativa.- 

PARA QUE EL ENLACE SE ABRA EN UNA NUEVA PESTAÑA:
Necesito colocar el atributo target="_blank" 

PARA SUBIR A CARPETAS ANTERIORES: ../ tantas veces como necesite. 

**Incrustar** contenido de otros sitios web: <iframe> en el boton compartir, tengo la opcion de incrustar, o embeber (embed), lo copio y lo pego en donde quiera que aparezca en mi pagina.- 
Puedo incrustar tambien un **boton de pago de mercado pago** la manera de incrustarlo depende de cada app

CLASE 4 
CSS - INTEGRACION DE SELECTORES - PROPIEDADES COLORES

Sintaxis: 3 elementos - Selectores, propiedades y valores.

Selector: refiere a uno o mas elementos del html (puede ser una clase, un id)
Propiedades: Valor. La propiedad refiere a lo que quiero cambiar: un color de letra, un color de fondo, una imagen de fondo, un borde, un tamaño de letra, un margen interno o externo. De cada propiedad se espera un valor. Cada par propiedad-valor se separa con un ; y van encerrados entre {}. 

Hay 3 formas de integrar css 
1- Css en linea embebido en HTML
 
En el caso de mi receta quedaria: 
<p style="color: red; text-align: center;">Lorem</p>

Me sirve para casos muy específicos cuando necesito cambiar algo muy puntual (quizás). No va porque se mezcla css con html. 

2- Internal CSS
En el head escribir una etiqueta <style> con sus selectores, propiedades y valores:

<style>
    p {
        color: red;
        text-align: center;
    }
</style>

3- Integrarlo en un archivo externo: Esta manera es la más recomendada.
Se hace en una carpeta aparte, luego se vincula el html con el css. En el head se crea la etiqueta link y la referencia a la carpeta css:

<link rel="stylesheet" href="css/estilo.css">

luego dentro de la carpeta css y la hoja de estilo estilo.css se referencia la etiqueta a la cual queremos darle un estilo específico:
para los párrafos tendremos:

SELECTORES POR ETIQUETA:

p {
    color: red;
    text-align: center;
}

para los enlaces:
a {
    color: rgb(247, 26, 63);

}

Propiedades:
*Color*: Podemos buscar color picker en google, y generar o buscar los colores. O con la app INSTANT EYEDROPPER para copiar colores como un cuentagotas.

*Align*: con ctrl+espacio me tira las opciones posibles.

*Text-decoration*: underline; Para subrayar.

*font-weight*: bold; Para poner la fuente en negrita

SELECTORES POR CLASE:
en la etiqueta HTML le agrego la class="nombredelaclase"
en el css agrego el nombre de la clase, anteponiendole un . y agrego las propiedades- valores ej: 

.verde-subrayado {
    color: rgba(7, 241, 31, 0.784);
    text-decoration: underline;
}

Para poner escritura en negrita le cambio el nombre a la clase y las propiedades:

.verde-negrita {
    color: rgb(8, 223, 29);
    font-weight: bold;
}

Para combinar dos clases en la etiqueta HTML debo escribirlas separadas por un espacio; por ello tambien es importante no separar los nombres de una clase con espacios, sino con un guión porque si no lo toma como dos clases separadas. Ej:
<p class="rojo verde-negrita"> 

SELECTORES POR ID:
Me permite asegurarme que ese estilo se aplique solo a un elemento y no a otro. Cada id es único. Si quiero seleccionar mas de un elemento, entonces utilizo clases.-

La alineacion funciona para los párrafos, no para los links. Para ponerle color y alineacion si los tengo encerrados entre <p> debo usar dos #. 

En css podemos ser tan restrictivos que podemos mandar a "buscar" la clase y dentro de ella las etiquetas que querramos, ej:

#recetaCaC a {
    color: rgb(167, 159, 1);
}

Todo lo que se puede cambiar con css puedo encontrar las propiedades en **w3school-css-Reference-Properties**

MULTICURSORES: Alt+clic
Palabras recurrentes que quiero marcar: ej: rojo las marco y ctrl+d tantas veces hasta llegar al final y marca todas las palabras "rojo" y puedo cambiar el nombre.-

CLASE 5
BLOCK INLINE DISPLAY STRONG EM UNIDADES PX EM REM

**Diferencia entre elementos de linea y elementos de bloque**

Los elementos de **bloque** ocupan todo el ancho disponible. Los proximos elementos se posicionan debajo, en una linea diferente, en un nuevo renglon. Son como cajas que ocupan todo el ancho posible de su contenedor y se apilan una debajo de la otra. 

-h1, h2
-Párrafos
-div
-video
-header
-elementos de una lista


Los elementos de **linea** se comportan ocupando solo un espacio, sin saltar a otra linea de abajo. Si no uno a continuacion de la otra. 

-Enlaces
-Imagenes
-Inputs
-br

Un elemento de línea no puede contener un elemento de bloque adentro, pero sí esto puede ser al reves. 

Para disponer elementos de linea en bloque, utilizando css puedo colocar:

img {
    display: block;
}

en este caso utilizamos los selectores por etiqueta, pero puedo usarlas por clase o id.

Puedo seleccionar varios elementos separandolos por comas ej : 
h1, h2 {
    display: inline;
}

Propiedad **inline-block**: Despliega mitad bloque, mitad en linea. Se le puede establecer un alto y un ancho al elemento. Lo trata como una caja en linea.- Se le puede establecer tambien margenes internos y externos. No añade un salto de linea, si no que se siguen posicionando uno al lado del otro. 

Css ---> Como se tienen que ver las cosas
HTML ---> Qué es cada cosa

Para marcar énfasis en una palabra, o que los buscadores se detengan en esa palabra utilizo la etiqueta <strong>:
<strong>consectetur</strong>

Para darle énfasis tambien puedo usar la etiqueta <em></em> (em de enfasis, marcar algo con énfasis como strong- como utilizaría la itálica)

Establecer TAMAÑOS DE FUENTES
Propiedad font-size
El valor que tiene que tener es un valor con una unidad absoluta o relativa.- 

En pixeles: Creo una clase y en css la detallo:

#especial {
    font-size: 20px;
}

Unidades absolutas: Son fijas. Son estáticas, no cambian según el dispositivo en el que yo vea el sitio.
Cm, mm, pulgadas, puntos, pica, pixeles.
Los pixeles son relativos, depende en que dispositivo lo vea los puedo distinguir o no... No dejan de ser medidas absolutas. Llega el momento en el que esto se ve afectado por la diversidad de dispositivos disponibles y necesito utilizar una unidad de medida relativa 

UNIDADES RELATIVAS:
Especifican su longitud, dependiendo de otra:

em: Es una medida relativa y equivale al tamaño actual de la fuente: 16 px. Toma el valor de su ancestro (etiqueta) más cercana.

rem: La referencia es al html. Es relativo siempre al font-size del html.
Para las fuentes es conveniente usar em y rem. 

Porcentaje: Se maneja como el em: si quiero 1em = 100%   2em = 200%    0.5em = 50%.

16px = 1em = 100%

Los h1, h2, h3 están basados en em. 