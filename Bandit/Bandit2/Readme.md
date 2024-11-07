# Bandit Level 1 -> Level 2 - Solución

En este nivel de **Bandit** en [OverTheWire](https://overthewire.org/wargames/bandit/bandit2.html), el objetivo es encontrar la contraseña para el siguiente nivel almacenada en un archivo llamado `-` en el directorio home. Una vez obtenida la contraseña, debes usarla para iniciar sesión en el nivel **bandit2** a través de **SSH**.

## Objetivo del Nivel
Descubrir la contraseña para el siguiente nivel, almacenada en un archivo llamado `-`, ubicado en el directorio home.

- **Host**: `bandit.labs.overthewire.org`
- **Puerto**: `2220`
- **Usuario**: `bandit1`
- **Contraseña**: La obtenida en el nivel [anterior](/Bandit1/Readme.md). Ver en Raw si es necesario. <!-- ZjLjTmM6FvvyRnrb2rfNW0Z0Ta6ip5If -->

---

## Paso 1: Conectarse al Servidor
Primero, inicia sesión en el servidor con las credenciales del nivel anterior:

```
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

---

## Paso 2: Listar Archivos en el Directorio Home
Una vez que inicies sesión en **bandit1** con la contraseña del nivel anterior, puedes utilizar el comando `ls` para listar los archivos en el directorio home y buscar el archivo `-`.

```
ls
```

Deberías ver una lista de archivos, entre ellos el archivo `-`.

---

## Paso 3: Leer el Contenido del Archivo
El archivo tiene un nombre especial, así que para leer su contenido, debes usar el comando `cat` junto con el nombre del archivo entre comillas. Esto evitará que el sistema interprete el `-` como una opción.

```
cat './-'
```

El archivo `-` debe contener la contraseña que necesitas para el siguiente nivel.

![image](https://github.com/user-attachments/assets/fcfd7fec-d7c9-42ba-b011-4b369bedcf3a)

---

## Paso 4: Anotar la Contraseña
Copia la contraseña que aparece y guárdala para el próximo nivel.

---

## Resumen de los Comandos Utilizados
* `ssh`: Conectarse a un servidor remoto mediante SSH.
* `cat`: Mostrar el contenido de un archivo.
* `ls`: Listar los archivos en un directorio.

---

¡Felicidades, has completado Bandit Level 2! Para continuar, ve a la página del siguiente nivel ([Level 2 -> Level 3](/Bandit3/Readme.md)).
