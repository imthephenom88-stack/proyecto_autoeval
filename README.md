Tarea1:
mkdir proyecto-autoeval-> Crear la carpeta de trabajo
cd proyecto-autoeval-> entrar en la carpeta de trabajo
git init-> Para inicializar un repositorio vacío nuevo de git en la carpeta de trabajo
code .-> Para abrir el vs code para crear este archivo

1.¿Para qué sirve el comando git init?¿Qué carpeta oculta se crea automáticamente para rastrear los cambios?
El comando sirve para inicializar el repositorio de git en la carpeta donde estes.
Se crea la carpeta .git, invisible a no ser que se use ls -a

2.¿Qué comando has usado para confirmar que tu identidad es la correcta antes de empezar?
git config --global user.name

Tarea 2:
Desde vscode creo los archivos index.html, secreto.txt y .gitignore.
Dentro de -gitignore escribo *.txt para que ignore todos los archivos .txt
Usando git status verifico que, efectivamente, git no rastrea los archivos .txt
Con git add index.html primero lo paso al Staging Area y con git commit -m "JOSE_ESPAÑA: Estructura inicial del HTML"
realizo el primer commit.

1.¿Por qué es importante el uso de .gitignore en proyectos profesionales?
Es importante para no subir por error archivos que no son del proyecto o que no quieres subir.

2.Si un archivo está "preparado"(staged),¿en qué área de git se encuentra y cuál es el comando para ver esta diferencia antes de confirmar?
Está en el área de preparación, preparado para realizar un commit. 
Se puede usar git status para ver el estado de los archivos actualmente.

Tarea 3:
Con git checkout -b incluir-estilos creo esa nueva rama y me cambio a ella.
En vscode creo el archivo estilos.css.
Con git add estilos.css y git commit -m "JOSE_ESPAÑA: Crear y aplicar estilos" dejo en commit el archivo .css.
Usando git log --oneline compruebo que la rama que hizo ese último cambio es  la rama incluir-estilos.
Con git chekout master vuelvo a la rama principal y compruebo que, desde esa rama, el proyecto no ha cambiado y el archivo .css no está pero en la otra rama si.

1.¿Qué ocurre con los archivos de tu carpeta local cuando saltas de una rama a otra?
Los archivos que se encuentran en la carpeta local cambian según la rama con la que trabajemos, en la rama master
estilos.css no existe mientras que en la rama incluir-estilos si que está.

2.¿Cuál es la principal ventaja de trabajar con ramas independientes en lugar de hacer todo en la rama main/master?
La principal ventaja es que podemos modificar el proyecto desde varias ramas diferentes sin cambiar el proyecto principal pudiendo
trabajar varias personas en el mismo proyecto sin molestarse mutuamente y aplicar los cambios que hagamos cada uno de forma independiente.

Tarea 4:
En mi cuenta de GitHub creo un nuevo repositorio público llamado proyecto_autoeval.
Con el comando git remote add origin https://github.com/imthephenom88-stack/proyecto_autoeval.git
conecto mi repositorio local con el remoto que acabo de crear.
Y con el comando git push -u origin master subo el archivo HTML del que hice el commit en la rama main/master.

1.Al clonar un repositorio,¿qué nombre recibe por defecto el servidor remoto en nuestra configuración local?
Con el comando git remote se ve que recibe el nombre origin.

2.¿Qué comando usarías para ver la URL del servidor remoto que acabas de configurar?
con git remote -v

Tarea 5:
Realizo los cambios en index.html desde GitHub y realizo un commit con mensaje "Cambio de titulo HTML de 'Autoevaluació Git' a 'Ejercicio de JOSE_ESPAÑA'.
Uso git fetch para comprobar si mi repositorio local está al día con el remoto y realizo un git pull origin master
para traerme los cambios al repositorio local.

1.¿Qué comandos has utilizado para comprobar si el repositorio local está actualizado?
git fetch y git status

2.¿Cuál es la diferencia fundamental entre ejecutar un git fetch y git pull según lo que acabas de experimentar?
git fetch se trae la información sobre si hay cambios en el repositorio remoto respecto a lo que tenemos en el repositorio local
y git pull nos actualiza nuestro repositorio local con los archivos del repositorio remoto.

Tarea 6:
Borro la línea *.txt de .gitignore para hacer visibles a git los archivos .txt.
Renombro el archivo README.txt a README.md con el comando mv README.txt README.md.
Y hago git add README.md/git commit -m "Añadiendo archivo README.md a GitHub"/git push origin master.

Preguntas de reflexión:

No hay comandos que me haya costado entender, ha sido más problema con las ramas. En un principio había hecho commit en master del archivo html vacío y lo modifiqué desde la rama 'incluir-estilos' introduciendo el contenido desde esa rama pero cuando puse el repositorio remoto lo hice desde master he hice push del html vacío, me dí cuenta al querer modificar el html desde GitHub y tuve que volver a la rama 'incluir-estilos' para copiar el contenido del html y volver ha hacerle push desde la rama master(en mi git es master y no main).  