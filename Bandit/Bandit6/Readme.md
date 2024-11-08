# Bandit Level 5 -> Level 6 - Solución

En este nivel de **Bandit** en [OverTheWire](https://overthewire.org/wargames/bandit/bandit5.html), el objetivo es encontrar la contraseña para el siguiente nivel. La contraseña está almacenada en un archivo oculto dentro del directorio `inhere`.

## Objetivo del Nivel
Descubrir la contraseña del siguiente nivel, que se encuentra en algún archivo dentro del directorio `inhere`. Este archivo tiene las siguientes características:

* Legible por humanos: el contenido del archivo debe estar en un formato que pueda leerse (no es binario).
* Tamaño exacto de 1033 bytes: el archivo mide exactamente 1033 bytes.
* No ejecutable: el archivo no tiene permisos de ejecución.

- **Host**: `bandit.labs.overthewire.org`
- **Puerto**: `2220`
- **Usuario**: `bandit5
- **Contraseña**: La obtenida en el nivel [anterior](/Bandit5/Readme.md). Ver en Raw si es necesario. <!-- 4oQYVPkxZ00E005pTW81FB8j8lxXGUQw -->

---

## Paso 1: Conectarse al Servidor
Primero, inicia sesión en el servidor con las credenciales del nivel anterior:

```
ssh bandit5@bandit.labs.overthewire.org -p 2220
```

---

## Paso 2: Listar ficheros y directorios
Utiliza el comando `ls` para comprobar que hay en el directorio actual:

```
ls
```

---

## Paso 3: Navegar al Directorio `inhere` y comprobar lo que hay dentro
Dirígete al directorio `inhere`:

```
cd inhere
ls -l
```

---

## Paso 4: Buscar el Archivo con `find`
Dado que el directorio inhere contiene muchos archivos distribuidos en varios subdirectorios, y solo uno cumple con las condiciones exactas, el comando find nos ayudará a identificarlo rápidamente.

Para localizar el archivo, ejecuta el siguiente comando:

```
find . -type f -size 1033c ! -executable -exec file {} +
```

## Explicación del Comando
Este comando `find` busca recursivamente en el directorio `inhere` y devuelve solo el archivo que cumple con las condiciones del reto. Vamos a desglosar cada parte:

* `.`: indica que el comando debe empezar a buscar en el directorio actual (`inhere` en este caso).
* `-type f`: restringe la búsqueda a archivos, ignorando directorios.
* `-size 1033c`: selecciona archivos de exactamente 1033 bytes (`c` indica "bytes exactos").
* `! -executable`: excluye archivos que tienen permisos de ejecución.
* `-exec file {} +`: ejecuta el comando `file` en cada archivo encontrado para verificar su tipo y confirmar que es legible por humanos.

Este comando devuelve la ruta y el tipo de archivo que cumple con las condiciones.

Salida:

```
./maybehere07/.file2: ASCII text, with very long lines (1000)
```

---

## Paso 5: Leer el fichero
Utilizamos cat sobre el fichero:

```
cat './maybehere07/.file2'
```

![image](https://github.com/user-attachments/assets/8a11f84f-f904-48b2-8d17-1932d5a2d546)

---

## Paso 6: Anotar la Contraseña
Copia la contraseña que aparece y guárdala para el próximo nivel.

---

## Resumen de los Comandos Utilizados
* `ssh`: Conectarse a un servidor remoto mediante SSH.
* `cat`: Mostrar el contenido de un archivo.
* `ls`: Listar los archivos en un directorio.
* `find`: Buscar archivos en un directorio.
* `file [filename]`: Mostrar el tipo de fichero.
---

¡Felicidades, has completado Bandit Level 6! Para continuar, ve a la página del siguiente nivel ([Level 6 -> Level 7](/Bandit7/Readme.md)).
