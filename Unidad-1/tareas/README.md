<div aling= "center">

# Gestion basica de git

## indice

[tareas de Configuracion](Tarea de configuracion)

## Tarea de configuracion

Configurar Git definiendo el nombre del usuario, el correo electrónico y activar el coloreado de la salida. Mostrar la configuración final.

```code 
  git config --global user.name "Your-Full-Name"
  git config --global user.email "your-email-address"
  git config --global color.ui auto
  git config --list
```
## Tarea: Creación de un repositorio
Crear un repositorio nuevo con el nombre dpl y mostrar su contenido.
```code
 mkdir dpl
 cd dpl
```
- Salida:
```
 dam@a108pc01:~/Documentos$ mkdir dpl
 dam@a108pc01:~/Documentos$ cd dpl
```
```code
- git init
- ls -la
```
- Salida:
```
 dam@a108pc01:~/Documentos/dpl$ ls -la
 total 8
 drwxrwxr-x 2 dam dam 4096 oct  3 14:57 .
 drwxr-xr-x 8 dam dam 4096 oct  3 14:57 ..
 dam@a108pc01:~/Documentos/dpl$ git init
 ayuda: Usando 'master' como el nombre de la rama inicial. Este nombre de rama predeterminado
 ayuda: está sujeto a cambios. Para configurar el nombre de la rama inicial - para usar en todos
 ayuda: de sus nuevos repositorios, reprimiendo esta advertencia, llama a:
ayuda: 
 ayuda: 	git config --global init.defaultBranch <nombre>
ayuda: 
 ayuda: Los nombres comúnmente elegidos en lugar de 'master' son 'main', 'trunk' y
 ayuda: 'development'. Se puede cambiar el nombre de la rama recién creada mediante este comando:
ayuda: 
 ayuda: 	git branch -m <nombre>
 Inicializado repositorio Git vacío en /home/dam/Documentos/dpl/.git/
```
## Tarea: Comprobar el estado del repositorio
- Comprobar el estado del repositorio.

- Crear un fichero indice.txt con el siguiente contenido:

  - Capítulo 1: Instalación de Git por el alumno XXX (donde XXX es el nombre del alumno).
  - Capítulo 2: Flujo de trabajo básico.


- Comprobar de nuevo el estado del repositorio.

- Añadir el fichero a la zona de intercambio temporal.

- Volver a comprobar una vez más el estado del repositorio.
```code
git status
```
- Salida:
```code
 dam@a108pc01:~/Documentos/dpl$  git status
En la rama master

No hay commits todavía no hay nada para confirmar (crea/copia archivos y usa "git add" para hacerles seguimiento)
```
```code
 cat > indice.txt
 Capítulo 1: Instalación de Git por el alumno XXX
 Capítulo 2: Flujo de trabajo básico
```
- Salida:
```code
dam@a108pc01:~/Documentos/dpl$ cat > indice.txt
Capitulo 1: Instalacion de Git por el Alumno Adonay
Capitulo 2: Flujo de trabajo basico 
```
```code
git status
git add indice.txt
git status
```
- Salida:
```code
dam@a108pc01:~/Documentos/dpl$ git status
En la rama master

No hay commits todavía

Archivos sin seguimiento:
  (usa "git add <archivo>..." para incluirlo a lo que se será confirmado)
	indice.txt

no hay nada agregado al commit pero hay archivos sin seguimiento presentes (usa "git add" para hacerles seguimiento)
dam@a108pc01:~/Documentos/dpl$ git add indice.txt
dam@a108pc01:~/Documentos/dpl$ git status
En la rama master

No hay commits todavía

Cambios a ser confirmados:
  (usa "git rm --cached <archivo>..." para sacar del área de stage)
	nuevos archivos: indice.txt
```
## Tarea: Realizando Commit´s

Realizar un commit de los últimos cambios con el mensaje Añadido índice de la asignatura DPL. y ver el estado del repositorio.
```code
git commit -m "Añadido índice de la asignatura DPL."
git status
```
- Salida:
```code
dam@a108pc01:~/Documentos/dpl$ git commit -m "Añadido índice de la asignatura DPL."
[master (commit-raíz) 5bad5e0] Añadido índice de la asignatura DPL.
 1 file changed, 2 insertions(+)
 create mode 100644 indice.txt
dam@a108pc01:~/Documentos/dpl$ git status
En la rama master
nada para hacer commit, el árbol de trabajo está limpio
```
## Tarea: Modificación de ficheros

- Cambiar el fichero indice.txt para que contenga lo siguiente:
  - Capítulo 1: Instalación de Git por el alumno XXX (donde XXX es el nombre del alumno)
  - Capítulo 2: Flujo de trabajo básico
  - Capítulo 3: Gestión de ramas
  - Capítulo 4: Repositorios remotos
- Mostrar los cambios con respecto a la última versión guardada en el repositorio.
- Hacer un commit de los cambios con el mensaje Añadido los capitulos 3 y 4.
```code
cat > indice.txt
Capítulo 1: Instalación de Git por el alumno XXX _(donde XXX es el nombre del alumno)_
Capítulo 2: Flujo de trabajo básico
Capítulo 3: Gestión de ramas
Capítulo 4: Repositorios remotos
Ctrl+D
git diff
git add indice.txt
git commit -m "Añadido los capitulos 3"
```
- Salida:
```code
dam@a108pc01:~/Documentos/dpl$ cat >indice.txt
Capítulo 1: Instalación de Git por el alumno Adonay _(donde Adonay es el nombre del alumno)_
Capítulo 2: Flujo de trabajo básico
Capítulo 3: Gestión de ramas
                                            

dam@a108pc01:~/Documentos/dpl$ git diff
diff --git a/indice.txt b/indice.txt
index ff4210e..b364195 100644
--- a/indice.txt
+++ b/indice.txt
@@ -1,2 +1,5 @@
-Capitulo 1: Instalacion de Git por el Alumno Adonay
-Capitulo 2: Flujo de trabajo basico
+Capítulo 1: Instalación de Git por el alumno Adonay_(donde Adonay es el nombre del alumno)_
+Capítulo 2: Flujo de trabajo básico
+Capítulo 3: Gestión de ramas
+
+
dam@a108pc01:~/Documentos/dpl$ git add indice.txt
dam@a108pc01:~/Documentos/dpl$ git commit -m "Añadido los capitulos 3"
[master d1c3c2d] Añadido los capitulos 3
 1 file changed, 5 insertions(+), 2 deletions(-)
```
## Tarea: Historial

- Mostrar los cambios de la última versión del repositorio con respecto a la anterior.
- Cambiar el mensaje del último commit por Añadido el capitulo sobre gestión de ramas al índice.
- Volver a mostrar los últimos cambios del repositorio.
```code
git show
git commit --amend -m "Añadido el capitulo sobre gestión de ramas al índice."
git show
```
- Salida:
```code
dam@a108pc01:~/Documentos/dpl$ git show
commit d1c3c2dbb0a82b74ba0ac268adc8cee773a3a962 (HEAD -> master)
Author: adogonz23 <adogonzalez75@gmail.com>
Date:   Tue Oct 3 16:15:22 2023 +0100

    Añadido los capitulos 3

diff --git a/indice.txt b/indice.txt
index ff4210e..b364195 100644
--- a/indice.txt
+++ b/indice.txt
@@ -1,2 +1,5 @@
-Capitulo 1: Instalacion de Git por el Alumno Adonay
-Capitulo 2: Flujo de trabajo basico
+Capítulo 1: Instalación de Git por el alumno Adonay_(donde Adonay es el nombre del alumno)_
+Capítulo 2: Flujo de trabajo básico
+Capítulo 3: Gestión de ramas
+
+
dam@a108pc01:~/Documentos/dpl$ git commit --amend -m "Añadido el capitulo sobre gestión de ramas al índice."
[master f4d7d70] Añadido el capitulo sobre gestión de ramas al índice.
 Date: Tue Oct 3 16:15:22 2023 +0100
 1 file changed, 5 insertions(+), 2 deletions(-)

dam@a108pc01:~/Documentos/dpl$ git show
commit f4d7d70ad1dd6e56c0089488f76a01f920db7380 (HEAD -> master)
Author: adogonz23 <adogonzalez75@gmail.com>
Date:   Tue Oct 3 16:15:22 2023 +0100

    Añadido el capitulo sobre gestión de ramas al índice.

diff --git a/indice.txt b/indice.txt
index ff4210e..b364195 100644
--- a/indice.txt
+++ b/indice.txt
@@ -1,2 +1,5 @@
-Capitulo 1: Instalacion de Git por el Alumno Adonay
-Capitulo 2: Flujo de trabajo basico
+Capítulo 1: Instalación de Git por el alumno Adonay _(donde Adonay es el nombre del alumno)_
+Capítulo 2: Flujo de trabajo básico
+Capítulo 3: Gestión de ramas
+
+

```

</div>
