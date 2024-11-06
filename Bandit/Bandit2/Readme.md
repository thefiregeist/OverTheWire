# Bandit Level 1 -> Level 2 - Solución

En este nivel de **Bandit** en [OverTheWire](https://overthewire.org/wargames/bandit/bandit2.html), el objetivo es encontrar la contraseña para el siguiente nivel almacenada en un archivo llamado `-` en el directorio home. Una vez obtenida la contraseña, debes usarla para iniciar sesión en el nivel **bandit2** a través de **SSH**.

## Objetivo del Nivel
La meta de este nivel es localizar el archivo `-` que contiene la contraseña para acceder al siguiente nivel. Los datos necesarios para la conexión son los siguientes:

- **Host**: `bandit.labs.overthewire.org`
- **Puerto**: `2220`
- **Usuario**: `bandit1`
- **Contraseña**: La obtenida en el nivel [anterior](/Bandit1/Readme.md). Ver en Raw si es necesario. <!-- ZjLjTmM6FvvyRnrb2rfNW0Z0Ta6ip5If -->

---

## Paso 1: Listar Archivos en el Directorio Home
Una vez que inicies sesión en **bandit1** con la contraseña del nivel anterior, puedes utilizar el comando `ls` para listar los archivos en el directorio home y buscar el archivo `-`.

```
ls
```

Deberías ver una lista de archivos, entre ellos el archivo `-`.

## Paso 2: Leer el Contenido del Archivo
El archivo tiene un nombre especial, así que para leer su contenido, debes usar el comando `cat` junto con el nombre del archivo entre comillas. Esto evitará que el sistema interprete el `-` como una opción.

```
cat './-'
```

El archivo `-` debe contener la contraseña que necesitas para el siguiente nivel.

![image](https://github.com/user-attachments/assets/fcfd7fec-d7c9-42ba-b011-4b369bedcf3a)

## Paso 3: Conectarse al Siguiente Nivel
Una vez que tengas la contraseña, puedes usar el comando `ssh` para iniciar sesión en el siguiente nivel bandit2:

```
ssh bandit2@bandit.labs.overthewire.org -p 2220
```

Introduce la contraseña que encontraste en el archivo `-` para completar la conexión.

---

## Resumen
* Conéctate a bandit1 usando la contraseña obtenida del nivel anterior.
* Usa `ls` para listar los archivos en el directorio home.
* Lee el contenido del archivo `-` con `cat './-'`.
* Conéctate al nivel siguiente con la nueva contraseña.

---

¡Felicidades, has completado Bandit Level 2! Para continuar, ve a la página del siguiente nivel ([Level 2 -> Level 3](/Bandit3/Readme.md)).
