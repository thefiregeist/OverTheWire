# Bandit Level 0 -> Level 1 - Solución

En este nivel de **Bandit** en [OverTheWire](https://overthewire.org/wargames/bandit/bandit1.html), el objetivo es encontrar la contraseña para el siguiente nivel almacenada en un archivo llamado `readme` en el directorio home. Una vez obtenida la contraseña, debes usarla para iniciar sesión en el nivel **bandit1** a través de **SSH**.

## Objetivo del Nivel
Descubrir la contraseña para el siguiente nivel, almacenada en un archivo llamado `readme`, ubicado en el directorio home.

- **Host**: `bandit.labs.overthewire.org`
- **Puerto**: `2220`
- **Usuario**: `bandit0`
- **Contraseña**: `bandit0`

---

## Paso 1: Conectarse al Servidor
Primero, inicia sesión en el servidor con las credenciales del nivel anterior:

```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

---

## Paso 2: Listar Archivos en el Directorio Home

Al iniciar sesión en **bandit0**, primero necesitamos ver qué archivos hay en el directorio home. Usamos el comando `ls` para listar los archivos:

```
ls
```

Este comando debería mostrar el archivo `readme` entre otros archivos que podrían estar presentes.

---

## Paso 3: Leer el Archivo `readme`
Ahora que sabemos que el archivo `readme` está presente en el directorio home, podemos usar el comando `cat` para leer el contenido del archivo y obtener la contraseña para el siguiente nivel:

```
cat readme
```

Este comando mostrará la contraseña para el nivel **bandit1.**

![image](https://github.com/user-attachments/assets/93f2b56d-bbe5-455a-9841-1c8c2c1c55e3)

---

## Paso 4: Anotar la Contraseña
Copia la contraseña que aparece y guárdala para el próximo nivel.

---

## Resumen de los Comandos Utilizados
* `ssh`: Conectarse a un servidor remoto mediante SSH.
* `cat`: Mostrar el contenido de un archivo.
* `ls`: Listar los archivos en un directorio.

---

¡Enhorabuena, ya has superado el primer desafío! Para continuar, ve a la página del siguiente nivel ([Level 1 -> Level 2](/Bandit2/Readme.md)).
