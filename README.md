# GitBasics

Repositorio para ayudar a quien lo necesite a usar la terminal y comandos basicos.

# Navegando con la y usando la terminal

Para agilizar nuestro desarrollo debemos conocer algunos comandos basicos de terminal sea cual sea y aprender a leerla.
Podemos usar powershell, bash, etc. Para estos ejemplos usaremos la terminal bash pero los comandos son iguales al usarlos en powershell.

Para fines practicos usaremos la terminal directamente desde nuestro IDE (vsCode) aunque tranquilamente puede abrirse una terminal desde cualquier carpeta.

<h2>Abrir una nueva terminal</h2>

Para abrir una terminal nueva simplemente clickearemos en nuestro VScode en "Terminal" => New terminal. O si lo prefieren pueden usar el comando indicado en la opción.

Al abrir la terminal nos indicará en que directorio estamos. En este ejemplo podemos ver que estamos en el escritorio.

<h2>Navegación con la terminal</h2>

Para navegar con la terminal usaremos el comando "cd" seguido por un espacio y las siguientes opciones:

<ul>
  <li>.. (Sube una carpeta.)</li>
  <li>"nombre de la carpeta a la que queremos trasladarnos"</li>
</ul>

Aca vemos como fuimos a la carpeta FACU, luego a la carpeta Arquitectura de computadoras, luego retrocedimos una carpeta y nos movimos a Fundamentos de Informatica.

Nota: Solo podemos movernos a carpetas que se encuentren dentro de la carpeta en la cual estamos parados.

¿Que pasa si no se que carpetas hay en la carpeta en la que estoy parado?

Para eso utilizamos el comando "ls". Este nos indica que carpetas / archivos existen en la carpeta donde estamos.

Acordate que podes moverte con la terminal usando "cd + nombre de carpeta" y podes conectarte directamente con la carpeta destino en una sola linea de este modo:

Otros comandos que podemos usar son:

<ul>
  <li>touch "nombre de archivo" (crea uno o mas archivos con el nombre y extension especificados)</li>
  <li>rm "nombre de archivo" (borra uno o mas archivos con el nombre y extension especificados)</li>
  <li>mkdir "nombre de carpeta" (crea una o mas carpetas con el nombre que especifiquemos)</li>
  <li>rmdir "nombre de carpeta" (borra la/s carpeta/s especificada/s)</li>
  <li>clear (limpia la terminal)</li>
</ul>

# Creando el repositorio

Al trabajar con GitHub, necesitaremos crear repositorios para trabajar.

Tenemos dos escenarios posibles al crear un repositorio personal. Veamoslos:

<h2>Caso 1: Crear la carpeta en nuestra computadora y luego conectarla con un repositorio en github</h2>

Primero vamos a crear nuestra carpeta (Buena oportunidad para utilizar los comandos que vimos en la sección de antes)

Recorda "cd" para moverte, "ls" para ver que hay donde estamos parados, "touch / mkdir" para crear.

<h3>En nuestro perfil de Github vamos al menu superior y seleccionamos la opción de repositorio nuevo.</h3>

Aqui vamos a nombrar a nuestro repositorio (Mi_Nuevo_repositorio en mi caso) y a escribir una breve descripción del mismo. Lo demas lo dejamos tal cual está y abajo de todo clickeamos crear repositorio. No toques nada ni cierres la pestaña, la necesitaras después.

<h3>Parados en nuestra carpeta que creamos con nuestros archivos usamos el comando "git init" para inicializar localmente un repositorio nuevo.</h3>

En github, en la pantalla de muestra, ve al segundo recuadro y copia el primer comando "git remote add origin ............."

Este comando es el que conecta nuestro repositorio local con nuestro repositorio de github.

Pega el comando que copiaste en tu terminal y ejecutalo para conectar los repositorios local y el de github.

<h3>Hagamos algunos cambios. Agregamos algunas cosas a nuestro archivo index.html y a nuestro archivoPython.py (No te olvides de usar ctrl + s para guardar los cambios)</h3>

Como ves, en nuestro vsCode podemos ver que tenemos cambios sin "subir" a nuestro repositorio de github y en que archivos estan dichos cambios.

<h3>Aca usamos nuestro segundo comando de terminal de tipo git: "git status"<h3>

Este comando nos proporciona informacion sobre como esta nuestro entorno de trabajo.

Podemos ver que estamos en la rama "main" (no te preocupes por las ramas por ahora)

Aun no hay "commits" hechos (no hay cambios guardados en el repositorio) y nos indica que los archicos en rojo no estan siendo trackeados para nuestro proximo commit.

<h3>Usamos un nuevo comando. git add "nombre/s" para decirle a nuestra terminal que añada los archivos que le indicamos a nuestro proximo commit</h3>

Como nosotros solo queriamos mostrar hello world en nuestro archivo python y crear una estructura inicial en nuestro html, vamos a hacer un commit de estos cambios (por ahora ignoramos el arhivo "archivoJavaScript.js)

Nota que al escribir git status otra vez, nos muestra que esos dos archivos (ahora en verde) estan siendo trackeados, no como el archivo "js" en rojo.

<h3>Para esto utilizamos un nuevo comando git. git commit -m "mensaje"</h3>

Aqui utilizamos la bandera -m para especificar un mensaje y entre comillas, escribimos el mensaje que queremos enviar (en este caso usamos "Mi primer commit").

Es hora de subir nuestros cambios a github. Por ser la primera vez que subimos algo a un repositorio nuevo, utilizamos el comando "git push -u origin main". Este comando simplemente esta diciendo que suban los archivos a la rama "main" del repositorio.

Recarga la pagina del repositorio de github y ve lo que pasa. Veras que ahora tiene tus archivos de python y html, tu mensaje de commit y cuando fue hecho.

<h3>Agreguemos algo a nuestro archivo .js y guardamos el archivo (console.log() es lo mismo que print() de python solo que se usa en javascript. Ambas funciones imprimen un mensaje en la consola)</h3>

Si utilizamos git status podemos ver que nuestro archivo js tiene modificaciones y no esta siendo trackeado para el proximo commit.

Si queremos añadir todos los archivos que hayan sufrido cambios, podemos usar "git add ." en vez de nombrar el/los archivos especificos. Si preferis ser mas especifico podes usar la version git add "nombre del archivo"

Haz un nuevo commit del mismo modo que antes y dale un mensaje.

A partir de ahora el comando que usaras para subir cambios a tu repositorio de github es simplement git push (siempre luego de los commits).

Nota: no necesitas "pushear" cada vez que hagas un commit, simplemente podes hacer varios commits para registrar los cambios y cuando termines de trabajar por el día, usar git push para subir todos los cambios a github.

Mas adelante veremos como dar marcha atras hasta un commit que sabemos que nuestro codigo funcionaba bien por si nos equivocamos en el código y queremos volver a una version mas estable/funcional de este.

Podemos ver que nuestro repositorio ya tiene los cambios hechos de nuestro primer commit y nuestro ultimo commit al archivo js.
