# Transcripciones — Relevamiento Facultad de Derecho UNNE (Campus Deodoro Roca)

Recorrido del 13/11/2026. Transcripción automática hecha en dos pasadas (audio original y audio con filtro de ruido) y unificada a mano.

Cómo leerla:

- **E:** la encargada de la red. **A:** alumnos (ustedes).
- `[inaudible]` = no se entiende en ninguna de las dos pasadas.
- `[¿...?]` = palabra dudosa; lo que está adentro es mi mejor interpretación.
- Se quitaron saludos y charla no técnica. Los tiempos son aproximados.

---

## Audio 0 — WhatsApp Ptt 09.44.39 (1:25) — Gabinete de planta baja, inicio del recorrido

**[0:00] E:** Ese es el que tiene menor velocidad. Y el de abajo [inaudible], ese es WiFi 6, y ese trabaja sobre [inaudible]. Arriba [¿Gigared?], abajo UNNE. Y el de arriba está desconectado, está desconectado el plato. O sea que el uplink está trabajando desde abajo: tiene la fibra, conecta, conecta, conecta, pero solamente planta baja está con los [inaudible].

**[0:30] E:** Son switches. Son switches que vienen, el de abajo, con módulo de fibra, y después lo que conecta...

**[0:45] E:** Acá van a ver que el switch viene por esta parte [¿serial / fibra?] y esta parte por UTP.

**[1:00] E:** Lo ideal sería que uno conecte un módulo de fibra con otro módulo de fibra, así no se pierde velocidad, pero no tenemos. Entonces tenemos un módulo de fibra abajo y después ya seguimos con esto [UTP].

---

## Audio 1 — Campus Deodoro Roca (4:59) — Sector A, decanato y gabinete principal

**[0:00] E:** Ahora vamos a ver cómo pasamos de WiFi 6 a la anterior, que trabajaba con [WiFi] 5, que son los Ubiquiti UniFi. Al sector A.

**[0:15] E:** Este que está acá, ¿ves? Ya bajamos a [inaudible] en este sector. Este sería el sector A, todas estas oficinas.

**[0:30] E:** Como el [¿director / rector?] quería darle el WiFi bueno a los estudiantes, para las oficinas se dejó la versión anterior, que a su vez queda acá por si se cae. Y para todo donde haya alumnos o eventos se pone el WiFi 6.

**[1:00] E:** Acá está el decanato. Se puso un plato de refuerzo más para allá, porque con dos paredes ya se cae [la señal].

**[1:15–1:40]** `[inaudible — entran a la sala del gabinete principal]`

**[1:45] E:** No toquen nada. Pasen de a dos porque no entran todos.

**[1:55] E:** Por ahí viene la fibra. ¿Ves el naranja? Ahí está el módulo de fibra. Y tenés la parte que va cableado de red, y todo lo que sea Omada es para el cableado WiFi. Acá está todo, este es el principal. Y todavía faltan los de Telco [Telecom], que le van a agregar más.

**[2:15] E:** Este es el servidor donde se configura en modo remoto cuando hay problemas. Debería estar prendido, no sé si está. Todo tiene su UPS.

**[2:30] E:** Y después los otros son cámaras. ¿Se entiende? Ahora salgan, que vean los otros chicos.

**[2:40] E:** Este es el gabinete principal. La fibra viene por el camino, ¿viste donde camina la gente?, en forma subterránea. Después sube y se conecta a Odontología. Nosotros dependemos del nodo Odontología. Entonces cuando hay una obra de construcción —playa de estacionamiento, agua— por ahí cortan la fibra y quedamos afuera.

**[3:05] A:** O sea, ¿esto viene de la calle y acá se deriva todo?
**E:** No es de la calle, es de allá, de dentro del campus. De la calle viene el de Telco.
**A:** ¿Pero esto le brinda todo para adentro?
**E:** Sí, todo. Alimenta toda la facultad.

**[3:20] A:** ¿Y acá qué dispositivos tiene?
**E:** Tenés switches Cisco, tenés el UniFi para la parte de Gigared. O sea que Gigared también está viniendo por acá. Vas a ver dos de fibra, lo que sea naranja: uno que viene por allá y otro por allá. Uno va a un equipo que es el de Gigared y el otro va al otro equipo, que es el nuestro.

**[3:45] E:** Y te vas a ubicar más o menos cuál es cuál porque los [cables] categoría 6 son los nuestros, y los 5 son los que trabajan con Gigared. O sea, acá tenemos las dos cosas. Si hay un problema eléctrico acá, queda afuera todo.

**[4:00] A:** ¿Estos monitores qué revisan?
**E:** Para configurar si cae algo, porque a veces un puerto se desconfigura, o para ver qué plato está caído.

**[4:10] A:** ¿Ustedes tienen algún sistema para monitorear todo?
**E:** Sí. La interfaz administradora no sé cómo se llama, pero trabaja sobre Linux. [Eso es] para la parte de Gigared. La otra en realidad va por Rectorado.

**[4:30] A:** Con respecto a los cortes, ¿tienen algún generador?
**E:** ¿Cómo se llama el que te da energía cuando hay cortes? Grupo electrógeno. No lo tenemos. Aguantan unos minutos [las UPS]. Somos pobres. Cuando hay un evento muy importante, se alquila.
**A:** O sea que el respaldo de energía son las UPS.
**E:** Sí, nada más.

**[4:55] E:** Y después tenemos una jabalina, no sé si la ves, que es la protección de puesta a tierra. Va por ahí y va a tierra. Esas son todas las normas.

**[5:05] E:** Y nos está faltando prolijar. Como verán, los cables están medio mal. Lo que vamos a hacer es, de ese [gabinete] que es muy grande, separar en dos, poner uno por acá y prolijar todo el cableado.

**[5:25] A:** ¿Ese equipo qué es?
**E:** Esta es una UPS. Tenemos una UPS tower ahí, que es de doble conversión online, o sea que aguanta mejor los cortes. Y esta es otra UPS. Ahí están todos los switches.

**[5:40] A:** ¿Y el tema de las VLAN?
**E:** Se pone una VLAN para estudiantes, una para docentes y otra para el personal. Así en general. En general te dicen "alumno" y "docente", y "alumno" le dan al personal también. Pero al separar por equipos, en realidad, si sos estudiante y estás en el primer piso estás por WiFi 6, [¿la red queda?] separada.

**[6:15] A:** ¿Acá abajo sería una VLAN para docentes?
**E:** No, porque no hay docentes acá. Este piso es la parte de oficinas.
**A:** ¿Y hay una VLAN para eso?
**E:** Hay dos VLAN: la de alumno y la de docente, pero en realidad las está ocupando la gente de oficina. Es mentira, no hay docentes ni alumnos. Quedó de antes, de cuando era todo Gigared.

**[6:40] E:** Primer piso y segundo están separados también entre docentes y estudiantes, pero ahí sí los ocupan realmente docentes y estudiantes. Después te cuento con las claves.

---

## Audio 2 — Campus Deodoro Roca 2 (4:31) — Sala de máquinas, segundo piso, secretaría

**[0:00] A:** ¿Está bien fresco ahí?
**E:** Sí. Es un pequeño aire, pero no se apaga.
**A:** ¿Es un aire convencional?
**E:** Sí.
**A:** ¿Cómo se llama la habitación?
**E:** La habitación principal, o sala de máquinas.

**[0:15–0:45]** `[inaudible — suben]`

**[0:50] E:** Acá, todo WiFi 6. Primer piso y segundo piso, WiFi 6.

**[1:00] E:** Y esto, como verán, está apagado. ¿Ves? [Este] está apagado, [este] prendido.

**[1:15–1:40]** `[inaudible]`

**[1:45] A:** ¿Todo el edificio, independientemente del piso, es sector A y sector B?
**E:** Sí. Este es sector B. Y hay un edificio nuevo que se está construyendo y reservamos cuatro platos para ahí.

**[2:00] E:** Este otro es salón de eventos, por eso hay refuerzo. Salón de usos múltiples.

**[2:15] A:** Eso estaba en el plano. ¿Cuántos platos tenía?
**E:** Acá están los platos.

**[2:30–2:45]** `[inaudible — algo sobre un plato que quedó afuera de la sala]`

**[2:50] A:** ¿Acá sale un cable de red entonces?
**E:** Sí, siempre. Y ocupan la red, pero de afuera nomás, no adentro.

**[3:00] A:** ¿Viene desde planta baja por fuera el uplink?
**E:** [El de Odontología] no lo van a poder ver porque es subterráneo. El uplink es entre un switch y otro, que va por fuera.

**[3:20] E:** Eso también va por bandeja. Esta fue la primera conexión que se hizo con el WiFi.

**[3:35] E:** Acá hay otro gabinete. [Secretaría de asuntos] estudiantiles. Es lo mismo que les mostré en biblioteca, y tengo acá otro Omada.
**A:** ¿Ese da para todo este piso?
**E:** Sí, exactamente.

**[4:15] A:** ¿Cuántos están reservados?
**E:** Cuatro. Dos por piso, porque la planta baja todavía no existe [en el edificio nuevo, no hay] dónde ponerlos.

**[4:30] A:** Entonces acá tienen solo switches y access points. ¿Son switches de capa 3?
**E:** Sí. `[resto inaudible]`

---

## Audio 3 — Campus Deodoro Roca 3 (7:30) — Exterior: cables entre gabinetes y recorrido de la fibra

**[0:00] E:** ¿Dónde estamos? Esto es lo que entra [por] fuera al gabinete, al switch de biblioteca.

**[0:30] E:** Se tuvo que romper la pared para que entre. ¿Ves? El cable está ahí, entró por acá. Lo seguís: uno va para arriba —¿se acuerdan que les dije?—, el uplink del otro [switch]. Y el otro viene de allá, pero viene por acá, tratando de protegerlo.

**[0:50] A:** ¿Qué tipo de cable era?
**E:** Es el 6, de exterior. Con el conector blindado.

**[1:00–1:15]** `[inaudible]`

**[1:20] A:** ¿Qué cantidad de metros se banca antes de degradar la señal?
**E:** ¿Un kilómetro? No, no. `[risas]` 100 metros. Entre 100 y 150.

**[1:45] E:** Fíjense: del gabinete principal, donde estuvimos, sale un cable que viene sostenido para allá, que es 6, con otro plato. Pero era como este plato; no pusimos un plato lindo acá, pusimos uno de los que descartamos, pero con cable 6.

**[2:05] E:** Y este es el principal. Van a ver que sobra fibra. Y este es el camino por donde viene la fibra.

**[2:20] E:** Después sube un pedacito allá por la playa de estacionamiento, ¿vieron dónde está el auto? Por ahí sube y va por fuera, porque hubo una obra de construcción en la playa de estacionamiento. Y pasamos por el edificio de Química [/ Exactas], y de ahí vamos a Odonto. Y en cualquier lugar que haya obra nos pueden cortar.

**[2:45] A:** O sea, ¿la fibra viene de Odonto?
**E:** Claro. De Odonto se va al edificio de Química, cruza por la playa de estacionamiento por arriba, baja, viene subterránea por acá y sale por acá.

**[2:55] A:** ¿Y todo este cable que estamos viendo de dónde sale?
**E:** Del gabinete que viste ahí adentro; se va hasta allá. O sea que la unión entre un gabinete y el otro, en este caso, va por fuera. Y de ahí también va por fuera del edificio para el otro switch.

**[3:15] A:** ¿Ese switch que está arriba es el que no pudimos entrar a ver?
**E:** Claro, es un Omada. Lo mismo que viste en biblioteca, pero arriba.

**[3:30] A:** Tenía dudas sobre cómo explicar mejor el tema de las VLAN. ¿Qué switch maneja cada VLAN?
**E:** No es con switch, es con puerto. Tenés un switch y decís: de tal puerto a tal puerto le asigno tal VLAN, y de tal otro puerto a tal otro, otra VLAN. Se programa por puerto.

**[3:55] E:** Y cada plato tiene nombre. Entonces cuando hacen el chequeo por el software de administración dicen: "el plato de prensa está caído". Te vas, mirás el cable de ahí, a dónde va, si hubo un problema con el puerto o con el plato. Suponete que le llovió, como le pasó al otro: muere el plato, pero el cable en realidad no tiene problema. Entonces sabés qué hay que reemplazar.

---

## Audio 4 — Campus Deodoro Roca 4 (7:16) — VLAN/SSID, asistencia, velocidades, stock

**[0:00] E:** ¿Ves? "Alumnos" y "docentes", las dos VLAN, con las claves. Sin embargo, todo lo que sea para el WiFi 6 es "gestión" e "invitado". Esas son las VLAN.

**[0:15] E:** A los docentes les tenemos que dar "gestión", y ahí entran. Y esta clave la comparte toda la UNNE. Entonces te vas de una facultad a otra y estás entrando. Yo ya lo vi en el Campus Cabral. `[cuenta que es docente en otras carreras — no técnico]`

**[0:50] A:** ¿Se maneja un WLC?
**E:** ¿Cómo?
**A:** El dispositivo WLC, para agrupar los access points y gestionar la WLAN.
**E:** Yo creo que no, que va por software, porque esa parte no la hago yo, la hace Rectorado. Era por el servidor ese que te decía.

**[1:25] A:** ¿Y el ruteo de todo se hace entonces con los switches de capa 3 nomás?
**E:** Sí. Y software.

**[1:30] E:** Por ejemplo, acá al lado hay un equipo —es otra parte, que no manejo yo—: un switch que no es administrable, que es para la asistencia en las aulas. A mí me convendría, por distancia, conectar el Omada con ese. Pero como no es administrable, sonamos. Entonces tenemos que bajar con el cable hasta el que es administrable.

**[2:05] A:** ¿Y los dispositivos rojos?
**E:** Son los lectores para la asistencia. Viene el estudiante, pone su tarjeta de estudiante y [marca] la asistencia. Impacta en [¿SIU Guaraní?]. También tienen cable y van a ese switch. `[parte inaudible]`

**[2:30] E:** `[inaudible]` ...los switches, mayoritariamente las interfaces son [¿Fast Ethernet y Gigabit?].

**[2:45] E:** La tasa de transferencia. Tratamos de ir siempre por la tasa más alta. Estamos tratando de llegar a 10 [¿gigabits?] `[inaudible]`. En el plano dice hasta dónde estamos tratando de llegar.

**[3:00] E:** Y nos van a hacer test de velocidad. Eso lo hacen [los de Rectorado], porque como los equipos son de Rectorado, no los compramos nosotros, nos hicieron tipo una donación.

**[3:20] A:** `[pregunta por la hoja pegada: "28"]`
**E:** Esa es de la calle Salta. La [VLAN] 28, del [puerto] 1 al 23. Pero eso es en la Salta. Y esta [la del campus] es una subred de [¿10.40.50?]. La 28 es de allá, de la Salta, que depende de Rectorado justamente.

**[4:00] E:** Y esto es un crecimiento desordenado: viene uno, después viene otro, viene otro... Eso nos falta [ordenar]. Esto lo hizo Klein. Hay dos nada más que trabajan con fibra en Corrientes: Cuevas, que es ingeniero, y Klein. Hay poca gente, y que fusione fibra, menos, porque el equipo para fusionar es bastante caro.

**[4:30] A:** La fibra que viene de afuera llega ahí abajo; después, cuando viene hacia acá, ¿viene por cobre nada más?
**E:** Sí. Los uplinks van por cable: por el 5 que yo te decía, y por 6 todo lo que sea Omada. Viene por fibra, y todos los Omada se hablan entre ellos con [cable categoría] 6, para no degradar la velocidad. Y los otros trabajan en 5, lamentablemente, pero anda bastante bien.

**[5:00] E:** A ver si tengo el [test] de la velocidad... No, no está. Nuestro objetivo es no bajar de esa velocidad. `[no dice el número]`

**[5:30] A:** `[inaudible — algo sobre VLAN y switch de capa 2]`

**[5:45] A:** ¿Usted le dice cobre o UTP?
**E:** `[en la cátedra, en Packet Tracer, le dicen "cable de cobre"]`. Nosotros siempre vamos por la categoría: categoría 5, categoría 6, porque no es lo mismo. O si es de exterior, o los conectores.

**[6:05] E:** Mirá, los equipos que están ahí son los que ocupamos, y acá están los que son para el otro edificio. Quedaron cuatro para el otro edificio. Inclusive [alguien] trató de poner uno, pero tuvo un problema con el cable; por eso [acá] hay tres. No terminaron la obra: al no terminar el cielorraso no lo permiten. Por eso quedó. Pero [el cable] ya está tendido.

**[6:35] A:** ¿Tema de servidores? ¿Acá no hay ninguno?
**E:** Sí, el servidor de abajo.
**A:** ¿Y qué brinda ese?
**E:** Administración para los Ubiquiti.
**A:** ¿Y los otros [Omada]?
**E:** No, no tenemos. Es por software.

**[7:00] E:** `[les dicta su mail de contacto — lo tienen anotado]`
