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

Primero vamos a posicicionarlos en la parte donde esta nuestro proyecto en la carpeta principal (mas adelante de explico porque nos ubicamos ahi) y dale click derecho y elige git bash ,bueno esa uso yo ,sera tu eleccion cual desees usar.

1.-Se nos abrira la terminal y el primer comando que usaremos sera: GIT INIT
esto comando le esta diciendo configura git para poder empezar a subir el proyecto.


2.-A continuacion escribimos el comando GIT STATUS , te apareceran nombres de tus archivos de tu proyecto en color rojo, importante aqui solo deben ver tus archivos de tu proyecto , si esta una carpeta o archivo como foto o videos que no sea del proyecto , cierra la ventana terminal y asegurarte estar dentro de la carpeta de tu proyecto de lo contrario luego tus archivos personales se subiran a github.

3.-Ya que te aseguraste que tus archivos son los de tu proyecto escribiremos el siguiente comando :GIT ADD . (agrega todos los archivos) | GIT ADD NOMBREDELARCHIVO (agrega de un archivo uno en uno)


4.- Escribe GIT COMMIT -M "ACABO DE SUBIR MI PROYECTO"
Esto se hace para guardar y versionar nuestro proyecto a modo local , si tu guardas un archivo de en uno en uno primero pondrias add y despues commit , y asi tendrias mucho mas versionado cada archivo de tu proyecto. 

5.- Ahora escribiremos git remote add origin urlderepo
para poder decirle a git a donde mandaremos nuestro proyecto

6.- escribe git remote -v
te tendran que salir el nombre de tu repo con las url (fetch y pull) , si no te aparece asegurate de poner la url de repositorio correctamente

7.-Ahora escribiremo git pull origin main (en ocasiones en lugar de main suele ser master)
Escribiremos git pull origin main, esto para que nuestro proyecto local se sincronice con el proyecto remoto, en este caso tenemos el archivo readme , y justo ahora despues de que escribir ese comando debera aparecerte en tu carpeta de proyecto el archivo readme.

8.-Ahora escribimos git push origin main 
para mandar nuestro proyecto a github y tu proyecto ya debera aparecer en github.


AHORA PARA CUANDO CLONAS UN PROYECTO DE GITHUB

simple elige la ubicacion de la carpeta o donde quieras descargar el proyecto del repositorio ,click derecho y git bash

1.- Escribe git clone urlreposorio
esto descarga el proyecto

2.-ahora dale en git status y si te aparecen carpetas o archivo con letras rojas ,  cierra la terminal y vuelvela abrir ya que te debe aparece "vacio" diciendo no ahi commit tu rama esta limpia (esta en ingles claro).

3.- escribe git remote -v 
te debe aparecer el repositorio remoto que clonaste (fetch pull)

4.- ahora si nosotros creamos un archivo o carpeta en el proyecto que clonamos y tu escribes git status te apareceran archivos con  letras rojas, eso y por ende tenemos que añadirlas al repo local para posterimente mandarlas a nuestro repositorio remoto.
OJO AQUI si nuestro proyecto tiene muchas carpetas es recomendable que te ubiques o te metas dentro de la carpeta del proyecto para asi saber donde y que carpeta estas actualizando EJEMPLO dentro proyecto tengo carpeta 1 y carpeta 2 , yo actualizo la carpeta dos tendria que hacer esto
primero escribo ls para ver que carpetas o archivos tiene mi proyecto
segundo ya que me asegure en este caso carpeta 2 ,seria cd carpeta 2 (para meterme dentro la carpeta 2)
tercero ahora si git add . / o nombre de archivo y posteriormente git commit -m "subir archivo en carpeta2"

ahora que pasa si modifique o añadi  un archivo en carpeta 1 , pues tengo que salir de carpeta 2 y ubicarme en carpeta 1
y lo hago asi cd .. (cd espacio dos puntos) esto me hace salir de carpeta 2 y me ubico en la carpeta del proyecto principal ahora entro carpeta 1 y hago los pasos de arriba.

ahora si hago el git push origin main y listo ya tendre todo en mi repositorio remoto.
