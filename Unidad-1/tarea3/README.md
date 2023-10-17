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

``







<a name="subirRama"></a>

<details>

<summary>Comandos</summary>

</details>


</div>

