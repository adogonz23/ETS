<div aling= "center">

 BY : Adonay González Gutiérrez

# Gestion avanzada de git

## indice
- [Ejercicio 1](#item1)
- [Ejercicio 2](#item2)
- [Ejercicio 3](#item3)
- [Ejercicio 4](#item4)
- [Ejercicio 5](#item5)
- [Ejercicio 6](#item6)
- [Ejercicio 7](#item7)


## Clonando el repositorio del profe
```code
am@a108pc01:~$ cd Documentos/
dam@a108pc01:~/Documentos$  git clone https://github.com/jpexposito/libro.git
Clonando en 'libro'...
remote: Enumerating objects: 21, done.
remote: Counting objects: 100% (21/21), done.
remote: Compressing objects: 100% (12/12), done.
remote: Total 21 (delta 2), reused 13 (delta 0), pack-reused 0
Recibiendo objetos: 100% (21/21), listo.
Resolviendo deltas: 100% (2/2), listo.
dam@a108pc01:~/Documentos$ cd libro/

```

<a name="item1"></a>

## Ejercicio 1 

- Mostrar el historial de cambios del repositorio.
- Crear la carpeta capítulos y crear dentro de ella el fichero capitulo1.txt con el siguiente texto: "Git es un sistema de control de versiones ideado por Linus Torvalds."

<details>
<summary>Comandos</summary>
  - git show 
  - mkdir capitulos 
  - cat > capitulos/capitulo.txt
</details>
- Salida
  
```code
dam@a108pc01:~/Documentos/libro$ git show
commit 1016a8a4e53ee1167750094aaac7d2018063a264 (HEAD -> main, origin/main, origin/HEAD)
Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
Date:   Wed Sep 27 15:50:15 2023 +0100

    se añade la segunda carpeta

diff --git a/prueba2/file2.clean b/prueba2/file2.clean
new file mode 100644
index 0000000..e69de29
dam@a108pc01:~/Documentos/libro$ mkdir capitulos
dam@a108pc01:~/Documentos/libro$ cat > capitulos/capitulo.txt
Git es un sistema de control de versiones ideado por Linus Torvalds.dam@a108pc01:~/Documentos/libro$ 
```

  - Añadir los cambios a la zona de intercambio temporal.
  - Hacer un commit de los cambios con el mensaje Añadido capítulo 1.
  - Volver a mostrar el historial de cambios del repositorio.
<details>
<summary>Comandos</summary>
  - git add  
  - git commit -m git show
</details>

- Salida:
  
```code
~/Documentos/libro$ git add .
dam@a108pc01:~/Documentos/libro$ git commit -m"aguacate"
[main e117b9b] aguacate
 1 file changed, 1 insertion(+)
 create mode 100644 capitulos/capitulo.txt
dam@a108pc01:~/Documentos/libro$ git show
commit e117b9b4099b39a3dbe5f18ba5ccc10ef22bb79d (HEAD -> main)
Author: adogonz23 <adogonzalez75@gmail.com>
Date:   Wed Oct 4 16:10:27 2023 +0100

    aguacate

diff --git a/capitulos/capitulo.txt b/capitulos/capitulo.txt
new file mode 100644
index 0000000..f4068a7
--- /dev/null
+++ b/capitulos/capitulo.txt
@@ -0,0 +1 @@
Git es un sistema de control de versiones ideado por Linus Torvalds.
\ No newline at end of file

```
<a name="item2"></a>

 ## Ejercicio 2

- Crear el fichero capitulo2.txt en la carpeta capítulos con el siguiente texto: "El flujo de trabajo básico con Git consiste en: 1- Hacer cambios en el repositorio. 2- Añadir los cambios a la zona de intercambio temporal. 3- Hacer un commit de los cambios".
  - __Comandos:__ 
    - cat > capitulos/capitulo2.txt
<detail>
  ```code
    dam@a108pc01:~/Documentos/libro$ cat > capitulos/capitulo2
  El flujo de trabajo básico con Git consiste en: 1- Hacer cambios en el repositorio. 2- Añadir los cambios a la zona de intercambio temporal. 3- Hacer un commit de los cambios
  ```
</detail>

- Añadir los cambios a la zona de intercambio temporal.
- Hacer un commit de los cambios con el mensaje Añadido capítulo 2.
- Mostrar las diferencias entre la última versión y dos versiones anteriores.

- __Comandos__:
  - git add  
  - git commit-m, 
  - git diff HEAD~2..HEAD 
- Salida
  ```code
  dam@a108pc01:~/Documentos/libro$ git add .
  dam@a108pc01:~/Documentos/libro$ git commit -m"Aguacates2"
  [main f05e0fb] Aguacates2
  1 file changed, 1 insertion(+)
  create mode 100644 capitulos/capitulo2
  dam@a108pc01:~/Documentos/libro$ git diff HEAD~2..HEAD
  diff --git a/capitulos/capitulo.txt b/capitulos/capitulo.txt
  new file mode 100644
  index 0000000..f4068a7
  --- /dev/null
  +++ b/capitulos/capitulo.txt
  @@ -0,0 +1 @@
  +Git es un sistema de control de versiones ideado por Linus Torvalds.
  \ No newline at end of file
  diff --git a/capitulos/capitulo2 b/capitulos/capitulo2
  new file mode 100644
  index 0000000..e13c7d8
  --- /dev/null
  +++ b/capitulos/capitulo2
  @@ -0,0 +1 @@
  +El flujo de trabajo básico con Git consiste en: 1- Hacer cambios en el repositorio. 2- Añadir los cambios a la zona de intercambio temporal. 3- Hacer un commit de los cambios
  \ No newline at end of file

  ```
 <a name="item3"></a>

## Ejercicio 3


- Crear el fichero capitulo3.txt en la carpeta capítulos con el siguiente texto.

- Añadir los cambios a la zona de intercambio temporal.
- Hacer un commit de los cambios con el mensaje Añadido capítulo 3.
- Mostrar las diferencias entre la primera y la última versión del repositorio.

- __Comandos__: 
  - cat > capitulos/capitulo3.txt

- Salida 
```code
adonay@adonay-VirtualBox:~/Documentos/libro$ cat > capitulos/capitulo3.txt
Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.

donay@adonay-VirtualBox:~/Documentos/libro$ git add .
adonay@adonay-VirtualBox:~/Documentos/libro$ git commit -m 
error: switch `m' requiere un valor
adonay@adonay-VirtualBox:~/Documentos/libro$ ""git commit -m "aguacate3"
[main 5175fea] aguacate3
 1 file changed, 2 insertions(+)
 create mode 100644 capitulos/capitulo3.txt
adonay@adonay-VirtualBox:~/Documentos/libro$
```
- __Comandos__:
  - git diff HEAD~3..HEAD
```code
adonay@adonay-VirtualBox:~/Documentos/libro$ git diff HEAD~3..HEAD
diff --git a/capitulos/capitulo1.txt b/capitulos/capitulo1.txt
new file mode 100644
index 0000000..f4068a7
--- /dev/null
+++ b/capitulos/capitulo1.txt
@@ -0,0 +1 @@
+Git es un sistema de control de versiones ideado por Linus Torvalds.
\ No newline at end of file
diff --git a/capitulos/capitulo2.txt b/capitulos/capitulo2.txt
new file mode 100644
index 0000000..e5ec949
--- /dev/null
+++ b/capitulos/capitulo2.txt
@@ -0,0 +1,5 @@
+ cat > capitulos/capitulo2.txt
+ El flujo de trabajo básico con Git consiste en:
+ 1- Hacer cambios en el repositorio.
+ 2- Añadir los cambios a la zona de intercambio temporal.
+ 3- Hacer un commit de los cambios.
\ No newline at end of file
diff --git a/capitulos/capitulo3.txt b/capitulos/capitulo3.txt
new file mode 100644
index 0000000..93d1665
:
```
<a name="item4"></a>

## Ejercicio 4


- Crea el fichero índice.txt la siguiente línea:
  - Indice de los cápitulos, con conceptos avanzados de git

- Añadir los cambios a la zona de intercambio temporal.
- Hacer un commit de los cambios con el mensaje "Indice de los cápitulos, con conceptos avanzados de git.
- Mostrar quién ha hecho cambios sobre el fichero indice.txt.
- __Comandos__: 
  - git cat >
  - git add .
  - git commit -m ""
  - git ammotate indice.txt
- Salida
```code
  adonay@adonay-VirtualBox:~/Documentos/libro$ cat > indice.txt
  Indice de los cápitulos, con conceptos avanzados de gitadonay@adonay-VirtualBox:~/Documentos/libro$ git add .
  adonay@adonay-VirtualBox:~/Documentos/libro$ git commit -m" se cre al indice de aguacate"
 [main 6ee938b]  se cre al indice de aguacate
 1 file changed, 1 insertion(+)
 create mode 100644 indice.txt
 adonay@adonay-VirtualBox:~/Documentos/libro$ git annotate indice.txt
 6ee938b2        ( adogonz23     2023-10-06 09:59:39 +0100       1)Indice de los cápitulos, con conceptos avanzados de git
```
<a name="item5"></a>

## Ejercicio 5

- Crear una nueva rama bibliografía y mostrar las ramas del repositorio.
- __Comandos:__
  - git branch bibliografia
  - git branch -av
- Salida:
```code
adonay@adonay-VirtualBox:~/Documentos/libro$ git branch bibliografia
adonay@adonay-VirtualBox:~/Documentos/libro$  git branch -av
  bibliografia        6ee938b  se cre al indice de aguacate
* main                6ee938b [adelante 4]  se cre al indice de aguacate
  remotes/origin/1    3ea9800 se crea la carpeta img #1
  remotes/origin/HEAD -> origin/main
  remotes/origin/main 1016a8a se añade la segunda carpeta
```
<a name="item6"></a>

## Ejercicio 6


- Crear el fichero capitulos/capitulo4.txt y añadir el texto siguiente:

  - En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.

- Añadir los cambios a la zona de intercambio temporal.
- Hacer un commit con el mensaje “Añadido capítulo 4.”
- Mostrar la historia del repositorio incluyendo todas las ramas.

- __Comandos__:
  - cat > capitulos/capitulo4.txt
En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.
  - git add .
  - git commit -m "Añadido capítulo 4."
  - git log --graph --all --oneline

- Salida:
```code
adonay@adonay-VirtualBox:~/Documentos/libro$ cat > capitulos/capitulo4.txt
En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.adonay@adonay-VirtualBox:~/Documentos/libro$  git add .
adonay@adonay-VirtualBox:~/Documentos/libro$ git commit - m "añadiendo aguactes4"
error: ruta especificada '-' no concordó con ningún archivo conocido por git
error: ruta especificada 'm' no concordó con ningún archivo conocido por git
error: ruta especificada 'añadiendo aguactes4' no concordó con ningún archivo conocido por git
adonay@adonay-VirtualBox:~/Documentos/libro$ git commit -m"añadiendo agucates4"
[main 516ecaf] añadiendo agucates4
 1 file changed, 1 insertion(+)
 create mode 100644 capitulos/capitulo4.txt
 adonay@adonay-VirtualBox:~/Documentos/libro$ git log --graph --all --oneline
* 516ecaf (HEAD -> main) añadiendo agucates4
* 6ee938b (bibliografia)  se cre al indice de aguacate
* 5175fea aguacate3
* 510960b aguacate 2
* d36206e a
* 1016a8a (origin/main, origin/HEAD) se añade la segunda carpeta
* 3f26704 mensaje
* 8a81c55 Se añade un título
* fbe91b2 closed #1
* 3ea9800 (origin/1) se crea la carpeta img #1
* 4dcb74b Initial commit

```
<a name="item7"></a>

## Ejercicio 7


- Cambiar a la rama bibliografía.
- Crear el fichero bibliografia.txt y añadir la siguiente referencia:

  - Chacon, S. and Straub, B. Pro Git. Apress.

- Añadir los cambios a la zona de intercambio temporal.
- Hacer un commit con el mensaje “Añadida primera referencia bibliográfica.”
- Mostrar la historia del repositorio incluyendo todas las ramas.

-__Comandos__:
   - git checkout bibliografia
  - cat > bibliografia.txt
    - Chacon, S. and Straub, B. Pro Git. Apress.
  - git add .
  - git commit -m "Añadida primera referencia bibliográfica."
  - git log --graph --all --oneline.

- __Salida__:
```code
  adonay@adonay-VirtualBox:~/Documentos/libro$ git checkout bibliografia
  Cambiado a rama 'bibliografia'
  adonay@adonay-VirtualBox:~/Documentos/libro$ cat > bibliografia.txt
  Chacon, S. and Straub, B. Pro Git. Apress.
  adonay@adonay-VirtualBox:~/Documentos/libro$ git add . 
  adonay@adonay-VirtualBox:~/Documentos/libro$ git commit -m"anñadimos bibliografia con agucates"
  [bibliografia fd32f7f] anñadimos bibliografia con agucates
  1 file changed, 1 insertion(+)
  create mode 100644 bibliografia.txt
  adonay@adonay-VirtualBox:~/Documentos/libro$ git log --graph --all --oneline
* fd32f7f (HEAD -> bibliografia) anñadimos bibliografia con agucates
| * 516ecaf (main) añadiendo agucates4
|/  
* 6ee938b  se cre al indice de aguacate
* 5175fea aguacate3
* 510960b aguacate 2
* d36206e a
* 1016a8a (origin/main, origin/HEAD) se añade la segunda carpeta
* 3f26704 mensaje
* 8a81c55 Se añade un título
* fbe91b2 closed #1
* 3ea9800 (origin/1) se crea la carpeta img #1
* 4dcb74b Initial commit


``` 

</div>

