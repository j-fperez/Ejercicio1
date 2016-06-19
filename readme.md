En el paso 11 utilizo el comando git reset --hard HEAD~1 porque es la forma de que pierda los cambios realizados en el working copy.

En el paso 12 ejecuto primero el comando git reflog para ver la lista de todas las acciones que hemos realizado.
Localizo el identificador 092ed31 que corresponde al commit que acabamos de deshacer.
Entonces ejecuto el comando git reset --hard 092ed31 para volver al último commit

En el paso 13 el merge no causa ningún conflicto porque no hemos modificado el archivo git-nuestro.md en ambas ramas en las mismas lineas.
En la rama style eliminamos la primera linea, así que no co coincide ninguna línea en las dos ramas.

El merge del paso 19 crea conflictos porque se modifica el archivo git-nuestro.md en ambas ramas en las mismas líneas.

El merge del paso 21 no crea conflictos porque el archivo git-nuestro.md es el mismo en las dos ramas.

En el paso 25 utilizo git log --graph
                      git log --decorate
                      git log --pretty=oneline
También pueden utilizarse varias opciones juntas, por ejemplo git log --graph --decorate --pretty=oneline
También pueden utilizarse alias para no tener que escribir todas las opciones

El merge del paso 26 podría ser fast forward. El puntero HEAd apunta tanto a master como a title. Los dos contienen los mismos commits, forman una lista.

En el paso 27 utilizo el comando git reset HEAD~1

En el paso 28 utilizo el comando git checkout -- git-nuestro.md

En el paso 29 utilizo el comando git branch -D title

En el paso 30 utilizo el comando git reflog para ver el hash del merge. Utilizo el comando git reset --hard 170e33b para rehacer el merge.

En el paso 32 primero utilizo git reflog para localizar el hash del commit inicial
y después el comando git reset --hard 271469b894ec85defaadb868e3f8fd4da6e888ce para volver al commit inicial cuando se creo el poema

En el paso 33 no veo la forma de hacerlo. Creo que posiblemente en el paso anterior tenia que haber hecho
 un git checkout 271469b894ec85defaadb868e3f8fd4da6e888ce para volver sin eliminar nada.

