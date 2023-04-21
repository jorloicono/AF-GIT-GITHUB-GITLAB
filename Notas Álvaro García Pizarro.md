# CREACIÓN Y ACTUALIZACIÓN DE REPOSITORIOS

## EJERCICIO 1
`git config --global user.name "Alvaro Garcia Pizarro"`

`git config --global user.email alvarogp99@ejemplo.com`

`El color viene activado por defecto`

`git config --list`

## EJERCICIO 2
`mkdir libro`

`cd libro`

`git init`

`dir`

## EJERCICIO 3
`git status`

`echo .>indice.txt`

`Edito manualmente el fichero con el notepad para agregar la info`

`git status`

`git add .`

`git status`

## EJERCICIO 4
`git commit -m "Añadido índice del libro."`

`git status`

## EJERCICIO 5
`Se modifica manualmente el archivo`

`git diff`

`git add .`

`git commit -m "Añadido capítulo 3 sobre gestión de ramas"`

## EJERCICIO 6
`git show`

`git commit --amend`

`En vim edito el contenido del commit`

`git log / git show`


# MANEJO DEL HISTORIAL DE CAMBIOS

## EJERCICIO 1
`git show`

`mkdir capitulos`

`cd capitulos`

`"Git es un sistema de control de versiones ideado por Linus Torvalds" > capitulo1.txt`

`git add .`

`git commit -m "Añadido capítulo 1"`

`git show`

## EJERCICIO 2
`"El flujo de trabajo básico con Git consiste en: 1- Hacer cambios en el repositorio. 2- Añadir los cambios a la zona de intercambio temporal. 3- Hacer un commit de los cambios." > capitulo2.txt`

`git add .`

`git commit -m "Añadido capítulo 2"`

`git log -p -2`

## EJERCICIO 3
`"Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas." > capitulo3.txt`

`git add .`

`git commit -m "Añadido capítulo 3."`

`git show`

## EJERCICIO 4
Se modifica manualmente el fichero de indice para incluir el capítulo 5

`git add .`

`git commit -m "Añadido capítulo 5 al índice"`

`git blame indice.txt`


# DESHACER CAMBIOS

## EJERCICIO 1
Se elimina manualmente la última línea del fichero indice.txt

`git status`

`git checkout -- indice.txt`

`git status`

## EJERCICIO 2
Se modifica manualmente el fichero de indice para eliminar su última línea

`git add .`

`git status`

`git reset indice.txt`

`git status`

`git checkout -- indice.txt`

`git status`

## EJERCICIO 3
Se elimina la última línea del fichero indice a mano y se guarda

`cd capitulos`

`del capitulo3.txt`

`echo > capitulo4.txt`

`git add .`

`git status`

`git reset`

`git status`

`git checkout`

`git status -- .`

## EJERCICIO 4
Se elimina la última línea del fichero indice.txt

se elimina el fichero capitulo

`git add .`

`git commit -m "Borrado accidental"`

`git status / git log`

`git reset --soft HEAD~1`

`git status`

`git commit -m "Borrado accidental"`

`git status`

`git log`

`git reset --hard HEAD~1`

`git log`


# GESTIÓN DE RAMAS

## EJERCICIO 1
`git branch bibliografia`

`git branch -a`

## EJERCICIO 2
`echo "En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto." > capitulo4.txt`

`git add .`

`git commit -m "Añadido capítulo 4"`

`git log --graph --oneline`

## EJERCICIO 3
`git checkout bibliografia`

`echo "Chacon, S. and Straub, B. Pro Git. Apress." > bilbiografia.txt`

`git add .`

`git commit -m "añadida primera referencia bibliografica"`

`git log --graph --oneline`

## EJERCICIO 4
`git checkout master`

`git merge bibliografia`

`git branch --delete bibliogafia`

`git log --graph --oneline --decorate`

## EJERCICIO 5
`git branch bibliogafia`

`git checkout bibliografia`

`bibliografia.txt`

Se modifica manualmente el contenido del fichero

`git add .`

`git commit -m "Añadida nueva referencia bibliográfica."`

`git checkout master`

`bibliografia.txt`

Se modifica manualmente el fichero

`git add .`

`git commit -m "Resuelto conflicto de bibliografía"`

`git log --graph --oneline --decorate`


# REPOSITORIOS REMOTOS

## EJERCICIO 1
`Se crea desde github.com un repo público llamado libro-git`

`git remote add github https://github.com/alvarogarciapiz/libro-git`

`git remote -v`

## EJERCICIO 2
`git push github master`

(Importante, los cambios aparecen en la rama master y no es la main), se debe cambiar de rama para ver los cambios

## EJERCICIO 3
me dan acceso a su repo
`git clone https://github.com/luis10laso/libro-git`

`echo > autores.txt`

`autores.txt`

Se añade manualmente el nombre y nombre de usuario al repo

`git add . git commit -m "Añado autor"`

`git push`


## EJERCICIO 4 
Se hace un fork desde https://github.com/asalber/libro-git

Una vez hecho el fork me clono el proyecto a mi equipo

`git clone https://github.com/asalber/libro-git`

`cd libro-git`

`git branch autoria`

`autores.txt`

Se añade manualmente mi Nombre y nombre de usuario

`git add .`

`git commit -m "Añadido un nuevo autor"`

`git push origin autoria`

Al no tener acceso a su repo nos salta un error de permisos

Se hace el pull request desde github






