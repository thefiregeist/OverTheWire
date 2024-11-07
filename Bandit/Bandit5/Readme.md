# Bandit Level 4 -> Level 5 - Solución

En este nivel de **Bandit** en [OverTheWire](https://overthewire.org/wargames/bandit/bandit4.html), el objetivo es encontrar la contraseña para el siguiente nivel. La contraseña está almacenada en un archivo oculto dentro del directorio `inhere`.

## Objetivo del Nivel
Descubrir la contraseña para el siguiente nivel dentro de un archivo legible por humanos en el directorio `inhere`. La contraseña se encuentra en el único archivo que puede leerse sin problemas.

Tip: Si experimentas problemas con la terminal, puedes intentar usar el comando `reset` para restaurarla.

- **Host**: `bandit.labs.overthewire.org`
- **Puerto**: `2220`
- **Usuario**: `bandit4
- **Contraseña**: La obtenida en el nivel [anterior](/Bandit4/Readme.md). Ver en Raw si es necesario. <!-- 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ -->

---

## Paso 1: Conectarse al Servidor
Primero, inicia sesión en el servidor con las credenciales del nivel anterior:

```
ssh bandit4@bandit.labs.overthewire.org -p 2220
```

---

## Paso 2: Listar ficheros y directorios
Utiliza el comando `ls` para comprobar que hay en el directorio actual:

```
ls
```

---

## Paso 3: Navegar al Directorio `inhere`
Dirígete al directorio `inhere`:

```
cd inhere
```

---

## Paso 4: Listar Archivos
Mostramos los ficheros con `ls`

```
ls
```

Salida:

```
-file00 -file01 -file02 -file03 -file04 -file05 -file06 -file07 -file08 -file09
```

---

## Paso 5: Buscar el archivo legible por humanos
Podriamos ir fichero a fichero utilizando cat para comprobar su contenido, pero vamos a utilizar un comando para comprobar cada tipo de fichero, ya que lo que buscamos es un fichero de texto plano. Para ello, utilizaremos `file`.

Recuerda, que como los nombres de los fichero empiezan por `-`, debemos utilizar comillas y escaparlo.
```
file './-file'*
```

Con este comando estamos indicando que queremos conocer el tipo de fichero de todos aquellos ficheros que comiencen por `-file`, el `*` del final indica que cualquier caracter o caracteres a continuacion.

Salida:

```
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
```

Esto nos indica que el fichero de texto plano que buscamos es el `-file07`.

---

## Paso 6: Leer el fichero
Utilizamos cat sobre el fichero:

```
cat './-file07'
```

![image](https://github.com/user-attachments/assets/4023fad4-4185-4da9-9b80-ae718b36b900)


---

## Paso 6: Anotar la Contraseña
Copia la contraseña que aparece y guárdala para el próximo nivel.

---

## Resumen de los Comandos Utilizados
* `ssh`: Conectarse a un servidor remoto mediante SSH.
* `cat`: Mostrar el contenido de un archivo.
* `ls`: Listar los archivos en un directorio.
* `file [filename]`: Mostrar el tipo de fichero.
---

¡Felicidades, has completado Bandit Level 5! Para continuar, ve a la página del siguiente nivel ([Level 5 -> Level 6](/Bandit6/Readme.md)).
