<div aling= "center">

 BY : Adonay González Gutiérrez

# Manipulacion avanzada de git, github y markdown

## indice
- [Crear una rama v0.2](#crearRama)
- [Añadir fichero 2.txt](#añadirFichero2)
- [Subir rama remota v0.2](#subirRama)
- [Merge directo](#mergeDirecto)
- [Merge con conflicto](#mergeConflicto)
- [Listado de ramas](#ListadoRamas)
- [Arreglar conflicto](#arreglarConflicto)
- [Borrar rama](#borrarRamas)
- [Listado de cambios](#listadoCambios)



<a name="crearRama"></a>

## Crear una rama v0.2

Crear una rama v0.2. <br>
Posiciona tu carpeta de trabajo en esta rama.
<details>

<summary>Comandos</summary>

- git branch
- git checkout nombreRama
</details>

**Salida**:

```code
dam@a108pc01:~/Documentos/ETS$ git branch v0.2
dam@a108pc01:~/Documentos/ETS$ git checkout v0.2
Cambiado a rama 'v0.2'
```
<a name="añadirFichero2"></a>

## Añadir fichero

Añadir un fichero 2.txt en la rama v0.2.
<details>

<summary>Comandos</summary>

- touch 2.txt
- git add .
- git commit -m"agucate2"

</details>

**Salida**
```code
dam@a108pc01:~/Documentos/ETS$ touch 2.txt
dam@a108pc01:~/Documentos/ETS$ git add .
dam@a108pc01:~/Documentos/ETS$ git commit -m"archivo2"
[v0.2 c7f239b] archivo2
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 2.txt
```

<a name="subirRama"></a>

## Subir rama remota v0.2

Subir los cambios al reposiorio remoto.

<details>

<summary>Comandos</summary>

- git push origin v0.2

</details>


**Salida**
```code
dam@a108pc01:~/Documentos/ETS$ git push origin v0.2
Enumerando objetos: 4, listo.
Contando objetos: 100% (4/4), listo.
Compresión delta usando hasta 12 hilos
Comprimiendo objetos: 100% (2/2), listo.
Escribiendo objetos: 100% (3/3), 333 bytes | 333.00 KiB/s, listo.
Total 3 (delta 0), reusados 1 (delta 0), pack-reusados 0
remote: 
remote: Create a pull request for 'v0.2' on GitHub by visiting:
remote:      https://github.com/adogonz23/ETS/pull/new/v0.2
remote: 
To github.com:adogonz23/ETS.git
 * [new branch]      v0.2 -> v0.2

```
<a name="mergeDirecto"></a>

## Merge Directo

Posicionarse en la rama master. <br>
Hacer un merge de la rama v0.2 en la rama master.

<details>

<summary>Comandos</summary>

- git checkout master (main en mi caso)
- git merge v0.2 -m "merge v0.2 sin conflictos"

</details>

**Salida**:
```code
dam@a108pc01:~/Documentos/ETS$ git checkout main
M	Unidad-1/tarea3/README.md
Cambiado a rama 'main'
Tu rama está actualizada con 'origin/main'.
dam@a108pc01:~/Documentos/ETS$ git merge v0.2 -m"merge sin conflictos"
Actualizando 15e022c..c7f239b
Fast-forward (no commit created; -m option ignored)
 2.txt | 0
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 2.txt

```
<a name="mergeConflicto"></a>

## Merge con conflicto

<details>

<summary>Comandos</summary>

- git checkout main
- echo "hola" >> 2.txt
- git add .
- git commit -m"hola en 2.txt"

</details>

**Salida**:
```code
dam@a108pc01:~/Documentos/ETS$ git checkout main
M	Unidad-1/tarea3/README.md
Ya en 'main'
Tu rama está adelantada a 'origin/main' por 1 commit.
  (usa "git push" para publicar tus commits locales)
dam@a108pc01:~/Documentos/ETS$ echo "hola" >> 2.txt
dam@a108pc01:~/Documentos/ETS$ git add .
dam@a108pc01:~/Documentos/ETS$ git commit -m"hola en 2.txt"
[main af2abef] hola en 2.txt
 2 files changed, 114 insertions(+), 3 deletions(-)
```
Posicionarse en la rama v0.2 y poner Adios en el fichero "1.txt" y hacer commit. <br>

Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2

<details>

<summary>Comandos</summary>

- git checkout v0.2
- echo "Adios" >> 2.txt
- git add .
- git commit -m"añadiendo adios 2.txt"
- git checkout main
- git merge v0.2
- vim 2.txt
- git add .
- git commit -m"arregalndo merge en 1.txt"
</details>

**Salida**:
```code
dam@a108pc01:~/Documentos/ETS$ git checkout v0.2 
Cambiado a rama 'v0.2'
dam@a108pc01:~/Documentos/ETS$ echo "Adios" >> 2.txt
dam@a108pc01:~/Documentos/ETS$ git add .
dam@a108pc01:~/Documentos/ETS$ git commit -m"añadiendo adios 2.txt"
[v0.2 056de3e] añadiendo adios 2.txt
 1 file changed, 1 insertion(+)
 dam@a108pc01:~/Documentos/ETS$ git merge v0.2
Auto-fusionando 2.txt
CONFLICTO (contenido): Conflicto de fusión en 2.txt
Fusión automática falló; arregle los conflictos y luego realice un commit con el resultado.
dam@a108pc01:~/Documentos/ETS$ vim 2.txt
No se ha encontrado la orden «vim», pero se puede instalar con:
apt install vim         # version 2:8.2.3995-1ubuntu2.12, or
apt install vim-tiny    # version 2:8.2.3995-1ubuntu2.12
apt install vim-athena  # version 2:8.2.3995-1ubuntu2.12
apt install vim-gtk3    # version 2:8.2.3995-1ubuntu2.12
apt install vim-nox     # version 2:8.2.3995-1ubuntu2.12
apt install neovim      # version 0.6.1-3
Solicite al administrador que instale uno de ellos.
dam@a108pc01:~/Documentos/ETS$ git add .
dam@a108pc01:~/Documentos/ETS$  nano 2.txt
dam@a108pc01:~/Documentos/ETS$ nano 2.txt
dam@a108pc01:~/Documentos/ETS$ git add .
dam@a108pc01:~/Documentos/ETS$ git commit -m"arreglando merge"
[main 440e665] arreglando merge


```


<a name="borrarRama"></a>

## Borrar rama

crear un tag **V0.2** <br>
Borrar la rama **v0.2**

<details>

<summary>Comandos</summary>

- git tag v0.2
- git brach -d v0.2

</details>

**Salida**
```code
dam@a108pc01:~/Documentos/ETS$ git tag v0.2
dam@a108pc01:~/Documentos/ETS$ git tag -d v0.2
Etiqueta 'v0.2' eliminada (era 440e665)
```


</div>

