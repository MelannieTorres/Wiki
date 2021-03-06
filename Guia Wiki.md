# Guía para editar la Wiki
El propósito de esta guía es que cualquier miembro del equipo de CaveLabs sea capaz de agregar, descargar y editar contenido cumpliendo con las políticas del departamento. En ella se podrán encontrar los pasos que se deben seguir para manejar el contenido de la Wiki además de un breve manual donde se explicará la sintaxis que será utilizada por el departamento de CaveLabs.

## Index
* [¿Qué es y cómo se come una Wiki?](#Wiki)

* [¿Qué es lo que va en el README y cómo va ordenado?](#README)

* [¿Cómo creo un nuevo documento y dónde lo guardo?](#NuevoDocumento)

* [¿Cómo nombro a mi nuevo documento?](#Nombro)

* [Ya tengo mi documento ¿Ahora qué?](#DocumentoListo)

* [No se agregar imágenes, links, etc aiuda](#Imagenes)

* [Bueno ahora ya se agregar imágenes pero ¿Que hago con las minutas?](#Minutas)

* [¿Por qué git y no drive?](#Git)

<a id="Wiki"></a>
## ¿Qué es y cómo se come una Wiki?

De acuerdo a wikipedia una wiki es 
> Un término que alude al nombre que recibe un sitio web, donde los mismos usuarios crean, modifican o eliminan contenidos que, generalmente, comparten.

Por lo tanto la wiki de Cavelabs será un sitio dónde se encontrará la documentación de los procesos, minutas, guías, formatos, scripts, políticas, estándares y tutoriales o cursos que ayuden al departamento a mejorar.

<a id="README"></a> 
## ¿Qué es lo que va en el README y cómo va ordenado? 
El README es la página principal de la Wiki, donde solamente puede contener un index donde se encontrarán los links a los documentos cuyo propósito sea general. Por ejemplo un link hacia la página de minutas, o la página de los procesos que son utilizados en arquitectura, configuración, planning, etc.

El index contiene dos apartados:
  * Procesos: Documentos que dirigen a los procesos de cada módulo del CMMI, por ejemplo, el link que te dirige a los procesos de configuración, calidad, requerimientos. 
  * General: Documentos que dirige a cosas generales, por ejemplo el link de las minutas o tutoriales.

![Readme](https://image.prntscr.com/image/S_Q9Ka2XQdqSKp23URZLQA.png)

El nombre del link debe de ser pequeño pero que explique a qué es lo que contiene. Debajo del nombre una pequeña descripción no mayor a un renglón de qué es lo que se encuentra en ese archivo.

<a id="NuevoDocumento"></a> 
## ¿Cómo creo un nuevo documento y dónde lo guardo?
Para cada guía y formato es necesario crear un documento nuevo que se encuentre en la carpeta de su fase correspondiente, por ejemplo la guía de requisitos de la fase de incepción se encontrará en la carpeta de “Incepción”; si es necesario se puede crear un documento nuevo para el script, sin embargo es preferible que todos los scripts se encuentren en el documento de su respectiva fase, por ejemplo el script de requerimientos que es utilizado en la fase inicial debería de estar en el documento de Fase Incepcion.md

Si la carpeta no está creada, se puede crear fácilmente de la siguiente manera
![carpetas](https://i.stack.imgur.com/9Ifmj.gif)

Todos los documentos con excepción de las minutas y los documentos donde estarán todos los links (configuracion.md, arquitectura.md, etc) deberán de estar en una carpeta específica para cada uno, por ejemplo todas las guías que son usadas en configuración serán guardadas en “configuracion/guias/Guia Ejemplo.md” y así sucesivamente.

![formato](https://image.prntscr.com/image/G-z1g-2jRz_-GzJoXsaBqg.png)

Los documentos donde se encuentran sólamente links (configuración.md, arquitectura.md, calidad.md, etc) estarán en el root del proyecto.

Las minutas deberán de ser un pdf, para saber más de las minutas puedes ir al apartado de [Minutas](#Minutas), mientras que los formatos deberán de estar como un documento de word.

Donde se escribe el nombre de la carpeta en el espacio correspondiente al nombre del archivo y despues se escribe “/” para indicar que es una carpeta. 

Si sólo se requiere un documento para un documento de propósito general puede ser creado en el root del proyecto.

<a id="Nombro"></a> 
## ¿Cómo nombro a mi nuevo documento?
El documento debe de tener el nombre en español y debe de utilizar espacios para que sea más fácil leer el nombre. La longitud del nombre de preferencia debe de ser de máximo dos palabras. Es importante recordar poner la extensión “.md” al final del nombre para que Github lo reconozca como un documento de markdown.

<a id="DocumentoListo"></a> 
## Ya tengo mi documento ¿Ahora qué?
Es importante tener como título principal el nombre del documento para que la persona tenga continuidad al documento que está leyendo. Después del título se debe de poner una pequeña introducción por si alguién no recuerda que es eso en específico. Después de la introducción, si el documento contiene varios apartados es necesario tener un index que vaya a los documentos necesitados o a las secciones del documento. Es importante seguir el siguiente formato de inicio para mantener una estandarización en toda la documentación del equipo.

![sintaxis](https://image.prntscr.com/image/qWt7qq-ESa_Ky4r3YVCyhg.png)

Para los documentos de procesos es necesario tener un apartado de "Procesos Generales" que son todos los procesos que son utilizados en cualquier momento del desarrollo, después, si es necesario, tiene que tener un apartado de "Procesos utilizados en incepción" , donde estarán todos los procesos que se utilizan sólamente en la fase de incepción y así sucesivamente con las fases restantes (construcción y transición). Dentro de cada apartado no sólo se encontraran los procesos sino que también debe de haber apartados dentro de éstos para guías, formatos, etc. en el apartado correspondiente, por ejemplo, la plantilla para crear procesos deberá de estar dentro del apartado de "Formatos" que se encuentra en "Procesos Generales" en el archivo "procesos.md"

Recuerda poner al final del documento "Última edición: @username mes dia, año.", por ejemplo "Última edición: @pirty6 enero 22, 2018". Si más personas aportaron al documento entonces se tienen que también poner sus usernames, por ejemplo "Última edición: @pirty6, @filyv enero 22, 2018".

Al terminar de editar el documento que se ha creado o uno ya hecho, siempre se tiene que hacer un commit donde se crea un pull request. Después el manager de configuración validará los cambios, si todo esta bien, entonces el manager de configuración hará el merge a master. 

De esta manera será posible ver cuándo un documento fue creado, que será cuando no tenga número, y el número de veces que fue modificado.

**Si lo único que hiciste fue corregir typos puedes hacer merge directamente.**

![rama](https://image.prntscr.com/image/k-CINQVrTs2_iyL_lO_oAA.png)

Al darle click en create a new branch aparecerá la siguiente pantalla

![pantalla](https://image.prntscr.com/image/u6dX_p8HTFan6Dfz2zMhrQ.png)

En esta pantalla sólo dale click a create pull request, y de ahí espera feedback del maanager de configuración.

<a id="Imagenes"></a> 
## No se agregar imágenes, links, etc aiuda 
Para agregar links que lleven a algún apartado dentro del mismo documento:

![anchors](https://image.prntscr.com/image/0aY45VJtQQaXv480psGp8g.png)

Lo que dice en el id tiene que ser exactamente lo mismo que se encuentra dentro del parentesis, mientras que lo que se encuentra dentro de los brackets es el nombre, por lo tanto si tienes un id que sea "hewwo" (id="hewwo") lo que está dentro del paréntesis despues del # tiene que ser hewwo (#hewwo).

Eso esta muy chido pero sigo sin saber como agregar una imagen.
Aquí hay una [guía oficial de Github](https://guides.github.com/features/mastering-markdown/) y esta otra [guía creada por el usuario adam-p](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet), que te ayudarán en tu viaje de aprendizaje de Markdown.

<a id="Minutas"></a>
## Bueno ahora ya se agregar imágenes pero ¿Que hago con las minutas?

El formato usado por el departamento para las minutas se encuentra en la carpeta Minutas/Formatos. Todos los formatos relacionados a las minutas deben de encontrarse en esa carpeta.

Todas las minutas deben de tener el siguiente nombre "Minuta Fecha" donde Fecha es la fecha en que se realizó, por ejemplo si hubo una minuta en el día 24 de enero de 2018, el documento se llamará "Minuta del 24 de enero del 2018". Las minutas deben de encontrarse en la carpeta que les corresponde dentro de minutas, que se encuentra en el root de la wiki, por ejemplo una minuta del equipo de "CADHU" debe de encontrarse en la dirección Minutas/CADHU. Las minutas tienen que estar en pdf para que se pueda integrar la foto de los presentes junto con su firma y los acuerdos y el resúmen de la junta. 

Después debe de haber un link en el archivo llamado “Minutas.md”, encontrado en el root de la wiki, en el apartado que le corresponda cuyo nombre sea “Minuta del dia, de mes, del año; por ejemplo una minuta general llevada a cabo el 19 de enero del 2018 debe de ser encontrada como "Minuta del 19 de Enero del 2018" que te dirija a la minuta en específico, y que se encuentre en el apartado de "Minutas Generales", lo mismo sucede con los formatos utilizados para las minutas.

## ¿Por qué git y no drive?
Porque git te permite tener un control de los cambios que se han realizado, quién lo hizo y cuándo se realizo. Toda esta información se encuentra en el botón de history que se encuentra en cualquier archivo de git. 

![history](https://image.prntscr.com/image/6wG8dwR0Te22gdfV7ehfgQ.png)

![thatsAll](https://i.ytimg.com/vi/0FHEeG_uq5Y/maxresdefault.jpg)
---

Última edición: @pirty6 enero 01, 2018.
