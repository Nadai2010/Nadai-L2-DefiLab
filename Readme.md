# Nadai Layer 2 DefiLab

## Introducción a layer 2 (5 min)

- Seguridad de la L1 o _Layer 1_ de Ethereum: El consenso de esta red blockchain se basa en pruebas de participación (POS) entre muchos nodos, siendo la red princpial de Ethereum.

- Problemas de las redes blockchain _el trilema_: Necesitan escalar la red, seguir luchando por la seguridad y descentralización.

![Trilemma](/im%C3%A1genes/trilema.png)

### Los 2 tipos de solución de escalabilidad pricipales (5 min)

- Sidechain: Esta red tiene su propia forma de validar la cadena, con su propio consenso, teniendo como principal inconveniente que no hereda la seguridad de Ethereum.

- Layer 2: Esta red si hereda la seguridad de Ethereum, pueden configurarse de diferentes formas que iremos tratando y tendrán diferencias entre las propias _Layer 2_, pero la principal ventaja frente a las Sidechain es que heredan la seguridad (POS) completa de Ethereum, a unos costes inferiores que en la red principal.


  ![Graph](/im%C3%A1genes/sidechain.png)



- Las Layer 2 son contratos inteligentes a simple vista de Ethereum: Debemos pensar que la forma en la que Layer 1 interactúa con Layer 2 son por Smarts Contracts, podemos ver como en [L2Beat](https://l2beat.com) analizan parámetros de actualizaciones y otros riesgos que evaluaremos al final.

- Layer 1 sólo le importa el estado: La salida y entrada deben coindir en ambas Layer, es decir, mientras que a la red principal de Ethereum le demuestren por pruebas de fraude (Optimism Rollup) o por pruebas de validez (Validity Proof, Star/Stark), les valdrá para verficar el estado correcto y añadirlo en la red principal o incorrecto y rechazarla.

## Conceptos (10 min) 

Podemos tener definiciones de muchos conceptos que al final ejecutan casi la misma función, así que debemos entender mejor cada uno de ellos y sus siglas antes de seguir. Es importante recalcar, que hay algunos proyectos que usan estas palabras para crear _fomo_ y caer en _la trampa_, no siendo lo que dicen ser. [Ejemplo: Shiba Layer2 forked de Matic/network](https://github.com/shibaswaparmy/contracts)
  
  ![Graph](/im%C3%A1genes/zkRollup.png)

- **Rollup:** La esencia central de un Rollup es envolver transacciones por lotes para reducir los costes y descongestionar los envíos que tiene la capa principal. Podemos analógicamente verlo como los envios de varios usuarios/protocolos de varias transaciones (mint NFT, swap, envios de ERC-20) en una sóla, como varios ciudadanos tomamos el Autobus o Metro para ir al mismo destino juntos y descongestionar la red principal a la vez que abaratamos costes.
- **Zk:** Prueba de conocimiento cero es una forma de dar vericidad de un secreto sin revelar ninguna información confidencial. Podemos verlo con varios ejemplos (Cueva de alibaba, Caja fuerte y reloj...)
- **Optimistic Rollup:** En un tipo de Layer 2 en que sus transacciones son del tipo de `Rollup `, heredando la seguiridad y Ethos (Valores, visión) de ETH. Estos Optimistic Roolup se basan en pruebas de fraude `Fraud Proof` para demostrarle a la Layer 1 de ETH que el estado es correcto, estas pruebas se basan en teoría de juegos y tienen un periodo de actuación para revisión, haciendo que retiro a la cadena principal pueda durar de 7 días usando su puente nativo.
- **Fraud Proofs (Optimistic Rollup):**Es el nombre reciben las pruebas de estado de validación a la cadena principal, las pruebas serán del tipo fraude para los Optimistic Rollup, que dejarán pasar las transacciones, se basan en la teoría de juegos y que siempre habrá un `"Revisor honesto"` comprobando que el estado sea el correcto. Tendrán un periódo de 7 dias para retiros y los secuenciadores que hayan añadido los lotes si enviaron una prueba errónea, `"perderán su garantía"`, no siendo muy rentable mientras haya un `"Verificador honesto"`.
- **Zk-Rollup o Validity Rollup:** Hacen referencia a unos tipos de Layer 2 que usan Rollup (Lotes de transacciones), que cumplen con zk (Conocimiento Cero), estos añaden una pruebas pruebas matemáticas supercomplejas que demuestran que el cálculo es el correcto sin tener que revelar todos los datos. Una parte de esos cálculos se realizan off-chain de la cadena principal no sobrecargándola. La definición de Validity Rollup salió de Starknet y sus Validity Proof (Pruebas de validez), que se diferencian en su cálculos de pruebas matemáticas las STARK frente las SNARK.
- **Zk-Proof o Validity Proof (Snark y Stark):** Las pruebas presentadas como Zk-Proof o Validity Proof son matemáticamente realizadas y comprobables, no teniendo que esperar ningún tiempo de retiro como las Pruebas de Fraude (Fraud Proofs), más allá del de la creación de las pruebas y envíos de estas pruebas. Todos los Validity Rollup y Zk-Rollup usan este tipo de pruebas para actualizar el estado correcto de la cadena principal. 
* En Starknet, creadores de STARK se les da el nombre de Validity Rollup a este tipo de soluciones haciendo muy parecida a Zk-Rollup en su definición. Usadno Validity Proof
* zkSync 2.0 son un Zk-Rollup que usan también estas pruebas matemáticas pero denominadas Zk-Proof,  sus pruebas se basan en SNARK, las diferencias entre ambas dependerá de mucho tecnisismo para diferenciarlos, pero la principal es que las STARK son algoritmos resistentes a un posible ataque cuántico.
  
![Graph](/im%C3%A1genes/Tabla.jpeg)

Con estos conceptos vemos como diferenciarlos, como crean tanta confusión por sus similitudes, el porque de tantos diversos nombres y como algunos malos actores se podrían aprovechar de esos juegos de palabras. 

## Analogía (10 min)

![Graph](/im%C3%A1genes/OptimismVszkRollup.jpg)

En ella haremos una comparación entre Layer 1 de Ethereum (Carretera General), con su seguridad PoS y Fundación (Sindicato Internacional de Carreteras) y cómo esta carretera general con sus normas, limitaciones, cogestiones de tráfico, busca soluciones para los conductores que puedan ir por otras carreteras secundarias (Layer 2) para llegar cada uno, a sus dos principales ciudades OptimisTrum y StarkSync (Optimism Rollup y Zk-Rollup o Validity Rollup). Veremos como se crean estas carreteras heredando los materiales para la seguridad del primero y como cada ciudad monta sus carreteras secundarias, peajes, con distintas tecnologías y pensamientos (Pruebas de Fraude o Pruebas de Validez) para volver a Layer 1 o carretera general).

### Carretera General 

* **Características:** Normas generales para todas las vías o `"Espacios"` que esten dentro de su juridicción o consenso.
* **Seguridad:** La seguridad máxima de todos los `Sindicatos de Carreteras Internacionales` (PoS).
* **Escalabilidad:** Su coste y transacciones por esta vía suelen ser elevadas, cumplen requisitos estandar (ETH) del Sindicato de Carreteras Internacionales y necesita un periodo para la votación de cambios, acepetación y ejecución para poder construir mejores carreteras sin congestionar todas las vias y colapsando a los conductores. (Ethereum y su roadmap)
* **Descentralización:** Aquí dependerá de como este organizado ese `Sindicatos de Carreteras Internacionales` y si son de verdad lo que quieren el pueblo y necesitan los conductores, adaptándose y teniéndoles en cuenta o simplemente hacen de organismo central y censura organizando las carreteras como les da la gana. En este caso son un buen organismo central que dejan que cada ciudad (Layer 2), proponga y cree unas carreteras secundarias, heredando la seguridad de la Carretera General (POS) dado que el Sindicato usará el mismo material y obreros con la que han fabricado la Carretera General, todo para no tener errores de Seguridad de `Empresas Pequeñas`.

Las empresas pequeñas crearán según sus necesidades, principios e ideas soluciones para poder ir a 2 ciudades. Algunas teniendo en cuenta más a sus ciudadanos con encuestas y otras no tanto, pero todas estas carreteras deberán cumplir con la norma de la Carretera General, que es muy simple. 

**`Deben coincidir el mismo número de entradas y salidas de coches. Fin`**

Entonces cada empresa pequeña (Layer 2) empieza a gestionar y ver distintos tipos de usos. Y cada ciudad **`OptimisTrum y StarkSync`** propone mediante sus ciudadanos unas formas diferentes de llegar a la carretera general y como construirlas. Son ciudades no muy alejadas pero si muy grandes y con mucho tráfico por la Carretera General para llegar a ellas todos los dias, ya que muchos van y vienen por motivos laborales. 

### OptimisTrum City y Carreteras

Desde la Carretera General hacia OptimisTrum se crearán unas carreteras secundarias, todas hacia una central de peajes, más baratos y directo en el que todos irán a OptimisTrum City. Esta descongestionará mucho la Carretera General. Esta ciudad se puso de acuerdo para ofrecer a sus ciudadanos la tranquilidad que todos los viajes en estas carreteras secundarias sean más económicos, pero deberán de cumplir las normas e irán en la medida de lo posible juntos en un mismo vehículo o en lotes de varios vehiculos. Está hecha para viajar en lotes humanos o de vehículos a OptimisTrum desde el peaje y descongestionar las horas puntas, aunque también puede optar por tardar más y pagando más e ir por Carretera General.

En el Control de Peaje sólo deberás verficar que el coche es tuyo, que eres tú el que lo conduce, tú matrícula, marca, modelo, seguro..., una fotocopia cuñada te valdrá. Al salir de nuevo en el peaje ellos verifcarán por encima esta fotocopia con estos datos, pero de una forma sencilla, también sonreriarás a la cámara/vigilante para la foto y te dirá **`(Ah si, creo que eres tú)`** (Pruebas de Fraude o Fraud Proof) y te dejará pasar, `que buena fé`.

Aunque puede ser que a los 7 días en tu registro de OptimisTrum City a través de los verificadores de la Carretera General y vean que no has sido de verdad el conductor principal y no has cumplido las normas, te llega la sanción correspondiente a ti o al que te haya dejado pasar, normalmente al que haya dejado la fianza y este comprobando como organismo de Carretera General su seguridad en el peaje, en este caso aquellos hombres que trabajan para el peaje y dan permiso o no a pasar las transacciones de los lotes de vehiculos serán los culpables de esta situación. El **"Ah si, creo que eres tú"** tiene un periodo de 7 dias antes de que pase nada, como vas todos los dias al trabajo se fian un poco más de lo normal, pero también algunos podrán perder su trabajo o sus sanciones corresponientes en caso de que no haya sido así.

### StarkSync City y carreteras.

Desde la Carretera General hacia StarkSync se crearán unas carreteras secundarias, todas hacia una central de peajes, más baratos y directo en el que todos irán a StarkSync City. Esta descongestionará mucho la Carretera General. Esta ciudad tendrá la misma visión general que OptimisTrum City, descongestionar la principal y que sus conductores puedan llegar a su ciudad de una forma más rápida y económica, pero sin perder la seguridad de sus carretera. 

Tienen una visión un poco más sofisticada pero respetando cumplir con la norma **"Deben coincidir el mismo número de entradas y salidas de coches. Fin"**. Así que pensaron ¿por qué no puedo dejar el coche en el peaje e irme en Autobus?. Las llaves biométricas (Validity Proof) pueden ser una prueba de que ese coche es el mío y sólo yo puedo arrancarlo (Zk), ya que para que el coche camine necesita esta validación matemática entre la llave, coche y usuario. 

La llave biométrica deberá guardarla bien, podrá circular con su coche hacia la ciudad en lotes humanos o de vehículos, también podrá viajar en Autobús, Tren o cualquier otro medio construido en el "Territorio" hacia StarkSync. Los trenes te pedirán una confirmación de que tienes permiso para ir a StarkSync, la llave y un lector será suficiente para saber que biométricamente es sólo la tuya y estas cumpliendo las normas. **(la ciudad es muy grande está Snark parte Alta y Stark parte baja...)** así que cada Tren o Autobus pueden usar un lector prueba distinta (Stark/Snark) pero todos verificarán matemáticamente lo mismo.

En el regreso a la Carretera General deberán volver por la central de peajes, pero estos informamos que son algo más sofisticado y no tendrá a ninguna cámara o empleado honesta verificando que eres tú el del coche. Funciona por cámaras y sensores que directamente sabe que es tú llave biométrica y tú coche, así que al menos que haya otra llave igual o otro conductor igual no creo que puedas evitar pasar el peaje **NO LO CREO**. También pueden cambiar otros datos y saber que cumples las normas (circular sin la matrícula, ir disfrazado o que tu vehiculo ahora luzca de otro color) no será motivo ni de revisión y automáticamente te deberían dejar pasar a la Carretera General. En un caso que tuvieras el Seguro vencido, no cumplirias con las normas de los `Sindicatos de Carreteras Internacionales` y tu prueba seguramente sea erróna, no te sorprendas si no te arranca el vehículo.

### Problemas en Peajes

Si todo va bien desde ambas ciudades podrá salir y entrar sin ningún problema, al menos que estén cerrados los peajes. Estos recuerden que aun no son Sindicatos Descentralizados como la Carretera General, si no que estan empezando y son empresas los que controlan y ejecutan todo esto con profesionalidad pero con el factor humano támbien dentro de la actualización.

Y como cada carretera secundaria mantiene una visión y misión igual pero a su vez distinta, estas ciudades y empresas pequeñas tendrán mucho poder, ya que la gente puede decide donde vivir. 

**Si te dejan salir, si.**

## L2 Beat, RISK and FEE (10)

- Principales Layer 2 [L2 Beat](https://l2beat.com/). 

Antes de entrar en cada Layer deberiamos aclarar como Starkware desarrolla StarkEx y es diferente a Starknet, este se implementa como disintos tipos de soluciones para intercambios sobre la LAYER 1

- StarkEx es un SaaS de capa 2 independiente y personalizable para intercambios que utiliza el sistema de prueba STARK para proporcionar una escalabilidad masiva. 

![Graph](/im%C3%A1genes/starkex.png)

- StarkNet es una red de uso general en la que puede escribir e implementar sus propios contratos inteligentes, interactuar con otros contratos, etc., al igual que Ethereum. Es un Validity Rollup descentralizado sin permiso (a menudo denominado Zk-Rollup). Opera como una red L2 sobre Ethereum, lo que permite que cualquier dApp alcance una escala ilimitada para su cálculo, sin comprometer la compatibilidad y la seguridad de Ethereum. Basadas en STARKs

![Grap](/im%C3%A1genes/Layer3.png)

- L2 Beat: Noc centraremos en las dos soluciones principales y Validum.

  - **(Optimism Rollup y Arbitrum Rollup,)** Rollup Optimistic
  - **(Dydyx y Loopring)** Zk-Rollup
  - **(InmutableX)** Validium (Zk-Rollup. Data no se guarda en Layer 1 la guarda DAC)
    
- [Riesgo:](https://l2beat.com/scaling/risk) Riesgos sobre TVL con el token de Gobernanza en las distintas Layer. Riesgos de centralización del prover o secuenciandor. Riesgos de actualización de contratos, tanto partes ventajosas como parte negativas de este tipo de Upgradabilidad. 
 Ventajas: Ante cualquier vulnerabilidad o xploit detectado `rápida` reacción. Con `Relay 14 días` no puedes actuar sino avisar.
 Desventaja: Ante cualquier vulnerabilidad, xploit no detectado o mala actualización `mala` reacción al no tener `Relay de tiempo` para avisar a los usuarios y tener márgen para actuar.
 Periodo de Salida forzosa a veces no acorde con el Relay y la Upgradabilidad, haciendo que algunas partes seguras no lo sean tanto.

Destacar que todas las soluciones de Layer 2 están por ahora centralizadas y están en continuas actualizaciones por seres humanos que llevan los proyectos, algunos serán muy buenos y profesionales o no, pero siempre seguirá estando el factor humano por medio hasta que esten completamentes acabadas. Por ejemplo, Starknet está en alpha 0.11 de testnet y en Cairo 1.0 de alpha en la mainnet. (Esta se basará en un regéneis para comenzar todo en su mainnet con lazamietno final de Cairo 1.0), en este paso la idea es tener descentralizado por completo prover (comprueba y ejecuta la prueba muy compleja) y secuenciador (añade la transacción con la prueba de prover en la capa principal). 

Esta parte de centralización suele usarse como analogías con los Bridges, recordar que muchos de ellos montados en Sidechain agregando capas de riesgo, al final las Layer 2 también tienen sus Contratos con sus Bridge pero más sofisticados y con otras seguridades. Como dijimos inicialmente a vista de Ethereum las Layer 2 sólo son Smart Contracts, pero no todas las Layer 2 funcionan igual como hemos visto, sus códigos internos no tienen porque ser iguales y sus VM (Virtal Machine) también varian en su equivalencia y compatibilidad con la EVM (Ethereum Virtual Machine). 

Algunos grandes avances en Layer 2 son Starknet y zkSync que están desarrollando grandes novedades sobre AA (Account Abstraction) y otras nuevas tecnologías con sus Pruebas de Validez (Stark/Snark) que pueden hacerse posible que una Layer 2 o Layer 3 mejore en privacidad, escalabilidad, herede la seguridad de Ethereum y una posible L3 a un coste por recursividad de las pruebas aún menor que en algunos casos de L2.

![Graph](/im%C3%A1genes/L2Risk.png)

## Guerra de Layer 2 y L2Beat (5 min)

Aquí es donde entra las guerras donde cada tipo de solución quiere ser más o menos compatible con Ethereum y su `ETHOS` o los principios que quieran mantener. 
 
Según VB podemos diferenciar en varios tipos de compatibilidades también su maquinas virtuales, códigos de programación de estos contratos inteligentes o herramientas utilizadas para su equivalencia no compatibilidad.

1. Tipo 1 (totalmente equivalente a Ethereum)
Los ZK-EVM de tipo 1 se esfuerzan por ser total e inflexiblemente equivalentes a Ethereum. No cambian ninguna parte del sistema Ethereum para facilitar la generación de pruebas. Su principal ventaja es la compatibilidad, y los proyectos de este tipo son necesarios para "hacer Ethereum más escalable".

    - Ventaja: compatibilidad perfecta
    - Desventaja: tiempo de prueba

Taiko  

2. Tipo 2 (totalmente equivalente a EVM)
Los ZK-EVM de tipo 2 se esfuerzan por ser exactamente equivalentes a EVM, pero no del todo equivalentes a Ethereum. Es decir que, si bien no es totalmente compatible con Ethereum, sí lo es con los contratos inteligentes creados en esta red.  

El objetivo es ser totalmente compatible con las aplicaciones existentes, pero realizar algunas modificaciones menores en Ethereum para facilitar el desarrollo y acelerar la generación de pruebas.

    - Ventaja: equivalencia perfecta a nivel de VM
    - Desventaja: tiempo de comprobación mejorado pero aún lento

    > Tipo 2.5 (equivalente a EVM, excepto para los costos de gas)

Scroll, y según Polygon [zkEvm Polygon](https://polygon.technology/blog/polygon-zkevm-within-vitaliks-framework-gaining-clarity-and-looking-ahead)

3. Tipo 3 (casi equivalente a EVM)
Los ZK-EVM de tipo 3 son casi equivalentes a EVM, estos ZK hacen (unos pocos sacrificios) para mejorar los tiempos de comprobación y las posibilidades de desarrollo.

    - Ventaja: más fácil de construir y tiempos de comprobación más rápidos
    - Desventaja: más incompatibilidad

zkEvm Polygon según Vitalik Buterin, aquí vemos la complejidad de poder evaluarlas.

    - Ventaja: más fácil de construir y tiempos de fermentación más rápidos
    - Desventaja: más incompatibilidad
<br>
4. Tipo 4 (equivalente a lenguaje de alto nivel)
Un sistema Tipo 4 funciona al tomar el código fuente del contrato inteligente escrito en un lenguaje de alto nivel (por ejemplo , Solidity , Vyper o algún intermedio en el que ambos se compilen) y compilarlo en algún lenguaje que esté diseñado explícitamente para ser compatible con ZK-SNARK.

    - Ventaja: tiempos de comprobación muy rápidos
    - Desventaja: más incompatibilidad

Starknet - zkSync

Por este tipo de variaciones cada una tiene su propia guerra, algunas con comunidades más fuertes, otros con ingenieros matemáticos muy buenos pero con un marketing no tan adecuado...Desde mi opinión tanto Optimism, algunas otra como zkSync 2.0, Scroll, zkEVM Polygon pueden estar muy bien, también creo que Starknet se está preparando a pruebas de bombas con todo lo incoporado en otras soluciones además de mejoras como Stark principalmente como algoritmo de cifrado resistente anti ataques de computación cuántica.

## Preguntas (20 min)
