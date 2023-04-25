# Daguerre, estudio de fotografía y formación estética.

Bienvenidas a Daguerre, estudio de fotografía y formación estética *ficticio*.  
A continuación podrán encontrar distintos links.  
- Link de [wireframes](https://drive.google.com/file/d/1RXgLptg6L6-x99ZQXYBniLrKhmlS9Bik/view?usp=sharing)
- Link de [pages](https://rnadiaceline.github.io/PF-Ruiz/)
- Link de [servidor](https://pf-ruiz.vercel.app/)


## Lista de contenidos
1. <a href="#paginas">Páginas</a>
    - <a href="#index">Índice</a>
    - <a href="#portfolio">Portfolio</a>
    - <a href="#courses">Courses</a> 
    - <a href="#workplace">Workplace</a> 
    - <a href="#about">About</a>
    - <a href="#contact">Contact</a>
2. <a href="#sass">SASS</a>
3. <a href="#seo">SEO</a>
4. <a href="#aclaraciones">Algunas aclaraciones</a>
5. <a href="#agradecimientos">Agradecimientos</a>

<h2 id="paginas">Páginas</h2>

<h3 id="index">Índice</h3>

En primer lugar, en la página de inicio podemos encontrar un carrusel con cinco fotos, que es visible solo en mobile, ya que luego se convierte en un header, de una imagen al lado de la otra, visible a partir de la resolución de 768px. Desde los 1200px las imágenes se ven en blanco y negro, y aplicando la pseudoclase `:hover` al posicionarse con el cursor sobre la imagen, se muestra a color.  
Mi idea inicial era hacer un header con una sola imagen y el título encima, pero me arrepentí cuando casi me da un pico de estrés con el bendito POSITION. Así que cuando me presentaron al carrusel dije “Mi salvación!!!” y lloré de la emoción, jajaja.  
En segundo lugar, hay una breve introducción junto con un video en bucle, que se aprecian en una columna en mobile, y en dos a partir de los 768px. Después está la sección de *últimos proyectos*, que se muestra a modo de columna en mobile (con tres proyectos visibles), y como grid de los 768px en adelante (con cuatro proyectos visibles). Este grid es caserito.  
Por último, hay una sección de cursos hecha con un acordeón de BS. En cada solapa hay una introducción sobre cada tipo de curso y un botón de *ver más*, que lleva a la página de cursos. 

<h3 id="portfolio">Portfolio</h3>

En el portfolio hay un texto que, como quedaba muy largo, en mobile tiene dos párrafos, y en resoluciones más grandes tiene tres párrafos. Luego hay 36 imágenes (por supuesto, libres de derechos de autor👀) ubicadas en columna en resoluciones pequeñas y, aplicando el sistema de grillas de BS, en filas de 3 imágenes a medida que la resolución crece.   
Mi intención para esta sección era que en cada fila las fotos tuvieran un color similar, siguiendo una especie de patrón para organizarlas y que a la vez sea estético y apreciable para los visitantes. Para estas imágenes utilicé el live box *Fresco*, que sinceramente me causa un poco de molestia que al estar abrir las imágenes se pueda scrollear. Además, dichas fotografías tienen aplicada una animación de animate.css para que aparezcan de una manera sutil.   

<h3 id="courses">Courses</h3>

En la página de cursos también hay un acordeón, que a mi parecer está bastante cargado, pero no creí correcto mostrar algunos cursos en mobile, y otros en desktop. Dentro de cada una de las tres categorías de cursos, encontramos un listado de dichos cursos acompañados por una breve introducción. Esta lista de cursos tiene vínculos que debería llevar a cada uno de ellos, pero lo hacen a la pantalla de error 404.   
Cuando continuamos scrolleando encontramos una sección de *calendario académico*, que tiene un calendario medio feito y que tarda un poco en cargar, pero fue el mejor que encontré. Pensaba utilizar el de google, pero cuando lo probé pareciera que no actualizan el diseño desde el 2010, y quedaba muy contrastado con el layout del sitio. Igualmente, el calendario está vacío. Y debajo de él, hay una oración que invita a visitar la página de *workplace*, y a la cual está vinculada. 


<h3 id="workplace">Workplace</h3>

Lo primero que tengo para destacar de esta página es que usé mi cerebrito para redactar los textos. El primer texto es una introducción general de los sectores laborales y de enseñanza físicos. Luego, hay descripciones más específicas debajo de los subtítulos de *estudio* y *labs*, y cada parte se acompaña de dos imágenes del lugar que se describe. Todo esto se aprecia en columna en mobile y, las imágenes, en dos columnas a partir de los 768px.

<h3 id="about">About</h3>

En primer lugar podemos encontrar una sección similar a la página anterior, con una introducción y dos imágenes, que se distribuyen de igual manera en las distintas resoluciones. Seguidamente, hay un acordeón donde se describen los servicios ofrecidos y el equipamiento con el que se cuenta. Al ser un listado con más listas dentro se complica un poco hacerlo amigable para mobile, pero decidí dejarlo con muy poco margin en el eje x, y a medida que la resolución crece, este también, para que haya aire!!

<h3 id="contact">Contact</h3>

En contact encontramos un formulario de contacto con inputs de texto, email, submit, y un textarea. Este formulario me pareció ideal para aplicar un extend, ya que los inputs de texto y email son similares al textarea, solo que éste último es más alto. Después hay datos de contacto, como email, WhatsApp, redes sociales y dirección, que se encuentran centrados en mobile. En desktop, al estar el formulario y los datos en distintas sections, las ubiqué en fila con `flex-direction`, acá los datos se ubican a modo de columna con el texto alineado a la izquierda. Debajo de esta sección hay un iframe de un mapa, con una dirección ficticia. Y por último, encontramos una sección de *preguntas frecuentes* hecha con un acordeón de seis solapas.

<h2 id="sass">SASS</h2>

En cuanto a SASS, cree partials para las variables, para las propiedades comunes a varias páginas, la nav, el footer, para las páginas que tienen modificaciones específicas y para los breakpoints, de modo que todo esté más organizado, y todo está vinculado en main.scss con @import. Además, utilicé nesting siempre que fue posible, mixins, extend y maps para todos los colores del sitio.  
En cuanto a las variables, fueron usadas para la fuente y para el tamaño de los distintos headings. Para ellos también apliqué los mixins, con variables de tamaño y ancho de fuente y alineación de texto. Otro mixin que utilicé fue uno para modificar la apariencia de los vínculos de la nav y del footer, con cuatro variables, de color, decoración de texto, tamaño y ancho de fuente. Finalmente, como nombré antes, usé un extend en la página de contacto, más exactamente en el formulario.  

<h2 id="seo">SEO</h2>

La parte de SEO fue bastante ligera, ya que fui bastante al pie de la letra en cuanto a lo que es semántica. Luego de esta clase, generé la página de error 404 con una imagen, un texto, y un botón que retorna a la página de inicio, dicha página se vincula en cada newsletter y en el formulario de contacto, además de los cursos mencionados anteriormente. Por último, utilicé el meta description, siendo uno personalizado para cada página, y meta author.

<h2 id="aclaraciones">Algunas aclaraciones</h2>

- La mayoría de los textos fueron creados con ayuda de la inteligencia artificial.
- No logré ocultar el archivo main.css.map, pero sí la carpeta node_modules y la de wireframes, de la primera entrega.
- El newsletter se encuentra dentro de la etiqueta footer, porque lo encontré más práctico, espero que no sea incorrecto utilizarlo de esta manera.
- Intenté purgar el css, pero habían algunas cosas que se desacomodaban, entonces dejé el CSS compilado de SASS.
- La parte del trabajo con la que más me demoré y me frustré fue con la búsqueda de imágenes, porque buscaba que coincidieran en cuanto a colores. Además, en un principio las había descargado en una resolución muy alta, así que las 36 fotos del portfolio pesaban alrededor de 4MB, y antes de la clase en la que nos presentaron a *photopea* las achiqué una por una con otra herramienta online. Adiós mi espalda jajaja  
- Con respecto a los acordeones aplicados en la totalidad del proyecto, tuve dificultades para agregar más de tres solapas, ya que al copiar el código y cambiar el contenido, se abrían y cerraban ambas solapas en simultáneo, pero quemando mis neuronas me di cuenta de que solo necesitaba cambiar los IDs 😀 También me volví un poco loca tratando de cambiar los colores originales del acordeón y  la nav, ya que al ser de BS, cuando hacía click en un vínculo se ponía azul. Sin embargo, pude arreglarlo metiendo mano en el SASS de bootstrap, modificando el valor de sus variables. 

<h2 id="agradecimientos">Agradecimientos</h2>  

- Laura, gracias por hacer las clases tan dinámicas y alegres con esa linda energía.   
- Macarena, gracias por tu atención y compromiso para con los alumnos, yo nunca commiteé antes de recibir mis correcciones!!! jajaja   
- Chat GPT, gracias por hacerme la vida más fácil jajajaja  
  
Gracias por todo, quedé totalmente motivada a seguir aprendiendo sobre este mundo nuevo para mí <3 
