# Introducción a Linux

# Introducción

Linux es uno de los sistemas más usados del mundo. Lo podemos encontrar en computadoras personales, servidores, consolas de videojuegos y hasta en smartphones. Pero como sé que todo esto te suena a marketing barato, te paso algunos datos más concretos. Según [algunos especialistas](https://truelist.co/blog/linux-statistics/), Linux y sus derivados son usados por:

* el 47% de los desarrolladores profesionales
    
* el 39,2% de los sitios webs cuyo sistema operativo se conoce
    
* el 85% de los smartphones
    
* las 500 supercomputadoras más veloces del mundo
    
* más del 96% de los servidores web más usados del mundo
    

Linux es el sistema operativo de los hackers. Fue creado y diseñado por hackers, en el sentido correcto de la palabra. Si queremos aprender a hackear, ya sea en el area de la programación o el penetration testing, tenemos que entender cómo funcionan los servidores. Y dado que la mayoría de ellos corren en Linux, no nos queda otra que aprender a usarlo.

Aparte Linux está bueno. Es gratis y libre, lo que significa que con él podés hacer lo que quieras sin que nadie te moleste con licencias o restricciones. Podés crear tu propio software y distribuirlo libremente, y lo mejor de todo: podés contribuir al código de Linux y ser parte de su desarrollo. Hasta hay distribuciones de Linux dedicadas al hacking y al penetration testing que incluyen todas las herramientas necesarias para que seas un experto de la seguridad informática.

Ahora que te convencí, seguí conmigo así juntos nos convertimos en Linux Hackers.

# Video

Dentro de poco estaré subiendo un video de YouTube.

# Historia

## Unix

Era el año 1969 cuando Dennis Ritchie y Ken Thompson desarrollaron el lenguaje de programación C y el sistema operativo Unix en los laboratorios de AT&T Bell Labs. Como eran buena gente, compartieron el código fuente con el resto del mundo, incluidos los alumnos de la universidad de Berkeley en California. De esta forma, muchos otros programadores comenzaron a contribuir en el desarrollo del sistema operativo, que llegó a tener alrededor de la mitad del código escrito por voluntarios.

*Ken Thompson y Dennis Ritchie*

![Ken Thompson y Dennis Ritchie](https://cdn.hashnode.com/res/hashnode/image/upload/v1677318875093/1cfc4fdf-9252-4947-b938-a83b35bcc102.jpeg align="center")

Hasta ahí todo muy lindo. Pero al tiempo AT&T comenzó a vender el mismo Unix que contenía código de los contribuidores y a estos no les cayó para nada bien. Como resultado de varias batallas legales, surgieron dos versiones de Unix: la oficial (la de AT&T) y la libre llamada BSD: Berkeley Software Distribution.

Ya por los años 80, algunas compañías como IBM, Sun Microsystems, HP y otras empezaron a desarrollar sus propios Unix y ahí el asunto empezó a irse de las manos. Cada empresa lo implementó de una forma diferente, y el resultado fue un caos de Unixes que proponían distintas formas de hacer exactamente lo mismo. Hasta que un día alguien intento traer un poco de orden al mundo de Unix, y la historia cambió.

## GNU

[Richard Stallman](https://es.wikipedia.org/wiki/Richard_Stallman), un físico y programador estadounidense, comenzó un nuevo proyecto llamado GNU (GNU's Not Unix - GNU no es Unix). Su meta era crear un sistema operativo que estuviera libremente disponible para todos, sin restricciones, con el que la gente pueda trabajar junta como solía hacerlo en los años felices. El resultado fue exitoso, y de hecho la mayoría de los comandos que se utilizan en la terminal de Linux hoy día son programas de GNU. Sin embargo, al sistema operativo GNU le faltaba algo muy importante: un corazón.

*Richard Stallman*

![Richard Stallman](https://cdn.hashnode.com/res/hashnode/image/upload/v1677317722651/eb24e08b-cfb3-485d-8dd3-9f1afc2b5f59.jpeg align="center")

## El Kernel

Según la [Wikipedia](https://es.wikipedia.org/wiki/N%C3%BAcleo_(inform%C3%A1tica)), el Kernel es el núcleo de un sistema operativo. Es el software responsable de facilitar a los distintos programas acceso seguro al hardware de la computadora. Es también el encargado de gestionar el uso de diversos recursos por medio de servicios de llamada al sistema.

Desde el inicio de los años 90 que el equipo de GNU se encuentra trabajando en un kernel llamado [GNU Hurd](https://www.gnu.org/software/hurd/), pero digamos que sin mucha prisa. Sin embargo, para el mismo tiempo un desarrollador finés llamado [Linus Torvalds](https://es.wikipedia.org/wiki/Linus_Torvalds) comenzó a desarrollar un kernel basado en los estándares POSIX y funcional para computadoras de arquitectura 386. En 1991 lo publicó en internet con el nombre de Linux.

De la combinación del sistema operativo GNU y el kernel Linux, surgió el sistema operativo GNU / Linux. Que, como ya te diste cuenta, es nuestro favorito.

*Linus Torvalds*

![Linus Torvalds](https://cdn.hashnode.com/res/hashnode/image/upload/v1677318141038/1de78fd5-7692-4832-a830-652e89c4e71e.jpeg align="center")

## GPL

Aparte de ser el principal ideador y desarrollador de GNU, Richard Stallman es un activista por la libertad en el uso del software. Fundó la [Free Software Foundation](https://www.fsf.org/) que tiene como meta difundir el Free Software (software libre - no necesariamente gratis), o sea, el software que otorga a sus usuarios las libertades de ejecutarlo, estudiarlo, modificarlo y compartir copias del mismo haya sido modificado o no.

La Free Software Foundation escribió la licencia [GPL](https://www.gnu.org/licenses/gpl-3.0.html), o GNU General Public License, la primera en implementar el concepto de [Copyleft](https://es.wikipedia.org/wiki/Copyleft), una cláusula de derecho de autor que protege al software con licencia GPL de volverse un software propietario.

**GNU / Linux es software bajo licencia GPL, por lo que podemos usarlo, estudiarlo, modificarlo y compartir copias del mismo libremente.**

Por otro lado, existe tambien otro concepto que está bueno mencionar, que es el [Open Source](https://es.wikipedia.org/wiki/Sistema_de_c%C3%B3digo_abierto) (código abierto). Básicamente todo software que permita el acceso a su código fuente, es de código abierto, pero no necesariamente [FOSS](https://itsfoss.com/what-is-foss/) (Free and Open Source Software - Software Libre y de Código Abierto).

Este tema es vital para entender el mundo de Linux y sus distribuciones. Pero por ahora lo dejamos acá así no nos aburrimos.

# Distribuciones

Como ya vimos, GPL nos deja jugar con Linux y modificarlo como querramos. Si quisieramos, podríamos hacer una versión modificada, ponerle nuestra marca y ¡hasta venderla!

Te re gustó la idea. Pero antes que te mandes y lances al mercado tu version llamada Robertox, quiero que sepas que ya hay varias de esas y se les llama distribuciones. Son diferentes linuxes tuneados a gusto y placer del autor y distribuidos, valga la redundancia, con diferentes nombres o marcas. En sentido estricto son colecciones de software que funcionan sobre un kernel Linux. Generalmente traen sus propias herramientas y aplicaciones de escritorio junto a un repositorio y manejador de paquetes.

Ahora vamos a ver las principales.

## Debian y derivadas

![Logo de Debian](https://cdn.hashnode.com/res/hashnode/image/upload/v1677320896425/8c40b709-1848-4076-9523-346ff14e920c.svg align="center")

La más usada se llama Debian y es una distribución comunitaria, lo que significa que no existe una compañía que la desarrolle. Está hecha por miles de programadores que eligen a un líder de proyecto cada dos años. Se la conoce por ser una de las más estables y la base de muchísimas otras distribuciones populares.

El software para Debian viene general empaquetado en el formato .deb y se puede descargar de los repositorios oficiales utilizando el comando `apt`. Viene en tres versiones: stable (estable), testing (de prueba) y unstable (inestable). Cada versión de Debian se llama como un personaje distinto de la película Toy Story.

Las distribuciones más famosas que derivan directa o indirectamente de Debian son las siguientes.

### Ubuntu

Desarrollada por la empresa Canonical, Ubuntu es la distribución de Linux más popular entre las computadoras de escritorio. Está basada en Debian y se caracteriza por contener gran variedad de drivers para diversos dispositivos, lo que lo hace fácil de instalar y configurar. Este motivo le dio mucha popularidad en la década del 2010 y continúa siendo una excelente opción. Hay versiones para escritorio y para servidores.

La versión oficial viene con un Gnome como administrador de escritorio, pero hay varios sabores con diferentes escritorios. Los más famosos son Kubuntu con KDE Plasma y Xubuntu con XFCE.

### Pop!\_OS

A diferencia de Ubuntu, Pop!\_OS no se basa en Debian, sino en el mismo Ubuntu. Es desarrollada por la empresa system76, que produce servidores y computadoras de escritorio. También usa Gnome como su administrador de escritorio.

### Linux Mint

Linux Mint es otra distribución basada en Ubuntu que se caracteriza por usar el administrador de escritorio Cinammon, desarrollado por ellos. A diferencia de Ubuntu y de Pop!\_OS, no está hecha por ninguna empresa, sino que es un esfuerzo de la comunidad.

Personalmente es mi favorita. Funciona perfectamente en la mayoría de las computadoras personales, es muy liviana y el administrador de escritorio es muy cómodo de usar.

## Red Hat y derivadas

![Logo de Red Hat](https://cdn.hashnode.com/res/hashnode/image/upload/v1677322607193/ea1c9dc1-4315-4d2f-91f2-7240eb48a364.png align="center")

Red Hat es una empresa multimillonaria que pone mucho esfuerzo en desarrollar Linux. Su negocio se basa en el desarrollo y la venta de una distribución muy estable llamada Red Hat Enterprise Linux, y el soporte de la misma. También proveen distintos servicios y productos de Cloud y CI/CD Pipeline.

El software para Red Hat viene general empaquetado en el formato .rpm y se puede descargar de los repositorios oficiales utilizando el comando `dnf`.

### Fedora

Red Hat invierte dinero en el desarrollo de una distribución comunitaria, la cual no tiene soporte oficial de Red Hat. Su nombre es Fedora y es muy popular.

Su versión oficial viene con el administrador de escritorio Gnome Shell, sin embargo hay sabores, llamados *spins*, que incluyen otros administradores como KDE, Cinammon, XFCE y otros.

A diferencia de otras distribuciones, esta sólo viene con free software por defecto, lo que significa que luego de instalarla deberíamos instalar drivers o paquetes propietarios manualmente de ser necesario.

## Arch y derivadas

![Logo de Arch](https://cdn.hashnode.com/res/hashnode/image/upload/v1677322872014/00d26f96-e9c4-4819-907d-fb8c0ae7973c.png align="center")

Arch es una distrubuición comunitaria. Está considerada como una distribución para hobbistas, ya que su instalación y configuración puede ser muy compleja para el usuario promedio. Es una *rolling release*, lo que no tiene nada que ver con la banda de rock, sino que significa que se actualiza constantemente sin que necesitemos instalar una nueva versión cada vez que salga. En sí no hay nuevas versiones, ya que lo que tenemos instalado siempre se va actualizando.

Es la distribución ideal para aquellos que les gusta tener lo último instalado y configurar cada parte del sistema exactamente como les apetece. No viene con gestor de escritorio, procesador de textos ni hoja de cálculos por defecto. Si la instalás te vas a topar con una pantalla negra solamente, donde tendrás que bajarte una por una cada aplicación que quieras, inclusive las más básicas para el funcionamiento normal de tu sistema.

Utiliza el gestor de paquetes `pacman` para los paquetes oficiales y `yay` para el AUR, un repositorio de aplicaciones subidas por los usuarios.

### Manjaro

Para todos aquellos que quieren correr un sistema Arch sin tener que pasar por el bardo de instalar todo a mano, existe una solución: Manjaro. Es una distro desarrollada por una pequeña empresa que también tiene otros productos de software. Viene en varios sabores que incluyen los gestores de escritorios más populares anteriormente mencionados.

# Comentarios finales

El mundo de GNU / Linux es apasionante, pero puede llegar a ser abrumador al principio. Con tantas opciones es difícil saber por donde empezar. En hackercore queremos aprender y llegar a ser expertos sin dejar el pragmatismo de lado. No nos vamos a volver locos intentanto instalar la distribución más *copada*, más *pro*, o la que luzca más *cool*. Vamos por la más fácil hasta que aprendamos a dominarla y de a poco continuaremos hacia otros horizontes.

A lo largo de este curso vamos a estar usando Linux Mint, pero todos los comandos utlizados funcionarán en la mayoría de las distribuciones, especialmente en las descendientes de Debian.

Un abrazo a todos, y a seguir hackeando.