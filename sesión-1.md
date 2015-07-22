# Racign Drones Workshop
### JBH, @escusado, 2015

> Disclaimers
> Este NO pretende ser un curso profesional de pilotaje de `UAV`'s, es un espacio
> hobbista de introducción al area de multicopters con enfoque en carreras.
>
> El vocabulario técnico usado en este taller será en inglés, dado que la mejor y
> más reciente información se encuentra en este idioma para hacer que el asistente
> se familiarice con el slang desde un principio.
> Ref: [Liang Glossary Guide](http://blog.oscarliang.net/quadcopter-acronyms-term-glossary-word-drone/)

## Overview

El objectivo de este taller es mostrar y compartir conocimientos básicos al respecto
de multicopters y Drones desde distintos puntos de vista.

## Intro

### Sociedad

Debemos de aceptar que el futuro ha llegado y que debemos lidiar con el. La industria
tecnologia de hoy en día es agresiva al respecto de empujar sus productos o servicios
al mercado. Comoditizando cada vez más y más necesidades y con costos cada vez
menores el acceso a tecnologias futuristas cada vez más está al alcance del
público en general y dejando de lado al mercado entusiasta.

## Los Drones no son teléfonos

Gracias al glamour de la industria muchos de los detalles detrás de tecnologias
complejas como la de `UAV`'s son dejados de lado, por favorecer a los conceptos
más escandalosos o "relevantes".

# Primero lo primero

## Drones? UAV's?

La tecnologia se ha ramificado bastante en los ultimos años y diferentes aplicaciones
han llamado a diferentes disciplinas para construir máquinas que solucionen
diferentes problemas. Estas máquinas por lo regular están diseñadas para operar
de manera automatizada a cierto grado y de ahí la confusión de que es que.

Actualmente se pueden separar en:

-  Multicopters: Tienen más de 1 juego de aspas, y necesitan estabilización.
-  Vehiculos de RC (Radio Control): Actualmente la mayoría de los multicopters
   se operan con alguna variación de tecnología de RC a la vista del piloto.
-  Drones: Cualquier tipo de vehiculo que se opere de manera autonoma (en diferentes grados).
-  UAV: Cualquier vehiculo aereo que no lleve tripulación a bordo.

La grán diferencia puede reducirse a: "Un Drone se opera solo".

Actualmente el término `Drone` se usa de manera intercambiable para referirse
tanto a los drones de guerra como el `Raptor` o multicopters de juguete. ¯\_(ツ)_/¯

## "y que tan lejos llega oiga..."

- Es un drone?
- No, es un helicoptero de RC.
- Que tal alto llega?
- Pues no se unos 500m.
- Cuanto le dura la pila?
- 3~5 min.
- Uuuuuuuy nomás? y cuanto cuesta?
- Pues este es de 80 dolares.
- Y que alcance tiene?
- Pues igual unos 500m.
- Y lo puedes usar para espiar a la vecina? jajaja
- Ehm. no?
- Y le puedes subir una GoPro?
... and so fucking on...

Esta va a ser la conversación que más vas a tener de ahora en adelante, al principio
es divertido compartir la experiencia, pero pronto verás que se vuelve tedioso
y hasta cierto punto insultante la manera en que los medios nos han presentado
la tecnologia e invitan a la banda a pensar que esos son los términos en los que
se debe leer la tecnología.

## "No es sobre que tan alto o que tán lejos..."

Bienvenido al magico gremio de piloto de multicopter. Como tal debes de asumir
una posición de autoridad al respecto y compartir la visión correcta al respecto
de la tecnología.

Un drone obedece a un **problema**, no es que tan alto, o que tan lejos, la pregunta
correcta es "Para que?".

Cada oferta que hay allá afuera tanto comercial como DIY obedece a una necesidad
y está en la ingeniería de la solución la razón de por que elegir piezas o soluciones
de ciertas caracteristicas.

# La Tecnología

## Multicopters

TODO: Historia

## Drones

TODO: Historia

## El Problema

La facilidad de tener aeronaves autopilotadas de grán eficiencia e inteligencia
han abierto la puerta a tratar de solucionar problemas que antes no era posible.

Es importante siempre mantener en mente el problema que un `UAV` trata de resolver
para poner en contexto el contenido que se nos es presentado.

## El Problema militar

TODO: Elaborar sobre drones militares

## El Problema de la industria privada

TODO: Surveilance
TODO: Data gathering
TODO: Film and photography
TODO: Arts
TODO: Hot areas and startups
TODO: Hobby and fun

El drone es una herramienta y debe de percibirse como tal, el "jueguete" está
interesante pero el fin es lo importante.

## Entretenimiento "It's like a hummingbird on crack"

La presicion de vuelo que posee un multicopter llamó a la industria de RC a una
micro revolución abriendo la posibilidad a vuelo acróbatico y de velocidad que
antes ningún vehiculo había tenido. A la par la tecnología se ha abaratado tanto
que es posible montar sistemas de video a bordo para transmisión de señal en vivo.

## Hubsan x4 - 101 (crash course)

El hubsan x4 es un multirotor en la cláse micro *(<200mm, más en clases sesión 2)*:

Hardware:
*(más sobre componentes en la sesión 2)*

- Tamaño: 60 x 60mm
- Motores (x4): Coreless Motor 8.5mm brushed
- Frecuencia de radio control: 2.4GHz
- Voltaje en operación: 3.7V
- Batería: 240mAh~500mah Li-Po Battery
- Tiempo de vuelo (stock): 6~ min.

[rcG - Thread](http://www.rcgroups.com/forums/showthread.php?t=1743358)

### Operacíon

#### Básico

Leé el manual

ACT: simulador

![axis diagram](/img/axis-diagram.png)
[ref](http://blog.tkjelectronics.dk/2012/03/quadcopters-how-to-get-started/)

- `Throttle` - Potencia de los motores
- `Yaw` - Giro en Z
- `Roll` - Giro en X
- `Pitch` Giro en Y

Dado que un quad como el hubsan pertenece a la familia de aeronaves capaces de
despegue vertical ([VTOL](https://es.wikipedia.org/wiki/VTOL)) es posible
levantar el quad con solo mandar poder a los motores.

Enviar potencia a los motores es lo más importante de volar multicopters. Es
importante siempre mantener control del `throttle` ya que es lo que mantiene el
quad en el aire a la altura deseada.

### Precheck

Antes de disponernos a volar, debemos verificar que el quad esté listo y espacio
disponible.

#### Field

Búsca un espacio donde puedas operar el quad en un area de alrededor de 5x5m.
Si hay personas contigo, déjales saber que vas a operar el hubsan en este lugar
y deben de estar al tanto, si pretendes grabar video o fotografía debes informar
a los presentes también.

Avisa cuando estés por despegar.

De preferencia no debe de haber viento, el hubsan puede operar perfectamente en
lugares cerrados, y no tener viento ayuda mucho al principio para entender los
controles.

#### Componentes

#### Baterías

Es recomendable que todo vuelo comience con baterias al 100% en el craft y cámara,
y estar conciente de cuanta carga tienen nuestros controles y receptores.

- Craft
- Cámaras (a bordo y tierra)
- Controles (craft y gimbal)
- FPV Rx

TODO: Capacity and features (discharge rate)

#### Props

Verificar que las props estén bien puestas, dando espacio de 1mm~ entre el motor
y la base del prop.

Es común que tratemos de estirar la vida de un prop, y el hubsan es conocido por
ser guerrero en cuanto a su desempeño, cuida que los props estén nivelados y que
no se doblen con facilidad, un prop puede aparentar estar bien verifica que puedas
flexionarlo sin romperlo.

Verifica que las props estén colocadas en el lugar correcto

```
B   A
 🚀
A   B
```

#### Motores

Los motores deben de girar si le soplas o flickeas el prop.

Si es un despegue después de inmediato uso previo, verifica que los motores estén
tibios al tacto, si están demasiado calientes, hay un problema y es mejor diagnosticar
antes de tratar de volar de nuevo.

#### Body

Verifica que las grapas de los brazos estén en su lugar, el frame está diseñado
para ceder antes de romperse, y las grapas en los brazos se abren en caso de choque
sólo vuelve a acomodarlas cuidando de no lastimar los cables.

#### Calibración

##### Controles

TODO: CALIBRATION DIAGRAM MANUAL

##### Acelerometro

TODO: CALIBRATION DIAGRAM MANUAL

Antes de volar coloca el quad en una superficie nivelada y calibra el acelerometro
con el uso el frame se deforma un poco y desnivela el `FC`.

# The kill rule

Es en este punto donde debes conocer la regla de oro:

**En caso de duda corta el `throttle`.**

No importa que tipo de duda sea:

- Voy en camino a chocar
- Volé demasiado lejos
- No se para donde está mi frente
- No se si le queda batería
- Creo que un prop está mal
- El quad hizo algo "raro"
- Estoy muy cerca de un arbol
- Perdí de vista el quad (pasaste por detrás de algo o algo se atravezó en tu linea de vista)
- etc.

Matar el poder hace lo más lógico tirar el quad del cielo, esto obedece a 2 cosas:

- Prevenir un accidente.
- Es mucho mejor rescatar "algo" que perder por completo el quad.
- Tratar de compensar o rescatarlo aumenta la posibilidad de daño.

# Safety first

El hubsan puede parecer un juguete pero es una máquina bastante capáz de ocacionar
heridas graves, pon siempre a la gente primero.

## Failsafe

TODO: resumen de lista de safety gidelines

## Flying

Dado que toma tiempo acostumbrarse a los controles es recomendable seguir una
serie de ejercicios iniciales para familiarizarse con los controles [ref](http://www.rchelicopterfun.com/rc-helicopter-training.html):

Comienza volando con el quad de frente todo el tiempo, hubsan indica su frente con
leds de colores:

Azul - Naríz
Rojo - Cola

![led](/img/hubsan-led.jpg)

Trata de siempre estar viendo al quiad por detrás, de esta manera alinearás los
controles con el craft.

1 `Throttle`: Lenvata el quad a una altura de alrededor de ~1m. y mantenlo a esa
altura, baja y sube entre 1/2 metro y ~2m. siempre en control de la altura deseada.

2  `Pitch & Roll`: Cuando comiences a levantarlo notarás que el quad se mueve un
poco, esto es debido a micro turbulencias ocacionadas por el mismo quad o viento
externo. Utiliza el stick derecho para mantener el quad en un espacio de ~1m.x1m.

Trata de mover el stick izquiedo hacia los lados cuando comiences a volar (no usar
`yaw` por el momento).

Acostumbrate a la potencia de los motores, y a la sensibilidad de los sticks,
piensa en un movimiento fino, como el acelerador de un coche, es raro que operes
con `full thtottle` siempre debes de mantenerte cerca de 50% y sólo acercarte
a los extremos cuando decidas cambiar de altura.

Haz esto hasta que estés confortable con los controles.

3 Cruz y circulos, cuando puedas mantener al quad en un lugar y altura fijos, comienza
a dibujar una cruz desde un punto central de referencia:

Haz esto de manera perpendicular y en diagonales:

![train-cross](/img/train-cross.jpg)
![train-diag](/img/train-diag.jpg)

de nuevo haz esto hasta que te sientas famliar con los controles, después trata
de dibujar circulos y patrones un poco más complejos.

Vuela un poco más lejos, siempre tratando de estár en control.

### Orientación

Lo más complejo de volar [LOS](http://oddcopter.com/2012/05/30/first-person-view-fpv-vs-line-of-sight-los/)
es mantener orientación, dado que el frente del quad puede cambiar en vuelo es
necesario poder mantener control sobre la nave sin importar para donde esté apuntando
el frente.

Repite los mismos ejercicios pero ahora con el quad orientado en 90, 270 y 180 grados.

Esto va a tomar semanas, es lo más complicado de volar. Cuando tengas dominado
el vuelo con orientación variable, puedes comenzar con vuelo de frente.

### Naríz al frente

La idea de conocer y conotrolar vuelo desalineado es poder volar con la naríz del
craft siempre hacia la dirección que se esté moviendo, aquí es donde puedes empezar
a usar `yaw` para mantener siempre tu `pitch` hacia el frente y usar `yaw` para
controlar la dirección.

Aquí puedes comenzar con cualquiera de estos 2 ejercicios:

- Ida y vuelta: traza una linea recta de lado a lado tratando de volar siempre
con naríz al frente, cuando llegues al extremo usa `yaw` para dar un giro de 180
y hacer el recorrido de regreso.

- Walk the dog: Camina detrás del quad y siempre mantenlo de frente a ti, usa
`yaw` para dar vuelta y siempre manten `forward momentum`. Este es el mejor de todos
los ejercicios ya que combina las habilidades de todos los anteriores y lo hace
bastante divertido, cuando te sientas comodo trata de salir con el quad y pasar
por lugares que reten tu control: debajo de bancas, entre ramas de arboles bajos,
etc. Retate cada día un poco más, hasta que te sea natural ir detrás del craft.

### Mantenimiento

TODO: Mantenimiento list

[ref](http://www.rcgroups.com/forums/showpost.php?p=23250512&postcount=30)

# LETS FLY!






