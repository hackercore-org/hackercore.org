# Cómo Aprender a Hackear

# ¿Qué es el hacking?

El "hacking" que trataremos en este documento es la programación exploratoria en un entorno open source (de código abierto). Si creés que el "hacking" tiene algo que ver con el crimen cibernético o los ataques de seguridad y viniste a aprender eso, ya te podés retirar. No hay nada para vos acá.

Hackear es primariamente un estilo de programación, y seguir las recomendaciones en este documento puede ser una manera efectiva de adquirir habilidades de programación de propósito general. No se garantiza que esta ruta funcione para todos. Pareciera funcionar mejor para aquellos que comienzan con un talento para la programación superior al promedio y un grado razonable de flexibilidad mental. La gente que aprende este estilo tiene a convertirse en generalistas con habilidades no fuertemente vinculadas a un lenguaje o dominio de aplicación particular.

Tené en cuenta que uno puede estar hackeando sin ser un hacker. Hackear, en su sentido amplio, es una descripción de un método y un estilo. Hacker implica que hackeás, y que también estás vinculado a una [cultura](http://catb.org/~esr/faqs/hacker-howto.html) particular o tradición histórica que utiliza este método. Propiamente dicho, "hacker" es un término honorífico otorgado por otros hackers.

El hacking no tiene un aparato formal suficiente como para ser una metodología completa como se suele referir en la ingeniería de software, pero tiene algunas características que tienden a diferenciarla de otros estilos de programación.

* *El hacking se realiza en open source.* Hoy, las habilidades de hacking son el micro-nivel inidividual de lo que suele llamarse "desarrollo open source" en el macro-nivel social. Un programador que trabaja con el estilo hacker espera y usa fervientemente las revisiones del código fuente por parte de sus pares (peer review) para suplementar sus habilidades.
    
* *El hacking es liviano y exploratorio.* Los procedimientos rígidos y especificaciones elaboradas a-priori no tienen lugar en el hacking. Por el contrario, la tendencia es "probá y fijate si funciona" con un tiempo de entrega veloz.
    
* *El hacking le da mucho valor a la modularidad y la reutilización.* En el estilo hacker, te esforzás mucho por no escribir código que pueda ser usado solo una vez. Te inclinás hacia la creación de herramientas o librerías generales que puedan ser especializadas en lo que necesitás por medio de bloquear algunos argumentos o variables, o al brindar un contexto.
    
* *El hacking prefiere "descartar y empezar de cero" a "emparchar y extender".* Una parte esencial del hacking es elminar sin piedad el código que se haya vuelto extremadamente complicado, no importa cuánto tiempo hayas invertido en él. El estilo hacker ha estado fuertemente asociado con la tradición técnica del sistema operativo Unix. Recientemente se pudo evidenciar que el hacking se lleva bien con el estilo de programación "agile". Las técnicas Agile tales como pair programming y feature stories se adaptan rápidamente al hacking y vice-versa. Esto se debe en parte a que los líderes iniciales del movimiento agile fueron influenciados por la comunidad open source. Pero ha habido tráfico en la otra dirección también, con proyectos de open source adoptando cada vez más técnicas como el test-driven development.
    

# Etapas del aprendizaje del hacking

Aprender a componer música tiene tres etapas. Primero tenés que aprender la técnica mecánica básica de un instrumento: la digitación y cómo tocar las escalas. Luego tenés que entrenar tu oído para entender los patrones musicales. Por último, debés entender cómo recombinar los patrones musicales para formar creaciones originales. El hacking es parecido.

El equivalente a la digitación en el hacking es aprender las capacidades de los lenguajes de programación, y las mecánicas de la utilización de herramientas como editores, intérpretes y compiladores. (Si no entendés estos términos, leé The [Unix and Internet Fundamentals HOWTO](http://www.tldp.org/HOWTO/Unix-and-Internet-Fundamentals-HOWTO/index.html)). No cubriremos esas mecánicas aquí, dado que varían demasiado según el lenguaje que estés usando. Hay tutoriales para todos los lenguajes que quieras utilizar en la Web. Usá un buscador.

El equivalente a tocar escalas es escribir pequeños programas, solo. Desafortunadamente, tocar escalas (a) no te enseña nada sobre música y (b) es aburrido como la gran siete. Similarmente, (a) escribir programas de juguete no tiende a enseñarte mucho sobre el hacking, y (b) tenderá a desmotivarte a menos que el programa resuelva inmediatamente un problema que te interese.

La mayor parte de la educación sobre programación se trata de tocar escalas y silencios. Por lo tanto, tiende a producir coders que no son buenos en el trabajo colaborativo y tienen el equivalente a la falta de oído en la música - una arquitectura y diseño de software con poco sentimiento.

# El ciclo de hacking incremental

Hay una mejor forma de aprender. Yo lo llamo el ciclo de hacking incremental.

1. Primero, elegí un programa que haga alto que te interese. Idealmente debería ser un programa que uses regularmente y tengas opiniones al respecto. La siguiente mejor cosa es un programa que no uses normalmente, pero que haga algo que creas que es interesante. Para que este método de aprendizaje funcione, deberías evitar intentar hackear sobre código que te aburra. El programa que elijas no tiene por qué se algo serio. Muchos programadores han perfeccionado sus habilidades mejorando juegos que disfrutaban. El único inconveniente con esto es que los juegos modernos son generalmente bastante largos y complicados, y podrían estar fuera del alcanza de un total principiante. Por esta razón, quizás podrías investigar alguno de los juegos clásicos basados en texto que todavía sobreviven. Un ejemplo es nethack, pero hay muchos otros.
    
2. Si no conocés el programa todavía, aprendé a usarlo. Leé la documentación. Desarrollá un modelo mental de cómo funciona.
    
3. Elige una característica pequeña para agregarle o modificar.
    
4. Busca el código hasta que encuentres la parte que deseas modificar. Nota: Deberías no intentar de leer el programa entero. Solo te cansarás y frustrarás si haces eso. Por el contrario, usá la estructura de módulos del código para enfocarte sólo en la parte que necesitas entender. En el camino vas a aprender cosas sobre cómo las diferentes partes del programa encajan entre sí. Esto es una buena excusa para agregar comentarios explicativos y notas en el código, a medida que vas descubriendo cosas sobre este. Esto ayudará a tu memoria y también ayudará a organizar tus pensamientos.
    
5. Compilá, testeá, debugueá y documentá tus cambios. Documentar tus cambios es importante. Si desarrollas el hábito de hacer esto temprano, vas a producir un trabajo de mayor calidad.
    
6. Enviá tu cambio como parche a los que mantienen el programa. Mirá la guía de [Software Release Practice HOWTO](http://www.tldp.org/HOWTO/Software-Release-Practice-HOWTO/index.html) para obtener tips sobre cómo hacer esto de forma efectiva y amable. Originalemtne describí esto como un paso opcional. Un sabio amigo me señaló que probablemente no debería haberlo hecho. Jugar con tu instrumento en solitario está bueno para practicar, pero la música se completa y valida cuando la creatividad en ella es escuchada por otra gente. Jugar solitariamente en tu computadora es similarmente bueno para la práctica, pero el hacking se completa cuando otra gente usa lo que vos escribiste. El test de la vida real es importante. En ocasiones (bastante seguido cuando recién empezás) tus parches van a ser rechazados. Tenés que aprender como sobrellevar eso. No significa que estás condenado a fallar en tu búsqueda. Usualmente significa que no leíste el código con el cuidado necesario, o (como suele suceder) te perdiste algo importante sobre la cultura y las prácticas del grupo de desarrollo al que intentás contribuir. Estos errores pueden ser reparados.
    
7. Ahora, preguntate a vos mismo: ¿Entiendo este programa entero? Si la respuesta es sí: terminaste. Sino, volvé al paso 3. Esta vez, elegí una parte diferente y quizás una cosa un poco más difícil para modificar.
    

El punto de este ejercicio es aprender cómo colarse en el problema de entender un programa, en vez de intentar de abarcar toda la complejidad al mismo tiempo. A medida que iteres este bucle varias veces, vas a desarrollar gradualmente una representación más completa en tu mente de la forma que todo el programa se ensambla. En algún punto vas a alcanzar el límite donde entenderás todo, o lo que sea necesario para cual sea tu propósito final.

# Desarrollar tu sentido del diseño

Para entrenarte, empezá de a poco. Si es posible, primero hacé el ciclo incremental de hacking como un ejercicio en programas muy pequeños o scripts de 10 a 50 líneas. Pueden ser difíciles de encontrar, ya que la mayoría de los programas de cualquier tipo son más largo que esto. La mayoría de los programas así de pequeños son scripts en shell, Perl, Python, o Tcl. Eso puede ser una característica a buscar cuando navegás en internet en búsqueda de ellos.

Cuando hayas terminado el cico de hacking incremental en varios programas muy pequeños (o si no tenés la suerte suficiente de encontrar ninguno pequeño que sea apropiado), intentá con programas ligeramente más grandes. Buscá códigos en el rango de 100-500 líneas. Cuando hayas dominado este nivel, andá a la orden de magnitud, 1000-5000 líneas. Cuando hayas dominado el nivel de 1K-5K habrás alcanzado el fondo del rango de capacidad de lo que se considera un programador habilidoso. Alrededor del nivel 1K-5K podrías ocasionalmente comenzar a notar que tenés inquietud por cambiar la estructura u organización de un programa. No solo sus características. Podés encontrarte pensando "este código es feo" y teniendo sentimientos acerca de embellezerlo o limpiarlo. Cuando eso sucede, prestá atención. Este es tu sentido del diseño intentando despertarse. No te apures en parchear ninguna otra característica. En vez de eso, empezá a explorar el programa que te da esta inquietud en un nivel más alto. Ahora podría ser una buena ocasión para intentar leer todo el código, pero no te preocupes mucho si no podés. La mayoría de los programas son demasiado grandes y enredados para tragarlos todo de una. Solo intentá entender lo suficiente para acomodar un poco las cosas. Ahora estás ingresando a la capa intermedia de aprender a hackear. Esto incluye no solo modificar características superficialmente visibles, sino realizar lo que se llama "refactoring": reorganizar el código internamente para que sea más limpio y tenga mejor arquitectura (mejor encapsulamiento de información, interfaces más pequeñas entre diferentes partes, mayor separación funcional entre módulos).

Una vez que tu sentido de diseño (tu equivalente al oído musical) se haya activado, encontrarás a menudo que empezás a refactorizar cada programa en el que trabajas al llegar a la tercera o segunda vuelta del ciclo incremental de hacking. De hecho, así es exactamente como los hackers experimentados encaran normalmente el código de programas grandes: retocando y refactorizando y rescribiendo hasta que asimilan de qué se trata. Se hacen cambios pequeños para entender cómo hacer cambios grandes. Si refactorizás tres o cuatro sistemas largos, no solo vas a desarrollar habilidades fuertes de programación, sino que también vas a estar encaminado a algo mucho más extraño y poderoso: volverte un arquitecto de software, alguien que puede hacer diseño original de sistemas grandes de software. Esta es la única forma que conozco para que los arquitectos de software novatos entrenen su sentido de diseño. Puede ser la única forma que exista.

# Ser original

En mi analogía con la música, dije que eventualmente necesitarías entender cómo recombinar los patrones musicales (los que aprendiste escuchando música y practicando su ejecución) para formar composiciones musicales. Elegí con cuidado esa forma para describir a la creatividad, porque aplica al software aún más de lo que aplica a la música. Antes de que hayas leído y absorbido las lecciones de un mondón de código, probablemente no tengas en tu mente la librería de patrones que necesitás para ser creativo en escalas más largas. Uno de los objetivos de usar el ciclo de hacking incremental es que te sumerjas en un montón de código (al aumentar escalas de complejidad) bajo circunstancias que te provean de motivación para seguir leyendo. Eventualmente vas a liderar proyectos de grupo y realizar trabajo enteramente original. No sientas que tenés que apurarte en esto o forzarlo. Si le das tiempo a tus habilidades para que maduren, tu primera composición original va a ser lo mejor para ello. Al contribuir efectivamente a proyectos de open source existente, vas a aprender las habilidades (incluyendo las de comunicación) que necesitás para llevar adelante tus propios proyectos.

*Copyright © 2014 Eric S. Raymond*

[Link al artículo original](https://www.catb.org/~esr/faqs/hacking-howto.html).