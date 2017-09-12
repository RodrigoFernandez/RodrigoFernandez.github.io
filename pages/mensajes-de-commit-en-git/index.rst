.. title: Mensajes de commit en Git
.. slug: mensajes-de-commit-en-git
.. date: 2017-09-12 00:01:06 UTC-03:00
.. tags: git, programacion
.. category: programacion 
.. link: 
.. description: Guía resumen de cómo escribir un mensaje de git.
.. type: text

Mensajes de commit en Git
-------------------------
-------------------------

Guía resumen de cómo escribir un mensaje de git. Se realizó en base a este post: `buenas practicas en commits de git <https://codigofacilito.com/articulos/buenas-practicas-en-commits-de-git>` y a este otro post <link>


Estructura del mensaje de commit
--------------------------------

    type: subject o título
  
    body
  
    footer


Type (Tipo)
-----------

Puede ser:

- *feat*: nueva característica
- *fix*: solución de un bug
- *docs*: cambios en la documentación
- *style*: se aplicó formato, comas y puntos faltantes, etc.; pero no cambios en el código.
- *refactor*: refactorización del código en producción
- *test*: se añadieron pruebas, refactorización de pruebas; pero sin cambios en el código
- *chore*: actualización de tareas de build, configuración del administrador de paquetes; pero sin cambio en el código


Subject (asunto) o título
-------------------------

- *Separar el título del cuerpo con una línea en blanco*: El texto sobre la primera línea en blanco en el mensaje del commit es tratado como el título del commit si luego se deja una línea en blanco, esto es usado en multiples comandos de git; el cuerpo del commit es necesario si hace falta una expliación del cambio.
- *Limitar título a 50 caracteres*: para que se pueda visualizar correctamente en herramientas de git como el comando log con el flag --oneline, o el comando shortlog.
- *Capitalizar el título*
- *No terminar el título con un punto*
- *Utilizar el modo imperativo en el título*: por ejemplo "Limita el cuerpo a 72 caracteres". El título tiene que ser capaz de completar la siguiente frase: If applied, this commit will <your subject line here>; por ejemplo, if applied, this commit will remove deprecated methods; si el título no se escribe en forma imperativa la frase no queda bien escrita.


Body (cuerpo)
-------------

- *Limitar el cuerpo a 72 caracteres*: las lineas que forman el cuerpo del commit tienen que tener un ancho de hasta 72 caracteres para que cuando se lista el mensaje del commit este se vea correctamente, pues git no ajusta el texto automáticamente.
- *Utiliza el cuerpo para explicar qué y por qué vs. cómo*: hay que centrarse en aclarar las razones por las que se realizó el cambio; como funcionaba antes del cambio y cuál era el problema de ese funcionamiento, la forma en que funciona ahora y el porque se decidió resolverlo así.


Footer (Pie)
------------

Es opcional y se usa para indicar el seguimiento de los ids de las incidencias, por ejemplo el id de un jira.
