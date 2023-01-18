# Nadai Layer 2 DefiLab

## Introducción a layer 2 (5 min)

- Layer 1 seguridad POS de Eth: Esta blockchain se basa en pruebas de participación entre muchos nodos, siendo la red princpial de ETH. 
- Problemas de ETH: Necesita descongestionar la red y seguir luchando por la seguridad y descentralización.
- Sidecheain: Esta blockchain tiene su propia forma de validar la cadena, con su propio conceso teniendo como principal inconveniente que no hereda la seguirdad de ETH.
- Layer 2 hereda seguridad POS de eth: Esta blockchain puede configurarse de diferentes formas que iremos tratando, pero la principal ventaja frente a la sidechain son que heredan la seguirdad completa en la capa de ETH.

  ![Graph](/im%C3%A1genes/sidechain.png)

  - Layer 2 son contratos inteligentes a simple vista de ETH, de ahí que en L2Beat marquen parámetros de actualizaciones y otros riesgos que evaluaremos al final.

  Layer 1 sólo le importa que la salida y entrada coindidan en ambas Layer, esto significa que mientras a la red principal de ETH le demuestren por pruebas de fraude (Optimism Rollup) o por pruebas matemáticas (Snark/Stark), verficarán que el estado es el correcto.

## Conceptos (5-10 min) 

  Solemos tener muchos conceptos que al final hacen casi la misma función, así que debemos entender un poco cada un de ellos y sus siglas antes de seguir y entender que muchos proyectos usan estas palabras para crear fomo y caer en la trampa de no ser lo que dicen ser. (Ejemplo Shiba Layer2 forked de Matic/network oficial de github)
  
  ![Graph](/im%C3%A1genes/zkRollup.png)

  - Rollup: La esencia central de un Rollup son envolver transacciones por lotes para reducir los costes de envios que tiene la capa principal.
  - Optimistic Rollup: Es un tipo de Rollup que se ejecutan como capa 2 heredando la seguiridad y camino de ETH, esta se basa en un tipo de pruebas de fraude para demostrar que el estado es correcto, estas pruebas se basan en teoria de juegos y tienen un periodo de actuación, retiro a la cadena principal de 7 dias usando su puente nativo. 
  - Zk: Prueba de conocimiento cero es una forma de dar vericidad de un secreto sin revelar ninguna información confidencial. Podemos verlo con varios ejemplos (Cueva de alibaba, Caja fuerte y reloj...)
  - Zk-rollup, Zk Proof o Validity Proof (Stark y Snark): Estos hacen referencia a un Rollup que cumple con zk, estos básicamente son pruebas matemáticas supercomplejas que demuestran que el cálculo es el correcto, no teniendo que esperar ningún tiempo más hayá del de la creación de las prueba y envío de prover al secuenciador. Estas básicamente son dos SNARK y STARK, las que se ejecutan prácticamente en todos los zk Rollup. En Straknet se les da el nombre de Validity Proof a este tipo de soluciones haciendo muy parecida a zk Rollup en su definición, aquí tendriamos que entrar en mucho tecnisimo para diferenciarlos y muchos aprovechan ese juego de palabras.

![Graph](/im%C3%A1genes/Tabla.jpeg)


## Analogía (10 min)

Aquí podemos empezar con la anología. 

![Graph](/im%C3%A1genes/OptimismVszkRollup.jpg)

Haremos una comparación entre Layer 1 de ETH (Carretera General), con su seguridad POS y Fundación (Sindicato Internacional de Carreteras) y cómo esta carretera general con sus normas, limitaciones, cogestiones de tráfico, busca soluciones para los conductores que puedan ir por otras carreteras secundarias (Layer 2) para llegar cada uno a sus dos principales ciudades Optimitrum y StarkSync (Optimism Rollup y zk Rollup o Validity Proof). Veremos como se crean estas carreteras heredando los materiales para la seguridad del primero y como cada ciudad monta sus peajes (Pruebas para volver a su Layer 1 o carretera general).

### Carretera General 

* Caractersiticas: Normas generales para todas las vías o "Espacios" que esten dentro de su juridcción o concenso.
* Seguridad: La seguridad máxima de todos los Sindicatos de Carreteras Internacionales (POS)
* Escalabilidad: Su coste y transsaciones por esta vía suelen ser elevadas, cumplen requisitos estandar de la Fundación del Sindicato y necesita un periodo para poder contruir mejores carreteras sin congestionar a los usuarios. (ETH y su roadmap)
* Descentralización: Aquí dependerá de como este organizado esos sindicatos y si son de verdad lo que quieren el pueblo y necesitan los conductores, adaptándose y teniéndoles en cuenta o simplemente hacen de organismo central y censura organizando las carreteras como les da la gana. En este caso son un buen organismo central que dejan que cada suborganismo (Layer 2) cree unas carreteras secundarias, heredando la seguridad de la Carretera General (dado que iran con el mismo material y obreros que han fabricado todo para no tener errores de compañias pequeñas).

Las compañias pequeñas crearán según sus necesidades y principios para poder ir a sus 2 ciudades. Algunas teniendo en cuenta a sus ciudadanos otras no tanto, pero con unas carreteras que cumplan con las normas de la Carretera General, que son muy simples. 

**`Tienen que entrar y salir los mismos coches. Fin`**

Entonces cada miniempresa empieza a gestionar y ver distintos tipos de usos, se le ocurre el crear una comunidad que "decida" como ir a OptimisTrum y StarkSync. Unas ciudades no muy alejadas pero si muy grande y con mucho tráfico por la Carretera General para llegar a ellas todos los dias, ya que muchos van y vienen por motivos laborales. Asi que deciden crear una carretera secundaria para desviarse y luego ir a sus ciudades.

### OptimisTrum City y carreteras

Al ir por esta carretera crean un divifurcación hacia una central de peajes, más baratos y directo en el que todos irán a OptimisTrum Cyty, así que se descongestionará mucho la carretera principal. Ellos ofrecen la tranquilidad que todos viajes juntos por los carril en un minímo de vehículos, ya que está hecho para viajar en lotes a la ciudad desde el peaje y descongestionar las horas puntas, ya que del resto pueden optar por el otro camino si quiseran.

En el peaje deberás verficar que el coche es tuyo, que eres tú el que lo conduce, tú matrícula, marca, modelo, seguro .... AL salir de nuevo en el peaje ellos verifcarán de nuevo estos datos, pero de una forma sencilla, sonreriarás a la cámara y te dirá **`(Ah si creo que eres tú)`** y te dejará pasar, `que buena fé`.

Aunque puede ser que a los 7 días en tu registro de OptimisTrum City a través de los verificadores de la Carretera Genereal y vean que no has sido de verdad el conductor principal y no has cumplido las normas, te llega la sanción corresponiednte a ti, o al que te haya dejado pasar está claro, normalmente al que haya dejado la fianza y este comprobando como organismo de Carretera General su seguridad en el peaje, en este caso aquellos hombres que trabajan para el peaje y dan permiso o no a pasar las transacciones de los lotes de vehiculos serán los culpable de esta situación el **"Ah si creo que eres tú"** tiene un periodo de 7 dias antes de que pase nada, pero vas todos los dias al trabajo y se fian un poco más de lo normal, pero también algunos podrán perder su trabajo o sus sanciones corresponientes en caso de que no haya sido así.

### StarkSync City y carreteras.

Esta carretera tendrá la misma visión general que OptimisTrum City, descongestionar la principal y que sus conductores puedan llegar a su ciudad de una forma más rápida y económica, pero sin perder la seguridad de sus carretera. Aunque tiene una visión un poco más hayá creyendo que no tienen que cumplir exactamente con las mismas normas que han querido hacer el sindicato de la Carretera General, es decir, la única norma que había era **"Tienen que entrar y salir los mismo coches. Fin"**. Así que bueno, ¿por qué no puedo dejar el coche en el peaje? solo aparcándolo, las llaves son mías así que no tengo por que dar más pruebas que estas a nadie creo yo, para que el coche matemáticamente me valide el arranque (Zk) 

Así que me las guardo en lugar muy seguro y procedo a subirme en un tren destino StarkSync, pueden haber varios trenes algunos te pedirán la llave para pasarla por un lector y saber que biometricamente es sólo la tuya y estas cumpliendo las normas, otros simplemente una firma, otros directamente iran en Autobus dado que les queda más cerca su casa **(la ciudad es muy grande está Snark parte Alta y Stark parte baja...)** así que cada uno puede pedir un tipo de prueba distinta, algunos directamente se van en su coche no quieren dejar las llaves a nadie.

Todos cuando terminan y vuelven a la Carretera General deberán pasar por el peaje, pero este informamos que es algo más sofisticado y no tendrá a nadie verificando que eres tú el del coche, va por cámaras y sensores que directamente sabe que tu llave sólo arrancaba ese coche y esa llave viene programada con una prueba biometrica a un único conductor, así que al menos que haya otra llave igual o otro conductor igual no creo que puedas evitar pasar el peaje **NO LO CREO**. También puede revisar otros datos y saber que cumples las normas aunque se te haya caido la matricula, vayas disfrazado o tu vehiculo ahora luzca de otro color, pero siempre te deberían dejar pasar a la Carreterera General

### Problemas en Peajes

Si todo va bien desde ambas ciudades podrá salir y entrar sin ningún problema, al menos que estén cerrado los peajes. Estos recuerden que aun no son Sindicatos Descentralizados como la Carretera General, si no que estan empezando y son empresas los que controlan y ejecutan todo esto con profesionalidad pero con el factor humano támbien dentro de la actualización.

Y como cada carretera secundaria mantiene una visión y misión igual pero a su vez distinta, estas ciudades y empresas pequeñas tendrán mucho poder, ya que la gente puede decide donde vivir no?. Si te dejan salir si.

## L2 Beat, RISK and FEE (10)

- Principales Layer 2. (L2 Beat). Antes de entrar en cada Layer deberiamos aclarar com Starware desarrolla StarkEx es diferente a Starknet, este se implementa como disintos tipos de soluciones para intercambios sobre la LAYER 1)

- StarkEx es un SAAS de capa 2 independiente y personalizable para intercambios que utiliza el sistema de prueba STARK para proporcionar una escalabilidad masiva. 

![Graph](/im%C3%A1genes/starkex.png)

- StarkNet es una red de uso general en la que puede escribir e implementar sus propios contratos inteligentes, interactuar con otros contratos, etc., al igual que Ethereum. Es un Validity-Rollup descentralizado sin permiso (a menudo denominado ZK-Rollup). Opera como una red L2 sobre Ethereum, lo que permite que cualquier dApp alcance una escala ilimitada para su cálculo, sin comprometer la compatibilidad y la seguridad de Ethereum. Basadas en Starks

![Grap](/im%C3%A1genes/Layer3.png)

- L2 Beat: Nombrar sólo las dos soluciones principales y Validum por encima

  **(Optimism Rollup y Arbitrum Rollup,)** Rollup Optimistic
  **(Dydyx y Loopring)** Zk Rollup
  **(InmutableX)** Validium (Zk Rollup Data no se guarda en Layer 1)


    
- Riesgo: Riesgos sobre TVL con el token de Gobernanza en las distintas Layer. Riesgos de centralización del prover o secuenciandor. Riesgos de actualización de contratos, tanto partes ventajosas como parte negativas de este tipo de Upgradabilidad. Periodo de Salida forzosa a veces no acorde con el Relay y la Upgradabilidad, haciendo que algunas partes seguras no lo sean tanto.

Destacar que todas las soluciones de Layer 2 están por ahora centralizada y están en continuas actualizaciones por seres humanos que llevan los proyectos, algunos serán muy buenos y profesionales o no, pero siempre seguirá estando el factor humano por medio hasta que esten completamentes acabadas. Por ejemplo Starknet está en alpha 0.11 de testnet y en Cairo 1.0 de alpha en la mainet. (Esta se basará en un regéneis para comenzar todo en su mainet), en este paso la idea es tener descentralizado por completo prover (comprueba y ejecuta la prueba muy compleja) y secuenciador (añade la transacción con la prueba de prover en la capa principal). 

Esta parte de centralización suele usarse como analogías con los Bridges, al final ellos también tendran Bridge, y como dijimos inicialmente a vista de ETH sólo son Smart Contract, por eso en Layer 2 como Starknet se están desarrollando grandes novedades sobre AA y como nuevas tecnologías pueden hacer pueden hacerse posible en una Layer 2 o 3 heredando la seguridfad de ETH y a un coste por recursividad aun menor en algunos casos.

![Graph](/im%C3%A1genes/L2Risk.png)

## Guerra de Layer 2 y L2Beat (5 min)

 Aquí es donde entra las guerras en que cada tipo de solución quiera ser más o menos compatible con ETH y los principios que quieran mantener. 
 
 Según VB podemos diferenciar en varios tipos de comptabilidades también su maquinas virtuales, códigos de programación de estos contratos inteligentes o herramientas utilizadas para su equivalencia no compatibilidad.

1. Tipo 1 (totalmente equivalente a Ethereum)
Los ZK-EVM de tipo 1 se esfuerzan por ser total e inflexiblemente equivalentes a Ethereum. No cambian ninguna parte del sistema Ethereum para facilitar la generación de pruebas. No reemplazan hashes, árboles de estado, árboles de transacciones, precompilaciones ni ninguna otra lógica consensuada, sin importar cuán periférica sea.

Ventaja: compatibilidad perfecta
Desventaja: tiempo de prueba

2. Tipo 2 (totalmente equivalente a EVM)
Los ZK-EVM de tipo 2 se esfuerzan por ser exactamente equivalentes a EVM, pero no del todo equivalentes a Ethereum. Es decir, se ven exactamente como Ethereum "desde adentro", pero tienen algunas diferencias en el exterior, particularmente en estructuras de datos como la estructura de bloques y el árbol de estado .

El objetivo es ser totalmente compatible con las aplicaciones existentes, pero realizar algunas modificaciones menores en Ethereum para facilitar el desarrollo y acelerar la generación de pruebas.

Ventaja: equivalencia perfecta a nivel de VM
Desventaja: tiempo de fermentación mejorado pero aún lento

Tipo 2.5 (equivalente a EVM, excepto para los costos de gas)

3. Tipo 3 (casi equivalente a EVM)
Los ZK-EVM de tipo 3 son casi equivalentes a EVM, pero hacen algunos sacrificios para lograr la equivalencia exacta para mejorar aún más los tiempos de fermentación y hacer que el EVM sea más fácil de desarrollar.

Ventaja: más fácil de construir y tiempos de fermentación más rápidos
Desventaja: más incompatibilidad

4. Tipo 4 (equivalente a lenguaje de alto nivel)
Un sistema Tipo 4 funciona al tomar el código fuente del contrato inteligente escrito en un lenguaje de alto nivel (por ejemplo , Solidity , Vyper o algún intermedio en el que ambos se compilen) y compilarlo en algún lenguaje que esté diseñado explícitamente para ser compatible con ZK-SNARK. .

Ventaja: tiempos de fermentación muy rápidos
Desventaja: más incompatibilidad

Por este tipo de variaciones cada una tiene su propia guerra, algunas con comunidades más fuertes, otros con ingenieros matemáticos muy buenos pero con un marketing no tan adecuado...Desde mi opinión tanto Optimism, algunas otra como zkSync 2.0 o Scroll pueden estar muy bien, pero creo que Starknet se está preparando a pruebas de bombas con todo lo incoporado en otras soluciones, mejoras como Stark principalmente como algoritmo de cifrado resistente a un ataque de computación cuántica.

## Preguntas (20 min)
