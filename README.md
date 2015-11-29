# campusscif repositorio para los ejercicios a entregar

#Adolfo voy incluyendo los comandos

2.1 REPOSITORIO CAMPUSCIFF

1. git clone https://github.com/Danielobit/campusciff.git

2.2 README
1. echo > readme.md

2.3 COMMIT Y PUSH INICIAL
2. git status

3. git add .

4. git commit -m"commit inicial"

2.4 IGNORAR ARCHIVOS
Creo carpeta y archivo privados
   mkdir privada
   echo "fichero privado" > privado.txt
   echo > .gitignore
   echo "C:\Users\MONSO\Downloads\GIT\campusciff\privada\" >> .gitignore
   echo "C:\Users\MONSO\Downloads\GIT\campusciff\privado.txt" >>.gitignore

2.5 CREAR EL TAG V0.1
1. echo > l.txt
2. git tag V0.1 
3. git add .
4. git commit -m"tercer commit"
5.git status
6.git push origin master

2.6 CREAR UNA RAMA REMOTA V0.2
1. git checkout -b v0.2
2. echo > 2.txt
2. git commit -am"cuatro commit"
3. git push origin v0.2:v0.2





