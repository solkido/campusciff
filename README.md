# campusciff


# 2.1 REPOSITORIO CAMPUSCIFF (I)

## Crear un repositorio en vuestro GitHub llamado campusciff.

	
 # 2.2 REPOSITORIO CAMPUSCIFF (II)
## Clonar vuestro repositio en local.
	$ git clone https://github.com/solkido/campusciff.git

# 2.3 README
## Crear (si no lo habéis creado ya) en vuestro repositorio local un documento README.md.
	touch README.md

# 2.4 COMMIT INICIAL
 ## Añadir al README.md los comanddos utilizados hasta ahora y hacer un coomit inicial con el 
mensaje commit inicial.
	git add .
	git commit -m "commit inicial"
    
 # 2.5 PUSH INICIAL
 ## Subir los cambios al repositorio remoto.
	git push origin master
    
 # 2.6 IGNORAR ARCHIVOS (I)
 ## Crear en el repositorio local un fichero llamado privado.txt.
	touch privado.txt
    
 ## Crear en el repositorio local una carpeta llamada privada.
 	mkdir privada
 # 2.7 IGNORAR ARCHIVOS (II)
## Realizar los cambios oportunos para que tanto el archivo como la carpeta sean ignorados por 
git.
	echo "privado.txt" > .gitignore
	echo "/privada" > .gitignore
	git add .
    git commit -m "añadido fichero .gitignore"
    
    
# 2.8 AÑADIR FICHERO 1.TXT
## Añadir fichero 1.txt al repositorio local.
	touch 1.txt
	git add .
	git commit -m "añadido 1.txt"
    
# 2.9 CREAR EL TAG V0.1
## Crear un tag v0.1.
	
	git tag v0.1
    
 # 2.10 SUBIR EL TAG V0.1
 
 ## Subir los cambios al repositorio remoto.
 	

	git push --tag origin master

# 2.13 CREAR UNA TABLA
## Crear una tabla de este estilo en el fichero README.md con la información de varios de tus 
compañeros de clase:

| NOMBRE | GITHUB |
| -- | -- |
| Miguel | https://github.com/miguelj93/campusciff.git |
| Rafa | https://github.com/RuFFuS4/campusciff.git |
| Miriam | https://github.com/MIRIAM-GIT/campusciff.git

# Avanzado


# 2.2 CREAR UNA RAMA V0.2
## Crear una rama v0.2.
	git branch v0.2
## Posiciona tu carpeta de trabajo en esta rama.
	git checkout v0.2

# 2.3 AÑADIR FICHERO 2.TXT
## Añadir un fichero 2.txt en la rama v0.2.
	touch 2.txt
	git add .
	git commit -m "añadido 2.txt"
    
 # 2.4 CREAR RAMA REMOTA V0.2
## Subir los cambios al reposiorio remoto.
	git push origin v0.2
    
  # 2.5 MERGE DIRECTO
  ## Posicionarse en la rama master.
  	git checkout master
    
## Hacer un merge de la rama v0.2 en la rama master.
	git merge v0.2 -m "merge v0.2 sin conflictos"
 # 2.6 MERGE CON CONFLICTO (I)
## En la rama master poner Hola en el fichero 1.txt y hacer commit.
	git checkout master
	echo "Hola" >> 1.txt
	git add .
	git commit -m "hola en 1.txt"


# 2.7 MERGE CON CONFLICTO (II)
## Posicionarse en la rama v0.2 y poner Adios en el fichero "1.txt" y hacer commit.
	git checkout v0.2
	echo "Adios" >> 1.txt
	git add .
	git commit -m "adios en 1.txt"

# 2.8 MERGE CON CONFLICTO (III)
## Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2
	git checkout master
	git merge v0.2
	nano 1.txt
	git add .
	git commit -m "arreglado merge en 1.txt"
    
# 2.9 LISTADO DE RAMAS
## Listar las ramas con merge y las ramas sin merge.
	git branch --merged
	git branch --no-merged

# 2.10 ARREGLAR CONFLICTO
 ## Arreglar el conflicto anterior y hacer un commit.
	nano 1.txt
	git add .
	git commit -m "arreglado merge en 1.txt"

# 2.11 BORRAR RAMA
## Crear un tag v0.2
	git tag v0.2
    
## Borrar la rama v0.2
	git branch -d v0.2
    
# 2.12 LISTADO DE CAMBIOS
 ## Listar los distintos commits con sus ramas y sus tags.
	git config --global alias.list 'log --oneline --decorate --graph --all'
	git list
