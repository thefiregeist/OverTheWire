# Bandit Level 6 -> Level 7 - Solución

En este nivel de **Bandit** en [OverTheWire](https://overthewire.org/wargames/bandit/bandit7.html), el objetivo es encontrar la contraseña para el siguiente nivel. La contraseña está almacenada en un archivo oculto dentro del directorio `inhere`.

## Objetivo del Nivel
Descubrir la contraseña del siguiente nivel, que se encuentra en un archivo que está almacenado en algún lugar del servidor y cumple con las siguientes características específicas:

* Propietario del archivo: Debe ser el usuario `bandit7`.
* Grupo propietario del archivo: Debe ser el grupo `bandit6`.
* Tamaño exacto: El archivo mide exactamente 33 bytes.

- **Host**: `bandit.labs.overthewire.org`
- **Puerto**: `2220`
- **Usuario**: `bandit6
- **Contraseña**: La obtenida en el nivel [anterior](/Bandit6/Readme.md). Ver en Raw si es necesario. <!-- HWasnPhtq9AVKe0dmk45nxy20cvUa6EG -->

---

## Paso 1: Conectarse al Servidor
Primero, inicia sesión en el servidor con las credenciales del nivel anterior:

```
ssh bandit5@bandit.labs.overthewire.org -p 2220
```

---

## Paso 2: Buscar el archivo con las condiciones indicadas
Utiliza el comando `find` para buscar los archivos que cumplan las condiciones mencionadas:

```
find
```

---

## Paso 3:
