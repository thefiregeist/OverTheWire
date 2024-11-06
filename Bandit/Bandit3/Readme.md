# Bandit Level 2 -> Level 3 - Solución

En este nivel de **Bandit** en [OverTheWire](https://overthewire.org/wargames/bandit/bandit3.html), el objetivo es encontrar la contraseña para el siguiente nivel almacenada en un archivo llamado `spaces in this filename` en el directorio home. Una vez obtenida la contraseña, debes usarla para iniciar sesión en el nivel **bandit3** a través de **SSH**.

## Objetivo del Nivel
La meta de este nivel es localizar el archivo `spaces in this filename` que contiene la contraseña para acceder al siguiente nivel. Los datos necesarios para la conexión son los siguientes:

- **Host**: `bandit.labs.overthewire.org`
- **Puerto**: `2220`
- **Usuario**: `bandit2`
- **Contraseña**: La obtenida en el nivel [anterior](/Bandit2/Readme.md). Ver en Raw si es necesario. <!-- 263JGJPfgU6LtdEvgfWU1XP5yac29mFx -->

---

## Paso 1: Listar los Archivos en el Directorio Home
Una vez que inicies sesión en **bandit2** con la contraseña del nivel anterior, utiliza el comando `ls` para listar los archivos en el directorio home y buscar el archivo con el nombre `spaces in this filename`.

```
ls
```

Deberías ver una lista de archivos, entre ellos el archivo `-`.

## Paso 2: Leer el Contenido del Archivo
El nombre del archivo contiene espacios, por lo que para leer su contenido, debes utilizar comillas alrededor del nombre del archivo con el comando `cat`.

```
cat 'spaces in this filename'
```

El archivo `spaces in this filename` debe contener la contraseña que necesitas para el siguiente nivel.

![image](https://github.com/user-attachments/assets/5322bb94-faab-4472-8fb3-aadc852f284b)

## Paso 3: Conectarse al Siguiente Nivel
Una vez que tengas la contraseña, puedes usar el comando `ssh` para iniciar sesión en el siguiente nivel **bandit3**:

```
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

Introduce la contraseña que encontraste en el archivo `spaces in this filename` para completar la conexión.

---

## Resumen
* Conéctate a `bandit2` usando la contraseña obtenida en el nivel anterior.
* Usa `ls` para listar los archivos en el directorio home.
* Lee el contenido del archivo `spaces in this filename` con `cat 'spaces in this filename'`.
* **Conéctate** al nivel siguiente con la nueva contraseña.

---

¡Felicidades, has completado Bandit Level 3! Para continuar, ve a la página del siguiente nivel ([Level 3 -> Level 4](/Bandit4/Readme.md)).
