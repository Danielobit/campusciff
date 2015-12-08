# Daniel Escuder - Ejercicios de      ![](https://git-scm.com/images/logo@2x.png)
Adolfo, a continuación ire copiando  [el código fuente utilizado][df1] en cada uno de los apartados de los ejercicios que nos has mandado. **Para mí, estos empiezan en el apartado 2.1 de los apuntes**

NOTA: he subido en el archivo imagenes.zip algunos pantallazos de las tareas realizadas se que comentan mas abajo.

#### 2.1 REPOSITORIO CAMPUSCIFF
1. Creo el repositorio en Github. La url es: https://github.com/Danielobit/campusciff.git
1. Me clono mi repositorio: git clone https://github.com/Danielobit/campusciff.git
#### 2.2 README
  - Genero el fichero con: echo > readme.md

#### 2.3 COMMIT Y PUSH INICIAL 
Se ejecutan los siguientes comandos para conseguirlos:
```sh
    1. git status
    2. git add .
    3. git commit -m"commit inicial"
    4. git push origin master
```
#### 2.4 IGNORAR ARCHIVOS
Se ejecutan los siguientes comandos para conseguirlo:
```sh
    1.mkdir privada
    2.echo "fichero privado" > privado.txt
    3.echo > .gitignore
    4.echo "C:\Users\MONSO\Downloads\GIT\campusciff\privada\" >> .gitignore
    5.echo "C:\Users\MONSO\Downloads\GIT\campusciff\privado.txt" >>.gitignore
```
#### 2.5 CREAR EL TAG V0.1
Se ejecutan los siguientes comandos para conseguirlo:
```sh
    1. echo > l.txt
    2. git tag V0.1 
    3. git add .
    4. git commit -m"tercer commit"
    5.git status
    6.git push origin master
    7. Aunque no se pide he asociado el tag v0.1 al commit realizado en el siguiente paso con: git tag v0.1 95195bf
```
#### 2.6 CREAR UNA RAMA REMOTA V0.2
Se ejecutan los siguientes comandos para conseguirlo:
```sh
    1. git checkout -b v0.2
    2. echo > 2.txt
    3. git commit -am"cuatro commit"
    4. git push origin v0.2:v0.2
```
#### 2.7 MERGE DIRECTO
Se ejecutan los siguientes comandos para conseguirlo:
```sh
    1. git checkout master
    2. git merge v0.2 (me devuelve Already up-to-date)
```

#### 2.8 MERGE CON CONFLICTO
Se ejecutan los siguientes comandos para conseguirlo:
```sh
   1. git checkout master
    2. echo "hola" > l.txt
    3. git commit -am "commit l.txt desde master"
    4. git checkout v0.2
    5. echo "adios" > l.txt
    6. git commit -am "commit l.txt desde v0.2"
    7. git checkout master
    8. git merge v0.2 (al hacer esto me da conflicto en l.txt)
    9. git branch --merged (me devuelve que la master esta mergeada)
    10. git branch --no-merged /me devuelve la v0.2 no lo esta)
    11. edito el fichero l.txt y dejo lo que estaba en la rama master , es decir, "hola". Ver pantallazo Solucionado conflicto merge
    12. git commit -am "solucionado conflicto"
    13. git merge v0.2
    14. Con esto ya me dice que todo esta up-to-date (es decir, sincronizado)
```

#### 2.9 BORRAR RAMA
Se ejecutan los siguientes comandos para conseguirlo:
```sh
    1. git tag v0.2
    2. git log --oneline --decorate --graph --all o si tenemos el alias de clase hacer git list (it config --global alias.list 'log --oneline --decorate --graph --all')
    3. git branch -d V0.2
```

#### 2.10 CUENTA DE GITHUB
Para realizar esta parte he seguido los siguientes pasos:
- Para la configuración del doble factor de autenticación ver la imagen: **Configuracion_autenticacion_doble_factor.jpg**
- Para la foto de perfil, como estoy nostálgico, me pongo una foto de mis dibujos favoritos.
- La clave pñublica la añadí en clase pero pongo un pantallazo (**clave publica.jpg**) para que puedas verificarlo.

#### 2.11 USO SOCIAL DE GITHUB
He navegado por los repositorios de algunos de mis compañeros y les he puesto la estrella, no puedo sobre todos porque ***no dispongo de la lista de todos los repositorios Github.***

#### 2.12 CREAR UNA TABLA

|        NOMBRE       |                GITHUB                |   |   |   |
|:-------------------:|:------------------------------------:|---|---|---|
|   Paloma Fernandez  | **https://github.com/PalomaCiffBigData** |   |   |   |
|     Juan Frances    |   **https://github.com/juanfrancesgg**   |   |   |   |
| Jose Manuel Cabrera |     **https://github.com/elelement**     |   |   |   |

#### 2.13 COLABORADORES
Adolfo, ya estas puesto como colaborador de mi repo (***https://github.com/Danielobit/campusciff***)

#### 2.14 CREAR UNA ORGANIZACIÓN
La creación de la organización aparece en la imagen (**2.14.Crear_organizacion.jpg**) Dicha organizacion se llama: [*campussciff - Danielobit*][df1]

#### 2.15 CREAR EQUIPOS
- La creación de los equipos aparece en la imagen : **2.15.Crear_equipos.jpg**
- Los permisos, una vez que se crea un repositorio para la organizacion los he fijado de la siguiente forma:
	>De escritura para los administradores

    >De lectura para los colaboradores se puede ver en la imagen: **2.15.fijar permisos.jpg**

#### 2.16 CREAR UN INDEX.HTML
Para realizar esta parte he seguido los siguientes pasos:
1. creo un repositorio dentro de la organizacion llamado campusciff-Danielobit.github.io
2. me lo bajo a mi local clonandolo: git clone https://github.com/campusciff-Danielobit/campusciff-Danielobit.github.io
3. Genero la pagina index dentro del repositorio que me he clonado con: echo "Pagina de Bienvenida de la organizacion de Danielobit" > index.html
4. Lo añado a staging y repositorio con:
	>git add index.html

	>git commit -m"añadir index"
5. Subo el fichero a mi repositorio remoto: git push origin master
6. Se puede navegar hasta la web creada tecleando: ***http://campusciff-danielobit.github.io/index.html***

#### 2.17. CREAR PULL-REQUESTS
Afolfo cojo uno de un compañero no es el de la organización pero es igual, creo que te lo forkeo a ti. Hago esto porque nadie me da un usuario que tenga la organizacion y el repositorio creado y necesito avanzar que ya estamos a finales de semana.
```sh
1. Primero he hecho desde github un fork del repositroio de element, que se llama elelement/campusciff-2015-1.github.io
2. Ahora desde git lo clono con: https://github.com/Danielobit/campusciff-2015-1.github.io
3. Voy a ese directorio: cd c/Users/MONSO/Downloads/GIT/campusciff-2015-1.github.io
4. Creo una rama nueva: git checkout -b v01 
5. echo "añado mi nombre Daniel" >> index.html
6. añado los cambios a mi index: git add index.html
7. hago un commit al repositorio: git commit -m"añado mi rama"
8. subo los cambios a mi repositorio remoto forkeado con: git push origin v01
9. Lanzo la peticiñon de pull - request en github. Si entras a mi perfil podras ver que colaboro en ese repositorio de mi compañero
```
Hago lo mismo para el repositorio de macarena: https://github.com/campusciff-macarenagaranena/campusciff-macarenagaranena.github.io, Adolfo lo he hecho con las únicas personas que tenían los repos creados cuando lo hice yo. No he podido subirlo hasta hoy porque me fui de puente y no pude llevarme el pc.

#### 2.18. ACEPTAR PULL-REQUESTS
Adolfo he aceptado las peticions que me han hecho.



