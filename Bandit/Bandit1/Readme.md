# Bandit Level 0 -> Level 1 - Solución

En este nivel de **Bandit** en [OverTheWire](https://overthewire.org/wargames/bandit/bandit1.html), el objetivo es encontrar la contraseña para el siguiente nivel almacenada en un archivo llamado `readme` en el directorio home. Una vez obtenida la contraseña, debes usarla para iniciar sesión en el nivel **bandit1** a través de **SSH**.

## Objetivo del Nivel
La meta de este nivel es localizar el archivo `readme` que contiene la contraseña para acceder al siguiente nivel. Los datos necesarios para la conexión son los siguientes:

- **Host**: `bandit.labs.overthewire.org`
- **Puerto**: `2220`
- **Usuario**: `bandit0`
- **Contraseña**: `bandit0`

---

## Paso 1: Listar Archivos en el Directorio Home

Al iniciar sesión en **bandit0**, primero necesitamos ver qué archivos hay en el directorio home. Usamos el comando `ls` para listar los archivos:

```
ls
```

Este comando debería mostrar el archivo `readme` entre otros archivos que podrían estar presentes.

## Paso 2: Leer el Archivo `readme`
Ahora que sabemos que el archivo `readme` está presente en el directorio home, podemos usar el comando `cat` para leer el contenido del archivo y obtener la contraseña para el siguiente nivel:

```
cat readme
```

Este comando mostrará la contraseña para el nivel **bandit1.**

![image](https://github.com/user-attachments/assets/93f2b56d-bbe5-455a-9841-1c8c2c1c55e3)

## Paso 3: Conectarse al Nivel 1
Una vez que tengamos la contraseña, podemos iniciar sesión en **bandit1** utilizando SSH con el siguiente comando:

```
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

Cuando se te pida la contraseña, introduce la que obtuviste en el archivo **readme.**

---

## Resumen de los Comandos Utilizados
`ls`: Listar los archivos en un directorio.

`cat`: Mostrar el contenido de un archivo.

`ssh`: Conectarse a un servidor remoto mediante SSH.

---

¡Enhorabuena, ya has superado el primer desafío! Para continuar, ve a la página del siguiente nivel ([Level 1 -> Level 2](/Bandit2/Readme.md)).
