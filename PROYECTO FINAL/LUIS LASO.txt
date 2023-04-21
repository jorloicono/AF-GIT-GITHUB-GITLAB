# CREACION Y ACTUALIZACION DE REPOSITORIOS

## EJERCICIO 1 

$ git config --global user.name luis10laso

$ git config --global user.email johndoe@example.com

Coloreado de la salida activado por defecto(se puede ver haciendo un "git branch" 
y viendo como se marca en verde la rama actual de un repositorio por ejemplo)

$ git config --list

## EJERCICIO 2

$ mkdir libro

$ git init

$ dir

## EJERCICIO 3

$ git status

$ notepad indice.txt (Abrir un bloc de notas y luego se edita desde este 
lo que queremos poner en el fichero)

$ git status (Se ve como el nuevo fichero indice.txt está sin trackear)

$ git add indice.txt (Pasa a estar en zona de preparación)

$ git status

##- EJERCICIO 4

$ git commit -m "Anadido indice del libro"

$ git status

## EJERCICIO 5

$ git diff

$ git add indice.txt

$ git commit -m "Anadido capitulo 3 sobre gestion de ramas"

## EJERCICIO 6

$ git log -p -2

$ git commit --amend (En el editor de texto se cambia el mensaje de commit)

$ git log -p -2 (Se ve como el mensaje de commit ha cambiado)

# MANEJO DEL HISTORIAL DE CAMBIOS

## EJERCICIO 1

$ git log -p

$ mkdir capitulos

$ cd capitulos

$ git add . (Anado todo el directorio pero como en este caso solo esta el fichero
es lo mismo que solo añadir el fichero)

$ git commit -m "Anadido capitulo 1"

$ git log -p

## EJERCICIO 2

$ notepad capitulo2.txt

$ git add .

$ git commit -m "Anadido capitulo 2"

$ git log -p -3

## EJERCICIO 3

$ notepad capitulo3.txt

$ git add .

$ git commit -m "Anadido capitulo 3"

$ git log (esto da los hashes de la primera y la ultima version)

$ git diff "Hash del primer commit" "Hash del ultimo commit"

## EJERCICIO 4

$ cd .. (Ir al directorio donde esta indice.txt)

$ Añadir con editor de texto

$ git add .

$ git commit -m "Anadido capitulo 5 al indice"

$ git log --pretty="%an" --follow indice.txt (formatear para que salga el autor y luego especificar el archivo)

# DESHACER CAMBIOS

## EJERCICIO 1

$ git status

$ git checkout -- indice.txt

$ git status

## EJERCICIO 2

$ git add .

$ git status

$ git reset HEAD indice.txt

$ git status

$ git checkout -- indice.txt

$ git status

## EJERCICIO 3

(Después de haber borrado y anadido nuevos ficheros)

$ git add .

$ git status

$ git reset HEAD . (a nivel de directorio en libro/)

$ git status

$ git checkout -- . (así deshago los cambios y vuelves a la versión anterior del repo)

$ git status

## EJERCICIO 4

$ git add .

$ git commit -m "Borrado accidental"

$ git log 

$ git reset HEAD~1

$ git log

$ git add .

$ git commit -m "Borrado accidental"

$ git reset HEAD~1

$ git checkout -- . (se podría haber hecho con "git reset --hard HEAD~1" 
tambien en vez de usar este comando y el anterior)

$ git log

# GESTION DE RAMAS

## EJERCICIO 1

$ git branch bibliografia

$ git branch

## EJERCICIO 2

$ git add .

$ git commit -m "Anadido capitulo 4"

$ git log --all

## EJERCICIO 3

$ git checkout bibliografia

$ git add .

$ git commit -m "Anadido primera referencia bibliografica"

$ git log --all

## EJERCICIO 4

$ git checkout master

$ git merge bibliografia

$ git branch --delete bibliografia

$ git log --all

## EJERCICIO 5

$ git checkout -b bibliografia

$ git add .

$ git commit -m "Anadida nueva referencia bibliografica"

$ git checkout master

(Hacer cambios en el fichero)

$ git add .

$ git commit -m "Anadida nueva referencia bibliografica"

$ git merge bibliografia

$ git commit -m "Resuelto conflicto de bibliografia"

$ git log --all

# REPOSITORIOS REMOTOS

## EJERCICIO 1

(Despues de haber creado el repositorio en github)

$ git remote add origin https://github.com/luis10laso/libro-git.git

$ git remote -v

## EJERCICIO 2

$ git push origin master

## EJERCICIO 3

$ mkdir libro-git-alvaro

$ cd libro-git-alvaro

$ git clone https://github.com/alvarogarciapiz/libro-git.git

$ echo luis10laso luis.diez@gruposantander.com > autores.txt

$ git add .

$ git commit -m "Anadido autor"

$ git push

## EJERCICIO 4

(Despues de hacer la bifurcación en github)

$ git clone https://github.com/luis10laso/libro-git-1.git

$ git checkout -b autoria

$ echo luis10laso email@address.com >> autores.txt

$ git add .

$ git commit -m "Anadido nuevo autor"

$ git push origin autoria

(Luego crear pull request, url de la Pull Request creada: https://github.com/asalber/libro-git/pull/138)
