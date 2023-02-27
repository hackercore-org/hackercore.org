# Primeros Pasos con C

C es un lenguaje de programación poderosísimo y se lo considera [la madre de todos los lenguajes](https://ict.iitk.ac.in/c-the-mother-of-all-languages/). Fue creado en los años 70 por Dennis Ritchie en los laboratorios de AT&T, y después de más de 50 años, se mantiene en el [puesto 7](https://www.hackerrank.com/blog/most-popular-languages-2023/) del top 15 de los lenguajes más usados del mundo. Hoy día puede llegar a considerarse un lenguaje de bajo nivel, lo que significa que el programador necesita prover más instrucciones y detalles al compilador para que realice una tarea específica. Sin embargo, esto lo hace muy eficaz a la hora de ejecutarse, ya que los programas compilados son directamente ejecutados por el procesador sin tener que hacer ningún tipo de procesamiento extra en tiempo de ejecución.

Debido a su buen rendimiento, se lo usa mucho para software crítico que, generalmente no interactúa con algún usuario, sino que es la base de otros programas. A esto se le llama system programming, e incluye softwares como motores gráficos para videojuegos (game engines) - que calculan la matemática necesaria para dibujar gráficos 3d en un medio bidimensional como una pantalla, sistemas embebidos - que corren directamente en un hardware específico, drivers - que establecen un puente entre un dispositivo electrónico y el sistema operativo de una computadora, sistemas operativos - que administran todos los recursos de un sistema y permiten a otros programas acceder a ellos, y otros softwares así y más complicados. **Nuestro sistema operativo favorito, Linux, está hecho en C**.

Es un lenguaje relativamente fácil de aprender, que te va a dar las bases necesarias para que puedas escalar y aprender cualquier otro con total facilidad. En un rato lo vamos a estar instalando y creando nuestro primer programa con él.

# Software necesario

## Compilador

Primero que nada, para poder trabajar con cualquier lenguaje compilado, necesitamos instalar el compilador. Si no sabés qué es un compilador, te lo explico en el siguiente encabezado. Si ya sabés, podés saltéartelo.

### Qué es un compilador

Las computadoras no entienden el lenguaje C. Tampoco Python, Java, ni ningún otro lenguaje de ese tipo. Las computadoras sólo entienden el lenguage binario, esto es ceros y unos. Los unos significan valores positivos, mientras que los ceros negativos. O sea, prendido o apagado, que a fin de cuentas terminan siendo momentos en los que se envían pulsos eléctricos o no por algún conductor.

Los procesadores vienen con un set de instrucciones que permiten justamente decirles qué hacer. Esta lista de cosas que tienen que hacer se llaman *programas*. Este set de instrucciones está en binario, y es diferente para cada tipo de procesador. Si nosotros quisiéramos programar en binario, tendríamos que escribir programas que luzcan más o menos así:

```c
0100100001100101011011000110110001101111001000000111011101101111011100100110110001100100
```

Una hermosura. ¿No? Te cuento que ese choclo de numeritos representa la frase "Hello world" en binario (ASCII).

Gracias a Dios existen los compiladores. Son programas que toman un código fuente escrito en algún lenguaje de programación, lo optimizan y lo convierten en código binario, para que lo ejecute la computadora. Esto significa que cada vez que programemos, vamos a tener que compilar nuestro código, así se genera el programa ejecutable que finalmente ejecutará el usuario final.

Hay otro tipo de lenguajes que son los interpretados, pero por ahora no nos vamos a ocupar de esos. Ya llegará el turno cuando veamos Python o JavaScript.

### Instalación

En Linux utilizamos un compilador llamado [gcc](https://gcc.gnu.org/). Puede que ya lo tengas instalado. Para verificarlo, abrí una terminal y corré el siguiente comando:

```bash
gcc --version
```

Al presionar enter, debería mostrarte algo así:

```bash
gcc (Ubuntu 11.3.0-1ubuntu1~22.04) 11.3.0
Copyright (C) 2021 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```

Si en vez de eso te tiró un error, significa que no lo tenés instalado. Lo podés instalar de la siguiente manera.

En Debian o derivados:

```bash
sudo apt update
sudo apt install build-essential
```

En Red Hat o derivados:

```bash
sudo dnf install gcc
```

En Arch o derivados:

```bash
pacman -S gcc
```

Y con eso ya tendríamos el compilador instalado.

# Editor de código

Hay muchos editores de código que podemos usar. Algunos gratis, otros pagos. Obvio, vamos a instalar uno gratis. Pero más allá de eso, vamos a instalar uno que sea muy usado así nos aseguramos que cuando algo no funcione o tengamos alguna duda, podamos acudir a internet y encontrar mucha información disponible.

Yo sé que los muy fanas de Linux y el open source me van a insultar, pero en este caso vamos a estar usando Visual Studio Code. Más allá de lo que se diga, es un editor de código muy bueno, versátil, open source (o semi) y casi un estándar en la programación. Sin embargo hay muchos otros, como NeoVim, que la están rompiendo. El tema es que son un poco más difícil de usar, y no quiero que nos rompamos la cabeza ahora con eso. Lo importante es aprender a programar en C, y luego aprenderemos a usar NeoVim en algún otro artículo.

### Instalación de VSCode

Entrá a la página de descarga de [Visual Studio Code](https://code.visualstudio.com/Download), y fijate en la sección de Linux. Si usás algún derivado de Debian, bajate el .deb, si usás algún derivado de Red Hat, bajate el .rpm.

![Descarga de VSCode](https://cdn.hashnode.com/res/hashnode/image/upload/v1677421164639/2a5b79d7-1f6f-41f2-8577-3fe0935ef4d2.png align="center")

Una vez que hayas descargado el archivo, dale botón derecho e instalalo con el administrador de paquetes que corresponda.

Si usás Arch, fijate [acá](https://wiki.archlinux.org/title/Visual_Studio_Code).

# Primer programa en C

A qué no sabés cuál será nuestro primer programa en C. Sorpresa.

## Código

Abrí Visual Studio Code, andá arriba a la izquierda, hacé click en *File* y dale a *Open Folder*:

![File / Open Folder](https://cdn.hashnode.com/res/hashnode/image/upload/v1677421806035/70a003fa-b0c2-4f09-8c66-4ef3e2090c03.png align="center")

Elegí un directorio donde vas a trabajar. Tené en cuenta que ese directorio tiene que estar libre y disponible sólo para este proyecto, así que te aconsejo tenerte uno creado de antemano.

En mi caso, es el directorio `/dawud/Code/CProgramming`

Una vez abierto, voy a poder ver la estructura de archivos y directorios que cuelga bajo mi directorio de trabajo. Eso aparece en la barra de navegación que está a la izquierda.

Al lado del directorio de trabajo hay un ícono de un archivito con un signo **+**. Hago click ahí para crear un nuevo archivo y le pongo de nombre *hola.c*.

![Crear nuevo archivo en VSCode](https://cdn.hashnode.com/res/hashnode/image/upload/v1677423684317/b1f6dfe9-e042-4184-8ae9-368c9f1ce45c.png align="center")

Ya creado el archivo, hago click sobre él para que me lo abra en el editor. Escribo el siguiente código en él y lo guardo.

```c
#include <stdio.h>

int main(void)
{
    printf("Hello, HackerCore!\n");
    return 0;
}
```

Lo podés copiar directo de este artículo, pero te aconsejo escribirlo vos mismo. De esta forma vas a asimilar y memorizar mejor esto, para que después lo puedas hacer solo.

## Explicación del código

Quedó muy copado, pero ¿qué significa todo eso? Vamos por parte dijo Jack.

### Include

```c
#include <stdio.h>
```

En la primera línea le estoy diciendo al compilador, que voy a utilizar una librería. ¿Qué es esto? Es código ya compilado que existe para que yo lo pueda utilizar sin escribirlo de nuevo. Una de las funciones que usaremos en este programa está definida en la librería `stdio.h`. Si no incluyo la librería al comienzo, no voy a poder usar esa función y cuando quiera hacerlo el proceso de compilación fallará. Así que por ahora la dejamos ahí.

### main

```c
int main(void)
{
    // este lo vemos después: printf("Hello, HackerCore!\n");
    return 0;
}
```

En C, como en muchos otros lenguajes, hay funciones. ¿Qué son? Ya lo vamos a ver. Pero en este momento lo que te puedo decir es que las funciones tienen un nombre, reciben un dato y devuelven otro. Esta función se llama `main` y recibe `void` como parámetro, que significa "vacío". O sea, no recibe nada por parámetro. Los parámetros es lo que está adentro del paréntesis, pero como dije, vamos a verlo más adelante. Por otro lado, main devuelve un valor del tipo `int`, que quiere decir un número entero (*integer*). Todo lo que está entre llaves `{}` es lo que sucede dentro de la función main, se le dice que es el cuerpo de la función.

Lo primero que se ejecuta al correr un programa hecho en C es la función `main`. Por lo tanto, si queremos que algo suceda en nuestro programa, tiene que estar ahí dentro.

Por último, como dijimos que la función `main` va a retornar un valor del tipo `int`, tengo que retornarlo. Y por eso es que pusimos `return 0;` que significa que estoy devolviendo el valor 0. En sistemas Unix esto significa que el programa terminó bien.

Dejame hacerte un comentario. Cuando veas en el código que hay dos barras así `//` o algo como lo siguiente, quiere decir que eso no se va a ejecutar. No es código.

```c
// Estoy escribiendo cosas que no se ejecutarán
/*
Estoy escribiendo cosas que no se ejecutarán
y uso más de una línea porque soy re heavy re jodido
*/
```

Se le llama comentario.

### printf

Ahora te cuento qué es lo que hicimos en esta línea de código:

```c
printf("Hello, HackerCore!\n");
```

Llamamos a una función cuyo nombre es `printf`. Cuando habíamos definido la función `main`, no la estábamos llamando, sino que la estábamos creando para que después la llame el programa nuestro ni bien inicie. En el caso de `printf` nosotros nunca la definimos, sino que solo la ejecutamos - se dice que la llamamos. ¿Quién la definió entonces? Algunos programadores re cracks que nos la dejaron para que la usemos sin tener que escribir todo el código de su funcionalidad de nuevo. La guardaron en la librería `stdio.h` y por eso tuvimos que hacer el `include` al principio de todo. Ahora podemos usar esa función al haber incluido dicha librería.

Lo que hace es mostrar en la terminal lo que sea que le pasemos por parámetros, o sea, entre paréntesis. En nuestro caso le estamos pasando el texto *Hello, HackerCore!* y lo tenemos que poner entre comillas para que el compilador se dé cuenta que no es el nombre de una variable ni de alguna palabra reservada de C, sino un texto común y corriente escrito por nosotros. Esto tiene un nombre, pero por ahora te dejo con la intriga así no te atorás con tanta data junta.

# Compilación y ejecución

Bueno, después de tanto código y hacking, es hora de correr nuestra obra maestra. Pero antes, como seguramente te acordarás, tenemos que compilar el código y convertirlo en ejecutable. Para esto nos vamos a la terminal que ya viene en Visual Studio Code.

![Abrir terminal en VSCode](https://cdn.hashnode.com/res/hashnode/image/upload/v1677423547113/d655b15b-4b33-459a-a3a0-601d16dd093a.png align="center")

Para eso, andate arriba de todo en el VSCode, hacé click en Terminal y después en New Terminal. Esto te va a abrir una terminal abajo de todo, adentro del mismo programa. En esta terminal tipeá lo siguiente y dale enter:

```bash
gcc hola.c
```

Con eso estás invocando al compilador de C y diciéndole que te compile el archivo hola.c, que es donde tiraste tanta belleza programabilística.

Si luego hacés un ls, vas a ver que te creó un nuevo archivito llamado a.out.

![a.out creado](https://cdn.hashnode.com/res/hashnode/image/upload/v1677423847599/09ea3665-9975-4179-bbca-6fa50c086d69.png align="center")

Ahora, en la misma terminal, corré el siguiente comando:

```bash
./a.out
```

Al poner `./` le estamos diciendo a Linux que ejecute el archivo `a.out` como un programa. Y Linux, de obediente que es, lo hace y nos devuelve lo siguiente:

![Resultado de la ejecución](https://cdn.hashnode.com/res/hashnode/image/upload/v1677424000664/c26e7cae-526b-49cb-8520-cd5c620cdf68.png align="center")

Como podemos ver, el texto "Hello, HackerCore!" aparece en la pantalla al ejecutar nuestro programa. Lo logramos, somos Hackers de C.

Antes de continuar, te paso un tip. Queda horrible que nuestro programa se llame `a.out`. SI querés cambiarle el nombre, podés pasarle un parámetro o *flag* a `gcc`.

Corré lo siguiente en la terminal para arreglarlo:

```bash
gcc -o elnombrequesetecante hola.c
```

El resultado es contundente:

![elnombrequesetecante](https://cdn.hashnode.com/res/hashnode/image/upload/v1677424219334/87d02424-4e21-4af8-9627-0e01eb594bb0.png align="center")

# Tarea

Ahora que sabés todo esto, seguro que ya te re agrandaste. Pero no caigas en la trampa de tu ego. Un buen programador, o programadora, necesita practicar mucho para llegar a un buen nivel. Así que te paso tarea para que ensucies tus manos con barro compilable.

## Mensaje de bienvenida

Crear un programa en C que, al ejecutarlo muestre un mensaje en la terminal que diga "Bienvenido a mi super programa".

El programa final ejecutable debe llamarse `bienvenida.hacker`.

# Comentarios finales

Por hoy eso es todo. Cualquier duda que tengas me la dejás en los comentarios. Saludos!

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677397483193/893f9262-6799-415d-83e7-47d2c4a75504.png?auto=compress,format&format=webp align="center")

This work is licensed under a [**Creative Commons Attribution-ShareAlike 4.0 International License**](http://creativecommons.org/licenses/by-sa/4.0/).