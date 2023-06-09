# Git

## General

Hoy en día, Git es, con diferencia, el sistema de control de versiones moderno más utilizado del mundo. Git es un proyecto de código abierto maduro y con un mantenimiento activo que desarrolló originalmente Linus Torvalds, el famoso creador del kernel del sistema operativo Linux, en 2005. Un asombroso número de proyectos de software dependen de Git para el control de versiones, incluidos proyectos comerciales y de código abierto. Los desarrolladores que han trabajado con Git cuentan con una buena representación en la base de talentos disponibles para el desarrollo de software, y este sistema funciona a la perfección en una amplia variedad de sistemas operativos e IDE (entornos de desarrollo integrados).

Git, que presenta una arquitectura distribuida, es un ejemplo de DVCS (sistema de control de versiones distribuido, por sus siglas en inglés). En lugar de tener un único espacio para todo el historial de versiones del software, como sucede de manera habitual en los sistemas de control de versiones antaño populares, como CVS o Subversion (también conocido como SVN), en Git, la copia de trabajo del código de cada desarrollador es también un repositorio que puede albergar el historial completo de todos los cambios.

![git](https://github.com/dimasx010/knowledge/assets/105082657/f30bcef5-e86f-47a1-9eed-c032c0672a39)

## Comandos basicos

-  Inicializamos el proyecto git. 
```git
git init
```
-  Agregar un archivo. 
```git
git add archivo1.txt
```
-  Enviar los cambios a la etapa commit. 
```git
git commit -m "texto"
```
-  Ver los cambios que se encuentran añadidos. 
```git
git diff --stated
```
-  Mostrar el todos los commit que hemos realizado en conjunto a una cadena alfanúmerico. 
```git
git log --oneline 
```
-  Mostrar la rama nosotros nos encontramos, si nos encontramos en la principal pues veremos la palabra main, e igualmente tendremos un listado de ramas creadas. 
```git
git branch 
```
-  Eliminar rama. 
```git
git branch -D nombre_rama
```
-  Crear una rama, y el texto sería igual al nombre de la rama y hacemos el switch a ella. 
```git
git checkout -b texto
```
-  Cambiar de rama. 
```git
git checkout nombre_rama
```
-  Traer los cambios de la rama secundaria indicada con el nombre "ramab" a la rama donde estemos. 
```git
git merge ramab
```
-  Subir los cambios a los repos remotos. 
```git
git push
```
-  Bajamos los datos de la rama que indicamos. 
```git
git pull origin ramaC
```
-  Declarar directorios de confianza. 
```git
git config --global --add safe.directory '%(prefix)//ENRUTADO'
```
-  Clonar proyecto. 
```git
git clone -b master URL_PROYECTO
```
-  Listar configuraciones ejecutadas. 
```git
git config --list
```
-  Enviar request al repo remoto. 
```git
git request-pull -p origin/main
```
-  Descartar cambios que se han realizado al directorio de trabajo. 
```git
git checkout
```
-  Remueve un enrutado de repo remoto. 
```git
git remote remove origin
```

## Referencias
- https://www.atlassian.com/es/git/tutorials/what-is-git
