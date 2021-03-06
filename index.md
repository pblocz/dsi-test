---
layout: default
title: "[DSI] Cygnus - Diseño Guiado por Objetivos"
---

* Table of contents
{:toc}


<!--
[test url](.{{ site.pages | where:"id","site-test" | map: "url" }})
-->

<h1>Grupo 4 de DSI</h1>

<h4>Autores:</h4>
- Alejandro Aguirre
- Pablo Cabeza
- Jesús Doménech
- Diego González


# Investigación

El proyecto no está realmente definido, sino que se pretende investigar cual sería la aplicación que mejor se adecúe a las necesidades actuales del ámbito universitario, centrándonos especialmente en el *sharing* de apuntes, prácticas, etc. entre todos los miembros de la comunidad educativa. Será importante también proporcionar herramientas que faciliten el *feedback* entre alumnos y profesores, e incluso con alumnos de años anteriores.

Como ejemplo, esta aplicación podría utilizarse para el programa de mentorías de la UCM (que presente ciertas carencias en este aspecto) o para que los alumnos colaboren en la elaboración de apuntes o materiales didácticos oficiales para las asignaturas.

Todo esto son algunas de las características que se prevé que van a ser demandadas por los usuarios finales, pero será durante el proceso de investigación cuando se decidirá las funcionalidades finales de la aplicación.

## Plan de Investigación

### Planificación temporal

En el siguiente diagrama de Gantt se muestra el plan de trabajo ideado para realizar el proyecto:

![diagrama de gantt]({{site.baseurl}}/assets/img/gantt.png)

Como se observa en amarillo, se dedicará la mayor parte del tiempo a la **investigación**, cuyo plan está adjunto.

Con la información obtenida en las entrevistas y cuestionarios se procederá a realizar el **diseño de personas** durante las navidades hasta final de año.

La **definición de requisitos** será principalmente llevada a cabo los diez primeros días de enero.  Se desarrollará el **framework de interacción** del 13 al 21 de enero.

Por último, la etapa de **refinamiento** dispondrá de todo el tiempo restante hasta la presentación.


### Plan de desarrollo

Queremos lograr 2 cosas con la investigación previa:

1. Definir concretamente la especificación de nuestra aplicación en función de las necesidades y requisitos de los usuarios (el ámbito ya está definido)

2. Usar los datos obtenidos para crear las interacciones y artefactos necesarios en las siguientes fases de diseño


#### Entrevistas y cuestionarios

Nuestra principal fuente de información *en profundidad* serán las entrevistas, mientras que para obtener información *en cantidad* usaremos cuestionarios a muchos usuarios.


##### Tipos de usuarios

Hemos dividido a los usuarios de manera previa en distintos grupos. Se han obviado algunos como los roles administrativos, que no son primarios en nuestra aplicación. Con esto hemos obtenido:

- Futuros alumnos
- Alumnos de primeros cursos
- Alumnos experimentados, haciendo especial hincapié en mentores
- Ex-Alumnos
- Profesores

Esperamos obtener datos de todos los tipos de usuario. Como son muchos tipos y por las restricciones de tiempo no podremos hacer suficientes entrevistas, haremos de 2 a 4 entrevistas y esperamos obtener datos del resto de usuarios con cuestionarios.

##### Datos a recoger (genéricos)

A la hora de pensar las entrevistas y generar los cuestionarios, vamos a intentar recabar la información relevante, haciendo énfasis en:

###### Datos demográficos

- edad
- sexo
- nivel académico
- posición académica (alumno o no, curso)


###### Conocimiento del dominio

- aplicaciones del ámbito que usa
- cómo usa esas aplicaciones
- actividades que realiza en ella
- qué hace más a menudo
- qué le gusta de lo que usa
- qué no le gusta de lo que usa


###### Expectativas del sistema.

- Generar contenido o sólo consumir
- Nivel de sociabilidad de la aplicación
- Niveles de visibilidad de las asignaturas / grupos


#### Análisis de la competencia

A la vez que la investigación en usuarios, se realizará un análisis de la competencia. Hay dos categorías: **herramientas de campus virtual** y de **sharing de documentos**. Estos dos ámbitos son muy separados, es decir, normalmente hay herramientas para el aula y fuera de esta para compartir trabajos y apuntes, pero no juntas.


##### Herramientas de campus virtual

Investigaremos las distintas herramientas de ámbito universitario que hay, que suelen ser muy direccionales (el profesor es el que genera contenido). Entre ellas:

- Moodle
- Sakai
- WebCT

##### Sharing de documentos

Este punto es muy genérico, así que lo centraremos en herramientas que se usen para compartir documentos de tipo apuntes, o en ámbito universitario. Por el momento son conocidas las herramientas de:

- Patatabrava
- Rincón del vago
- Google Drive
- Dropbox


## Resultados

### Análisis de la competencia
{% include include_id page_id='analisis-competencia' %}

### Entrevista

Se han realizado finalmente tres entrevistas, hemos insistido mucho para poder conseguir la entrevista al profesor porque temíamos pocas respuestas en los cuestionarios, finalmente conseguimos entrevistar a un profesor y dos alumnos dejando los siguientes resultados:

+ Alumno UNED [(transcripción)]({{site.baseurl}}/assets/documents/alumno_uned_entrevista.txt).

+ Alumno [(transcripción)](./assets/documents/alumno_entrevista.txt).

De los alumnos, obtenemos principalmente que usan el campus virtual para revisar si hay apuntes del profesor y que les es muy pesada esta actividad porque en la mayoría de las situaciones no hay nada nuevo y han perdido mucho tiempo entrando. Otro punto sería que los alumnos prefieren tener tutorías presenciales antes que escribír un mensaje al profesor. Y por último, enlazado con el primer punto, les gustaría que hubiese un sistema de notificaciones para no perderse nada de lo relaccionado con la universidad.

+ Profesor [(transcripción)](./assets/documents/profesor_entrevista.docx).

Del profesor vemos principalmente que tiene apetito por usar las nuevas tecnologías con sus alumnos pero no da de sí las herramientas de que dispone. Además no ha querído aprender a usar nuevas herramientas porque le parecen demasiado complicadas para lo poco que le van a aportar. Desea que haya una mejor integración con las clases de hoy en día. Notamos también que el profesor prepara sus apuntes aparte y luego los sube a la aplicación. Por costumbres previas a ser profesor, revisa el email con frecuencia y usa con bastante frecuencia el ordenador.


### Encuestas

{% include include_id page_id='resumen-encuestas' %}


# Modelado

## Plan de Modelado

{% include include_id page_id='plan-modelado' %}

## Resultados

### Hipótesis de personas

{% include include_id page_id='hipotesis-personas' %}

#### Profesores

{% for variable in site.data.cooper.profesores.variables %}
	{% assign personas = site.data.cooper.profesores.personas %}
	{% include cooper_var.html %}
{% endfor %}

#### Alumnos

{% for variable in site.data.cooper.alumnos.variables %}
	{% assign personas = site.data.cooper.alumnos.personas %}
	{% include cooper_var.html %}
{% endfor %}


### Esqueletos

{% include panel-show.html panel_show_folder="esqueletos" %}

### Personas

{% include panel-show.html panel_show_folder="personas" %}


# Definición de requisitos

## Plan de Requisitos

{% include include_id page_id='plan-requisitos' %}

## Resultados

{%comment%}
{% assign probvisis = site.pages | where:'type','probvisi' %}
{% for prob in probvisis %}
{% include probvisi.html %}
{%endfor%}
{%endcomment%}

{% include include_id page_id='problemas-visiones' %}

### Expectativas de personas

#### Juan Martín de la Torre (prof nov)

+ Avanzado en nuevas tecnologías, tiene poca dificultad en aprender y usar nuevas herramientas web, móvil le presenta un poco más de dificultad.

+ Quiere impartir las clases verticales pero con cierta tendencia a la horizontalidad, es decir, impartir sus conocimientos, pero que el alumno esté muy implicado en la asignatura y con el resto de compañeros.

+ Usar el campus le parece una buena idea para agrupar a los alumnos y comunicarse con ellos.

+ Quiere que el campus le permita utilizarlo sin que él tenga que cambiar sus metodologías docentes (p.e. ponderación de notas).

+ Quiere que sus alumnos tengan los apuntes durante las clases, y los lleven al día.

#### Eva Maria (Prof exp)

+ Se ha podido adaptar un poco a las nuevas tecnologías, pero no se siente cómoda aprendiendo a usar una nueva herramienta.

+ Sus clases siempre han sido verticales, aunque los últimos cambios legislativos la han obligado ha hacer participar más activamente a sus alumnos.

+ Usa el campus como lugar para dejar los apuntes y olvidarse de ello.

+ Le gustaría que el campus resultase más fácil de utilizar.

#### Diego García (Alumno)

+ Nativo de las nuevas tecnologías que no tiene problema en aprender y usar una nueva herramienta basada en web o móvil, además lo usa como base para todo: comunicación, buscar información, hacer trabajos, colaborar,...

+ Todas sus clases hasta hace poco han sido verticales (magistrales), el profesor enseña y ellos aprenden, la comunicación y enseñanza en horizontal con sus compañeros se limitaba a compartir apuntes y experiencia.

+ Quiere que cuando usa el campus no tenga que preocuparse de si han subido algo nuevo o tiene que entregar algo, si no que la aplicación le avise de manera cómoda de ello para no tener que entrar todos los días y a diario.

+ Para comunicarse con sus amigos usa las redes sociales y otras aplicaciones, así que no quiere usar el campus para ello, su uso del campus se limita al ámbito académico y de aprendizaje

+ Al comunicarse con los profesores de manera rápida está acostumbrado a ir a buscarlos en persona porque teme molestarlos o que no lo vean / le respondan, además de ser más personal

+ Comparte prácticas, apuntes, libros, enlaces… con sus compañeros a través del correo, dropbox u otras aplicaciones


### Escenarios de contexto y requisitos

{% include panel-show.html panel_show_folder="escenarios" %}

# Framework de diseño

## Plan de Diseño

{% include include_id page_id='plan-diseno' %}

## Factor de forma, la postura y métodos de entrada ##

El factor de forma viene definido en los escenarios de contexto, en resumen se podría decir que se trata de una interacción por medio de un ordenador habitual y las notificaciones en el móvil.

En lo referido a la postura, se trata principalmente de postura soberana ya que tu interactúas directamente con la aplicación. Aunque posee características de postura temporal en el tema de notificaciones en el móvil o las notificaciones de escritorio.

Para terminar este punto, los métodos de entrada utilizados son los de cualquier PC, es decir, trackpad, ratón, teclado o pantalla táctil.

## Elementos de datos y funcionales ##

Después de dos iteraciones generamos los siguientes elementos de datos y funcionales.

### Datos

![Requisitos de datos]({{site.baseurl}}/assets/img/requisitos_datos.png)

### Funcional

{% include panel-show-content.html panel_show_folder="funcional" %}


## Bocetos ##

{% include panel-show-images.html panel_show_folder="bocetos" %}

## Prototipo con Pencil ##

A partir de los bocetos en papel realizados por cada miembro del equipo y los realizados en común, se decidió realizar un boceto más detallado mediante la herramienta *Pencil*, de manera que tubieramos un primer esbozo de nuestro diseño y con el pudiesemos trabajar en la pantalla para poder configurar de todos los elementos.

Las principales ideas que se plasmaron en este boceto fueron:

+ Área común: Se dejá la zona izquierda de la pantalla para incluir el calendario, el correo y las diferentes asignaturas, de manera que estubieran siempre accesibles desde cualquier página de la aplicación.

+ Navegación por pestañas: Para que fueran sencillo ir de una sección a otra, se decidió que los diferentes apartados como temas, ejercicios, etc. estarían en pestañas de fácil acceso.

+ Notificaciones: Era muy importante que las novedades y otros contenidos importantes se resaltaran correctamente para que el usuario final pueda reconocerlas facilmente

Todos estos detalles se pueden apreciar en la siguiente imagen, que cmuestra la página incial de una de las asignaturas.
![Pencil]({{site.baseurl}}/assets/img/Pencil.jpg)

Sin embargo, *Pencil* tiene muchas deficiencias en cuanto a diseño gráfico e interactividad, por lo que se decidió que para realizar el primer prototipo se utilizaría una herramienta un poco más completa, *Axure*, en el incluiría parte de lo mencionado anteriormente, se añadirían elementos nuevos y se descartarían algunos que no nos gustaron en este boceto preliminar.


## Prototipo con Axure ##

<a target="_blanck" href="{{site.baseurl}}/assets/proto/" alt="Prototipo"> Prototipo</a>

Como se a comentado anteriormente, se decidió utilzar *Axure* para desarrollar nuestro prototipo porque permitía mayor interacción con el usuario, al tiempo que resultaba sencillo de manejar. 

Se mantienen muchas de las funciones del boceto anterior (area común, notificaciones, navegación en pestañas, etc.), pero se han introducido algunos cambios:

+ Se ha incluido una barra superior donde el usuario pude acceder a la mayor parte de la información: búsqueda rápida, información del usuario, notificaciones, correo y configuración.

+ Sigue habiendo una zona a la izquierda, pero ahora solo incluye el calendario y los eventos más proximos que se hayan añadido a la agenda.

+ Se ha incluido un panel de chat en la esquina inferior derecha, desplegable, para facilitar la comunicación de los usuarios.

+ Se le ha dado bastante importancia al componente visual de la aplicación de manera que se incorporaron iconos, botones y secciones que el usuario pueda reconocer y usar de manera intutitiva.

+ Se decidió que nuestra aplicación estaría dividida en dos partes: por un lado, las *asignaturas*, donde se pude encontrar toda la información relativa a dicha materia: apuntes, problemas,etc., además de permitir subir prácticas propias, compartir archivos con otros compañeros y consultar dudas.
. Por otra parte, la otra sección se dedicaría al *alumno*, donde se almacena la información que se ha ido recopilando de las diferentes asignaturas.

+ Los archivos mostrados tanto en *apuntes* como en *problemas* muestran siempre la opción de *guardar en favoritos*, representada por un corazón, lo que permite verlos en la sección correspondiente del alumno, y que de esta manera sean más fácil acceder a ellos. Además, los nuevos archivos que no hayan sido examinados presentarn un icono de notificación para ser facilmente distinguibles.

+ En la sección extras, los alumnnos pueden subir nuevo material para compartirlo con los demás. Estas aportaciones pueden ser votadas mediante los iconos correspondientes y dicha votación puede verse juanto al nombre del archivo, de manera que se pueda apreciar la utilidad de dicho material extra.

+ En la sección de prácticas están disponibles tanto los enunciados como la opción de subir dichas prácticas. También se puede ver el estado actual de la práctica: fecha límite, estado, calificación etc.

+ Hemos icluido una sección de dudas para que los alumnos pongan sus preguntas. Éstas pueden ser respondidas por el profesor o por otros alumnos y ser votadas como en la sección de material extra para ver su utilidad.

+ La última sección de la aplicación sería las calificaciones, donde pueden verse de manera resumida las notas obtenidas en los distintos apartados de cada asignatura y la nota media.

La interactividad de este prototipo nos permitió presentarlo a varios compañeros de la asignatura para que fuera evaluado. Los detalles de dicha evaluación y los cambios que se ralizaron por motivo de ella se detallan en otra sección.


## Escenarios key path ##

### Alumno ###

Diego Garía entra en la aplicación para ver si se ha subido algún material nuevo. Cuando entra se encuentra con la **lista de sus asignaturas** y además **al lado de cada una ve si ha habido cambias la asignatura**.

Observa el **icono de notificaciones global** y ve que en total hay 3 notificaciones, pincha sobre él para ver cuales son y descubre que ha subido problemas nuevos. **Pincha sobre la notificación y le lleva a la hoja de problemas** dentro de la  asignatura correspondiente.

Como esta hoja es importante y le gustaría poder acceder rápido, **usa el botón de guardar** para guardarlo entre sus apuntes, además como va a usarlo en clase le da al **botón de descargar** para imprimirlo y llevarlo a clase.

Después de esto, antes de salir entra a su perfil pulsando en **botón de acceso al perfil**. Ahí entra en la **sección de dudas** y **pincha en responder una duda**, que ha estado pensando en la solución y quiere compartirla.

Finalmente va al **calendario** a ver qué es lo que tenía que hacer, para que no se le pase nada y ver cuando era la fecha límite de su próxima entrega. 

### Profesor

Juan tiene clase después y quiere poner las hojas de problemas a sus alumnos para que los resuelvan en clase. Entra a la aplicación y se encuentra una **lista de asignaturas en las que da clase**. Entra en la asignatura y va a **sección de problemas**, allí usa la **barra de búsqueda** y encuentra la hoja de problemas. **Pulsa el botón de hacer visible la hoja** y que esté disponible para los alumnos. También tenía una hoja especial que había preparado, así que pulsa en el **botón de subir nuevo archivo**, aparece un formulario para rellenar los datos de la nueva hoja de problemas y lo sube.

Se da cuenta de que ha aparecido una **notificación**, la mira y ve que han subido una duda nueva. **Pincha sobre la notificación** y le lleva a la duda en la  sección de dudas de la asignatura. Lee la duda y las respuesta y ve que no van por el buen camino, así que decide responder a la duda pulsando el **botón responder**.

Tenía que escribirle a un alumno para comentarle una cosas de una de sus entregas, así que pincha en el **chat inferior**, en la parte de asignaturas y escribe el nombre del alumno. Abre un chat con él y le escribe lo que tenía que decir sobre la entrega para que lo lea cuando se conecte.

## Escenarios de validación ##

Al seguir el proceso y las distintas iteraciones fuimos considerando distintas posibilidades y casos con los prototipos para validarlos al hacer las puestas en común en las iteraciones. No generamos artefactos, pero usamos estas discusiones para refinar los prototipos.

Esto nos sirvió para pasar del prototipo de *pencil* al de *axure*. Algunos de los cambios que decidimos de esta forma:

- **Interfaz más visual**: listas de asignaturas con imágenes y siglas ya que con un simple vistazo es más sencillo encontrarlas.
- **Barra superior** donde mostrar información global, por ser más consistente con lo que el usuario está acostumbrado.

## Prototipo de alta fidelidad

- [prototipo de alta fidelidad](https://pblocz.github.io/cygnus-hifi-prototype/)

Este prototipo surge como parte final del diseño guiado por objetivo después de remodelar el prototipo de axure a causa de las evaluaciones heurísticas.

Para desarrollarlo usamos [cactus](https://github.com/koenbok/cactus) como generador web estático con plantillas html y [bootstrap](http://getbootstrap.com/) con diversos plugins para las diversas interacciones y vistas. La razón de esto es que Axure nos parecía que estaba muy alejado de la realidad del proceso de desarrollo y con muchas restricciones.


<!--

1. investigación

2. Modelado

3. Requisitos / Escenarios de contexto

4. Framework de diseño / prototipos iniciales

5. prototipo de alta fidelidad

6. evaluación


cada sección

- organización del trabajo
- resultados/productos
- principales conclusiones

mostrar producto / fotos
- capturas de pantalla
- no hace falta contarlos en detalle
- recordad que luego los leeremos a fondo

-->

# Evaluaciones heurísticas

## Plan de Evaluación Heurística

{% include include_id page_id='plan-heuristicas' %}

## Resultados

### Evaluadores
{% include panel-show.html panel_show_folder="expertos" %}


### Observaciones de uso

Aprovechando que eran estudiantes, posibles usuarios objetivo, les pedimos que nos comentasen lo que iban haciendo y con lo que tenían dudas para hacernos una primera idea de las impresiones que causaba la interfaz.

También aprovechamos esta oportunidad para hacer una pequeña observación de uso y apuntar defectos y fallos de concepto que pudiesen haber. Así lo que anotamos es:

+ El material subido a la sección `extra` lo ve el profesor.
+ La sección `extra` no entendían bien para qué era.
+ Uno los evaluados casi no accedió al perfil.
+ Han interactuado muy poco con el calendario, lo han ignorado hasta bien avanzada la prueba.
+ El icono del corazón no les quedaba claro para que servía.
+ La `x` en dudas para marcar una duda cerrada no la han entendido.
+ Al añadir a favoritos un apunte no sabe donde se guarda, poco visible en el perfil.
+ Las notificaciones les han liado un poco.


## Conclusiones

Debido a las anotaciones anteriores y a los fallos de usabilidad reportados, descubrimos problemas y desviaciones de concepto, además de algunas funcionalidades y elementos que nosotros le dábamos importancia, ellos no. 

- **Eliminamos el calendario**. En este prototipo tenía un peso muy importante, casi un 30% de la interfaz, ya que querían saber cuando ocurrían los eventos, pero no tuvo el impacto deseado, hasta pasado casi el 60% de la prueba ni lo consideraron.
- **Añadimos un desplegable al perfil**. Los evaluadores entraron al perfil y sin revisarlo mucho salieron (antes de ver que había sub-secciones). En el perfil aglutinamos la mitad de la funcionalidad dedicada a que los alumnos accedan rápido a su contenido, así que era importante darle visibilidad a las sub-secciones para que las explorasen.
- **Carteles informativas en algunas secciones**: Algunas secciones no se entendió bien su propósito, al ser funcionalidades a las que no están acostumbrados (compartir o guardarte apuntes en un campus virtual), así que añadimos una ayuda con el propósito de secciones conflictivas que se puede eliminar para no estorbar al alumno.
- **Alerta y feedback más informativo al realizar acciones**. En las acciones como guardar un apunte de una asignatura el resultado principal está reflejado en el perfil, así que añadimos mensaje de *qué acción* se ha realizado y *dónde se ve el resultado* de dicha acción.
- **Eliminamos la `x` de dudas**. No entendieron para qué servía y en conversaciones posteriores vimos que no era tan relevante esta funcionalidad.

# Evaluaciones de usuarios

## Plan 
Queremos proceder a realizar la evaluación porque hemos terminado dos fases de diseño y desarrollado un prototipo de alta fidelidad. Queremos dar paso al desarrollo de la aplicación, pero para ello queremos verificar que el prototipo real tiene un diseño que agrade a usuarios reales.

Por ello nos planteamos una serie de preguntas a las que queremos dar respuesta, que son:

- ¿Los usuarios saben encontrar los materiales y la información relacionada con una asignatura?
- ¿Los usuarios entienden el funcionamiento de los bookmarks (favoritos)?
- ¿Los usuarios encuentran sus calificaciones o resumen general de las mismas?
- ¿Los usuarios ven las notificaciones?
- ¿Los usuarios entienden el sistema de chat?
- ¿Los usuarios son capaces de compartir contenido y valorar otros contenidos?

Para esto hemos seleccionado a unos usuarios que se asemejan a Diego García, son tres chicas universitarias de enfermería y de CAFYD (antiguo inef). No se les va a realizar un cuestionario previo, porque las conocemos con anterioridad suficiente, en los tres casos han pedido en alguna ocasión ayuda con su campus a uno de nosotros y sabemos que se asemejan suficiente a Diego García (salvo el género).

Para proceder con la evaluación vamos a pedir una serie de tareas a nuestros usuarios:

"0". Movimiento libre (poco tiempo), vuelve a inicio.
A. Consultar las calificaciones de todas las asignaturas.
B. Marcar como favorito, un apunte de Análisis Numérico.
C. Subir un archivo a Análisis Numérico.
D. Consultar que es PC en análisis Numérico y votar las respuestas.
E. Ver el calendario de entregas de este mes.
F. Escribir a un miembro del grupo4 de DSI.
G. Consultar detalles de una entrega.
H. Consultar tus datos guardados.

La tarea "0" la realizarán los tres usuarios, con ella queremos comprobar si las notificaciones sugieren suficiente como para abrirlas, o el mensaje pendiente. 

El resto de tareas se repartirá del siguiente modo:

Ana: A-B-C-F-G-H
Patricia: B-E-F-G-H
Clara: A-B-C-D-F-H

Es decir, todos harán B,F y H por ser las tareas que cubren los casos más demandados.

Las sesiones se realizarán en su zona de estudio habitual con un ordenador portátil, por lo que usarán trackpad salvo que posean ratón propio. Para recoger las evaluaciones grabaremos la aplicación, al usuario y le pediremos que detalle que va haciendo. Tendrá a su lado un moderador que cubrirá las carencias del prototipo. Los observadores no hablarán en ningún momento con los usuarios hasta una vez finalizada la prueba, se ha verificado que en las salas de estudio elegidas caben los observadores sin interferir.

Las carencias del prototipo que se prevé aparezcan, son:
1- Subir un archivo no surtirá efecto.
2- Votar, no cambiará el número de votos.
3- No se abrirá una ventana de chat rápida. 
4- No se producirá un cambio de vista de las listas.
5- Los eventos del calendario, no se corresponden con la realidad.
6- No existen archivos que descargar.

Además el moderador tomará nota de los eventos más importantes sin necesidad de apuntar el minuto exacto para evitar distracciones. Y animará al usuario a no dejar de hablar detallando que hace, piensa y siente.

Posteriormente el moderador, preguntará motivos de las acciones que le hayan llamado la atención. Esto se hará de manera distendida merendando. Cabe la posibilidad de hacer este último paso, con Clara y Ana al mismo tiempo, dado que se ha quedado en el mismo lugar por limitación de tiempo, pero la evaluación si será separada (primero una y luego la otra sin capacidad de influenciarse).

La observación y análisis de los resultados consistirá en evaluar las tareas completadas sin ayuda y las que se ha recibido alguna ayuda (no esperada por las carencias). Se anotarán iconos no comprendidos. Y los caminos no correctos (o numero de vueltas dadas) hasta que el usuario completa cada tareas.

### Documento para el usuario
Querida [NOMBRE]:

Lo primero agradecerte que quieras colaborar con nosotros en el
proceso de evaluación del prototipo de Cygnus. Este prototipo ha sido
desarrollado con todo nuestro cariño para facilitar el acceso a la
información relevante e interesante de las asignaturas de un
universitario. 

Para ponerte en situación, tu estas matriculada en tres asignaturas,
DSI, IS y ANUM (luego te digo que significa). Y vas a realizar las
siguientes tareas, por favor supón que es un día normal de
universidad. Y no hagas caso ni de los observadores, e intenta actuar
como si el moderador no estuviese. Sabes que el proceso se grabará la
pantalla y tus reacciones, así como el sonido para posteriormente
analizarlo. Agradecemos que nos cuentes constantemente como te
sientes, incluso si es nervios y que nos narres en la medida de lo
posible, porque realizas ciertas acciones. Por ejemplo, si tu tarea
consiste en ponerte un sándwich, irías a la cocina y dirías estoy
yendo a la cocina porque es allí donde tengo la comida, cogerías el
pan y dirías cojo primero el pan porque es donde va el contenido y en
ese sentido lo demás. De todos modos tranquila, todo lo que digas será
analizado solo por nosotros, nadie más verá estos vídeos y audios. Por
favor, no tengas miedo en criticar. 

Simplemente se tu misma, pero hablando sola en voz alta.

Tus tareas son:

[TAREAS SEGÚN PERSONA]

Gracias.
Cygnus

## Resultados


### Ana

[Vídeo](https://www.dropbox.com/s/adx6l4nj8a6b7gv/Ana.avi?dl=0)

El escenario concreto es su mesa de estudio lugar donde suele consultar su campus. Tiene 23 años y estudia CAFYD.

#### Tabla de Reacciones

| 00:00 |  | Comienza Movimiento Libre |
| 00:10 |  | Se queda leyendo el mensaje explicativo de guardado |
| 00:20 |  | Entiende el icono de subir prácticas. |
| 00:40 |  | No sabe como ver si esta corregida la práctica |
| 01:23 |  | No entiende guardar dudas, ni como crear una. Piensa crearla desde buscar |
| 01:50 |  | Consulta notas sin problemas pero le parece pobre la vista |
| 02:30 |  | Compartir un archivo lo confunde con entregar un archivo al profesor |
| 02:48 |  | Confunde El botón notificaciones y dudas, como objetivos para subir un archivo |
| 03:30 |  | No entiende el concepto compartir apuntes. |
| 03:50 |  | Encuentra e identifica la nube como icono para subir archivos. |
| 04:00 | 04:20 | Le sigue molestando compartir cosas con todos |
| 04:40 | 04:55 | Guarda correctamente un archivo pero no sabe si lo ha hecho porque busca una estrella o corazón |
| 05:35 | 06:30 | No entiende el concepto guardar de nuevo. |
| 06:35 |  | Lo encuentra pero no sabe ni como lo ha hecho. |
| 07:10 |  | Le molesta la distribución de pestañas. |
| 07:30 | 07:40 | No sabe donde ver más detalles de una entrega. |
| 08:00 |  | Abre el lugar que busca pero no es capaz de identificarlo. |
| 08:20 | 09:00 | Sigue sin saber donde está, de hecho no se siente en la página de su universidad. |
| 09:10 |  | Falta un link en la vista general de la asignatura donde podría ver su objetivo. |
| 09:40 |  | Busca el enunciado de una entrega, en problemas o apuntes. |
| 10:15 |  | Cambiamos de tarea sin lograrlo. |
| 10:40 |  | Pincha repetidas veces el icono de mensajes intentando que se le habrá una página, no se fija en el desplegable. |
| 11:08 |  | Pincha la palabra contactos para intentar abrir la lista de contactos |
| 11:20 |  | Pide perdón reconociendo que no había visto la barra de chat. |
| 12:00 |  | Usa intro para enviar y no funciona, se mete otra linea. |
| 12:10 |  | El icono de envío de mensaje esta tapado por la pestaña Contactos. |

### Clara

[Vídeo](https://www.dropbox.com/s/lzxcoc9dpb7b6ih/Clara.avi?dl=0)

El escenario concreto es su mesa de estudio, aunque ella suele estudiar de pie, consulta el campus sentada, utiliza ratón enchufado a su portátil. Tiene 22 años y estudia enfermería.

#### Tabla de Reacciones

| 00:00 |  | Comienza Movimiento libre |
| 00:10 | 00:16 | Lo primero a por los botones de ordenar las listas |
| 00:45 | | Vuelve a al inicio pinchando en asignatura |
| 01:13 | 01:33 | Confusión Favorito y guardar |
| 02:02 | 02:50 | No encuentra el botón de subir archivos en compartido |
| 02:50 | | Moderador interviene para aclarar el icono de la nube |
| 03:15 | 03:30 | Encuentra las dudas fácilmente pero no se fija en los votos para ver la mejor respuesta |
| 04:15 | | Entra en versión completa de chat antes que la miniatura. |
| 04:44 | | Encuentra perfectamente sus datos guardados en el desplegable del perfil |
| 05:05 | | Le llama la atención el icono de las notificaciones |

### Patricia

[Vídeo](https://www.dropbox.com/s/iybunuzc88w3hco/patri.avi?dl=0)

El escenario es tirados en el suelo, ella siempre estudia en bibliotecas o en el suelo, la postura distendida la ayuda a concentrarse. Acaba de cumplir 20 años y estudia enfermería

#### Tabla de Reacciones

| 00:00 | | Comienza Movimiento Libre |
| | | Lo primero que hace es ver que ha guardado y que ha entregado usa constantemente el desplegable del perfil en vez de las pestañas. |
| 00:50 | | Mira notificaciones y los nuevos mensajes y lo comprende sin problemas |
| 01:20 | | Duda de si el bookmark es el icono de guardar pero lo entiende perfectamente. |
| 01:40 | | Busca el calendario de entregas, se conforma con una lista de entregas, seguido ve la otra vista y parece agradarle. |
| 02:17 | | Quiere hablar con alguien de DSI y abre la asignatura |
| 02:57 | | Prueba a buscarlo |
| 03:03 | | Abre el desplegable y busca el grupo en la pestaña grupos |
| 03:40 | | Encuentra los detalles de la entrega, el enunciado y las dudas sin problemas. |
| 04:10 | | usa el acceso directo a las dudas y las encuentra sin problema. |
| 04:25 | | No reconoce que la duda esta abierta. |
| 04:50 | | Recuerda perfectamente que tiene una pestaña de cosas guardadas en su perfil. |

### Usuario Extra: Estrella

[Vídeo](.https://www.dropbox.com/s/pn0fo4g5o384k42/Estrella.avi?dl=0)

Por los asombrosos resultados de la evaluación de Patricia, decidimos realizar la evaluación con esta usuaria que casualmente nació el mismo día y estudia en la misma universidad. Estrella tiene 20 años y estudia Psicología. El escenario es en la cama donde suele estudiar y tocar la guitarra.

#### Tabla de Reacciones

| 00:00 | | Comienza el Movimiento Libre |
| | | Se mete lo primero en una asignatura |
| 00:36 | | Quiere ver los detalles de las prácticas desde general de la asignatura. (el link no funciona) |
| 01:10 | | No sabe si sabría volver al inicio, pero lo hace sin problemas. |
| 01:35 | | No sabe como guardarse el documento |
| 01:40 | | Prueba el botón derecho para guardárselo. |
| 01:50 | | Reconoce el bookmark y se lo guarda |
| 02:20 | | Busca los detalles de las entregas en entregas, todo sin problemas. |
| 02:40 | | Intenta ir al calendario y el botón no reacciona correctamente, pincha una segunda vez y si |
| 03:10 | | Pincha en el sobre buscando escribir un mensaje y que se abriese una ventana pero no lo hace. |
| 03:40 | | Busca el grupo en la ventana grande de chat |
| 04:00 | | Intenta enviar un mensaje con el intro y no funciona. |
| 04:15 | | ve el chat desplegable |
| 04:50 | | Encuentra el grupo 4 de DSI |
| 05:17 | 05:40 | Internet se cae |
| 05:45 | | encuentra la entrega perfectamente |
| 06:20 | | Sabe perfectamente donde descargarse el enunciado y donde preguntar una duda |
| 06:50 | | Intenta añadir una duda con la búsqueda |
| 07:14 | | Recuerda perfectamente que guardo unos apuntes en el perfil y encuentra guardado sin ningún problema |
| 07:50 | | Busca una duda en su perfil sin haberla guardado. |
| 08:10 | | Guarda su duda sin ningún problema |

## Conclusiones

El proceso de evaluación con usuarios, consideramos ha sido todo un éxito. Comenzamos evaluando a Ana y Clara dos chicas que llevan tiempo en la universidad y que se podría decir que tienen experiencia con campus virtuales. Las herramientas más novedosas en la interfaz les resultó complicado de entender, una vez se explicó el concepto supieron utilizarlo sin problemas. Mientras que la evaluación posterior a Patricia, que esta en segundo de grado, resultó poder realizar todas las acciones a la primera. Dada esta discordancia de resultados, decidimos probar con otro usuario de la misma edad (como hemos explicado anteriormente) que Patricia (nacida el mismo día), Estrella, que está en segundo de Psicología y los resultados como puede observarse son similares. Por eso, consideramos los cambios que describiremos más adelante, para poder soportar nuevos alumnos y alumnos veteranos. Estos dos tipos de alumnos no han podido ser identificados en la fase de investigación, aunque los teníamos como hipótesis de personas, por los motivos que se explican en ese apartado. Por ello las soluciones que se plantean están más orientadas a solucionar los problemas de los veteranos con ayudas visuales.

+ Para el problema de identificación de iconos, probablemente se cambiaría el icono de subir al "cloud" con uno similar al de descarga, y el resto se mantendrían aunque se pudiesen perfilar los diseños, con líneas más finas. El icono de bookmark se mantendría pero dejando claro que no es un favorito, sino guardar en tu perfil, en ningún lado se haría referencia a la palabra favorito.

+ Para el problema de añadir archivos, dudas y subir contenidos. La solución iría por agrandar el icono y darle color, habría que probar el resultado de estas medida. Otra solución podría ser quitar el icono y poner directamente la palabra.

+ Para el problema de utilizar la barra de búsqueda para todo menos buscar, podríamos plantear nuevos diseños de barra, como redondear los bordes o moverlo al lado derecho, hacer que no ocupe una posición tan principal para una función no primaria.

+ Para el problema de utilizar grupos en el chat, se buscará unificar la vista completa y la vista miniatura del chat, permitiendo en ambos lados la navegación por pestañas o combinar todas las pestañas, esta decisión habría que evaluarla, pero si que se unificarían por consistencia.

+ Para el problema de la no utilización del chat en miniatura, moveríamos el icono de maximizar o cambiar los colores de modo que no sea ese el botón que primero se pincha, sin desplegar el chat en pequeño.

+ Para el problema de consultar todas las notas de golpe con scroll, seguramente se pueda solucionar fácilmente, poniendo dos columnas como en el resto de páginas o iniciando la vista con el acordeón agrupado en vez de expandido, dado que nadie ha usado esa opción. Esta decisión debería pasar por un proceso de diseño.

+ Para el problema de identificación del perfil, podría valer con colocar "Mi perfil" en algún punto. Además habría que añadir las opciones de configurar y cerrar sesión dentro del desplegable y seguramente en la vista del perfil. 

+ Por último, para el problema de la no identificación de los detalles de una práctica, se puede poner la palabra "descripción" o buscar una forma de indicar eso, cambiando los colores o posición o forma del botón enunciado. Además habría que añadir algo que indicase el estado de la entrega sin necesidad de abrirla, dado que el botón gris si esta entregada no se aprecia frente al negro.

Así no nos hemos planteado solucionar el concepto de guardado, ni de compartir, dado que los usuarios que comiencen a usar esta herramienta sin haber utilizado otras o empezando a utilizarlas por primera vez, podrán empezar asociando al campus virtual el concepto de compartir, colaborar y ser activo en el mismo, olvidándose de la posición pasiva que se tiene ahora mismo por las limitaciones del sistema.



