# Linux: Comandos Básicos

# Intro

En nuestro camino hacia el hacking, es vital dominar diferentes sistemas operativos. Linux es el sistema operativo más usado del mundo. Sí. Según el siguiente sitio, el 47% de los desarrolladores profesionales usan Linux. Linux es el sistema en el que corren el 39.2% de los sitios webs cuyo sistema operativo se conoce. No solo eso, Linux está detrás del 85% de los smartphones. [Fuente](https://truelist.co/blog/linux-statistics/).

Al margen de esto, los hackers usan Linux. Cientos de desarrolladores contribuyen al *kernel* del sistema operativo. Se les llama *Kernel Hackers*. La mayoría de las herramientas para *ethical hacking* están disponible en Linux, y hay distribuciones como [Parrot OS](https://www.parrotsec.org/), [Kali Linux](https://www.kali.org/), [Black Ubuntu](https://blackbuntu.org/) y [Black Arch](https://www.blackarch.org/) que están dedicadas exclusivamente al *penetration testing*. Y como si fuera poco, Eric Raymond, el célebre escritor de varias guías sobre cómo iniciarse en el hacking, usa Linux.

Espero que con todo esto no te queden dudas de qué sistema operativo tenés que aprender primero. Así que empezamos ahora con los comandos más comunes en Linux. A hackear.

# Video

Te dejo un video de mi canal que explica todos los comandos. Pero está en inglés. Pronto estaré subiendo la versión en español.

%[https://www.youtube.com/watch?v=jAGRP-hT4Oo] 

# Shell

El *shell* es un programa que permite que escribas comandos para que el sistema operativo los ejecute. Casi todas las operaciones básicas de un sistema operativo se pueden hacer desde el shell. Por ejemplo, copiar o eliminar archivos, directorios, etc. En muchas distribuciones de linux al shell se lo conoce como *Terminal* o *Console*.

Hay diferentes shells, pero el que generalmente viene configurado por defecto es el que se llama *bash* (bourne again shell). En este post nos enfocamos en bash.

# Comandos

## Dónde estoy parado

El primer comando que vamos a ver se llama *pwd* (print working directory) y te muestra en qué directorio estás parado actualmente en esa sesión del shell.

```bash
pwd
```

Solo tenés que escribir pwd en una terminal y presionar la tecla enter. Te va a mostrar algo como lo siguiente (pero con tu nombre de usuario):

```bash
/home/dawud
```

Esto significa que estás en el directorio /home/dawud. Este es tu directorio personal. Si ahora creás otro directorio yo un archivo, te lo va a crear ahí adentro. Así que prestá atención.

## Cambiar de directorio

El comando que se usa para cambiar de directorio es *cd* (change directory). Tenés que pasar por parámetro a qué otro directorio querés ir.

```bash
cd
```

Ponés el comando en la terminal, apretás enter, y te sal