2º SMR **AW - CSS**

Para crear diseños web profesionales, es imprescindible conocer y dominar los selectores de CSS. Una regla de CSS está formada por una parte llamada "selector" y otra parte llamada "declaración". 

La declaración indica *"qué hay que hacer" * y el selector indica *"a quién hay* *que hacérselo" *. Por lo tanto, los selectores son imprescindibles para aplicar de forma correcta los estilos CSS en una página. 

A un mismo elemento HTML se le pueden aplicar varias reglas CSS y cada regla CSS puede aplicarse a un número ilimitado de elementos. En otras palabras, una misma regla puede aplicarse sobre varios selectores y un mismo selector se puede utilizar en varias reglas. 

El estándar de CSS 2.1 incluye una docena de tipos diferentes de selectores, que permiten seleccionar de forma muy precisa elementos individuales o conjuntos de elementos dentro de una página web. 

No obstante, la mayoría de páginas de los sitios web se pueden diseñar utilizando solamente los cinco selectores básicos. 

1. Selectores básicos

**1.1. Selector universal**

Se utiliza para seleccionar todos los elementos de la página. El siguiente ejemplo elimina el margen y el relleno de todos los elementos HTML \(por ahora no es importante fijarse en la parte de la declaración de la regla CSS\):

\* \{

margin: 0; 

padding: 0; 

\}

El selector universal se indica mediante un asterisco \(\*\). A pesar de su sencillez, no se utiliza habitualmente, ya que es difícil que un mismo estilo se pueda aplicar a todos los elementos de una página. 

1





2º SMR **AW - CSS**

No obstante, sí que se suele combinar con otros selectores y además, forma parte de algunos *hacks * muy utilizados, como se verá más adelante. 

**1.2. Selector de tipo o etiqueta**

Selecciona todos los elementos de la página cuya etiqueta HTML coincide con el valor del selector. El siguiente ejemplo selecciona todos los párrafos de la página:

p \{

... 

\}

Para utilizar este selector, solamente es necesario indicar el nombre de una etiqueta HTML \(sin los caracteres < y >\) correspondiente a los elementos que se quieren seleccionar. 

El siguiente ejemplo aplica diferentes estilos a los titulares y a los párrafos de una página HTML:

h1 \{

color: red; 

\}

h2 \{

color: blue; 

\}

p \{

color: black; 

\}

Si se quiere aplicar los mismos estilos a dos etiquetas diferentes, se pueden encadenar los selectores. En el siguiente ejemplo, los títulos de sección h1, h2 y h3comparten los mismos estilos: h1 \{

2





2º SMR **AW - CSS**

color: \#8A8E27; 

font-weight: normal; 

font-family: Arial, Helvetica, sans-serif; 

\}

h2 \{

color: \#8A8E27; 

font-weight: normal; 

font-family: Arial, Helvetica, sans-serif; 

\}

h3 \{

color: \#8A8E27; 

font-weight: normal; 

font-family: Arial, Helvetica, sans-serif; 

\}

En este caso, CSS permite agrupar todas las reglas individuales en una sola regla con un selector múltiple. Para ello, se incluyen todos los selectores separados por una coma \(,\) y el resultado es que la siguiente regla CSS es equivalente a las tres reglas anteriores: 
`h1, h2, h3 \{`

`color: \#8A8E27;` 

`font-weight: normal;` 

`font-family: Arial, Helvetica, sans-serif;` 

`\}`

En las hojas de estilo complejas, es habitual agrupar las propiedades comunes de varios elementos en una única regla CSS y posteriormente definir las propiedades específicas de esos mismos elementos. El siguiente ejemplo establece en primer lugar las propiedades comunes de los títulos de sección \(color y tipo de letra\) y a continuación, establece el tamaño de letra de cada uno de ellos:

3





2º SMR **AW - CSS**

h1, h2, h3 \{

color: \#8A8E27; 

font-weight: normal; 

font-family: Arial, Helvetica, sans-serif; 

\}

h1 \{ font-size: 2em; \}

h2 \{ font-size: 1.5em; \}

h3 \{ font-size: 1.2em; \}

**1.3. Selector descendente**

Selecciona los elementos que se encuentran dentro de otros elementos. 

Un elemento es descendiente de otro cuando se encuentra entre las etiquetas de apertura y de cierre del otro elemento. 

El selector del siguiente ejemplo selecciona todos los elementos <span> de la página que se encuentren dentro de un elemento <p>: p span \{ color: red; \}

Si el código HTML de la página es el siguiente:

<p> 

... 

<span>texto1</span> 

... 

<a href="">...<span>texto2</span></a> 

... 

</p> 

El selector p span selecciona tanto texto1 como texto2. El motivo es que en el selector descendente, un elemento no tiene que ser descendiente directo del otro. La única condición es que un elemento debe estar dentro de otro elemento, sin importar el nivel de profundidad en el que se encuentre. 

4





2º SMR **AW - CSS**

Al resto de elementos <span> de la página que no están dentro de un elemento <p>, no se les aplica la regla CSS anterior. 

Los selectores descendentes permiten aumentar la precisión del selector de tipo o etiqueta. Así, utilizando el selector descendente es posible aplicar diferentes estilos a los elementos del mismo tipo. El siguiente ejemplo amplía el anterior y muestra de color azul todo el texto de los <span> contenidos dentro de un <h1>: p span \{ color: red; \}

h1 span \{ color: blue; \}

Con las reglas CSS anteriores:



`Los`

`elementos <span> que`

`se`

`encuentran`

`dentro`

`de`

`un`

`elemento <p> se muestran de color rojo.` 



Los

elementos <span> que

se

encuentran

dentro

de

un

elemento <h1> se muestran de color azul. 



El resto de elementos <span> de la página, se muestran con el color por defecto aplicado por el navegador. 

La sintaxis formal del selector descendente se muestra a continuación: selector1 selector2 selector3 ... selectorN

Los selectores descendentes siempre están formados por dos o más selectores separados entre sí por espacios en blanco. El último selector indica el elemento sobre el que se aplican los estilos y todos los selectores anteriores indican el lugar en el que se debe encontrar ese elemento. 

En el siguiente ejemplo, el selector descendente se compone de cuatro selectores:

p a span em \{ text-decoration: underline; \}

Los estilos de la regla anterior se aplican a los elementos de tipo `<em>` que se encuentren dentro de elementos de tipo `<span>,` que a su vez se encuentren dentro de elementos de tipo `<a>` que se encuentren dentro de elementos de tipo `<p>.` 

No debe confundirse el selector descendente con la combinación de selectores:

/\* El estilo se aplica a todos los elementos "p", "a", "span" y "em" \*/

5





2º SMR **AW - CSS**

p, a, span, em \{ text-decoration: underline; \}

/\* El estilo se aplica solo a los elementos "em" que se encuentran dentro de "p a span" \*/

p a span em \{ text-decoration: underline; \}

Se puede restringir el alcance del selector descendente combinándolo con el selector universal. El siguiente ejemplo, muestra los dos enlaces de color rojo:

p a \{ color: red; \}

<p><a href="\#">Enlace</a></p> 

<p><span><a href="\#">Enlace</a></span></p> Sin embargo, en el siguiente ejemplo solamente el segundo enlace se muestra de color rojo:

p \* a \{ color: red; \}

<p><a href="\#">Enlace</a></p> 

<p><span><a href="\#">Enlace</a></span></p>
el `*` nos obliga a que haya algo, con lo que sólo se aplicará a los que tengan 

`(p) (cualquier random) (aa)`

**1.4. Selector de clase**

Si se considera el siguiente código HTML de ejemplo:

<body> 

<p>Lorem ipsum dolor sit amet.. </p> 

<p>Nunc sed lacus et est adipiscing accumsan...</p> 

<p>Class aptent taciti sociosqu ad litora...</p> 6





2º SMR **AW - CSS**

</body> 

¿Cómo se pueden aplicar estilos CSS sólo al primer párrafo? El selector universal \(\*\) no se puede utilizar porque selecciona todos los elementos de la página. El selector de tipo o etiqueta \(p\) tampoco se puede utilizar porque seleccionaría todos los párrafos. Por último, el selector descendente \(body p\) tampoco se puede utilizar porque todos los párrafos se encuentran en el mismo sitio. 

Una de las soluciones más sencillas para aplicar estilos a un solo elemento de la página consiste en utilizar el atributo class de HTML sobre ese elemento para indicar directamente la regla CSS que se le debe aplicar:

<body> 

<p class="destacado">Lorem ipsum dolor sit amet.. </p> 

<p>Nunc sed lacus et est adipiscing accumsan...</p> 

<p>Class aptent taciti sociosqu ad litora...</p> 

</body> 

A continuación, se crea en el archivo CSS una nueva regla llamada destacado con todos los estilos que se van a aplicar al elemento. 

Para que el navegador no confunda este selector con los otros tipos de selectores, se prefija el valor del atributo class con un punto \(.\) tal y como muestra el siguiente ejemplo:

.destacado \{ color: red; \}

El selector .destacado se interpreta como *"cualquier elemento de la página* *cuyo atributo class sea igual a destacado" *, por lo que solamente el primer párrafo cumple esa condición. 

Este tipo de selectores se llaman selectores de clase y son los más utilizados junto con los selectores de ID que se verán a continuación. La principal característica de este selector es que en una misma página HTML varios elementos diferentes pueden utilizar el mismo valor en el atributo class:

<body> 

<p class="destacado">Lorem ipsum dolor sit amet.. </p> 

<p>Nunc sed lacus et <a href="\#" class="destacado">est adipiscing</a> accumsa n...</p> 

7





2º SMR **AW - CSS**

<p>Class aptent taciti <em class="destacado">sociosqu ad</em> litora...</p> 

</body> 

Los selectores de clase son imprescindibles para diseñar páginas web complejas, ya que permiten disponer de una precisión total al seleccionar los elementos. Además, estos selectores permiten reutilizar los mismos estilos para varios elementos diferentes. 

A continuación se muestra otro ejemplo de selectores de clase:

.aviso \{

padding: 0.5em; 

border: 1px solid \#98be10; 

background: \#f6feda; 

\}

.error \{

color: \#930; 

font-weight: bold; 

\}

<span class="error">...</span> 

<div class="aviso">...</div> El elemento <span> tiene un atributo class="error", por lo que se le aplican las reglas CSS indicadas por el selector .error. Por su parte, el elemento <div> tiene un atributo class="aviso", por lo que su estilo es el que definen las reglas CSS del selector .aviso. 

En ocasiones, es necesario restringir el alcance del selector de clase. Si se considera de nuevo el ejemplo anterior:

<body> 

<p class="destacado">Lorem ipsum dolor sit amet.. </p> 8





2º SMR **AW - CSS**

`<p>Nunc sed lacus et <a href="\#" class="destacado">est adipiscing</a> accumsa n...</p>` 

`<p>Class aptent taciti <em class="destacado">sociosqu ad</em> litora...</p>` 

`</body>` 

¿Cómo es posible aplicar estilos solamente al párrafo cuyo atributo class sea igual a destacado? Combinando el selector de tipo y el selector de clase, se obtiene un selector mucho más específico: p.destacado \{ color: red \}

El selector p.destacado se interpreta como *"aquellos elementos de tipo <p> que* *dispongan de un atributo class con valor destacado" *. De la misma forma, el selector a.destacado solamente selecciona los enlaces cuyo atributo class sea igual a destacado. 

De lo anterior se deduce que el atributo .destacado es equivalente a \*.destacado, por lo que todos los diseñadores obvian el símbolo \* al escribir un selector de clase normal. 

No debe confundirse el selector de clase con los selectores anteriores:

/\* Todos los elementos de tipo "p" con atributo class="aviso" \*/

p.aviso \{ ... \}

/\* Todos los elementos con atributo class="aviso" que estén dentro de cualquier elemento de tipo "p" \*/

p .aviso \{ ... \}

/\* Todos los elementos "p" de la página y todos los elementos con atributo class="aviso" de la página \*/

p, .aviso \{ ... \}

Por último, es posible aplicar los estilos de varias clases CSS sobre un mismo elemento. La sintaxis es similar, pero los diferentes valores del atributo class se separan con espacios en blanco. En el siguiente ejemplo:

<p class="especial destacado error">Párrafo de texto...</p> 9





2º SMR **AW - CSS**

Al párrafo anterior se le aplican los estilos definidos en las reglas .especial, .destacado y .error, por lo que en el siguiente ejemplo, el texto del párrafo se vería de color rojo, en negrita y con un tamaño de letra de 15 píxel:

.error \{ color: red; \}

.destacado \{ font-size: 15px; \}

.especial \{ font-weight: bold; \}

<p class="especial destacado error">Párrafo de texto...</p> Si un elemento dispone de un atributo class con más de un valor, es posible utilizar un selector más avanzado:

.error \{ color: red; \}

.error.destacado \{ color: blue; \}

.destacado \{ font-size: 15px; \}

.especial \{ font-weight: bold; \}

<p class="especial destacado error">Párrafo de texto...</p> En el ejemplo anterior, el color de la letra del texto es azul y no rojo. El motivo es que se ha utilizado un selector de clase múltiple .error.destacado, que se interpreta como *"aquellos elementos de la página que dispongan de* *un atributo class con al menos los valores error y destacado" *. 

**1.5. Selectores de ID**

En ocasiones, es necesario aplicar estilos CSS a un único elemento de la página. Aunque puede utilizarse un selector de clase para aplicar estilos a un único elemento, existe otro selector más eficiente en este caso. 

El selector de ID permite seleccionar un elemento de la página a través del valor de su atributo id. Este tipo de selectores sólo seleccionan un elemento de la página porque el valor del atributo id no se puede repetir en dos elementos diferentes de una misma página. 

10





2º SMR **AW - CSS**

La sintaxis de los selectores de ID es muy parecida a la de los selectores de clase, salvo que se utiliza el símbolo de la almohadilla \(\#\) en vez del punto \(.\) como prefijo del nombre de la regla CSS:

\#destacado \{ color: red; \}

<p>Primer párrafo</p> 

<p id="destacado">Segundo párrafo</p> 

<p>Tercer párrafo</p> 

En el ejemplo anterior, el selector \#destacado solamente selecciona el segundo párrafo \(cuyo atributo id es igual a destacado\). 

La principal diferencia entre este tipo de selector y el selector de clase tiene que ver con HTML y no con CSS. Como se sabe, en una misma página, el valor del atributo id debe ser único, de forma que dos elementos diferentes no pueden tener el mismo valor de id. Sin embargo, el atributo class no es obligatorio que sea único, de forma que muchos elementos HTML diferentes pueden compartir el mismo valor para su atributo class. 

De esta forma, la recomendación general es la de utilizar el selector de ID

cuando se quiere aplicar un estilo a un solo elemento específico de la página y utilizar el selector de clase cuando se quiere aplicar un estilo a varios elementos diferentes de la página HTML. 

Al igual que los selectores de clase, en este caso también se puede restringir el alcance del selector mediante la combinación con otros selectores. El siguiente ejemplo aplica la regla CSS solamente al elemento de tipo <p> que tenga un atributo id igual al indicado: p\#aviso \{ color: blue; \}

A primera vista, restringir el alcance de un selector de ID puede parecer absurdo. En realidad, un selector de tipo p\#aviso sólo tiene sentido cuando el archivo CSS se aplica sobre muchas páginas HTML diferentes. 

En este caso, algunas páginas pueden disponer de elementos con un atributo idigual a aviso y que no sean párrafos, por lo que la regla anterior no se aplica sobre esos elementos. 

No debe confundirse el selector de ID con los selectores anteriores: 11





2º SMR **AW - CSS**

/\* Todos los elementos de tipo "p" con atributo id="aviso" \*/

p\#aviso \{ ... \}

/\* Todos los elementos con atributo id="aviso" que estén dentro de cualquier elemento de tipo "p" \*/

p \#aviso \{ ... \}

/\* Todos los elementos "p" de la página y todos los elementos con atributo id="aviso" de la página \*/

p, \#aviso \{ ... \}

**1.6. Combinación de selectores básicos**

CSS permite la combinación de uno o más tipos de selectores para restringir el alcance de las reglas CSS. A continuación se muestran algunos ejemplos habituales de combinación de selectores. 

.aviso .especial \{ ... \}

El anterior selector solamente selecciona aquellos elementos con un class="especial" que se encuentren dentro de cualquier elemento con un class="aviso". 

Si se modifica el anterior selector:

div.aviso span.especial \{ ... \}

Ahora, el selector solamente selecciona aquellos elementos de tipo <span> con un atributo class="especial" que estén dentro de cualquier elemento de tipo <div>que tenga un atributo class="aviso". 

La combinación de selectores puede llegar a ser todo lo compleja que sea necesario:

ul\#menuPrincipal li.destacado a\#inicio \{ ... \}

El anterior selector hace referencia al enlace con un atributo id igual a inicio que se encuentra dentro de un elemento de tipo <li> con un atributo class igual a destacado, que forma parte de una lista <ul> con un atributo id igual a menuPrincipal. 

12





2º SMR **AW - CSS**

2. Selectores avanzados

Utilizando solamente los selectores básicos de la sección anterior, es posible diseñar prácticamente cualquier página web. No obstante, CSS

define otros selectores más avanzados que permiten simplificar las hojas de estilos. 

Desafortunadamente, el navegador Internet Explorer 6 y sus versiones anteriores no soportaban este tipo de selectores avanzados, por lo que su uso no era común hasta hace poco tiempo. Si quieres consultar el soporte de los selectores en los distintos navegadores, puedes utilizar las siguientes referencias:



Lista completa de los selectores que soporta cada versión de cada navegador



Test online en el que puedes comprobar los selectores que soporta el navegador con el que realizas el test

**2.1. Selector de hijos**

Se trata de un selector similar al selector descendente, pero muy diferente en su funcionamiento. Se utiliza para seleccionar un elemento que es *hijo directo * de otro elemento y se indica mediante el *"signo de* *mayor que" *\(>\):

p > span \{ color: blue; \}

<p><span>Texto1</span></p> 

<p><a href="\#"><span>Texto2</span></a></p> En el ejemplo anterior, el selector p > span se interpreta como *"cualquier* *elemento <span> que sea hijo directo de un elemento <p>" *, por lo que el primer elemento <span>cumple la condición del selector. Sin embargo, el segundo elemento <span> no la cumple porque es descendiente pero no es hijo directo de un elemento <p>. 

El siguiente ejemplo muestra las diferencias entre el selector descendente y el selector de hijos:

p a \{ color: red; \}

13





2º SMR **AW - CSS**

p > a \{ color: red; \}

<p><a href="\#">Enlace1</a></p> 

<p><span><a href="\#">Enlace2</a></span></p> El primer selector es de tipo descendente y por tanto se aplica a todos los elementos <a> que se encuentran dentro de elementos <p>. En este caso, los estilos de este selector se aplican a los dos enlaces. 

Por otra parte, el selector de hijos obliga a que el elemento <a> sea hijo directo de un elemento <p>. Por lo tanto, los estilos del selector p > a no se aplican al segundo enlace del ejemplo anterior. 

**2.2. Selector adyacente**

El selector adyacente se emplea para seleccionar elementos que en el código HTML de la página se encuentran justo a continuación de otros elementos. Su sintaxis emplea el signo \+ para separar los dos elementos: elemento1 \+ elemento2 \{ ... \}

Si se considera el siguiente código HTML:

<body> 

<h1>Titulo1</h1> 

<h2>Subtítulo</h2> 

... 

<h2>Otro subtítulo</h2> 

... 

</body> 

La página anterior dispone de dos elementos <h2>, pero sólo uno de ellos se encuentra inmediatamente después del elemento <h1>. Si se quiere aplicar diferentes colores en función de esta circunstancia, el selector adyacente es el más adecuado:

h2 \{ color: green; \}

14





2º SMR **AW - CSS**

h1 \+ h2 \{ color: red \}

Las reglas CSS anteriores hacen que todos los <h2> de la página se vean de color verde, salvo aquellos <h2> que se encuentran inmediatamente después de cualquier elemento <h1> y que se muestran de color rojo. 

Técnicamente, los elementos que forman el selector adyacente deben cumplir las dos siguientes condiciones:



elemento1 y elemento2 deben ser *elementos hermanos*, por lo que su elemento padre debe ser el mismo. 



elemento2 debe aparecer inmediatamente después de elemento1 en el código HTML de la página. 

El siguiente ejemplo es muy útil para los textos que se muestran como libros:

p \+ p \{ text-indent: 1.5em; \}

En muchos libros, suele ser habitual que la primera línea de todos los párrafos esté indentada, salvo la primera línea del primer párrafo. Con el selector p \+ p, se seleccionan todos los párrafos de la página que estén precedidos por otro párrafo, por lo que no se aplica al primer párrafo de la página. 

**2.3. Selector de atributos**

El último tipo de selectores avanzados lo forman los selectores de atributos, que permiten seleccionar elementos HTML en función de sus atributos y/o valores de esos atributos. 

Los cuatro tipos de selectores de atributos son:



\[nombre\_atributo\], selecciona los elementos que tienen establecido el atributo llamado nombre\_atributo, independientemente de su valor. 



\[nombre\_atributo=valor\], 

selecciona los elementos que tienen

establecido un atributo llamado nombre\_atributo con un valor igual a valor. 



\[nombre\_atributo~=valor\], selecciona los elementos que tienen establecido un atributo llamado nombre\_atributo y al menos uno de los valores del atributo es valor. 

15





2º SMR **AW - CSS**



\[nombre\_atributo|=valor\], 

selecciona los elementos que tienen

establecido un atributo llamado nombre\_atributo y cuyo valor es una serie de palabras separadas con guiones, pero que comienza con valor. Este tipo de selector sólo es útil para los atributos de tipo lang que indican el idioma del contenido del elemento. 

A continuación se muestran algunos ejemplos de estos tipos de selectores:

/\* Se muestran de color azul todos los enlaces que tengan un atributo "class", independientemente de su valor \*/

a\[class\] \{ color: blue; \}

/\* Se muestran de color azul todos los enlaces que tengan un atributo "class" con el valor "externo" \*/

a\[class="externo"\] \{ color: blue; \}

/\* Se muestran de color azul todos los enlaces que apunten al sitio "http://www.ejemplo.com" \*/

a\[href="http://www.ejemplo.com"\] \{ color: blue; \}

/\* Se muestran de color azul todos los enlaces que tengan un atributo "class" en el que al menos uno de sus valores sea "externo" \*/

a\[class~="externo"\] \{ color: blue; \}

/\* Selecciona todos los elementos de la página cuyo atributo

"lang" sea igual a "en", es decir, todos los elementos en inglés \*/

\*\[lang=en\] \{ ... \}

16





2º SMR **AW - CSS**

/\* Selecciona todos los elementos de la página cuyo atributo

"lang" empiece por "es", es decir, "es", "es-ES", "es-AR", etc. \*/

\*\[lang|="es"\] \{ color : red \}

3. Agrupación de reglas

Cuando se crean archivos CSS complejos con decenas o cientos de reglas, es habitual que los estilos que se aplican a un mismo selector se definan en diferentes reglas:

h1 \{ color: red; \}

... 

h1 \{ font-size: 2em; \}

... 

h1 \{ font-family: Verdana; \}

Las tres reglas anteriores establecen el valor de tres propiedades diferentes de los elementos <h1>. Antes de que el navegador muestre la página, procesa todas las reglas CSS de la página para tener en cuenta todos los estilos definidos para cada elemento. 

Cuando el selector de dos o más reglas CSS es idéntico, se pueden agrupar las declaraciones de las reglas para hacer las hojas de estilos más eficientes:

h1 \{

color: red; 

font-size: 2em; 

font-family: Verdana; 

\}

El ejemplo anterior tiene el mismo efecto que las tres reglas anteriores, pero es más eficiente y es más fácil de modificar y mantener por parte de los diseñadores. Como CSS ignora los espacios en blanco y las nuevas líneas, también se pueden agrupar las reglas de la siguiente forma: 17





2º SMR **AW - CSS**

h1 \{ color: red; font-size: 2em; font-family: Verdana; \}

Si se quiere reducir al máximo el tamaño del archivo CSS para mejorar ligeramente el tiempo de carga de la página web, también es posible indicar la regla anterior de la siguiente forma: h1 \{color:red;font-size:2em;font-family:Verdana;\}

4. Herencia

Una de las características principales de CSS es la herencia de los estilos definidos para los elementos. Cuando se establece el valor de una propiedad CSS en un elemento, sus elementos descendientes heredan de forma automática el valor de esa propiedad. Si se considera el siguiente ejemplo:

<\!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 

"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 

<html xmlns="http://www.w3.org/1999/xhtml"> 

<head> 

<meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1" /> 

<title>Ejemplo de herencia de estilos</title> 

<style type="text/css"> 

body \{ color: blue; \}

</style> 

</head> 

<body> 

<h1>Titular de la página</h1> 

<p>Un párrafo de texto no muy largo.</p> 

</body> 

</html> 

18





2º SMR **AW - CSS**

En el ejemplo anterior, el selector body solamente establece el color de la letra para el elemento <body>. No obstante, la propiedad color es una de las que se heredan de forma automática, por lo que todos los elementos descendientes de <body>muestran ese mismo color de letra. Por tanto, establecer el color de la letra en el elemento <body> de la página implica cambiar el color de letra de todos los elementos de la página. 

Aunque la herencia de estilos se aplica automáticamente, se puede anular su efecto estableciendo de forma explícita otro valor para la propiedad que se hereda, como se muestra en el siguiente ejemplo:

<\!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 

"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 

<html xmlns="http://www.w3.org/1999/xhtml"> 

<head> 

<meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1" /> 

<title>Ejemplo de herencia de estilos</title> 

<style type="text/css"> 

body \{ font-family: Arial; color: black; \}

h1 \{ font-family: Verdana; \}

p \{ color: red; \}

</style> 

</head> 

<body> 

<h1>Titular de la página</h1> 

<p>Un párrafo de texto no muy largo.</p> 

</body> 

</html> 

En el ejemplo anterior, se establece en primer lugar el color y tipo de letra del elemento <body>, por lo que todos los elementos de la página se 19





2º SMR **AW - CSS**

mostrarían con ese mismo color y tipo de letra. No obstante, las otras reglas CSS modifican alguno de los estilos heredados. 

De esta forma, los elementos <h1> de la página se muestran con el tipo de letra Verdana establecido por el selector h1 y se muestran de color negro que es el valor heredado del elemento <body>. Igualmente, los elementos <p> de la página se muestran del color rojo establecido por el selector p y con un tipo de letra Arialheredado del elemento <body>. 

La mayoría de propiedades CSS aplican la herencia de estilos de forma automática. Además, para aquellas propiedades que no se heredan automáticamente, CSS incluye un mecanismo para forzar a que se hereden sus valores, tal y como se verá más adelante. 

Por último, aunque la herencia automática de estilos puede parecer complicada, simplifica en gran medida la creación de hojas de estilos complejas. Como se ha visto en los ejemplos anteriores, si se quiere establecer por ejemplo la tipografía base de la página, simplemente se debe establecer en el elemento <body> de la página y el resto de elementos la heredarán de forma automática. 

5. Colisiones de estilos

En las hojas de estilos complejas, es habitual que varias reglas CSS se apliquen a un mismo elemento HTML. El problema de estas reglas múltiples es que se pueden dar colisiones como la del siguiente ejemplo: p \{ color: red; \}

p \{ color: blue; \}

<p>...</p> 

¿De qué color se muestra el párrafo anterior? CSS tiene un mecanismo de resolución de colisiones muy complejo y que tiene en cuenta el tipo de hoja de estilo que se trate \(de navegador, de usuario o de diseñador\), la importancia de cada regla y lo específico que sea el selector. 

El método seguido por CSS para resolver las colisiones de estilos se muestra a continuación:

20





2º SMR **AW - CSS**

1. Determinar todas las declaraciones que se aplican al elemento para el medio CSS seleccionado. 

2. Ordenar las declaraciones según su origen \(CSS de navegador, de usuario o de diseñador\) y su prioridad \(palabra clave \!important\). 

3. Ordenar las declaraciones según lo específico que sea el selector. 

Cuanto más genérico es un selector, menos importancia tienen sus declaraciones. 

4. Si después de aplicar las normas anteriores existen dos o más reglas con la misma prioridad, se aplica la que se indicó en último lugar. 

Hasta que no se expliquen más adelante los conceptos de tipo de hoja de estilo y la prioridad, el mecanismo simplificado que se puede aplicar es el siguiente:

1. Cuanto más específico sea un selector, más importancia tiene su regla asociada. 

2. A igual *especificidad*, se considera la última regla indicada. 

Como en el ejemplo anterior los dos selectores son idénticos, las dos reglas tienen la misma prioridad y prevalece la que se indicó en último lugar, por lo que el párrafo se muestra de color azul. 

En el siguiente ejemplo, la regla CSS que prevalece se decide por lo específico que es cada selector:

p \{ color: red; \}

p\#especial \{ color: green; \}

\* \{ color: blue; \}

<p id="especial">...</p> Al elemento <p> se le aplican las tres declaraciones. Como su origen y su importancia es la misma, decide la especificidad del selector. El selector \* es el menos específico, ya que se refiere a *"todos los elementos* *de la página" *. El selector pes poco específico porque se refiere a *"todos los* *párrafos de la página" *. Por último, el selector p\#especial sólo hace referencia a *"el párrafo de la página cuyo atributo idsea igual a especial" *. 

Como el selector p\#especial es el más específico, su declaración es la que se tiene en cuenta y por tanto el párrafo se muestra de color verde. 

21



