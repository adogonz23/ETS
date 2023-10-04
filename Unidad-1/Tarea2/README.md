<div aling= "center">

# Gestion avanzada de git

## indice
- [Ejercicio 1](#item1)
- [Ejercicio 2](#item2)
- [Ejercicio 3](#item3)
- [Ejercicio 4](#item4)
- [Ejercicio 5](#item5)
- [Ejercicio 6](#item6)


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
  - __comandos:__"git show" "mkdir capitulos" "cat > capitulos/capitulo.txt"
  
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
  - __Comandos:__ "git add ." "git commit -m" "git show"

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
  - __Comandos:__ "cat > capitulos/capitulo2.txt"
<detail>
  ```code
    dam@a108pc01:~/Documentos/libro$ cat > capitulos/capitulo2
  El flujo de trabajo básico con Git consiste en: 1- Hacer cambios en el repositorio. 2- Añadir los cambios a la zona de intercambio temporal. 3- Hacer un commit de los cambios
  ```
</detail>

- Añadir los cambios a la zona de intercambio temporal.
- Hacer un commit de los cambios con el mensaje Añadido capítulo 2.
- Mostrar las diferencias entre la última versión y dos versiones anteriores.
  - __Comandos__:"git add .", "git commit-m", "git diff HEAD~2..HEAD "
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




</div>

