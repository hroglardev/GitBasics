# GitBasics

Repositorio para ayudar a quien lo necesite a usar la terminal y comandos basicos.

# Navegando con la terminal y usandola

Para agilizar nuestro desarrollo debemos conocer algunos comandos basicos de terminal sea cual sea y aprender a leerla, una vez que te acostumbras a trabajar con la terminal es mucho mas comodo para crear archivos y carpetas en tus proyectos.
Podemos usar powershell, bash, etc. Para estos ejemplos usaremos la terminal bash pero los comandos son iguales al usarlos en powershell.

Para fines practicos usaremos la terminal directamente desde nuestro IDE (vsCode) aunque tranquilamente puede abrirse una terminal desde cualquier carpeta.

<h2>Abrir una nueva terminal</h2>

Para abrir una terminal nueva simplemente clickearemos en nuestro VScode en "Terminal" => New terminal. O si lo prefieren pueden usar el comando indicado en la opción.

<img src="https://r2.easyimg.io/m5pkohofj/1crearterminal.jpg" />

Al abrir la terminal nos indicará en que directorio estamos. En este ejemplo podemos ver que estamos en el escritorio.

<img src="https://r2.easyimg.io/m5pkohofj/2terminalcreada.jpg" />

<h2>Navegación con la terminal</h2>

Para navegar con la terminal usaremos el comando "cd" seguido por un espacio y las siguientes opciones:

<ul>
  <li>.. (Sube una carpeta.)</li>
  <li>"nombre de la carpeta a la que queremos trasladarnos"</li>
</ul>

Aca vemos como fuimos a la carpeta FACU, luego a la carpeta Arquitectura de computadoras, luego retrocedimos una carpeta y nos movimos a Fundamentos de Informatica.

<img src="https://r2.easyimg.io/m5pkohofj/3moviendonos.jpg" />

Nota: Solo podemos movernos a carpetas que se encuentren dentro de la carpeta en la cual estamos parados.

Recomendacion: Utiliza la tecla "tab" para completar el nombre del directorio luego de escribir las primeras letras.

¿Que pasa si no se que carpetas hay en la carpeta en la que estoy parado?

Para eso utilizamos el comando "ls". Este nos indica que carpetas / archivos existen en la carpeta donde estamos.

<img src="https://r2.easyimg.io/m5pkohofj/4lsbasico.jpg" />

Acordate que podes moverte con la terminal usando "cd + nombre de carpeta" y podes conectarte directamente con la carpeta destino en una sola linea de este modo:

<img src="https://r2.easyimg.io/crfmorton/oneline.jpg" />

Otros comandos que podemos usar son:

<ul>
  <li>touch "nombre de archivo" (crea uno o mas archivos con el nombre y extension especificados)</li>
  <li>rm "nombre de archivo" (borra uno o mas archivos con el nombre y extension especificados)</li>
  <li>mkdir "nombre de carpeta" (crea una o mas carpetas con el nombre que especifiquemos)</li>
  <li>rmdir "nombre de carpeta" (borra la/s carpeta/s especificada/s)</li>
  <li>clear (limpia la terminal)</li>
</ul>

# Creando / Clonando un repositorio

Al trabajar con GitHub, necesitaremos crear repositorios para trabajar.

Tenemos dos escenarios posibles al crear un repositorio personal, crear una carpeta y conectarla a un repositorio de github, o clonar un repositorio de github. Veamoslos:

<h2>Caso 1: Crear la carpeta en nuestra computadora y luego conectarla con un repositorio en github</h2>

Primero vamos a crear nuestra carpeta (Buena oportunidad para utilizar los comandos que vimos en la sección de antes)

Recorda "cd" para moverte, "ls" para ver que hay donde estamos parados, "touch / mkdir" para crear.

<img src="https://r2.easyimg.io/m5pkohofj/5lsycreorepo.jpg" />

<img src="https://r2.easyimg.io/m5pkohofj/6creandoarchivos.jpg" />

En VScode movete a la nueva carpeta donde creaste los archivos clickeando en open folder (hay mejores maneras de hacer esto pero por ahora hazlo así)

<img src="https://r2.easyimg.io/m5pkohofj/7vamosalanueva_carpeta.jpg" />

En nuestro perfil de Github vamos al menu superior y seleccionamos la opción de repositorio nuevo.

<img src="https://r2.easyimg.io/m5pkohofj/8creo_repo.jpg" />

Aqui vamos a nombrar a nuestro repositorio (Mi_Nuevo_repositorio en mi caso) y a escribir una breve descripción del mismo (DEJA DESMARCADA LA OPCION DEL ADD README. Si por accidente la marcaste, salta al caso 2 para directamente clonar (descargar) el repositorio creado a tu computadora). Lo demas lo dejamos tal cual está y abajo de todo clickeamos crear repositorio. No toques nada ni cierres la pestaña, la necesitaras después.

<img src="https://r2.easyimg.io/m5pkohofj/9creorepo.jpg" />

Parados en nuestra carpeta(en VScode) que creamos con nuestros archivos usamos el comando "git init" para inicializar localmente un repositorio nuevo.

<img src="https://r2.easyimg.io/m5pkohofj/gitinit.jpg" />

En github, en la pantalla de muestra, ve al segundo recuadro y copia el primer comando "git remote add origin ............."

<img src="https://r2.easyimg.io/m5pkohofj/10connect.jpg" />

Este comando es el que conecta nuestro repositorio local con nuestro repositorio de github.

Pega el comando que copiaste en tu terminal y ejecutalo para conectar los repositorios local y el de github.

<img src="https://r2.easyimg.io/m5pkohofj/linkrepoaddorigin.jpg" />

Hagamos algunos cambios. Agregamos algunas cosas a nuestro archivo index.html y a nuestro archivoPython.py (No te olvides de usar ctrl + s para guardar los cambios)

<img src="https://r2.easyimg.io/m5pkohofj/11htmlcambios.jpg" />

<img src="https://r2.easyimg.io/m5pkohofj/11cambiospython.jpg" />

Aca usamos nuestro segundo comando de terminal de tipo git: "git status"

Este comando nos proporciona informacion sobre como esta nuestro entorno de trabajo.

Podemos ver que estamos en la rama "main" (no te preocupes por las ramas por ahora)

Aun no hay "commits" hechos (no hay cambios guardados en el repositorio) y nos indica que los archivos en rojo no estan siendo trackeados para nuestro proximo commit.

<img src="https://r2.easyimg.io/m5pkohofj/12gitstatus.jpg" />

Usamos un nuevo comando. git add "nombre/s" para decirle a nuestra terminal que añada los archivos que le indicamos a nuestro proximo commit

Nota que al escribir git status otra vez, nos muestra que los dos archivos que agregamos con "git add" (ahora en verde) estan siendo trackeados, no como el archivo "html" en rojo.

<img src="https://r2.easyimg.io/m5pkohofj/13gitadd.jpg" />

Para esto utilizamos un nuevo comando git. git commit -m "mensaje"

Aqui utilizamos la bandera -m para especificar un mensaje y entre comillas, escribimos el mensaje que queremos enviar (en este caso usamos "Mi primer commit").

<img src="https://r2.easyimg.io/m5pkohofj/14primercommit.jpg" />

Es hora de subir nuestros cambios a github. Por ser la primera vez que subimos algo a un repositorio nuevo, utilizamos el comando "git push -u origin main". Este comando simplemente esta diciendo que suban los archivos a la rama "main" del repositorio.

Recarga la pagina del repositorio de github y ve lo que pasa. Veras que ahora tiene tus archivos, tu mensaje de commit y cuando fue hecho.

<img src="https://r2.easyimg.io/m5pkohofj/15gitpush.jpg" />

Agreguemos algo a nuestro archivo .js y guardamos el archivo (console.log() es lo mismo que print() de python solo que se usa en javascript. Ambas funciones imprimen un mensaje en la consola)

Si utilizamos git status podemos ver que nuestro archivo js tiene modificaciones y no esta siendo trackeado para el proximo commit.

<img src="https://r2.easyimg.io/m5pkohofj/16cambiosajs.jpg" />

Si queremos añadir todos los archivos que hayan sufrido cambios, podemos usar "git add ." en vez de nombrar el/los archivos especificos. Usamos "git add ." para incluir nuestro archivo html en nuestro nuevo commit.

Haz un nuevo commit del mismo modo que antes y dale un mensaje.

A partir de ahora el comando que usaras para subir cambios a tu repositorio de github es simplement git push (siempre luego de los commits).

<img src="https://r2.easyimg.io/m5pkohofj/17segundocommit.jpg" />

Nota: no necesitas "pushear" cada vez que hagas un commit, simplemente podes hacer varios commits para registrar los cambios y cuando termines de trabajar por el día, usar git push para subir todos los cambios a github.

Mas adelante veremos como dar marcha atras hasta un commit que sabemos que nuestro codigo funcionaba bien por si nos equivocamos en el código y queremos volver a una version mas estable/funcional de este.

Podemos ver que nuestro repositorio ya tiene los cambios hechos de nuestro primer commit y nuestro ultimo commit al archivo js.

<h2>Caso 2: Crear el repositorio directamente en github y clonarlo a nuestra computadora</h2>

Ese caso no solo sirve para crear un nuevo repositorio, sino que ademas sirve para bajar repositorios a nuestra computadora. Al clonar un repositorio en vez crearlo como en el caso 1, el repositorio local y el repositorio de github ya estarán conectados.

Para trabajar de esta manera, crea un repositorio nuevo tal cual lo hicimos en el Caso anterior solo que esta vez marca la opcion de Add README (Si por accidente no tildaste la opcion de ADD README, checkea el Caso 1 descrito anteriormente)

<img src="https://r2.easyimg.io/m5pkohofj/readme.jpg" />

Luego de esto, veremos que nuestro repositorio solamente tiene un archivo README.md con una breve descripción del proyecto.

Para clonar este repositorio en nuestra computadora, haremos click en el boton verde "code" y clickearemos el boton de copiar para copiar el link que se muestra (Elegir la opcion https de momento)

<img src="https://r2.easyimg.io/m5pkohofj/clone.jpg" />

En nuestro VScode usaremos el comando "git clone" seguido del link que copiamos de github. Recuerda que debes ejecutar el comando desde la carpeta donde quieres guardar tu repositorio en tu pc.

<img src="https://r2.easyimg.io/m5pkohofj/cloning.jpg" />

Una vez que termine, simplemente nos traslamos a la carpeta del repositorio para comenzar a trabajar.

<img src="https://r2.easyimg.io/m5pkohofj/ready.jpg" />

Prueba escribir en tu terminal, parado en la carpeta de tu repositorio clonado el comando "code ." (code "punto")

¿Que sucedio?

Felicidades, puedes cerrar tu primera ventana de VSCode y trabajar con la que se acaba de abrir donde esta tu nuevo proyecto.

A partir de aca. La mecánica para trabajar es exactamente igual que en el caso anterior.

Solamente necesitas usar los comandos git add, git commit y git push para subir los cambios necesarios.

Ten en cuenta que no necesitas linkear el repositorio local al repositorio de github ya que al clonarse directamente, esto ya es automatico.

Prueba crear archivos / carpetas, moverte a esta carpeta y crear archivos dentro. Hace commits y pushealos para ir probando.
