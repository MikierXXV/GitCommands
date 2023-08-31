# Comandos de git curso openwebinaris

### working directory - staged in - repository
stages

### Comando git log --oneline
6ee3ed8 (HEAD -> dev_transfromador, origin/dev_transfromador) Dev: delete
37556b8 Fix: redirect works correctly
3a95004 Dev: añadida la parte del transformador
af7b3c6 (origin/dev, dev) NEW: Multiple evaluations grading method finish
92e4a5c NEW: Multiple gradebook putted inside a hierarchical form
6742ad9 Weightedevaluations now using AMD modules
385782a Weighted evaluations in the grade config wizard
6022025 WIP: Weighted evaluations now using AMD modules
8fd76d8 WIP: bug fix totals order
706e8a0 WIP: remove gradeitem categories
bceb22b WIP: bug fixes
20ce845 WIP: add gradeitem category UNDER CONSTRUCTION
9b3ada2 WIP: dashboard add gradeitems and grade categories
c66be9a WIP: fix bug adding multiple categories in weightedevaluations
739eea8 WIP: fix add multiple categories break eventlisteners
f689197 WIP: save and exit buttons
b0562cb WIP
70d1611 WIP
db2b1d7 WIP: bug fixes
c7767e2 WIP: bug fix
ad23059 WIP: bug fix
db81a99 WIP: bug fixes
5857114 WIP: multipleevaluations mockup with js
5643c15 WIP: add links to formula creator and multipleevaluations
bc966fd Initial commit
9785c1b (origin/pre, origin/master, origin/HEAD, master) Initial commit


### .gitignore
*.tmp // ignora ficheros con extension tmp

### git diff
muestra diferencias existentes

### git diff --staged
compara con el area de preparacion
sin el staged comparo staged con el working directory

### git difftool
herramienta para visualizar cambios

### git rm
remove

### git mv
renombramos fichero i lo ponemos en el area stage. git mv readme.md readme2.md

### git log --pretty=format:"%h %an %ar - %s"
muestra log en un mejor formato

### git show
muestra contenido de un cierto momento del codigo: git show (hash del git log a mostrar)

### git init, git remote add https://... , git fetch, git pull origin master
obtener un repo sin git clone, git fetch (bajarte codigo), git pull (ponerlo en la rama)

### rm -rf
borrar de forma recursiva forzando

### git clone https://.../folder .
clonar un repo sin la carpeta folder, contenido se guarda sin la carpeta de un nivel superior

### git push origin master

### git checkout master
cambiar de rama, en este caso a master

### git checkout -- . // git checkout -- master (documento)
traer todos los archivos de la revision al directorio actual

### git checkout (HEAD/hash) fichero

### git checkout HEAD~1 fichero
traete uno menos

### git reset HEAD fichero
sacar de stage in area

### git reset --hard (hash)
quita elementos area stage in y recupera contendio del hash

### git revert (hash)
revertir cambios a hash especificado

### git revert HEAD...HEAD~2 --no-edit
revierte todos los cambios des de head a head -2 sin preguntar por los cambios

### git branch -v -a
listado de branches con informacion

### git merge new_master master
merge del contenido de new master a master

### git branch -d (namebranch)
eliminar rama

### git diff --cache
muestra los cambios en stage in

### git log -p
muestra los logs con los cambios del commit

### git log -p -n 2
muestra los logs con los cambios del commit solo los dos ultimos cambios

### git log --since="2 weeks ago" --until="2 days ago"

### git blame (filename)
muestra autores que han intervenido en el fichero

### git blame -L 51,52 (filename)
muestra autores que han intervenido en el fichero en las lineas indicadas

### git cherry-pick origin/master (hash)
hacer merge del proyecto remoto a partir de una version

### git cherry-pick --continue
continuar con el cherry-pick

### git checkout -theirs .
Quedarme con el contenido remoto, no el mio

### git checkout -ours .
Quedarme con mi version

### git rebase --interactive --root
comprimir historial de commits, interactive proporciona pantalla interactiva para seleccionar cambios
root especifica el inicio donde empezar a comprimir. (ej cambiando root: HEAD HEAD~4, serian los ultimos cuatro cambios)

interactive:
pick -> esta en uso
squash -> comprimir


### git show (tag)
muestra informacion asociada al tag

### git tag -a v1.5 -m "Esta es la version 1.5"
crear un tag con conjuntos de cambios:
tag v1.0
Tagger: miguel.gutierrez.jariod <miguel.gutierrez.jariod@upcnet.es>
Date:   Sat Jul 15 10:53:20 2023 +0200

version 1.0

commit 315f21b406775675b7881dfbaa17ac58d20fe7e5 (HEAD -> ramatest, tag: v1.0)
Author: miguel.gutierrez.jariod <miguel.gutierrez.jariod@upcnet.es>
Date:   Sat Jul 15 10:22:22 2023 +0200

    escenario 9

### git commit --amend (mover puntero en el tiempo)
permite corregir commit y incluir ficheros que no fueron añadidos (untracked fields)
despues agregar fichero y hacer segunda confirmacion
### git stash
salva stage in area (guarda una foto que permite recuperar con: git stash apply)


