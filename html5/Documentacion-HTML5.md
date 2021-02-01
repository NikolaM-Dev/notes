# Documentacion de HTML5

[toc]

## Vocabulario Web

- **IP:** Es el identificador numerico de una pagina web, es unico y representa la direccion donde esta el ordenador que contiene esa pagina web.
- **Dominio web / URL:** Uniform Resources locator. Es el nombre asociado a la IP que utilizamos para solicitar recursos, en nuestro caso un sitio web.
- **DNS:** Domain Name System. Es un servicio cuya principal funcion es traducion el nombre de dominio a su identificador unico.
- **Sitio Web:** Es un conjunto de uno o varios recursos web alojados en el mismo dominio.

- **Servidor web:** Es un ordenador cuyo objetivo es servir recursos web.

- **Hosting:** Es el almacenamiento del servidor web. El disco duro donde el servidor guarda los recursos.

- **Peticion:** Es la accion de pedir recursos a un servidor.

## Estructura de un Sitio Web

```html
<!-- Establece el tipo de estandar del documento (HTML5) -->
<!DOCTYPE html>

<!-- Inicio del documento HTML -->
<html lang="es">
<!-- Datos que le pasamos al navegador con información de nuestra página web -->

<head>
  <meta charset="UTF-8" />
  <title>Mi primera página web</title>
</head>

<!-- Representa todo el contenido de nuestra página web -->

<body>
  Body de nuestra página web en un servidor local
</body>

</html>
```

## Titulos y Parrafos

```html
<h1></h1> <!-- Etiqueta de Encabezados de h1 al h6 -->
<p></p> <!-- Etiqueta de Parrafos -->
```

Los encabezados en `html5` tienen ciertas propiedades y siguen una regla de descendencia por importancia, empezando con `h1` (Solo debe existir uno en todo la pagina) y sus descendientes dividiendo el contenido por importancia dandole un mensaje semantico.

_Ejemplo:_

``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Títulos y párrafos</title>
</head>
<body>
    <h1>Harry Potter</h1>
    <h2>Sinopsis</h2>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellat consequatur quia aut nesciunt pariatur ab recusandae magni! Obcaecati quia, molestiae atque in placeat veritatis officiis temporibus modi architecto aliquam cupiditate!</p>
    <h2>Novelas</h2>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nulla consequuntur porro debitis recusandae nobis molestias ratione. Veniam ab consequuntur, libero tempore deserunt minus cumque, obcaecati molestiae necessitatibus a molestias praesentium.</p>
    <h3>Harry Potter y la Piedra Filosofal</h3>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nostrum assumenda voluptatibus eius voluptatum natus reprehenderit, dicta blanditiis cupiditate? Dolorem, iure. Sunt dignissimos corrupti fugit porro error eius provident sed eum.</p>
    <h4>Personajes</h4>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente, excepturi molestiae ratione assumenda veniam eaque culpa nam. Dolor explicabo perferendis deleniti voluptate fugit, sit natus repellendus est sapiente accusantium minima.</p>
    
</body>
</html>
```

## Secciones de Contenido

- **Header:** Esta etiqueta se emplea para poner todo lo referente a la cabecera de la pagina, aqui podemos encontrar elementos como la navegacion y el logo.
- **Nav:** En esta etiquta ira la navegacion de nuestra pagina.
- **Main:** Como su nombre lo indica aqui ira todo el contenido principal y aqui ira todo lo referente al contenido de nuestra pagina.
- **Footer:** Aqui va el contenido que finaliza la pagina independiente del main, donde podemos encontrar redes sociales, un menu o datos de contacto.
- **Section:**  Es un contenedor genérico que agrupa contenido que está relacionado. Cuando creamos bloques cuyo contenido es parte de un bloque total usaremos section.
- **Article:**Es un contenedor que respresenta contenido independiente, es decir, podemos leer ese fragmento en cualquier otro sitio y tendría sentido por sí mismo.
- **Aside:** Se utiliza para representar contenido indirectamente relacionado pero que no forma parte del contenido principal.

### Anidamiento

Un section puede contener articles, por ejemplo, si tenemos varios artículos que hablan sobre noticias, deben ir dentro de un section, ya que es contenido relacionado entre sí, y los article serían cada una de las noticias porque podríamos leer cada una sin haber leido el resto, y seguiría teniendo sentido.

 El article es definido como un componente de la página de contenido independiente, esto implica que esta etiqueta pueda tener un header y un footer propios.

También existe el caso en el que un article contenga varias secciones, el artículo independiente podría ser navegadores y este contener dentro secciones como navegadores más utilizados en 2020.

```html
<body>
  <header>
    <h1>Cursos de desarrollo web gratuitos</h1>
  </header>
  <aside>Visita mi canal de YouTube</aside>
  <main>
     <section>
      <h2>Section como contedor</h2>
      <section>
        <h3>Noticias Del Día</h3>
        <article>
          <header>
            <h4>Noticia 1</h4>
          </header>
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iure exercitationem saepe animi unde perspiciatis
            accusantium totam repudiandae aut, delectus aspernatur nisi sequi velit temporibus accusamus quasi? Vitae
            enim
            quaerat in!</p>
          <footer>La noticia 1 ocurrió en Madrid</footer>
        </article>
        <article>
          <h4>Noticia 2</h4>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum eaque nihil possimus cum excepturi, id
            dolorum, vero perferendis magni deleniti unde, a laudantium. Sequi consequuntur corrupti id aspernatur
            eligendi eos?</p>
        </article>
        <article>
          <h4>Noticia 3</h4>
          <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolorem nostrum ad libero ut harum saepe alias
            ratione quasi. Vitae autem aut cupiditate, voluptatem exercitationem ipsa quod vel iste animi placeat?</p>
        </article>
      </section>
    </section>
	
    <article>
      <h2>Navegadores más utilizados en 2020</h2>
      <section>
        <header>
          <h3>Chrome</h3>
        </header>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Officiis facilis dolor amet iure aspernatur
          molestias dolore, dolorum reiciendis quisquam corporis nesciunt consequuntur nam tempore tenetur? Soluta
          aliquid inventore consequatur ratione?</p>
        <footer>Creado por Google</footer>
      </section>
      <section>
        <h3>Firefox</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Totam, quo quam deserunt aliquid consectetur qui ex,
          quia vero iusto dolorem odit, est a architecto dolor asperiores modi! Qui, minus sunt!</p>
      </section>
    </article>
  </main>
  <footer>4-11-2020</footer>

</body>
```

## Elementos de Bloque

Los elementos de bloque van a ocupar todo el ancho disponible   aunque su contenido no lo haga, por lo que los elementos que pongamos a continuacion saltaran a la siguiente linea

```html
<h1>Soy un elemento de bloque</h1>
<p>Soy otro elemento de bloque</p>
<span>Soy un elemento de línea</span>
<span>Soy otro elemento de línea</span>
```

### Otros elementos de bloque

- **address** Se utiliza para aportar información de contacto para el article más cercano o para todo el body
- **blockquote** Se utiliza para marcar las citas a otros autores o documentos. Se puede incluir el atributo cite para poner un enlace al documento original o fuente.
- **pre** Se utiliza para tener código preformateado que necesita ser representado igual que se esribió.
- **div** Se usa como división del documento, semánticamente no significa nada, es un contenedor genérico que se usa generalmente para dar estilos a través de css o para usar algo denominado "delegación de eventos" en javascript.
- **hr** horizontal rule, se utiliza para decirle al navegador que vamos a cambiar de tema

_Ejemplo:_

```html
<body>
    <address>
        Tony Stark <br>
        Malibú 10880 <br>
        90265 <br>
        California
    </address>

    <blockquote cite="https://www.entrepreneur.com/article/312598">
        <p>
Hay cosas que nunca le pregunté a mi padre. Hay preguntas que me hubiera gustado hacerle: cómo se sentía por lo que hacía su empresa, si estaba conflictuado, si tenía dudas (…). Vi a jóvenes estadounidenses ser asesinados por las armas que creaba para defenderlos y protegerlos. Me di cuenta que era parte de un sistema que no rinde cuentas.
        </p>
    </blockquote>

    <pre>
                        Hola,
        ¿qué tal?
    </pre>

    <div>
        <h2>Nombre</h2>
        <p>email</p>
        <p>Descripción</p>
    </div>
    <div>
        <h2>Nombre</h2>
        <p>email</p>
        <p>Descripción</p>
    </div>

    <hr>
</body>
```



## Elementos de Linea

Los elementos de linea van a ocupar el ancho de su contenido, por lo que los elementos no saltaran de linea.

- **em** Enfasis.
- **strong** Mas enfasis.
- **small** Menos enfasis que el texto normal.
- **br** Forzar un salto de linea.
- **wbr** Salto de linea si hiciera falta.
- **time** Se usa para representar un contenido de hora/fecha.
- **i** Italic.
- **b** Bold.
- **u** Underline.
- **sup** Superindice.
- **sub** Subindice.


_Ejemplo:_

```html
<p>
    <em>El dinero </em>es importante pero <strong> la salud </strong>es lo más importante.<small>Saludos!</small>
  </p>

  <p>
    Lorem ipsum dolor sit amet <br>
    consectetur adipisicing elit. Saepe velit nihil quis, perferendis voluptas tempora ipsam
    distinctio vero repellat nemo deserunt similique voluptates eveniet? Necessitatibus
    repudiandae neque officiis saepe itaque?
  </p>

  <p>http://127.0.0.1:5500/<wbr>cursos/<wbr>html/<wbr>elementos/<wbr>elementos-de-linea.html</p>
  <time>24/10/2020 10:35</time>
  <p>
    <i>Italic</i>
    <b>Bold</b>
    <u>Underline</u>
  </p>

  <p>4 elevado al cuadrado se representa así 4<sup>2</sup></p>

  <p>
    Agua oxigenada tiene la fórmula H<sub>2</sub>O<sub>2</sub>
  </p>
```

## Otros elementos en linea

- **span** Es un contenedor de línea, equivalente a div, se suele usar para encerrar palabras o pequeños textos y darles estilo a través de CSS o localizarlos desde javascript. Semánticamente no significa nada
- **q** Es el equivalente a blockquote, significa quote, por eso el de bloque se llama block - quote. Sirve para poner citas pero en línea.
- **code** Sirve para encerrar código que queremos representar visualmente, suele ir unido con la etiqueta pre.
- **Entidades especiales en HTML - Código ASCII**
      https://ascii.cl/es/codigos-html.htm

_Ejemplo:_

```html
<body>

    <p>Lorem, ipsum dolor sit amet <span> consectetur adipisicing </span>elit. Soluta nam voluptatum neque omnis commodi
        molestiae vitae impedit id. Molestias laboriosam, ad nemo aliquam ullam vitae rerum deserunt dicta voluptatibus
        voluptate.</p>
    <q cite="">Yo soy Iron Man</q>

    <pre>
        <code>
            span {
                color: red;
            }
        </code>
    </pre>
    <p>La etiqueta <code>&lt;h1&#62;</code> se utiliza para representar títulos de primer nivel</p>
    <!-- Símbolo de copyright -->
    &copy;
    &sbquo;
</body>
```

## Atributos

Los atributos son valores adicionales que configuran los elementos y/o ajustan su comportamiento.

En terminos generales hay dos tipos de atributos:

- **Comunes:** Su sintaxis es `atributo=valor`
- **Booleanos:** Su sintaxis es `atributo`

## Atributos Comunes

- **class** Este atributo se usa para dar estilos a traves de CSS.
- **id** Es un identificador unico que se utiliza para seleccionar el elemento desde JS y para hacer navegacion a traves de anclas.
- **title** es un atributo que ayuda a la accesibilidad mostrando una descripcion del elemento al que pertenece. Aparece el mensaje en un tooltip.
- **data-*** Es un atributo que nos permite guardar algun valor en la etiqueta HTML

_Ejemplo:_

```html
 <style>
        .parrafo-1 {
            color: red
        }

</style>
<body>
    <p class="parrafo-1">Clases</p>
    <p id="parrafo">Identificador a través de un ID</p>
    <p title="Este es un ejemplo del atributo title">Título con tooltip</p>
    <p id="parrafo-2" data-ejemplo="Datos de ejemplo">Datos pasados en la etiqueta</p>

    <script>
        const p = document.getElementById('parrafo')
        const parrafo2 = document.getElementById('parrafo-2')

        console.log(p.textContent)
        // Identificador a traves de ID
        console.log(parrafo2.dataset.ejemplo)
        // Datos de ejemplo
    </script>
</body>
```

## Enlaces

Conocidos también por links popularmente. Su objetivo es conectar una página web con otra página web, con un recurso tanto interno como externo, o con otro sitio web.

Tienen el atributo obligac    Tienen el atributo obligatorio href, donde le especificamos la ruta del recurso o sitio que queremos obtener.

También tiene el atributo target, que configura cómo queremos visualizar el recurso o sitio que solicitamos.

Existen dos tipos de rutas:

### Rutas Absolutas

Tienen un protocolo, http o https y son unicas en la red.

Se suelen utilizar para rutas externas.

### Rutas Relativas         

Pueden ser relativas al punto donde nos encontramos o relativas a la raiz del proyecto. 

No usan protocolo.

Si el recurso se encuentra al mismo nivel (en la misma carpeta) pondremos unicamente el nombre del archivo.

Si necesitamos salir de la carpeta actual usaremos ../ y se pone uno por cada nivel (carpeta) de la que queramos salir.

### Atributos de los enlaces

- **target**         target: define donde se abrirá el recurso solicitado. Por norma general siempre que useis rutas absolutas pondréis como valor `_blank`.

  El valor por defecto es `_self` (es como no poner nada).

- **download** Atributo booleano, sirve para descargar el recurso solicitado.

  **IMPORTANTE** el recurso debe estar en tu mismo servidor.

```html
<body>
    <h1>Home</h1>
    <!-- Rutas Relativas-->
    <nav>
        <p><a href="/paginas/blog.html#post-1">Post 1</a></p>
        <p><a href="/paginas/blog.html#post-2">Post 2</a></p>
        <p><a href="/paginas/blog.html#post-3">Post 3</a></p>
        <p><a href="/paginas/blog.html#post-4">Post 4</a></p>
        <p><a href="/paginas/blog.html#post-5">Post 5</a></p>
    </nav>
    <a href="/paginas/blog.html">Ir al blog</a>
    <!-- download-->
    <a href="/assets/images/gato.jpg" download>Descargar
        gato
    </a>
    <!-- Rutas Absolutas -->
    <a href="https://google.com" target="_blank">Ir a google</a>
</body>
```

## Listas 

Las listas en HTML sirven para listar contenido. En función del tipo de contenido de nuestra lista tenemos tres tipos de listas:

- **ul** -> **unordered list:** Se utilizan cuando el orden de los elementos no influye (lista de la compra).

- **ol** -> **ordered list:** Se utilizan cuando el orden de los elementos es importante (top 10).

  Cada elemento de la lista se representa con la etiqueta `<li>`, tanto en las `ul` como en las `ol`.

- **dl** -> **definition list:** Se utilizan para hacer una lista de definiciones (diccionario).

  Cada elemento de una lista de definición lleva 2 etiquetas:

  - **dt**-> **Definition term:** El término que vamos a definir.
  - **dd**-> **Definition description:** La descripción del término.

_Ejemplo:_

```html
<body>
    <h1>Listas</h1>
	<!-- listas desordenadas -->
    <nav>
        <ul>
            <li><a href="#post-1">Post 1</a></li>
            <li><a href="#post-2">Post 2</a></li>
            <li><a href="#post-3">Post 3</a></li>
            <li><a href="#post-4">Post 4</a></li>
            <li><a href="#post-5">Post 5</a></li>
        </ul>
    </nav>
    
    <h2>Lista de la compra</h2>
    <ul>
        <li>Pan</li>
        <li>Huevos</li>
        <li>Leche</li>
    </ul>
    
    <!-- listas ordenadas -->
    <h2>Orden de aprendizaje en el desarrollo web</h2>
    <ol>
        <li>HTML</li>
        <li>CSS</li>
        <li>JavaScript</li>
    </ol>
	
    <!-- listas de definiciones -->
    <h2>Lenguajes para el desarrollo web</h2>
    <dl>
        <dt>HTML</dt>
        <dd>HyperText Markup Language: Es un lenguaje de marcado que se usa para estructurar datos en una página web
        </dd>

        <dt>CSS</dt>
        <dd>Cascade Style Sheets: Es un lenguaje de diseño que se utiliza para dar estilos al HTML</dd>

        <dt>JavaScript</dt>
        <dd>Es un lenguaje de programación para dar interactividad a un sitio web.</dd>
    </dl>
</body>
```

Se pueden construir listas anidadas teniendo en uno de los li otro ul/ol según sea necesario.

_Ejemplo:_

```html
 <ol>
     <li>
         HTML
         <ul>
             <li>Estructura</li>
             <li>Sintaxis</li>
             <li>Etiquetas</li>
         </ul>
     </li>
     <li>CSS</li>
     <li>JavaScript</li>
</ol>
```

### Atributos de listas

- **ol** 
  - **type** Estilo de numeracion (1, A, a, I, i).
  - **start** Inicio de las secuencias.
- **ul**
  - **type** Estilo de los items (disc, square, circle).

## Tablas

Las tablas en HTML sirven para mostrar contenido tabulado.

La estructura basica de una tabla se compone de:

- **table** -> Etiqueta que encierra una tabla.
- **tr** -> **table row**, etiqueta que contruye una fila.
- **td** -> **table data**, etiqueta que construye una celda.

**Truco:** El numero de celdas dentro de un `td` establecera el numero de colummnas de la tabla.

_Ejemplo:_

```html
<body>
    <table>
        <tr>
            <td>Lunes</td>
            <td>Martes</td>
            <td>Miercoles</td>
            <td>Jueves</td>
            <td>Viernes</td>
        </tr>
        <tr>
            <td>Matematcias</td>
            <td>Sociales</td>
            <td>Ciencias</td>
            <td>Ingles</td>
            <td>Matematicas</td>
        </tr>
    </table>
</body>
```

El codigo anterior es equivalente a:

| Lunes       | Martes   | Miercoles | Jueves | Viernes     |
| ----------- | -------- | --------- | ------ | ----------- |
| Matematicas | Sociales | Ciencias  | Ingles | Matematicas |

Los titulos de las tablas se establecen con la etiqueta `caption`, es una etiqueta opcional, y segun la especificacion esa etiqueta se coloca justo despues de la etiqueta `table`.  

Las cabeceras de las tablas se establecen con la etiqueta `thead`.

Dentro tendremos una etiqueta `tr` normal, pero en el caso de las celdas, las estableceremos con la etiqueta `th` en lugar de `td`.  

El contenido de la tabla debe ir dentro de una etiqueta `tbody` para representar el cuerpo de la tabla.

De forma opcional podemos colocar un `tfoot` a la tabla para establecer un pie de tabla, esto es algo que algunas tablas tienen como la suma de las cantidades totales.

Para hacer que las celdas ocupen mas de una fila o mas de una columna tenemos 2 atributos:

- **rowspan:** Sirve para que una celda ocupe mas de una fila, el valor por defecto es 1.
- **colspan:** sirve para que una celda ocupe mas de una columna, el valor por defecto es 1.

Cuando necesitamos seleccionar una columna, tenemos la etiqueta `colgroup`, que nos permite seleccionar una columna en concreto. Dentro pondremos tantas etiquetas `col` como columnas tengamos, cada etiqueta `col` equivaldra a una columna siguiendo el mismo orden que tiene en la tabla.

Si necesitamos que una etiqueta `col` agrupe mas de una columna, tenemos el atributo `span`, que funciona exactamente como rowspan y colspan.

_Ejemplo:_

```html
<body>
	<table>
      <caption>
        HORARIO DE CLASES
        <colgroup>
          <col span="5" />
          <col />
        </colgroup>
      </caption>
      <thead>
        <tr>
          <th></th>
          <th>L</th>
          <th>M</th>
          <th>X</th>
          <th>J</th>
          <th>V</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>8:30 - 9:30</td>
          <td>Matematicas</td>
          <td>Matematicas</td>
          <td>Sociales</td>
          <td>Matematicas</td>
          <td>Matematicas</td>
        </tr>
        <tr>
          <td>9:30 - 10:25</td>
          <td>Lengua</td>
          <td>Lengua</td>
          <td>Matematicas</td>
          <td>Ciencias</td>
          <td>Lengua</td>
        </tr>
        <tr>
          <td>10:25 - 11:20</td>
          <td>Educacion Fisica</td>
          <td>Ciencias</td>
          <td>Lengua</td>
          <td>Lengua</td>
          <td>Educacion Fisica</td>
        </tr>
        <tr>
          <td>11:20 - 11:45</td>
          <td colspan="5">Recreo</td>
        </tr>
        <tr>
          <td>11:45 - 12:40</td>
          <td>Ingles</td>
          <td>Sociales</td>
          <td>Ingles</td>
          <td>Tutoria</td>
          <td>Ingles</td>
        </tr>
        <tr>
          <td>12:40 - 13:35</td>
          <td rowspan="2">Tecnologia</td>
          <td>Educacion Fisica</td>
          <td>Plastica</td>
          <td>Religion</td>
          <td rowspan="2">Tecnologia</td>
        </tr>
        <tr>
          <td>13:35 - 14:30</td>
          <td>Frances</td>
          <td>Tecnologia</td>
          <td>Frances</td>
        </tr>
      </tbody>
      <tfoot>
        <tr>
          <td colspan="5">Total de asignaturas</td>
          <td>12</td>
        </tr>
      </tfoot>
    </table>
</body>
```

![2021-01-29_15-12](/home/nikola/Pictures/2021-01-29_15-12.png)

## Formularios

### Estructura basica

La estructura básica de un formulario se compone de 4 elementos

- **form** Es la etiqueta que engloba nuestro formulario.
- **label** Sirve para escribir el nombre del campo a rellenar debe tener el atributo `for` al cual se le indica un id que lo que hará será emparejar el `label` con su `input` correspondiente.
- **input** Sirve para crear un campo que permitirá al usuario interactuar. El único atributo obligatorio del input es `name`.
- **button** Crea un botón que permitirá enviar el formulario.

_Ejemplo:_

```html
<body>
    <form>
        <!-- Label e input enlazados de la manera mas comun -->
        <label for="name">Nombre</label>
        <input id="name">
        
        <!-- Label e input enlazados, esta forma se utiliza usualmente para interaccion -->
        <label>
            Nombre
            <input>
        </label>
        
        <!-- Boton -->
        <button>Enviar formulario</button>
    </form>

</body>
```

### Tipos de Input

- **button** Se comporta igual que un boton `<button>`.
- **submit** Se utiliza para enviar el formulario.



- **date** Se utilza para introducir unua fecha.

- **datetime-local** fecha y hora, no funciona en firefox.

- **time** Se utiliza para introducir la hora.

  **TIP**
  ****** Se recomienda usar date y time para seleccionar fecha y hora.

  

- **month** Se utiliza para introducir mes.

- **week** Se utiliza para introducir el numero de semana del ano.



- **search** Se utiliza para barras de busqueda.
- **tel** se utiliza para introducir numeros telefonicos.

- **email** Se utiliza para  introducir un e-mail.
- **password** Se utiliza para contrasenas.
- **url** Se utiliza para introducir URLs.



- **color** Se utiliza para especificar color.

- **number** Se utiliza para valores numericos.
- **range** Se utilza para establecer un rango.
- **reset** Se utiliza para resetear el formulario.
- **text** Valor por defecto.
- **hidden** Campo oculto, puede contener valor pero no se mostrara.

_Ejemplo:_

```html
<body>
    <form>
        <input type="color">
        <input type="number">
        <input type="range" step="5" min="0" max="20">
        <input type="reset">
        <input type="text">
        <input type="date">
        <input type="datetime-local">
        <input type="date">
        <input type="time">
        <input type="month">
        <input type="week">

        <div>
            <label> search
                <input type="search">
            </label>
        </div>
        
        <div>
            <label> teléfono
                <input type="tel">
            </label>
        </div>
        
        <div>
            <label> email
                <input type="email">
            </label>
        </div>
        
        <div>
            <label> password
                <input type="password">
            </label>
        </div>
        
        <div>
            <label> url
                <input type="url">
            </label>
        </div>
    </form>
</body>
```



### Inputs de Seleccion

- **radio** Permite seleccionar una única opción de una lista de opciones relacionadas. Para que funcione cada uno de los inputs tipo `radio` deben tener el mismo valor en su atributo `name`.

_Ejemplo:_

```html
<body>
    <form>
        <h2>Género</h2>
        <label>Masculino
            <input 
                   type="radio"
                   name="gender"
                   value="masculino"
                   checked
          	/>
        </label>
        <label>Femenino
            <input
                   type="radio"
                   name="gender" 
                   value="femenino"
		/>
        </label>
        <label>Desconocido
            <input 
                   type="radio" 
                   name="gender" 
                   value="desconocido"
		/>
        </label>
    </form>
</body>
```



- **checkbox** Permite seleccionar varias opciones de una lista de opciones relacionadas. Al igual que los `radio` estas tambien se enlazan por el atributo `name`.

_Ejemplo:_

```html
<body>
   	<form>
        <h2>Lenguajes que conoces</h2>
        <label>
            HTML
            <input 
                   type="checkbox"
                   name="languages"
                   value="html" 
                   checked
		/>
        </label>
        <label>
            CSS
            <input 
                   type="checkbox" 
                   name="languages" 
                   value="css" 
                   checked
		/>
        </label>
        <label>
            JavaScript
            <input 
                   type="checkbox"
                   name="languages" 
                   value="javascript"
		/>
        </label>
    </form>
</body>
```



- **select**  Crea una lista de opciones donde podemos seleccionar una o varias opciones.

  Cada opción irá dentro de una etiqueta `<option> </option>`.

_Ejemplo:_

```html
<body>
    <form>
        <select name="lenguajes" multiple>
            <option value="html">HTML</option>
            <option value="css">CSS</option>
            <option value="javascript">JavaScript</option>
		</select> 
    </form>
</body>
```



Si tenemos muchas opciones podemos ordenarlas por categorías a través de la etiqueta `<optgroup></optgroup>` con el atributo label para nombrar la categoría.

_Ejemplo:_

```html
<body>
    <form>
        <select name="mascotas" multiple>
            <optgroup label="4 patas">
                <option value="perro">Perro</option>
                <option value="gato">Gato</option>
                <option value="hamster">Hamster</option>
                <option value="conejo">Conejo</option>
            </optgroup>
            <optgroup label="aves">
                <option value="loro">Loro</option>
                <option value="canario">Canario</option>
            </optgroup>
            <optgroup label="otras">
                <option value="serpiente">Serpiente</option>
                <option value="tarantula">Tarántula</option>
            </optgroup>
        </select>
    </form>
</body>
```



- **datalist** Se utiliza para proporcionar una función de "autocompletar" para `<input>`  elementos. Los usuarios verán una lista desplegable de opciones predefinidas a medida que ingresan datos. 

  Necesitaremos como base un input de tipo `list` con el atributo `list` que debe tener igual valor al `id` de la etiqueta `datalist`.

_Ejemplo:_

```html
<body>
    <h1>Elementos seleccionables</h1>
    <form>
        <input type="list" list="pets">
        <datalist id="pets">
            <option value="dog"></option>
            <option value="gato"></option>
            <option value="hamster"></option>
            <option value="conejo"></option>
            <option value="loro"></option>
            <option value="canario"></option>
            <option value="serpiente"></option>
            <option value="tarantula"></option>
        </datalist>
    </form>
</body>
```

### Mas elementos

- **fieldset**  Se utiliza para agrupar elementos dentro de un formulario.
- **legend** Representa una etiqueta para el contenido del fieldset.
- **file** Este input se utiliza para cargar archivos y enviarlos desde un formulario.
- **meter** Representa un valor dentro de un rango conocido
- **progress** Representa el progreso de una tarea.
- **textarea** Se utiliza para introducir texto en un formulario.

_Ejemplo:_

```html
<body>
    <form>
        <fieldset>
            <legend>Datos Personales</legend>
            <div>
                <label for="name">Nombre</label>
                <input type="text" id="name">
            </div>
            <label for="surname">Apellidos</label>
            <input type="text" id="surname">
        </fieldset>
        
        <input type="file">
        
        <label for="fuel">Combustible</label>
        <meter 
               id="fuel"
               min="0"
               max="100"
               value="60"
               low="30"
               high="75"
               optimum="50"
		>
        </meter>
        <label for="task">Tarea 1</label>
        <progress id="task" max="100" value="10"></progress>
        
        <label for="message">Mensaje</label>
        <textarea name="" id="message" cols="10" rows="10"></textarea>
    </form>

</body>
```

### Atributos de Formularios

- **placeholder** Da una pista de lo que el usuario tiene que introducir.
- **required** Hace que un campo sea obligatorio
- **readonly** Hace que un campo sea de solo lectura.
- **disabled** Desactiva el campo, no se podrá escribir en el.
- **min - max** Establece el mínimo y máximo de un campo numérico.
- **minlenght - maxlenght** Establece el minimo y máximo de caracteres de un campo de texto.
- **selected** Equivale a checked en los select, sirve para establecer una opción por defecto.
- **autofocus** Para poner el foco por defecto al cargar el formulario.
- **multiple** Cuando está presente, especifica que el usuario puede ingresar más de un valor en el ` <input>`elemento. 

_Ejemplo:_

```html
<body>
    <form>
        <input 
               type="text" 
               placeholder="Introduce tu nombre"
               required
		/>
        
        <input type="text" value="Hola" readonly/>
        
        <input type="text" value="Hola" disabled/>
        
        <select name="numbers">
            <option value="one">One</option>
            <option value="Two" selected>Two</option>
        </select>
        
        <input type="number" min="5">
        
        <input 
               type="text"
               minlength="3"
               maxlength="5"
               required
               autofocus
		/>
        
        <input type="submit">
    </form>
</body>
```



## Contenido Embebido

El contenido embebido es todo el contenido que nos traemos desde fuera.

Estos archivos son los que mas peso (tamano) anaden a un sitio web.

Los tipos mas conocidos son:

### Imagenes

Los formatos de imagenes para web los podemos clasificar en 2 tipos:

- **Vectoriales**

  - **svg** (recomendado siempre que se pueda). Estos no agregan nada de peso a nuestro sitios web. 

    Usar este formato para elementos decorativos o que no sean principales por ejemplo iconos de redes sociales, logos...

- **Mapa de bits**

  - **jpg**.
  - **png 8 y 24** (si necesitas transparencia).
  - **gif** (si necesitas una imagen animada).
  - **webp** (el formato que menos pesa y deberiamos intentar usar). Para transformar imagenes a este formato puedes usar la siguiente pagina [online-convert](https://imagen.online-convert.com/es/convertir-a-wbmp).

Para introducir imagenes dentro de html tenemos variaas formas, de base tenemos la etiqueta `img` con dos atributos `src` donde ira la ruta relativa de la imagen y `alt` que es la representacion de la imagen o lo que quiere dar a entender esta.

_Ejemplo:_

```html
<body>
    <img
         src="/contenido-embebido/assets/images/portada.jpg" 
         alt="Imagen de portada"
	/>
</body>
```



Cuando utilizas `svg` tienes dos opciones, en archivo separado y dentro el html, cuando tenes que modificarlo en tiempo real o trabajar con el desde css o js hazlo embebido en el html, de lo contrario usarlo como archivo.

#### Device Pixel Ratio

**DPR** (Device Pixel Ratio)
	Es la relación que existe entre los píxeles reales que tiene el dispositivo y los píxeles que tenemos disponibles para "pintar" contenido.

**DPR** = pixeles reales / pixeles disponibles.

El `DPR` es relevante a la hora de saber que imagen tener en funcion del tamano del dispositivo. Cuando tenemos una pantalla grande la foto debe estar mucho mas hd en comparacion de una pantalla pequena por esto debemos gestionar las imagenes que ponemos en funcion del tamano.

El `DPR` de un desktop es de 1x y para tablets y celulares es de 2x, 3x...

Aqui entra el juego el atributo `srcset` que nos permite elegir un listado de n opciones de imagenes.

_Ejemplo:_

```html
<!--
	Cuando el DPR sea de 1x utilizara portada.webp (si el navegador soporta el formato webp) de lo contrario cargara portada.jpg y si el dispositivo tiene 2x o mas cargara portada-mobile.webp que seria para un dispositvo movil.

Ademas anadimos una copia de seguridad que el el src por si el navegador no soporta srcset.
-->
<img 
     srcset="            
    /contenido-embebido/assets/images/portada.webp,
    /contenido-embebido/assets/images/portada.jpg,
    /contenido-embebido/assets/images/portada-mobile.webp 2x,
    /contenido-embebido/assets/images/portada-mobile.jpg 2x" 
     src="/contenido-embebido/assets/images/portada.jpg"
     alt="Imagen de portada"
/>
```

#### Imagenes en Funcion de Tamanos

Con la etiqueta `picture` tenemos la posibilidad de agregar dentro de ellas la etiqueta `source` que acepta el atributo `media` con el cual le podemos dar medidas para que use una u otra imagen en funcion del tamano. Para el siguiente ejemplo la imagen del `srcset` es decir la de vista mobial solo aparecera cuando la pantalla sea menor o igual de 1200px.

_Ejemplo:_

```html
<picture>
    <source
            srcset="
			/contenido-embebido/assets/images/portada-mobile.webp,
        	/contenido-embebido/assets/images/portada-mobile.jpg" 
            media="(max-width:1200px)"
	/>

    <img 
         src="/contenido-embebido/assets/images/portada.jpg" 
         alt=""
	/>
</picture>
```



#### Cuando necesitas una Imagen con descripcion

```html
 <figure>
        <img
             src="https://images.pexels.com/photos/2558605/pexels-photo-2558605.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260"
             
            alt="gato tumbado"
		/>
        <figcaption>Gato común tumbado</figcaption>
</figure>
```

### Audio

```html
<audio 
       src="/contenido-embebido/assets/audio/oomiee.mp3" 
       controls 
       autoplay 
       muted
>
</audio>
```



### Videos

```html
 <video 
        src="/contenido-embebido/assets/video/Creux De Van.mp4" 
        controls 
        muted 
        loop
        poster="/contenido-embebido/assets/images/portada.jpg" 
        autoplay
>
</video>
```



### Iframes

Es un pedazo de web que introducimos en nuestra pagina web.

```html
<iframe 
        width="560" 
        height="315" 
        src="https://www.youtube.com/embed/0e_lA0HLI3s"
>
</iframe>
```



## Etiquetas meta

Las etiquetas meta suelen llevar la estructura de la etiqueta `meta` con los atributos `name` que indica que tipo de meta es y el atributo `content` que define como su nombre lo indica el contenido de esta.

_Ejemplo:_

```html
<head>
    <meta 
          name="description" 
          content="Pagina de para adoptar un gatito"
	/>
    <meta 
          name="author"
          content="NikolaM-Dev"
	/>
</head>
```



## Como construir nuestro Favicon

 En este sitio encontraras un generador de favicons que incluyen todos lo tipos para los diferentes dispositovos [Favicon-Generator](https://www.favicon-generator.org/).

Estando alli subes la imagen y eliges la opcion de `Generate icons for Web, Android, Microsoft, and iOS (iPhone and iPad) Apps` y luego le das a `Create Favicon`, como resultado te dara un archivo a descargar y las etiquetas que debes usar para usar estos archivos.

**PDT** Revisa que las rutas relativas de las etiquetas que te da la pagina con el lugar donde tu guardaste los archivos.



## Libreria de Iconos

[Font Awesome](https://fontawesome.com/icons?d=gallery).



## Accesibilidad

Hay deferentes personas que visitan tu pagina web, la accesibilida se encarga de ayudar a estas personas a consumir nuestro contenido.

Tenemos atributos como:

- **tabindex** Este atributo dice el orden en que nos podemos desplazar con el tabulador.

_Ejemplo:_

```html
<p tabindex="1">
    Parrafo 1
</p>
<p tabindex="2">
    Parrafo 1
</p>
<p tabindex="2">
    Parrafo 3
</p>
```



- **aria-label** Indica a la persona mas sobre esto para aquello que no ven el contenido sino que lo escuchan por un lector de paginas.

_Ejemplo:_

```html

<!--
	Como se aprecia el link que dice `leer mas` para una persona invidente no le indica de que quiere leer mas, hay es donde la informacion del aria-label le dira a los usuario que es sobre la noticia del agua en Marte.
-->
<a 
   href="#"
   aria-label="Leer mas sobre la noticia del agua en Marte"
   >
    Leer mas
</a>
```



- **role** Indica el rol que cumple determinado elemento.

_Ejemplo:_

```html
<button role="button">
    like
</button>
```



## Open Graph Protocol

[OGP Documentacion](https://ogp.me/).



## Twitter Card

Es el igual a `OGP ` pero hecho por twitter

[Twitter Card Documentacion](https://developer.twitter.com/en/docs/twitter-for-websites/cards/overview/abouts-cards).



Para mas informacion de determinado tema siempre pueden consultar la documentacion de [MDN](https://developer.mozilla.org/es/).

