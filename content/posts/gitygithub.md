---
title: "Git y GitHub"
date: 2022-04-24
description: 'Uso de comandos basicos y entendiendo la diferencia'
---

Primero tenemos git que en pocas palabras seria el software "la terminal" ,bash,gui shell,cmd, en el puedes hacer muchisimas cosas.<br>
Segundo Github es la plataforma web (como el facebook XD) , el sitio donde se alojan tus archivos,proyectos, etc.<br>
Asi que asi de facil es entender la diferencia de ambos.

Acontinuacion de mostrare un poco de lo que e aprendido , y espero que a ti te ayude muchisimo, quizas sea algo basico pero muy importante en el dia a dia, en el mundo de la programacion.


## Uso de **git bash en windows**

Primero lo primero ve a github y crea un repositorio, agregale una descripcion y elige opcion readme (para que se nos cree un archivo md en nuestro proyecto) y presiona el boton create repository<br>

![image](https://user-images.githubusercontent.com/94188197/165134496-44531c5b-fa27-46d5-996b-f00532964e10.png)


### Cuando creamos un proyecto en nuestro pc y despues queremos subirlo a github, los pasos que haremos seran los siguientes:

Primero vamos a posicicionarlos en la parte donde esta nuestro proyecto en la carpeta principal (mas adelante de explico porque nos ubicamos ahi) y dale click derecho y elige git bash here quiere decir abrir git aqui, bueno esa uso yo sera tu eleccion cual desees usar.

![image](https://user-images.githubusercontent.com/94188197/165135952-e2bb6f35-77e3-4d2a-9854-288ef23c47d3.png)


#### 1.-Se abrira la terminal y el primer comando que usaremos sera: git init

Este comando **git init** le esta diciendo configura git para poder empezar a subir el proyecto.

![image](https://user-images.githubusercontent.com/94188197/165136398-3d7d29a7-a6a3-4069-b497-18dc777b0e6a.png)


#### 2.-A continuacion escribiremos el comando git status

Ahora con **git status** apareceran nombres de tus archivos de tu proyecto en color rojo, importante aqui solo deben ver tus archivos de tu proyecto , si esta una carpeta o archivo como foto o videos que no sea del proyecto , cierra la ventana terminal y asegurarte estar dentro de la carpeta de tu proyecto de lo contrario luego tus archivos personales se subiran a github.<br>
![image](https://user-images.githubusercontent.com/94188197/165148504-959ca5e3-4161-4105-9537-47f1d76831de.png)


#### 3.- Ahora escribiremos el comando :git add . "agrega todos los archivos"  o git add nombredelarchivo "agrega de un archivo uno en uno"
Ya que te aseguraste que tus archivos son los de tu proyecto escribiremos el comando de arriba y vuelves a escribir git status y veras que ahora el nombre de tus archivos cambio a letra color verde.
![image](https://user-images.githubusercontent.com/94188197/165136959-6120aa2c-adf5-4fb1-a7f9-544cfc9b71f3.png)


#### 4.- Escribe git commit -m "acabo de subir mi proyecto"
Esto se hace para guardar y versionar nuestro proyecto a modo local , si tu guardas un archivo de en uno en uno primero pondrias add y despues commit , y asi tendrias mucho mas versionado cada archivo de tu proyecto. 
![image](https://user-images.githubusercontent.com/94188197/165137133-5bfb6d85-5d07-4cd6-936c-298fce71164b.png)


#### 5.- Ahora escribiremos git remote add origin urlderepo <br>
Para poder decirle a git a donde mandaremos nuestro proyecto la url la obtienen de aqui.
![image](https://user-images.githubusercontent.com/94188197/165137466-fd9f1b72-27e4-4218-8f91-2c48b159a3af.png)

Escribimos el comando arriba mencionado.
![image](https://user-images.githubusercontent.com/94188197/165148831-3b8586bb-4112-4ab2-b21c-6ad4301541aa.png)


#### 6.- Escribe git remote -v <br>
Te tendran que salir el nombre de tu repo con las url (fetch y push) , si no te aparece asegurate de poner la url de repositorio correctamente.
![image](https://user-images.githubusercontent.com/94188197/165137799-5e1cf458-04a2-45ce-9878-7aaf7da77f41.png)

#### 7.-Ahora escribiremo --git pull origin main-- (en ocasiones en lugar de main suele ser master)<br>
Escribiremos **git pull origin main** , esto para que nuestro proyecto local se sincronice con el proyecto remoto, en este caso tenemos el archivo readme , y justo ahora despues de que escribir ese comando debera aparecerte en tu carpeta de proyecto el archivo readme.

![image](https://user-images.githubusercontent.com/94188197/165140535-c38d39f9-4355-471d-ac05-c8fc73878030.png)<br>

Presta atencio aqui porque cuando nosotros iniciamos un proyecto aqui en git el nombre de la rama sera master y cuando añadimos el de github el nombre de la rama es main, asi que antes de hacer pull o push cambia el nombre de la rama con el siguiente comando : **git branch -M master main**  (master es de git y le digo ahora nombrala main para que coincida con la de github de lo contrario te dara problemas que en github se creo una nueva rama e hicieron pull).

##### Primero cambiamo el nombre de la rama para que sea el mismo
![image](https://user-images.githubusercontent.com/94188197/165151163-5cfdb0b0-a864-4fff-b4d3-6b25046cd9f1.png)

##### Segunfo ahora si hacemos el pull
![image](https://user-images.githubusercontent.com/94188197/165151915-add43288-9562-4c66-9894-4da04c1fd109.png)


#### 8.-Ahora escribimos git push origin main<br> 
Para mandar nuestro proyecto a github escribimos el comando.
![image](https://user-images.githubusercontent.com/94188197/165142576-5d6c6b6b-9c4e-4bea-a79b-f54b6b9207b8.png)
Y ya debe aparecer en tu repositorio remoto de github.
![image](https://user-images.githubusercontent.com/94188197/165142758-e8e49af6-7141-4217-9cf8-e0806ccf12ec.png)


### AHORA PARA CUANDO CLONAS UN PROYECTO DE GITHUB

Simple elige la ubicacion de la carpeta o donde quieras descargar el proyecto del repositorio ,click derecho y git bash (para este caso elegiremos el mismo proyecto de arriba , aqui ya elimine el proyecto que tenia localmente mi carpeta esta vacia).
![image](https://user-images.githubusercontent.com/94188197/165153913-bc30d936-6d8f-4032-b77f-ae4fe12c0cc1.png)


#### 1.- Escribe git clone urlreposorio
Lo que hara **git clone urlrepo** es descargar el repositorio.
Podras ver que una ves escribo el comando y presiono enter se descargan los archivos.
![image](https://user-images.githubusercontent.com/94188197/165154209-0bbcef25-f2c6-4dd3-b494-21336759ed67.png)


#### 2.-ahora dale en git status y si te aparecen carpetas o archivo con letras rojas ,  cierra la terminal y vuelvela abrir ya que te debe aparece "vacio" diciendo no ahi commit tu rama esta limpia (esta en ingles claro).
Aqui aparecen carpetas que no deberan mostrarse asi que cerramos la terminal y la volvemos a abrir .
![image](https://user-images.githubusercontent.com/94188197/165154448-cda3c406-c5b2-421e-ac0e-b70a7fe69604.png)

Aqui vemos volvi a abrir la terminal en la misma carpeta donde descarque el repositorio (paso clave abre la terminal donde veas la carpeta .git que esta oculta tendras que modificar como ver carpetas ocultas en tu terminal si es que no te aparece).
Bueno regresando escribimos **git status** y debe aparecer asi: 
![image](https://user-images.githubusercontent.com/94188197/165154903-0ff6ece1-df80-43fc-a39f-8dcfe5875d73.png)


#### 3.- Escribe git remote -v 
Te debe aparecer el repositorio remoto que clonaste (fetch push)
![image](https://user-images.githubusercontent.com/94188197/165155064-93da762e-735d-46f2-8583-3762b049eb34.png)


#### 4.- Ahora si nosotros creamos un archivo o carpeta en el proyecto que clonamos y tu escribes git status te apareceran archivos con  letras rojas, y por ende tenemos que añadirlas al repo local para posterimente mandarlas a nuestro repositorio remoto.
OJO AQUI si nuestro proyecto tiene muchas carpetas es recomendable que te ubiques o te metas dentro de la carpeta del proyecto para asi saber donde y que carpeta estas actualizando.

EJEMPLO escribire **ls** en la terminal y me apareceran mis carpeta y archivos del repositorio.
![image](https://user-images.githubusercontent.com/94188197/165155617-39c3caf9-42d7-499b-9adc-70c026edb11a.png)

Si yo quiero agregar o modifique un archivo de la carpeta 2 primero accedo o me ubico dentro de ella de la siguiente manera: **cd carpeta2
![image](https://user-images.githubusercontent.com/94188197/165156014-97ba9285-499c-46dc-b02b-76beb9ca4e29.png)

Agregare un archivo( de forma manual) a carpeta 2 y luego escribire **git status** y veran que aparecera en letras rojas 
![image](https://user-images.githubusercontent.com/94188197/165156353-d1f1ccf8-baa7-4b00-8d6f-301af34a7e28.png)

Escribo **git add .** ya que solo es un archivo pero si fuesen varios escribiria uno a uno con su nombre, despues procedo a hacer el commit y un ls.
Como podran ver agregue un archivo localmente a git.
![image](https://user-images.githubusercontent.com/94188197/165156701-7cc882cb-dcab-41a9-9f34-2c3080913761.png)

Ahora haremos **git push origin main** y revisaremos nuestro repositorio.
![image](https://user-images.githubusercontent.com/94188197/165157204-58e40972-d48c-4882-b61d-61dfb6f19511.png)

Aqui checando que efectivamente se subio el archivo.
![image](https://user-images.githubusercontent.com/94188197/165157301-1109ebd4-188c-4caf-ae3d-f8cb493a5f72.png)



#### 5.-Ahora que pasa si modifique o añadi  un archivo en carpeta 1 , pues tengo que salir de carpeta 2 y ubicarme en carpeta 1
Escribo **cd ..** (cd espacio dos puntos ) para salirme de carpeta2 y luego un ls veran las dos carpetas, ahora escribo **cd carpeta1** y repito los proceso de **git add .** , ** git commit -m "nombre de commit", y por ultimo **git push origin main** y ya tendre todo en mi repositorio remoto.
![image](https://user-images.githubusercontent.com/94188197/165158011-50ecf035-5074-47ea-867b-9ed074e679fe.png)

Espero te haya ayudado mucho y que sigas aprendiendo y vueles hasta el infinito y mas alla :D.




