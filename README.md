# HTML

HTML (HyperText Markup Language), es un lenguaje de marcado para estructurar o maquetar páginas web y/o apps moviles. La versión más actual es HTML5 con nuevas etiquetas con significado semantico, uso de audio y vídeo sin necesidad de plugins y mucho más. Para ver las diferencias de versiones, visite [el artículo de wikipedia sobre HTML5: Diferencias entre HTML5 y HTML4/XHTML](http://es.wikipedia.org/wiki/HTML5#Diferencias_entre_HTML5_y_HTML4.2FXHTML).

## Tabla de contenido

- [Estructura base de un archivo en HTML5](#estructura-base-de-un-archivo-en-html5).
- [Estructura base HTML5 y Bootstrap](#estructura-base-html5-bootstrap).
- [LLamar un archivo CSS](#llamar-un-archivo-css).
- [Llamar un archivo JS](#llamar-un-archivo-js).
- [Etiqueta header](#etiqueta-header).
- [Etiqueta nav](#etiqueta-nav).
- [Etiqueta section](#etiqueta-section).
- [Etiqueta article](#etiqueta-article).
- [Etiqueta aside](#etiqueta-aside).
- [Etiqueta footer](#etiqueta-footer).
- [Etiqueta figure](#etiqueta-figure).
 - [Etiqueta figcaption](#etiqueta-figcaption).
- [Etiqueta video](#etiqueta-video).
- [Etiqueta audio](#etiqueta-audio).
- [Etiqueta canvas](#etiqueta-canvas).
- [Etiqueta hgroup](#etiqueta-hgroup).
- [Etiqueta word break](#etiqueta-word-break).
- [Etiqueta time](#etiqueta-time).
- [Entidades HTML](#entidades-html).
- [Microdatos](#microdatos).
- [Hacer anclajes](#hacer-anclajes).
- [Listas de definición](#listas-de-definicion).
- [Estructura base de una tabla](#estructura-base-de-una-tabla).
- [Ejemplo de un formulario en HTML](#ejemplo-de-un-formulario-en-html).
- [Referencias](#referencias).
- [FAQs](#faqs).
	- [¿Cómo está compuesto un diseño web?](#como-esta-compuesto-un-diseno-web).
	- [¿Que diferencia existe entre la etiqueta strong vs b?](#diferencia-entre-la-etiqueta-strong-vs-b).
	- [¿Que diferencia existe entre la etiqueta em vs i?](#diferencia-entre-la-etiqueta-em-vs-i).

## Estructura base de un archivo en HTML5
```html
<!DOCTYPE html>
<html lang="es-ES"> 
	<head>
		<meta charset="UTF-8">
		<meta name="description" content="160 caracteres max.">
		<meta name="viewport" content="width=device-width, initial-scale=1"> <!-- Controla el comportamiento de la ventana del dispositivo. -->
		<title>70 caracteres max.</title>
		<!--[if lt IE 9]><script src="dist/html5shiv.min.js"></script><![endif]-->
		<link href="folder/favicon.ico" rel="icon" />
		<link rel="stylesheet" href="tuarchivo.css" />  <!-- El atributo type="text/css" y media ="valor" son opcionales -->
	    <script src="tuarchivo.js"></script>
	</head>
	<body>
		<header>
			<h1>Uno solo por documento.</h1>	<!-- También es común encontrar un menú en el cabecero: -->
			<nav>
				<ul>
					<li><a href="#">Home</a></li>
					<li><a href="#">About</a></li>
					<li><a href="#">Contact</a></li>
				</ul>
			</nav>
		</header>
		<section> 
			<!-- permite dividir el contenido del sitio en varias secciones. Ejemplo: 
			Un blog tiene un section para el post y otro para el gestor de comentarios -->
			<article> 
				<!-- Para definir contenido independiente, ejemplo: Si tenemos 1 post y
				10 comentarios, entonces tenemos 2 <section>, uno para el post y otro para el gestor de comentarios y 11 <article> uno por cada comentario. -->
			</article>
			<aside>
				<!-- Lo que no hace parte del contenido principal de nuestro sitio web y
				puede ir en cualquier parte de la estructura. -->
			</aside>
		</section>
		<footer>
			<!-- Exclusivo para el pie de página como el copyright y repetir el menú principal-->
			<nav>
				<ul>
					<li><a href="#">Home</a></li>
					<li><a href="#">About</a></li>
					<li><a href="#">Contact</a></li>
				</ul>
			</nav>
		</footer>
	</body>
</html>
```

## Estructura base HTML5 Bootstrap

```html
<!DOCTYPE html>
<html lang="es">
<head>
	<meta charset="UTF-8">
	<meta name="description" content="160 caracteres max.">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>70 caracteres max.</title>
  	<!--[if lt IE 9]>
    		<script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
    		<script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
	 <![endif]-->
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">
	<link rel="stylesheet" href="../css/custom.css"><!-- Tus propios estilos -->
	<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js"></script>
	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
</head>
<body>
	<div class="container">
		<div class="row">
			<!--columns here-->
		</div>
	</div>
</body>
</html>
```
## LLamar un archivo CSS

Colocar dentro de la etiqueta `<head>` y debajo del `<title>` la siguiente linea de código:

**Sintaxis**:

`<link rel="stylesheet" href="tuarchivo.css" />`

## Llamar un archivo JS

Colocar dentro del `<head>` y debajo de los archivos CSS llamados la siguiente linea de código:

**Sintaxis**:

`<script src="tuarchivo.js"></script>`

Algunos llamados de archivos en JS es mejor insertarlos antes de cerrar la etiqueta `</body>`, como por ejemplo el uso de la librería jQuery.

## Etiqueta header

Es una de las novedades de la versión HTML5 y sirve para estructurar el cabecero de nuestro sitio web.

**Sintaxis:**

```html

<header>Título, logo, etc...</header> <!-- dentro de la etiqueta <body></body> -->

```

## Etiqueta nav

Etiqueta nueva desde la versión 5 de HTML y se usa para referir en nuestra estructura el menú de navegación de nuestro sitio web. Esta etiqueta se puede usar en cualquier parte de nuestra estructura, pero es común verla dentro de la etiqueta `<header></header>`

**Sintaxis:**

```html

<header>
	<nav>
		<ul>
			<li>Enlace 1</li>
			<li>Enlace 2</li>
			<li>Enlace 3</li>
		</ul>
	</nav>
</header>

```

## Etiqueta section

Etiqueta nueva desde la versión HTML5 y en ella se coloca todo el contenido de nuestra web.

**Sintaxis:**

```html

<section>
contenido de mi web.
</section>

```

## Etiqueta article

Etiqueta nueva desde la versión HTML5 y sirve para colocar todos los artículos de nuestro sitio web. Es común ver esta etiqueta dentro de la etiqueta `<section></section>`, aunque no es obligatorio.

**Sintaxis:**

```html

<section>
	<article>
		<h2>Titulo de articulo 1</h2>
		<p>Lorem ipsu...</p>
	</article>
	<article>
		<h2>Titulo de articulo 2</h2>
		<p>Lorem ipsu...</p>
	</article>
</section>


```

## Etiqueta aside

Sirve para estructurar toda la infomación que no es tan relevante en nuestro sitio web, ejemplo: las columnas laterales que traen banners, acceso de usuario, etc... Puede ir en cualquier parte de la estructura dentro de la etiqueta body.

**Sintaxis:**

```html

<aside>
	banners, login, enlaces secundarios, etc...
</aside>

```

## Etiqueta footer

Una de las novedades de HTML5, la cual se utiliza para estructurar nuestro pie de página y colocar todas las amenazas de copyright, repetición del menú principal, contacto, etc...

**Sintaxis:**

```html

<footer></footer> <!-- dentro de la etiqueta <body></body> -->

```


## Etiqueta figure

Sirve para insertar imágenes.

Dentro del `<body>` se coloca las siguientes lineas de código:

**Sintaxis**:

```html
<figure id="">
	<img src="" width="" height="" alt="" />
</figure>
```

Se recomienda ponerle un id a la etiqueta `<figure>`.

### Etiqueta figcaption

Sirve para ponerle una descripción a la imagen dentro de la etiqueta figure.

**Sintaxis:**

```html
<figure id="">
	<img src="" width="" height="" alt="" />
	<figcaption>Just description of the image...</figcaption>	
</figure>
```


## Etiqueta video

Se inserta con la etiqueta `<video>` dentro del `<body>`.  Debe tener una id para estilos, un ancho y alto para visualizar el video. El elemento **controls** nos permite tener funciones adicionales por medio de botones en el vídeo, ejemplo: botón play, stop, etc…

**Sintaxis**:

```html
<video id="mejorandola" width="640" height="320" controls> <!-- atributos adicionales: autoplay, loop, preload, muted, poster [cargar una imagen de presentación] -->
	<source src="video.mp4" type="video/mp4" /><!-- Formato de video H.264 -->
	<source src="video.webm" type="video/webm" /> <!-- Formato de video WebM -->
	Su navegador no soporta video en HTML5.
</video>
```

## Etiqueta audio

Para insertas un reproductor de audio en nuestro sitio web.

Formatos compatibles:

1. Mp3.
2. Ogg.
3. Wav.

**Sintaxis:**

```html
<audio controls> <!-- preload autoplay lopp -->
	<source src="track.mp3" type="audio/mp3" />
	<source src="track.ogg" type="audio/ogg" />
	Su navegador no soporta audio en HTML5.
</audio>
```

**Parámetros adicionales:**
- preload: Descarga el archivo en el reproductor sin necesidad de darle play. Tiene tres opciones de configuración:
 - preload="auto" carga el archivo sin necesidad de darle play.
 - preload="metadata" carga solo la información del archivo. 
 - preload="none" no hacer nada.
- autoplay: Inicia el reproductor automáticamente. Si este atributo esta en uso, el preload no tendrá efecto alguno.
- loop: Repite el audio automáticamente. 

## Etiqueta canvas

Sirve para dibujar directamente en nuestro sitio web, con la ayuda de javascript. Al final, el dibujo se convierte en una imágen de mapas de bits o imágen matricial.

Ejemplo:

```html

<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;">
Tu navegador no soporta canvas.
</canvas>
<script type="text/javascript">
var x = document.getElementById("myCanvas");
var ctx = x.getContext("2d");
ctx = fillStyle="blue";
ctx = fillRect=(50, 10, 200, 100);
</script>

```


## Etiqueta hgroup

Sirve para asociar encabezados (h1, h2,... h6) que tiene relación entre ellos, por ejemplo:

```html
<h1>Titulo del sitio web o encabezado de artículo</h1>
<h2>Slogan del sitio o subtítulo</h2>
```

Sintaxis:

```html
<hgroup>
	<h1>Titulo del sitio web o encabezado de artículo</h1>
	<h2>Slogan del sitio o subtítulo</h2>
</hgroup>
```

## Etiqueta word break

Sirve para romper una palabra usualmente larga en dos o más veces, usando la etiqueta `<wbr>`

**Sintaxis:**

```html

<p>Estoesuna<wbr>palabramuy<wbr>larga</p> <!--Simplemente lo introducimos donde queremos romper la palabra en dos o más veces-->

```

## Etiqueta time

Sirve para darle a entender al navegador, un indexador o un buscador que lo que esta encerrado dentro de dicha etiqueta, hace referencia de tiempo.

**Sintaxis:**

```html

<p>Hoy es <time>2015-03-01</time></p>

```

**Otro ejemplo:**

```html

<p><time datetime="2015-03-01">Hoy</time> es el evento de lanzamiento del nuevo producto</p>

```

## Entidades HTML

Algunos caracteres no pueden ser visualizados en un navegador con HTML. Algunos de estos son:

- Los caracteres que utiliza HTML para definir sus etiquetas (<, > y ") no se pueden utilizar libremente.
- Los caracteres propios de los idiomas que no son el inglés (ñ, á, ç, ¿, ¡, etc.) pueden ser problemáticos dependiendo de la codificación de caracteres utilizada.

La solución a la primera limitación consiste en sustituir los caracteres reservados de HTML por unas expresiones llamadas **entidades HTML** y que representan a cada carácter:

![Entidades en HTML](https://github.com/victorhtorres/ingenieria-informatica/blob/master/html/images/entidades-html.png?raw=true)

Para mostrar correctamente los caracteres de la imagen de ejemplo en el contenido de una página HTML, se debe sustituir cada carácter especial por su entidad HTML en el documento. Ejemplo:

```html
<p>Para iniciar un documento HTML5, se debe colocar <!DOCTYPE html> como primera línea del código</p>
```
por

```html
<p>Para iniciar un documento HTML5, se debe colocar &lt;!DOCTYPE html&gt; como primera línea del código</p>
```

La solución a la segunda limitación es simplemente guardando nuestro documento HTML con formato `utf-8` o intercambiando el caracter conflictivo por su entidad. Alguno de ellos:

![Entidades en HTML](https://github.com/victorhtorres/ingenieria-informatica/blob/master/html/images/entidades2-html.png?raw=true)

## Microdatos

Los microdatos se usan para darle sentido semantico a ciertas partes de nuestra información, la cual estas carecen de una etiqueta creada en HTML5, como por ejemplo, cuando usamos la etiqueta `<header>` le decimos al navegador y a los buscadores que este es el cabecero de mi sitio web, pero si dentro de mi información está mi nombre o formas de contacto, pues el navegador y los buscadores no lo van a saber interpretar como lo que son y para eso se usa los microdatos.

Ejemplo:


```html

<div itemscope itemtype="http://schema.org/Person">
	<h1 itemprop="name">My name</h1>
	<img itemprop="photo" src="profile.png" alt="This is me" />
</div>

```

Requiere de tres elementos:

1. itemscope: Le dice al navegador que esto es un contenedor de datos.
2. itemtype: Donde sacamos la definición de los datos. Para eso, existe la colección de esquemas de http://schema.org/.
3. itemprop: El dato referido.

Microdatos anidados:

```html

<div itemscope ItemType = "http://schema.org/Movie">
  <h1 itemprop = "nombre" & g; Avatar </h1>
  <div itemprop = "director" itemscope ItemType = "http://schema.org/Person" >
  Directora: <span itemprop = "nombre"> James Cameron </span> (nacido <span itemprop = "fecha de nacimiento" > 16 de agosto 1954) </span>
  </div>
  <span itemprop = "género"> Ciencia ficción </span>
  <a href="../movies/avatar-theatrical-trailer.html" itemprop="trailer"> </a> Remolque
</div>

```

## Hacer anclajes

Su uso es muy importante si queremos realizar una especie de tabla de contenido en un artículo muy extenso, en la cual, cada item de la tabla tenga un enlace que nos lleve directamente al contenido de interés.

Consiste de dos partes:

1. Colocar una referencia al título que llevará el anclaje.
2. Poner la referencia en el contenido que se desea llegar con el título anclado.

Sintaxis:

```html

<a href="#nombre_referencia">Item 1</a>		<!-- En la tabla de contenido -->

```

```html

<a name="nombre_referencia">			<!-- Contenido enlazado al título anclado -->

```

## Listas de definicion

Se emplea para definirle a cada elemento de una lista terminos y definiciones (como un diccionario) y se construye con las etiquetas dl, dt y dd.

- La etiqueta dl define la lista de definición.
- La etiqueta dt se emplea para definir los términos o títulos de los elementos de una lista de definición.
- La etiqueta dd se emplea para indicar las definiciones de los elementos de una lista de definición.

Ejemplo:

```html
<dl>
	<dt>Ingeniero informático:<dt>
		<dd>Su mayor interés es aprender como funciona la caja negra.</dd>
	<dt>Ingeniero de Sistemas:</dt>
		<dd>Su mayor interés es construir dicha caja negra.</dd>
</dl>

```

Resultados en un navegador:

![Imagen de muestra de una lista de definición](https://github.com/victorhtorres/ingenieria-informatica/blob/master/html/images/ejemplo-listas-de-definicion.png?raw=true)


## Estructura base de una tabla

```html

<table>									<!-- Una tabla se compone de dos partes: Encabezado y cuerpo. Opcional: pie -->
  <caption>Título de la tabla</caption>
  <thead>								<!-- Creamos el encabezado. -->
    <tr>								<!-- Creamos una fila en la tabla. -->
    	<th>Serie de tv</th>			<!-- Título de la primera columna o celda -->
    	<th>Cadena</th>
    	<th>Calificación por edades</th>
  </tr>									<!-- Fin de la primera fila. -->
</thead>								<!-- Fin del encabezado de la tabla. -->
  <tbody>								<!-- Inicio del cuerpo de la tabla. -->
    <tr	>								<!-- Segunda fila de la tabla creada. -->
      <td>The walking dead</td>			<!-- segunda celda de la primera columna. -->
      <td>AMC</td>						<!-- Segunda celda de la segunda columna -->
      <td>TV-14</td>
    </tr>
    <tr>								<!-- Tercer fila... -->
      <td>Braking bad</td>				<!-- tercera celda de la primera columna. -->
      <td>AMC</td>
      <td>TV-14</td>
    </tr>
    <tr>
      <td>Game of thrones</td>
      <td>HBO</td>
      <td>TV-14</td>
    </tr>
  </tbody>								<!-- Fin del cuerpo de la tabla -->
<!--  <tfoot>		// Ponerle un pie a la tabla es opcional y por lo general se usa para totalizar datos.
    <tr>
      <td></td>
      <td></td>
      <td></td>
    </tr>
  </tfoot> -->
</table>								<!-- Fin de la tabla -->
<!-- Puede usar el atributo <td colspan="valor"> para combinar celdas -->

```

## Ejemplo de un formulario en HTML


```html
<form method="POST" action="enlace_otro_archivo">		<!-- El atributo action se conecta con un archivo php,
 asp, etc... para recibir y procesar la info. del formulario -->
	<fieldset>			<!-- Agrupa controles que tiene alguna relación -->
		<legend>Datos personales</legend>		<!-- Titulo al fieldset -->
		<p><label for="nombre">Nombre: <input type="text" id="nombre" name="nombre" maxlength="15" required></label></p>
		<!-- label sirve para darle título al control (en este caso input),
		 al igual que darle estructura a nuestro formulario y también, 
		 al darle clic al título, activa la casilla. El id se utiliza para
		  ser reconocido por javascript. El for debe llamarse igual al id.
		  El atributo name es de referencia para el servidor. El atributo 
		  maxlength le da un maximo de tamaño de caracteres a ingresar. -->
		<p><label for="correo">Correo: <input type="email" id="correo" name="correo"></label></p>
		<p><label for="telefono">Teléfono: <input type="text" id="telefono" name="telefono"></label></p>
	</fieldset>
	<fieldset>
		<legend>Estado civil</legend>
		<p><label> <input type="radio" name="estado" value="Soltero">Soltero</label></p>
		<p><label> <input type="radio" name="estado" value="Casado">Casado</label></p>
		<p><label> <input type="radio" name="estado" value="UnionLibre">Unión Libre</label></p>
	</fieldset>
	<fieldset>
	  <legend>Intereses</legend>
	  <p><label> <input type="checkbox" name="interest" value="Deporte"> Deporte </label></p>
	  <p><label> <input type="checkbox" name="interest" value="Internet"> Internet </label></p>
	  <p><label> <input type="checkbox" name="interest" value="Viajes" checked=""> Viajes </label></p>	<!-- checked selecciona
	   un valor como predefinido -->
	  <p><label> <input type="checkbox" name="interest" value="Programación"> Programación</label></p>
	</fieldset>
	<p>Profesonal en: 
		<select name="profesional" multiple=""> <!-- Crea una lista desplegable y el
		 atributo miltiple (opcional) los muestra todos a la vez -->
			<option value="pro1">Administración de Empresas</option>
			<option value="pro2" selected="">Ingeniería Industrial</option>
			<option value="pro3">Igeniería Informática</option>
			<!--Existe otro atributo para organizar las opciones por grupos, con <optgroup> Ejemplo:
			<optgroup label="Europa">
				<option value="DE">Alemania</option>
				<option value="FR">Francia</option>
			</optgroup>
			<optgroup label="America">
				<option value="CO">Colombia</option>
				<option value="CH">Chile</option>
			</optgroup>
		-->
		</select>
	</p>
	<p><label for="aboutme">Acerca de mi: <textarea name="aboutme" id="aboutme" cols="50" rows="5" maxlength="1000">  </textarea></label></p>
	<p><input type="submit" value="Enviar"></p>
	<p><input type="reset" value="Borrar todo"></p>
	<p><button type="submit">Enviar</button><!-- Otra forma de crear botones de formulario con la ventaja de que puedo ponerle imagenes, iconos, etc... -->
	<p><input type="hidden" name="sitio" value="Este formulario fue enviado desde el sitio: tusitio.com" /></p><!-- No visible para el usuario pero si para el backend o donde envien la información -->
</form>

````

## Referencias

- [Curso de diseño web en Mejorandola](https://cursos.mejorando.la/diseno-web-online).
- [Codificación de caracteres en Librosweb](http://librosweb.es/xhtml/capitulo_3/codificacion_de_caracteres.html).
- [Diferencia entre etiqueta strong y b por Desarrolloweb.com](http://www.desarrolloweb.com/faq/diferencias-etiquetas-b-strong.html).
- [Formatos en HTML por W3school](http://www.w3schools.com/html/html_formatting.asp).
- [Listas de definicion por librosweb](http://librosweb.es/xhtml/capitulo_5/listas_de_definicion.html).
- [Codecs de video por Mozilla](https://developer.mozilla.org/es/docs/HTML/Formatos_admitidos_de_audio_y_video_en_html5).
- [Microdatos](http://www.marcofolio.net/webdesign/html5_microdata_what_is_it_and_why_should_you_care_.html).

## FAQs

### Como esta compuesto un diseno web

Todo empieza por la base de datos (MySQL, Postgres, MongoDB, etc...), luego tenemos el BACKEND con sus respectivos lenguajes de programación o frameworks (Php, Djando, Express.js, Node.js, Socket.io) y por último tenemos en FRONTEND (HTML5, CSS3, Javascript [jquery, y otros frameworks]) donde el único lenguaje de programación para el frontend es el Javascript y los demás son frameworks o lenguajes modelados de datos o estilos como HTML5 y CSS3.

### Diferencia entre la etiqueta strong vs b

Ambas etiquetas ponen en estilo negrita las palabras que se encierren en dichas etiquetas, pero cada una tiene un uso particular de semantica.

- Etiqueta strong: indica que el texto que engloba se tiene que reforzar (de mayor importancia). El navegador es el que interpreta cómo se debe mostrar un texto reforzado, más fuerte, y todos los navegadores han decidido que para mostrar un texto más fuerte lo que harán es poner una negrita. 

- Etiqueta b: indica una negrita y nada más que eso.

### Diferencia entre la etiqueta em vs i

Ambas etiquetas ponen en estilo cursiva las palabras encerradas en dichas etiquetas, pero cada una tiene un significado de semantica, al igual que las etiquetas p y strong.

- Etiqueta em: Para dar mayor importancia de énfasis en el texto.
- Etiqueta i: Define el texto en cursiva, sin ninguna importancia adicional.
