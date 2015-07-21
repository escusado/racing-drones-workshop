# Sesión 2
### JBH, @escusado, 2015

> Disclaimers
> Este NO pretende ser un curso profesional de pilotaje de `UAV`'s, es un espacio
> hobbista de introducción al area de multicopters con enfoque en carreras.
>
> El vocabulario técnico usado en este taller será en inglés, dado que la mejor y
> más reciente información se encuentra en este idioma para hacer que el asistente
> se familiarice con el slang desde un principio.
> Ref: [Liang Glossary Guide](http://blog.oscarliang.net/quadcopter-acronyms-term-glossary-word-drone/)

# Autoproclaimed Aeronautic Engineer

El diseño de multirotores está basado en la cantidad de motores que colaboran al
lift de la nave.

## #1 Rule

- Aim for simplicity: Lo que no está a bordo no puede fallar.

No solo se vuelve sencilla la ingenieria del craft, también reduce el peso y
contribuye al lift.

## Design and iteration (Build, fly, crash, repeat)

No importa si estás desarrollando un craft desde 0, armando uno de partes compradas
ó customizando uno comercial, estarás tomando desciciones sobre la ingeniería del
craft. Esta es una **breve introducción** al diseño e ingeniería de multirotores de
carreras, aún así la matoría de los puntos aplican para cualquier tipo de multirotor.

# Design

## Problema -> solución

Piensa primero en la necesidad que el quad debe cubrir, evalua el peso y tamaño
del payload que quieres en el aire:

- Cámaras
- Sensores
- Sistemas de entrega
- Paracaídas
- Luces
- etc.

La regla para comenzar a decidir es buscar que los motores generen el thrust
suficiennte para levantar el doble del peso del craft que está dado por
el peso del payload más el peso de los componentes:

```
peso_del_craft = payload + componentes;
thrust_mínimo_deseado = peso_del_craft * 2;
```
Lo que sigue es saber cuantos motores queremos, existen varias configuraciones
de multirotres y todas cubren una necesidad especial, pero la relga es: `Más helices
hacen a un craft más estable` dado que mueven aire en un area más grande (como
si cada motor fuera un punto de apoyo).

Por tanto necesitamos decidir la cantidad de helices que necesitamos y poder
así decidir que motores montar:

```
thrust_por_motor = thrust_mínimo_deseado / cantidad_de_motores_deseada;
```

Para poder decidir la `cantidad_de_motores_deseada` es necesario conocer los
tipos de multirotores y sus usos:

[ref](http://blog.oscarliang.net/how-to-choose-motor-and-propeller-for-quadcopter/)

# Multicopter Types

Cáda configuración ofrece caracteristicas distintas, pero después de 4 las configuraciones
simetricas se comportan igual. Existen algunas asimetricas después de 3, pero son un
poco exóticas:

[ref](http://www.dronethusiast.com/what-you-should-know-about-multicopter-configurations/)

## BiCopter

Considerado el más simple ya que sólo cuenta con 2 motores que se alinean con servos
para lograr el `yaw`, el menos robusto de la familia ya que sólo cuenta con 2
motores el rango de carga es muy corto. Poco popular en el mundo de RC ya que
son difícil de configurar y por su poca practicidad es considerado más un reto
técnico que un craft funcional:

![bicotper](/img/bicopter.jpg)
![bicotper-diag](/img/bicopter-diag.jpg)

[avar gunship](http://flitetest.com/articles/Avatar_Gunship_Scratch_Build)

## Tricopter

Cuenta con 3 motores que pueden ser configurados en posiciones `Y` o `T` usualmente
con una separación de 120º entre ellos, cuenta con 2 motores montados en los
brazos y 1 uno más en la cola, este último controla el `yaw` utilizando un `servo`,
Esto vuelve su ingeniería un poco más compleja ya que añade un segundo tipo de
componente motorizado y controlado desde tierra que comparte control del craft
con el motor de cola. Lo intenresante del tri es que precisamente esta caracteristica
lo vuelven extremadamente ágil y con un tipo de vuelo muy particular que no se
logra con otras configuraciones.

![tricotper](/img/tricopter.jpg)
![tricotper-diag](/img/tricopter-diag.jpg)

[quanum trifecta](https://www.youtube.com/watch?v=wD3rhzxb9I8)

## Quadcopter

El más popular dado que es la configuración mínima para maniobrar con un sólo tipo
de motor. Existen várias configuraciónes:

# `X`

Excelente maniobrabilidad, dado que su centro de masa está justo al centro, perfecto
para vuelo acrobático.

![x-quad](/img/x-quad.jpg)

# `+`

Dado que su vuelo se asemeja más al de un avión, hay quién prefiere este tipo de
dirección, pero presentan problemas si es necesario montar una cámara que mire al
frente dado que las hélices obstruirían la vista.

![plus-quad](/img/plus-quad.jpg)

# `H`

El más popular en el mundo de FPV dado que tiene un area más gránde para el payload
y permite montar los componentes muy fácil además, dado que los motores están
separados al frente permite colocar las cámaras mirando al frente sin ningún problema.

![h-quad](/img/h-quad.jpg)

## Pentacopter




## Cláses


## Common Mods

Angled motors
Wider lens
Angle cameras