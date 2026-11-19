# Actividad final de repaso: crea la web de SENDERANDO

**HTML5 · Práctica individual · Sin CSS ni JavaScript**

## 1. Tu misión

Imagina que trabajas para **SENDERANDO**, una empresa de senderismo que quiere presentar una ruta y ofrecer recomendaciones a sus clientes. Tu misión es **observar una web ya publicada y reproducirla desde cero usando únicamente HTML5**.

No recibirás el código HTML de esa web ni archivos de ejemplo. **Este README es el único documento que necesitas descargar**: aquí encontrarás las instrucciones, las etiquetas que debes practicar y las comprobaciones previas a la entrega.

Al finalizar debes haber creado **dos páginas HTML enlazadas**:

- **`index.html`**: la página principal, con la presentación de la ruta, una galería de imágenes, el itinerario, una tabla de horarios y un vídeo.
- **`recursos.html`**: la página de consejos para senderistas, con navegación para volver a la página principal.

Tu trabajo consiste en reproducir **el contenido, el orden de los apartados y el funcionamiento de la navegación**. No es necesario que inventes otra empresa ni diseñes una página diferente.

> **Norma fundamental:** trabaja exclusivamente con HTML. No utilices hojas de estilos CSS, `<style>`, atributos `style` ni JavaScript. Puedes utilizar los atributos HTML solicitados, como `width`, `height`, `rowspan`, `colspan` y `border`.

## 2. Accede a la web que debes reproducir

<a href="https://practicahtml-eight.vercel.app/" target="_blank">https://practicahtml-eight.vercel.app/</a>



Sigue estas indicaciones:

1. Abre esa dirección en el navegador.
2. En la portada, selecciona **«Ver la web que tienes que replicar»**. El modelo se abrirá en otra pestaña.
3. Recorre la **primera página** de arriba abajo y observa la cabecera, el menú, las secciones, las imágenes, el itinerario, la tabla, el vídeo y el bloque «Antes de salir...».
4. Comprueba que **Nuestra ruta**, **Galería**, **Itinerario** y **Vídeo** te llevan a apartados de la misma página.
5. Pulsa **Consejos** y examina la **segunda página**. Comprueba cómo se vuelve a la primera y cómo se enlaza a apartados concretos de ella.
6. Vuelve a la portada cuando quieras acceder al **test de 30 preguntas**.

**Importante:** observa la web **en el navegador**. No tienes que descargar ni copiar los archivos de la web publicada. El reto es construir tú mismo su código HTML a partir de lo que ves y de esta guía.

## 3. Prepara tu proyecto

Crea una carpeta con esta estructura:

```text
senderando/
├── index.html
├── recursos.html
└── imagenes/
    └── paseo.jpg       (o las imágenes locales que elijas)
```

- Los nombres de los archivos deben coincidir con los que utilices en los enlaces.
- **`index.html` será tu página principal**. 
- Guarda una imagen propia en la carpeta de  `imagenes` y enlazala.
- Muestra otra imagen usando la url. En el banco de imagenes unsplash puedes elegir una imagen y copiar la direccion de esa imagen. Así podrás mostrarla. 
- Recuerda que tienes que usar imágenes libres de derechos. 

## 4. Primera página: `index.html`

Reproduce los siguientes apartados en el **mismo orden** que aparecen en la web publicada.

### A. Estructura inicial del documento

En el head incluye un favicon y un título. 

### B. Cabecera y menú

En la **cabecera** (`<header>`) coloca:

- El nombre **SENDERANDO** en un encabezado `<h1>`.
- El lema **«Descubre nuevos rincones, paso a paso.»** en un párrafo `<p>`.

Debajo, crea un **menú** con `<nav>` y enlaces `<a>`. Este navegador son anclas es decir enlaces a secciones de la misma página. Excepto el enlace consejos que enlazará con una segunda página que tendrás que crear. 

Aquí tienes un ejemplo. 

| Texto visible | Atributo `href` |
|---|---|
| Nuestra ruta | `#presentacion` |
| Galería | `#galeria` |
| Itinerario | `#itinerario` |
| Vídeo | `#video` |
| Consejos | `recursos.html` |

Los primeros cuatro son **enlaces internos con anclas**; el último abre **otra página de tu proyecto**.

**Recuerda:** `href="#galeria"` busca un elemento con `id="galeria"` en la misma página. Los identificadores deben escribirse exactamente igual y **no pueden repetirse** dentro del documento.

### C. Presentación de la ruta

Dentro de `<main>`, crea una sección `<section id="presentacion">` con:

- Un `<h2>`: **Ruta del Bosque y el Mirador**.
- Dos párrafos `<p>` que presenten la empresa y el carácter ficticio de la ruta.
- Un bloque `<article>` con `<h3>`: **Características de la ruta**.

**Aquí debes utilizar una lista desordenada `<ul>`**, porque las características no siguen un orden temporal. Cada dato debe ir en un `<li>`:

- **Distancia:** 6 km.
- **Duración:** 3 horas.
- **Dificultad:** baja.
- **Modalidad:** senderismo.

Utiliza `<strong>` para destacar los nombres de las características.

### D. Galería de imágenes

Crea `<section id="galeria">` con el encabezado **Imágenes de la ruta** y un párrafo introductorio.

Incluye **dos imágenes una al lado de la otra** dentro de un `<figure>`, seguidas por un `<figcaption>` que las describa. Cada `<img>` debe tener:

- `src`: ubicación correcta de la fotografía (archivo local o URL directa).
- `alt`: descripción útil de lo que aparece en ella.
- `width="320"`.
- `height="210"`.

**Cómo intentar que aparezcan una junto a la otra sin CSS:** coloca las dos etiquetas `<img>` seguidas, sin un `<p>` ni un `<figcaption>` entre ellas. Si la ventana tiene espacio suficiente podrán quedar en la misma línea; **no es obligatorio garantizarlo en todos los tamaños de pantalla**.


### E. Itinerario: lista ordenada

Crea `<section id="itinerario">` y el encabezado **Itinerario de la jornada**.

**Aquí debes utilizar una lista ordenada `<ol>`**, ya que las etapas suceden en este orden:

1. Encuentro y bienvenida.
2. Caminata por el bosque.
3. Descanso en el mirador.
4. Regreso al punto de partida.

Cada etapa se escribe en un `<li>`.

### F. Tabla de horarios: `rowspan` y `colspan`

Debajo del itinerario, reproduce la tabla titulada **Programa de actividades**. Debe contener **tres columnas**: **Hora**, **Actividad** y **Lugar**.

Utiliza estas etiquetas:

- `<table>` para crear la tabla; se permite `border="2"` para ver sus bordes en esta práctica.
- `<caption>` para el título de la tabla.
- `<thead>` para la fila de encabezados y `<tbody>` para los datos.
- `<tr>` para las filas.
- `<th scope="col">` para los tres encabezados de columna.
- `<th scope="row">` para las horas cuando corresponda.
- `<td>` para las demás celdas.

**Atención a las dos celdas especiales:**

**1. `rowspan="2"`: une dos filas.** En la hora **09:30–11:00**, una sola celda de la columna **Hora** corresponde a las actividades **Caminata / Sendero** y **Observación de flora / Bosque**. Escribe `rowspan="2"` en la celda de la hora. **En la fila siguiente no vuelvas a crear una celda para la hora**: ya está ocupada por la celda expandida.

**2. `colspan="2"`: une dos columnas.** En la última fila, a las **12:00**, el texto **Regreso y despedida** debe ocupar conjuntamente las columnas **Actividad** y **Lugar**. Coloca `colspan="2"` en esa celda y **no añadas otra celda para Lugar**.

Resumen de lo que debes ver en el modelo:

| Hora | Actividad | Lugar |
|---|---|---|
| 09:00 | Bienvenida | Punto de encuentro |
| 09:30–11:00 *(hora compartida por dos filas)* | Caminata | Sendero |
| *(la misma celda de hora continúa)* | Observación de flora | Bosque |
| 12:00 | Regreso y despedida *(ocupa Actividad y Lugar)* | |

> Esta tabla del README es una **explicación**, no la tabla HTML resuelta. En tu web debes utilizar los atributos `rowspan` y `colspan` para conseguir la unión real de celdas.

### G. Vídeo de YouTube

Crea `<section id="video">` con el título **Descubre la naturaleza en vídeo**, un párrafo introductorio y un `<iframe>`.

El `<iframe>` debe contener el enlace que te facilita you tube. 


### H. Información complementaria: «Antes de salir...»

Crea una `<section>` con un encabezado `<h2>` y **una lista desordenada `<ul>`** con estos consejos, cada uno en su `<li>`:

- Consultar el tiempo mediante **un enlace externo** a `https://www.eltiempo.es`.
- Llevar suficiente agua.
- Utilizar ropa y calzado cómodos.
- Llevar protección solar y una gorra.
- Consultar la segunda página de consejos mediante un enlace a `recursos.html`.

Haz que el enlace externo se abra en otra pestaña con `target="_blank"`.

### I. Pie de página

Crea un `<footer>` con:

- El nombre de la empresa y el año.
- Un enlace a `#presentacion` para volver al inicio de la ruta.
- Un enlace a `recursos.html` para entrar en la página de consejos.

## 5. Segunda página: `recursos.html`

**También debes reproducir la segunda página que se ve al pulsar «Consejos» en el sitio publicado.** No se entrega su código; debes observar su aspecto, sus textos y sus enlaces.

Como mínimo, comprueba que tu página:

- Es un documento HTML5 completo, con `<title>` propio y `lang="es"`.
- Tiene cabecera, menú, contenido principal y pie de página bien estructurados. El contenido de esta página es libre.
- Debe garantizar la usabilidad de forma que el usuario pueda volver a la página de origen (index).



La segunda página **no es opcional**: es una parte fundamental de la práctica.

## 6. Accesibilidad y usabilidad

Debes aplicar **al menos tres medidas de accesibilidad**. Puedes utilizar estas opciones, todas compatibles con HTML sin JavaScript:

| Buena práctica | Cómo aplicarla |
|---|---|
| Idioma del documento | `lang="es"` en `<html>`. |
| Imágenes comprensibles | `alt` descriptivo en las imágenes informativas. |
| Títulos bien jerarquizados | `<h1>` principal, `<h2>` para secciones y `<h3>` para apartados. |
| Enlaces claros | «Consejos para senderistas» en vez de «Haz clic aquí». |
| Tabla fácil de entender | `<caption>`, `<th>` y `scope` donde corresponda. |
| Vídeo identificado | `title` descriptivo en el `<iframe>`. |
| Estructura semántica | Uso correcto de `<nav>`, `<main>`, `<section>`, `<footer>`, etc. |

La usabilidad se demuestra, entre otras cosas, cuando el menú resulta claro, los enlaces llevan al destino esperado y es fácil volver a la página principal.

**El contraste entre texto y fondo también es importante**, pero en esta práctica no debes aplicar CSS: conserva los colores predeterminados del navegador. Lo trabajaremos en la siguiente fase del proyecto.

No se pide programar controles de teclado. Los enlaces nativos de HTML ya permiten navegar con teclado sin JavaScript.

## 7. Comentarios HTML

Añade **al menos un comentario HTML**. Puedes señalar los bloques principales, por ejemplo:

```html
<!-- MENÚ DE NAVEGACIÓN -->
```

Los comentarios sirven para organizar el código y no se muestran como texto en la página. Comprueba que los cierras correctamente con `-->`.

## 8. Test de 30 preguntas

Desde **la misma URL publicada del apartado 2**, vuelve a la portada y entra en **«Realizar el test de 30 preguntas»**.

El test repasa HTML5, estructura del documento, etiquetas, atributos, listas, tablas, enlaces, accesibilidad, usabilidad y comentarios. No tienes que descargar ningún archivo del test: se realiza desde el navegador.

## 9. Errores habituales

- Escribir `href="galeria"` en vez de `href="#galeria"` para un enlace a una sección.
- Repetir un mismo `id` en dos elementos de una página.
- Enlazar a `recursos.html` sin haber creado ese archivo.
- Poner la URL de una **página web** en el `src` de una imagen en vez de la URL directa de la fotografía.
- Confundir `<ul>` (lista sin orden) con `<ol>` (lista con secuencia).
- Crear celdas de más después de usar `rowspan="2"` o `colspan="2"`.
- Omitir la fuente de alguna fotografía o utilizarla sin comprobar su licencia.
- Olvidar `alt` en las fotografías o `title` en el vídeo incrustado.
- Incorporar CSS o JavaScript, que todavía no forman parte de esta práctica.

## 10. Lista de comprobación antes de entregar

- [ ] He visitado la **web publicada** y he examinado sus dos páginas.
- [ ] He creado `index.html` y `recursos.html` desde cero.
- [ ] Los dos documentos tienen estructura HTML5 completa y `lang="es"`.
- [ ] La cabecera muestra SENDERANDO y su lema.
- [ ] Funcionan las cuatro anclas del menú.
- [ ] Se puede ir de la primera página a Consejos y regresar.
- [ ] He utilizado `<ul>` para las características de la ruta.
- [ ] He utilizado `<ol>` para las etapas del itinerario.
- [ ] Aparecen las dos imágenes con `src`, `alt`, `width` y `height`.
- [ ] He indicado la fuente de **cada imagen** y revisado su licencia.
- [ ] La tabla tiene tres columnas, `<caption>` y encabezados.
- [ ] La hora 09:30–11:00 utiliza `rowspan="2"`.
- [ ] «Regreso y despedida» utiliza `colspan="2"`.
- [ ] El vídeo está insertado mediante `<iframe>` con `title`.
- [ ] El `<aside>` contiene una lista `<ul>` de recomendaciones.
- [ ] Funciona el enlace externo para consultar el tiempo.
- [ ] He aplicado al menos tres medidas de accesibilidad.
- [ ] He incluido al menos un comentario HTML.
- [ ] No he utilizado CSS, JavaScript ni `style`.
- [ ] He realizado el test de 30 preguntas en la página publicada.

## 11. Entrega de la actividad

**Lo que recibes:** únicamente este archivo `README.md` y el enlace a la web publicada. **No se entregan archivos HTML modelo**, porque debes escribirlos tú.

**Lo que debes entregar:** un **único archivo ZIP** con los archivos que hayas creado y las imágenes locales que utilices:

```text
senderando.zip
└── senderando/
    ├── index.html
    ├── recursos.html
    └── imagenes/
        └── ...
```

Antes de comprimir, abre las dos páginas directamente en el navegador y revisa que funcionan los enlaces, las anclas, las imágenes y el vídeo. No entregues capturas de pantalla en sustitución del HTML.

## 12. ¿Para qué servirá después este proyecto?

Esta práctica es la **primera fase de un proyecto**. Ahora construirás la estructura, los contenidos y la navegación con HTML5. Más adelante, cuando estudiemos **CSS**, podremos utilizar estas mismas páginas para añadir colores, tipografías, espaciado, una galería adaptable a móviles y un menú visualmente diseñado.

**Primero construimos una web correcta, comprensible y accesible; después trabajamos su apariencia.**
"# practicaHTML" 
