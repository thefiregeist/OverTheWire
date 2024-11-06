# Bandit Level 0 - Solución

En este primer nivel de **Bandit** en [OverTheWire](https://overthewire.org/wargames/bandit/bandit0.html), el objetivo es conectarnos al servidor remoto mediante **SSH** usando las credenciales proporcionadas.

## Objetivo del Nivel
Conectarnos al servidor utilizando SSH con las credenciales específicas del usuario. Los datos necesarios para la conexión son los siguientes:

- **Host**: `bandit.labs.overthewire.org`
- **Puerto**: `2220`
- **Usuario**: `bandit0`
- **Contraseña**: `bandit0`

---

## Paso 1: Entender el Comando SSH

**SSH** (Secure Shell) es un protocolo que permite acceder de forma segura a servidores remotos. Para conectarse a través de SSH, utilizaremos el comando:

```
ssh username@host -p port
```

En nuestro caso:

```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

## Paso 2: Conectarse al Servidor
Abre una terminal y escribe el comando de conexión. Se te pedirá la contraseña después de ejecutar el comando.

```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

## Paso 3: Ingresar la Contraseña
Introduce la contraseña bandit0 cuando se te solicite. Si todo está correcto, te conectará al servidor y te mostrará un mensaje de bienvenida.

![image](https://github.com/user-attachments/assets/36cf6bae-cc27-4c5e-bad0-68352ab64839)

## Paso 4: Confirmar la Conexión
Una vez que inicies sesión correctamente, estarás en la cuenta del usuario bandit0 en el servidor bandit de OverTheWire. Esto indica que has completado el primer nivel.

Puedes comprobarlo observando que la terminal ahora muestra el prompt:

```
bandit0@bandit:~$
```

El `bandit0@bandit:~$` indica que estamos en la cuenta `bandit0` en el servidor remoto.

Para proceder, dirígete a la página del siguiente nivel ([Level 0 -> Level 1](/Bandit1/Readme.md)) para continuar con el próximo desafío.
