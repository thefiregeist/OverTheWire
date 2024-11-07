# Bandit Level 3 -> Level 4 - Solución

En este nivel de **Bandit** en [OverTheWire](https://overthewire.org/wargames/bandit/bandit4.html), el objetivo es encontrar la contraseña para el siguiente nivel. La contraseña está almacenada en un archivo oculto dentro del directorio `inhere`.

## Objetivo del Nivel
La meta de este nivel es localizar el archivo oculto que contiene la contraseña para acceder al siguiente nivel. Los datos necesarios para la conexión son los siguientes:

- **Host**: `bandit.labs.overthewire.org`
- **Puerto**: `2220`
- **Usuario**: `bandit3`
- **Contraseña**: La obtenida en el nivel [anterior](/Bandit3/Readme.md). Ver en Raw si es necesario. <!-- MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx -->

---

## Paso 1: Conectarse al Servidor
Primero, inicia sesión en el servidor con las credenciales del nivel anterior:

```
ssh bandit3@bandit.labs.overthewire.org -p 2220
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

## Paso 4: Listar Archivos Ocultos
En este caso, sabemos que el archivo está oculto. Para listar archivos ocultos, usamos el comando `ls -a`, que muestra todos los archivos, incluidos los que comienzan con un punto (`.`):

```
ls -a
```

Salida:

```
.  ..  ...Hiding-From-You
```

### Explicación del Resultado
En la salida de `ls -a`, los elementos `.` y `..` representan el directorio actual y el directorio superior, respectivamente. El tercer elemento, `...Hiding-From-You`, es el archivo que buscamos. Visualmente, todos los nombres se muestran en la misma línea, lo que puede dar la impresión de que el archivo tiene un nombre más largo.

Para evitar confusión, podemos listar cada archivo en una línea separada con `ls -a -1`:

```
ls -a -1
```

Esto muestra:

```
.
..
...Hiding-From-You
```

De esta manera, queda claro que el nombre real del archivo es `...Hiding-From-You`.

---

## Paso 5: Leer el Archivo Oculto
Ahora que identificamos el nombre correcto, utilizamos `cat` para ver el contenido del archivo y obtener la contraseña:

```
cat '...Hiding-From-You'
```

Esto mostrará la contraseña que usaremos para el siguiente nivel.

![image](https://github.com/user-attachments/assets/acf5f210-8c3a-4ea1-8d03-228dac5618ef)

---

¡Felicidades, has completado Bandit Level 4! Para continuar, ve a la página del siguiente nivel ([Level 4 -> Level 5](/Bandit5/Readme.md)).
