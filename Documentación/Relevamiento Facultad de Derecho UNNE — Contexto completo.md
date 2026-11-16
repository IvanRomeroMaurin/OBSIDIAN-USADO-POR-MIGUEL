# Relevamiento Facultad de Derecho UNNE — Contexto completo

Nov 14, 2026 · @Facu

## 1. Qué es este documento y de dónde sale

Reúne todo lo que se sabe de la red de la Facultad de Derecho y Ciencias Sociales y Políticas de la UNNE (Campus Deodoro Roca, Corrientes), relevada el 13/11/2026 para el trabajo de relevamiento de Redes de Datos (FaCENA, 2026). Lo dudoso está marcado en cada punto y reunido en el documento aparte de pendientes.

| Fuente | Qué es | Confiabilidad |
| --- | --- | --- |
| 5 audios del recorrido | Explicación de la encargada de la red, con preguntas del grupo. Uno es de WhatsApp (inicio del recorrido), cuatro son "Campus Deodoro Roca 1 a 4" | Media: mucho ruido de pasillo, transcripción automática en dos pasadas |
| Transcripciones curadas del compañero | Los mismos 5 audios, transcriptos con otra herramienta y limpiados a mano | Media: sirvió para cruzar y completar |
| Notas.txt | Apuntes tomados durante el recorrido | Alta para lo que dicen, pero muy resumidas |
| 3 planos draw.io (fotos 0060, 0074, 0107) | Planta baja, primer y segundo piso del "Proyecto de Mejora de la conexión WIFI 6", con racks y AP | Alta, con anotaciones a mano sin explicar |
| 55 fotos restantes | Gabinetes, AP, recorrido exterior del cable, stock de equipos, lectores de asistencia, cámaras | Alta para lo que se ve; pocos modelos legibles |
| 3 trabajos modelo | Poder Judicial de Corrientes (2025), Lx Argentina (2025), IPS Corrientes (2021) | Referencia de estructura |

Quién habla en los audios: la voz de mujer es la encargada de la red de la facultad, que además es docente en otras carreras de la UNNE. Las voces de hombre son los integrantes del grupo.

Lo que no quedó grabado: el tramo anterior al gabinete de planta baja y varios momentos dentro de la sala de máquinas y del segundo piso.

## 2. Resumen general

La facultad está a mitad de una migración y hoy conviven dos redes en el mismo edificio. La anterior es de Gigared, con equipos Ubiquiti UniFi, WiFi 5 y cable categoría 5. La nueva es de la UNNE, con equipos TP-Link Omada donados por Rectorado, WiFi 6 y cable categoría 6/6A.

La red nueva se instaló donde hay alumnos y eventos: primer y segundo piso, auditorio y salón de usos múltiples. La anterior quedó en las oficinas del sector A y como respaldo si cae la nueva.

La topología física es un árbol. La fibra llega desde el nodo de la Facultad de Odontología al gabinete principal de planta baja. De ahí salen enlaces de cobre a los gabinetes de biblioteca, primer piso y segundo piso, y cada gabinete alimenta sus access points.

La gestión está repartida: la facultad administra la parte Ubiquiti desde un servidor propio, y Rectorado administra la parte Omada por software. No hay grupo electrógeno; el respaldo son UPS que aguantan unos minutos.

&#91;embedded content: topología física · 2 entradas, 1 gabinete principal, 3 racks de distribución\]

El gabinete principal es el único punto de paso: si cae, cae todo el edificio. El gabinete mural de planta baja (HP, UniFi y TP-Link JetStream) no está dibujado porque no quedó claro de dónde cuelga.

## 3. El edificio

El edificio relevado tiene planta baja y dos pisos, y toda la facultad se divide en sector A y sector B. Entrando por el acceso, el sector A queda a la derecha y el sector B a la izquierda (según las notas).

| Planta | Qué hay (según planos y recorrido) | Red predominante |
| --- | --- | --- |
| Planta baja | Oficinas del sector A, decanato, hall de acceso, salón auditorio / sala de eventos, biblioteca, sala de máquinas con el gabinete principal, bar/kiosco, playones de estacionamiento, espacio cultural | Gigared WiFi 5 en oficinas; WiFi 6 en auditorio y biblioteca |
| Primer piso | Aulas 20 a 32, Sala CONEAU, Dpto. Sistemas, Gabinete Informático, pasillo "Constitución", centro de estudiantes | UNNE WiFi 6 |
| Segundo piso | Aulas 20 a 32, SUM (salón de usos múltiples), Secretaría de Asuntos Estudiantiles | UNNE WiFi 6 |

Las medidas del edificio figuran en los planos: el frente suma unos 93 m (18 + 28 + 12 + 28 + 7), el salón auditorio mide 29,75 x 14,79 m y el hall de acceso 19,60 x 11,93 m.

Hay un edificio nuevo en construcción dentro del campus. Tiene equipos reservados y el cable ya tendido, pero la obra no terminó (ver sección 14).

La facultad tiene además una sede en calle Salta 459, que depende de Rectorado y no forma parte del recorrido (ver sección 14).

## 4. Las dos redes que conviven

Cada red tiene su propia fibra de entrada, sus propios switches, su cableado y sus access points; solo comparten el gabinete principal y las bandejas.

| Aspecto | Red nueva (UNNE / Rectorado) | Red anterior (Gigared) |
| --- | --- | --- |
| Proveedor del enlace | Red de la UNNE, por el nodo Odontología | Gigared |
| Marca de equipos | TP-Link Omada | Ubiquiti UniFi |
| Estándar WiFi | WiFi 6 | WiFi 5 |
| Cableado | UTP categoría 6 / 6A, conector blindado | UTP categoría 5 |
| Dónde se usa | Primer y segundo piso, auditorio, SUM, biblioteca: donde hay alumnos o eventos | Oficinas del sector A, decanato, kiosco |
| Redes inalámbricas | "gestión" (docentes) e "invitado" | "alumnos" y "docentes" |
| Quién la administra | Rectorado, por software | La facultad, desde un servidor en planta baja |
| Origen de los equipos | Donación de Rectorado | Instalación anterior |
| Rol actual | Red principal para estudiantes y docentes | Oficinas y respaldo si cae la nueva |

Por qué se repartió así: la conducción de la facultad quiso dar el WiFi bueno a los estudiantes, así que las oficinas se quedaron con la versión anterior. La encargada lo cuenta al pasar del sector B al sector A (audio 1).

Cómo distinguirlas a simple vista en un gabinete: el cable categoría 6 es de la red UNNE y el categoría 5 es de Gigared. En el gabinete principal entran dos fibras naranjas, una para cada equipo.

Antes de la migración todo el edificio era Gigared con Ubiquiti WiFi 5. Varios de esos platos viejos se reutilizaron o descartaron; uno murió por ingreso de agua (foto 0117).

## 5. Acometida de fibra

La facultad no recibe la fibra de la UNNE desde la calle: depende del nodo de la Facultad de Odontología, dentro del mismo campus. Ese único enlace alimenta a toda la facultad.

Recorrido, desde el origen hasta el gabinete principal (audios 1 y 3):

1. Sale del nodo de Odontología.
2. Pasa por el edificio de Química / Exactas.
3. Cruza la playa de estacionamiento por arriba, a la vista. Va por fuera porque una obra en la playa obligó a sacarla del suelo.
4. Baja y sigue subterránea por el camino peatonal.
5. Sube y entra a la sala de máquinas de planta baja. En el gabinete se ve fibra sobrante enrollada.

Consecuencias que la propia encargada señala:

- Cualquier obra en el campus (construcción, estacionamiento, agua) puede cortar la fibra y dejar a la facultad sin servicio.
- Si hay un problema eléctrico en el gabinete principal, queda afuera todo el edificio.
- La fibra de "Telco" sí viene de la calle, y todavía falta agregar ese equipamiento al gabinete principal. El compañero lo interpreta como Telecom; ella no nombra la empresa.

Sobre quién trabaja la fibra: en Corrientes hay muy poca gente que fusione fibra, porque el equipo es caro. Nombra a dos personas, Cuevas (ingeniero) y Klein, y dice que la instalación actual la hizo Klein (audio 4).

## 6. Gabinete principal (sala de máquinas)

Está en planta baja, en una habitación propia del sector de oficinas que la encargada llama "habitación principal o sala de máquinas". En el plano figura como "Rack Principal". Es el único punto por donde entra la conectividad al edificio.

| Elemento | Detalle | Fuente |
| --- | --- | --- |
| Rack | Abierto, de piso, negro. Uno solo y "muy grande"; planean dividirlo en dos | Audio 1, fotos 0126, 0134, 0145 |
| Fibra | Dos entradas (patchcords naranjas): una al equipo de Gigared y otra al equipo de la UNNE | Audio 1 |
| Switches | Cisco, más el equipo UniFi de Gigared y los TP-Link Omada de la red WiFi 6. "Ahí están todos los switches" | Audio 1 |
| Servidor | Uno, para configurar en modo remoto cuando hay problemas. Administra los Ubiquiti. Trabaja sobre Linux | Audios 1 y 4, fotos 0148, 0156 |
| Monitores | Dos pantallas en la pared para ver si cae un plato o si un puerto se desconfiguró | Audio 1, foto 0151 |
| Cámaras | Equipos de videovigilancia en la misma sala | Audio 1 |
| UPS | Una UPS tower online de doble conversión, más otra UPS. "Todo tiene su UPS" | Audio 1 |
| Puesta a tierra | Jabalina conectada al rack | Audio 1, foto 0169 (cable verde) |
| Climatización | Un aire acondicionado convencional chico, que no se apaga | Audio 2 |

Estado: el cableado está desordenado, con patchcords cruzados por el frente y sin peinar. La encargada lo describe como "crecimiento desordenado: viene uno, después viene otro". El plan es separar el rack en dos y prolijar todo.

Pendiente de instalar: el equipamiento de Telco.

## 7. Gabinetes secundarios y enlaces entre gabinetes

Además del principal hay al menos cuatro gabinetes de distribución. Todos tienen solo switches (de capa 3, administrables) y de ellos cuelgan los access points; no hay servidores fuera de la sala de máquinas.

| Gabinete | Ubicación | Qué tiene | Fuente |
| --- | --- | --- | --- |
| Mural de planta baja | Pasillo de planta baja, colgado alto (marca Gabitel) | Arriba un switch HP de 24 bocas; debajo un switch Ubiquiti UniFi; debajo un TP-Link JetStream TL-SX3206HPP (el de WiFi 6, que recibe la fibra); abajo dos UPS chicas (Kozumi y Forza) | Audio de WhatsApp, foto 0110, notas |
| Biblioteca | Dentro de la biblioteca, planta baja. En el plano: "Rack" | Switch Omada conectado por SFP, 5 cables de red para las PC de la biblioteca, UPS | Notas, audios 2 y 3 |
| Primer piso | Zona Dpto. Sistemas / Gabinete Informático. En el plano: "Rack Omada" | Switch Omada y 4 AP | Plano foto 0074 |
| Segundo piso | Secretaría de Asuntos Estudiantiles; en el plano el "Rack Omada" está junto al aula 22 | "Otro Omada", igual al de biblioteca. Distribuye a todo el segundo piso | Audio 2, notas, plano foto 0107 |

Las fotos 0115, 0122 y 0150 muestran un gabinete Gabitel de piso con puerta de vidrio y una UPS negra apoyada arriba. Por las notas ("UPS en biblioteca") probablemente es el de biblioteca, pero no está confirmado.

### Cómo se conectan entre sí

- **Fibra solo hasta planta baja.** La fibra llega al gabinete principal y al switch de WiFi 6 de planta baja, que tiene módulo de fibra.
- **De ahí en adelante, cobre.** Los uplinks entre gabinetes van por UTP: categoría 6 para todo lo Omada ("los Omada se hablan entre ellos con 6, para no degradar la velocidad") y categoría 5 para lo de Gigared.
- **Fibra en un extremo, UTP en el otro.** En el gabinete de planta baja el enlace sale por el puerto de fibra de un lado y entra por UTP al puerto SFP del otro switch. La encargada dice que lo ideal sería módulo de fibra contra módulo de fibra, pero no tienen módulos, y así se pierde velocidad.
- **Por fuera del edificio.** La unión entre el gabinete principal y el de biblioteca, y la subida a los pisos, va por la fachada con cable categoría 6 de exterior y conector blindado. Para entrar a biblioteca hubo que romper la pared (audio 3, fotos 0118, 0131, 0162, 0163, 0167, 0170).
- **Por bandejas adentro.** En los pasillos la distribución va por bandeja portacables sobre el cielorraso (fotos 0112, 0159).
- **Distancia.** Consultada por el alcance del cable, responde 100 metros, "entre 100 y 150".

En el gabinete mural de planta baja, según las notas, el switch de abajo es el de la UNNE y el de arriba corre sobre Gigared; el plato del de arriba está desconectado, así que el uplink trabaja desde el de abajo.

## 8. Cableado y medios de transmisión

Se usan tres medios: fibra óptica para la entrada, UTP para todo el tendido interno y entre gabinetes, y WiFi para el acceso de los usuarios.

| Medio | Dónde | Detalle |
| --- | --- | --- |
| Fibra óptica | Nodo Odontología → gabinete principal; entrada de Gigared; gabinete de planta baja | Patchcords naranjas, módulos de fibra en los switches. No se relevó si es monomodo o multimodo |
| UTP categoría 6 / 6A | Toda la red Omada: uplinks entre gabinetes y bajadas a los AP WiFi 6 | Los planos dicen "cableado UTP 6A"; la encargada dice siempre "6". Conectores blindados. Versión de exterior en los tramos por fachada |
| UTP categoría 5 | Toda la red Gigared / Ubiquiti | "Lamentablemente, pero anda bastante bien" |
| WiFi 6 | Primer y segundo piso, auditorio, SUM, biblioteca | AP de techo TP-Link Omada |
| WiFi 5 | Oficinas del sector A, decanato, kiosco | AP de techo Ubiquiti UniFi |

Otros datos sueltos sobre el cableado:

- La encargada nombra el cable por categoría, tipo (interior o exterior) y conector, no como "cobre" o "UTP" a secas, "porque no es lo mismo".
- Las interfaces de los switches serían mayoritariamente Fast Ethernet y Gigabit Ethernet (audio 4, poco claro).
- El objetivo declarado es ir siempre por la tasa más alta y "llegar a 10"; la unidad no se entiende, probablemente 10 Gb. El modelo de switch que se ve en fotos (TL-SX3206HPP) es de puertos 10 GbE, lo que es consistente.
- Rectorado les hace pruebas de velocidad. No se obtuvo ningún valor medido.
- El compañero registró una mención a categoría 7 que no pude confirmar en el audio.
- Según las notas, los AP están repartidos en dos switches "porque si ponen sobre el mismo salta el voltaje". No aparece en los audios; podría referirse al límite de potencia PoE por switch.

## 9. Red inalámbrica: access points

Los planos marcan 16 access points de techo (8 en planta baja, 4 por piso), a los que se suman refuerzos y platos sueltos que aparecen en el recorrido. La encargada les dice "platos".

| Planta | AP en el plano | Desde qué rack | Observaciones |
| --- | --- | --- | --- |
| Planta baja, oficinas | 4 | Rack Principal | Los cuatro tienen un "No" escrito a mano. Zona que quedó con WiFi 5 |
| Planta baja, auditorio | 4 (2 hacia el salón, 2 hacia la biblioteca) | Rack de biblioteca | Sala de eventos: "satura adentro, hay dos platos" |
| Primer piso | 4, en los pasillos | Rack Omada (Dpto. Sistemas) | WiFi 6 |
| Segundo piso | 4, en los pasillos | Rack Omada (junto al aula 22) | WiFi 6 |

Platos que no están en los planos o son refuerzos:

- **Decanato:** un plato de refuerzo, porque con dos paredes la señal ya se cae. Hay otro adentro que no se pudo ver.
- **SUM / salón de eventos del segundo piso:** refuerzo por la cantidad de gente en eventos.
- **Bar / kiosco:** un plato WiFi 5; en el plano hay una línea a mano desde el Rack Principal hasta el bar.
- **Cerca del gabinete principal (interior):** un plato viejo de los descartados, pero conectado con cable categoría 6.
- **Una sala del segundo piso:** el plato quedó afuera; "ocupan la red, pero de afuera nomás, no adentro".
- **Edificio nuevo:** 4 reservados, 2 por piso.

Datos de operación:

- Cada plato tiene nombre en el software de administración (ejemplo que da: "el plato de prensa está caído"). Eso permite ir directo al cable y al puerto.
- En el segundo piso se vieron platos apagados y otros prendidos (los prendidos muestran una luz azul; fotos 0079, 0125, 0133, 0164, 0171).
- Un plato Ubiquiti anterior murió porque le entró agua; el cable quedó sano (foto 0117). Otro cuelga de su cable (foto 0114). Todos los AP son de interior: el grupo confirmó que no hay AP exteriores.
- La primera conexión WiFi que se hizo en el edificio es la del sector que se muestra en el audio 2, tendida por bandeja.

Una inconsistencia de los planos: los círculos de los AP están rotulados "Ubiquiti" aunque el proyecto es de WiFi 6 y el rack dice "Omada". En el stock fotografiado los AP nuevos son TP-Link de montaje en techo.

## 10. VLAN, redes inalámbricas y direccionamiento

La segmentación se hace con VLAN asignadas por puerto de switch, y cada red física tiene su propio par de redes inalámbricas. Es el punto donde las fuentes más se contradicen.

| Red | Nombre | Quién la usa en la práctica |
| --- | --- | --- |
| Gigared (WiFi 5) | "alumnos" | En planta baja, la gente de oficina; no hay alumnos ahí |
| Gigared (WiFi 5) | "docentes" | En planta baja, la gente de oficina; no hay docentes ahí |
| UNNE (WiFi 6) | "gestión" | Docentes: "a los docentes les tenemos que dar gestión" |
| UNNE (WiFi 6) | "invitado" | No se dijo; por descarte, estudiantes y visitantes |

Lo que dice la encargada, en orden:

- **Audio 1:** "se pone una VLAN para estudiantes, una para docentes y otra para el personal". Enseguida aclara que en general se habla de "alumno" y "docente", y que "alumno" se le da también al personal.
- **Audio 1:** en planta baja hay dos VLAN, alumno y docente, pero las ocupa la gente de oficina. "Quedó de antes, de cuando era todo Gigared".
- **Audio 1:** en primer y segundo piso también están separados docentes y estudiantes, y ahí sí los usan docentes y estudiantes.
- **Audio 3:** las VLAN no se asignan por switch sino por puerto: de tal puerto a tal puerto una VLAN, del resto otra.
- **Audio 4:** "alumnos y docentes, las dos VLAN, con las claves; sin embargo todo lo que sea para el WiFi 6 es gestión e invitado".

La clave de la red WiFi 6 es la misma en toda la UNNE: se puede pasar de una facultad a otra y seguir conectado. La encargada lo comprobó en el Campus Cabral.

Hay un cartel impreso en la facultad con el nombre y la clave de dos redes, "Alumnos" y "UNNE-Invitado" (fotos 0109 y 0119). Las claves no se copian en este documento y no deberían ir al informe.

### Direccionamiento

- La red del campus sería una subred que suena a "10.40.50" (audio 4), sin máscara. Dato poco confiable.
- La sede de calle Salta usa la VLAN 28; un switch HP de ahí tiene la IP 10.10.28.3/24 (ver sección 14).
- No se relevaron ID de VLAN del campus, ni quién entrega direcciones (DHCP), ni DNS.

## 11. Gestión, monitoreo y ruteo

La administración está partida en dos: la facultad maneja lo Ubiquiti desde su servidor, y Rectorado maneja lo Omada por software.

| Tema | Cómo se resuelve | Fuente |
| --- | --- | --- |
| Administración de los Ubiquiti | Servidor en la sala de máquinas, sobre Linux. La encargada no sabe el nombre de la interfaz | Audios 1 y 4 |
| Administración de los Omada | Por software, a cargo de Rectorado. La facultad no tiene servidor para eso | Audio 4 |
| Controladora inalámbrica (WLC) | No hay equipo físico. Preguntada, dice "creo que no, va por software" | Audio 4 |
| Ruteo | Con los switches de capa 3 "y software" | Audio 4 |
| Monitoreo | Dos monitores en la sala de máquinas: muestran qué plato está caído o qué puerto se desconfiguró | Audio 1 |
| Diagnóstico de fallas | Por nombre de plato: se identifica el AP caído, se sigue su cable y se revisa puerto y equipo | Audio 3 |
| Acceso remoto | El servidor permite configurar en modo remoto cuando hay problemas | Audio 1 |
| Pruebas de velocidad | Las hace Rectorado, porque los equipos son suyos | Audio 4 |

No se mencionó en ningún momento un firewall, ni servidores de DHCP o DNS propios, ni servicios alojados en la facultad. Lo más probable es que esa capa esté en Rectorado, pero nadie lo dijo.

Una restricción práctica: los Omada necesitan colgar de un switch administrable. Por eso no se pueden conectar al switch de asistencia aunque esté más cerca (ver sección 13).

## 12. Energía, puesta a tierra y climatización

El único respaldo eléctrico son UPS: no hay grupo electrógeno, y ante un corte la red aguanta unos minutos.

| Elemento | Situación | Fuente |
| --- | --- | --- |
| Grupo electrógeno | No tienen. Para eventos muy importantes alquilan uno | Audio 1 |
| UPS de la sala de máquinas | Una UPS tower online de doble conversión ("aguanta mejor los cortes") y otra UPS adicional | Audio 1 |
| UPS de gabinetes | Gabinete mural de planta baja: dos UPS chicas, Kozumi y Forza. Biblioteca: una UPS | Foto 0110, notas |
| Autonomía | "Aguantan unos minutos". No se dio un valor | Audio 1 |
| Puesta a tierra | Jabalina a la que se conecta el rack principal. "Esas son todas las normas" | Audio 1 |
| Climatización | Solo en la sala de máquinas: un aire acondicionado convencional chico, encendido en forma permanente. El grupo notó la sala fresca | Audio 2 |
| Gabinetes de pasillo | Sin climatización; ventilación pasiva por las rejillas del gabinete | Fotos 0110, 0160 |

Un problema eléctrico en la sala de máquinas deja sin red a todo el edificio, porque ahí están las dos entradas de fibra.

## 13. Otros sistemas: asistencia en aulas y cámaras

### Control de asistencia

Cada aula tiene en la puerta un lector de tarjetas (el dispositivo rojo de las fotos 0063, 0111, 0129 y 0152). El estudiante apoya su tarjeta y queda registrada la asistencia.

- Los lectores están cableados a un switch propio, que no es administrable.
- Ese sistema no lo maneja la encargada de la red; "es otra parte".
- La asistencia impacta en un sistema cuyo nombre no se entiende en el audio (podría ser SIU Guaraní).
- El compañero registró que los docentes la consultan desde una aplicación; no pude confirmarlo en el audio.
- Efecto sobre la red: por distancia convendría conectar un Omada a ese switch, pero como no es administrable no se puede. Hay que tender cable hasta un switch administrable, más lejos.

### Videovigilancia

Hay cámaras en pasillos y exteriores (fotos 0106 y 0159) y equipos de cámaras dentro de la sala de máquinas. No se relevó cuántas son, qué grabador usan ni si van por una VLAN propia.

### Salón con audio

La foto 0139 muestra una sala con estrado y micrófonos de mesa. No se habló de ese equipamiento en los audios.

## 14. Sede calle Salta, stock y edificio nuevo

### Sede calle Salta 459

No es parte del campus ni del recorrido, pero hay tres hojas pegadas en una pared de la facultad con fotos de sus racks (fotos 0137, 0168 y la imagen de WhatsApp de las 11:28). Depende de Rectorado.

| Rack | Qué dice la hoja |
| --- | --- |
| Rack Biblioteca de Posgrado | Switch marca HP. Anotado a mano: "SW 10.10.28.3/24", "VLAN 28 1-23", "uplink puerto 24" |
| Pachera primer piso | Patch panels con sectores rotulados A, 1, 2, B |
| Rack principal | "Cisco 2960 de 24 puertos", "Cisco 2960 Catalyst de 24 puertos", "módulo de fibra" |

La encargada confirma en el audio 4 que la VLAN 28, puertos 1 a 23, es de la sede Salta. Sirve como ejemplo documentado de asignación de VLAN por puerto, que en el campus no se pudo ver.

### Equipos en stock

En un rincón hay unas 15 cajas TP-Link apiladas (fotos 0135 y 0166):

- 4 cajas de switch "JetStream 6-Port 10GE L2+ Managed Switch with 4-Port PoE++" (el mismo modelo TL-SX3206HPP que está instalado en planta baja).
- Unas 11 cajas de access point de techo. La etiqueta parece decir "AXE11000 Ceiling Mount Quad-Band Wi-Fi 6E", pero no se lee nítida.

La encargada explica que una parte son equipos en uso o por usar y otra parte los reservados para el edificio nuevo.

### Edificio nuevo

- Tiene 4 access points reservados, 2 por piso. La planta baja todavía no tiene dónde ponerlos.
- El cable ya está tendido.
- No se instalaron porque la obra no terminó: sin cielorraso no se permite colocarlos.
- Se intentó instalar uno y hubo un problema con el cable; por eso en el depósito había tres a la vista y no cuatro.

## 15. Personas y responsabilidades

La red tiene tres responsables distintos según la parte, y no se relevó cuántas personas trabajan en el área de sistemas de la facultad.

| Quién | Qué maneja |
| --- | --- |
| Encargada de la red de la facultad (la entrevistada) | Red Gigared / Ubiquiti, servidor de administración, gabinetes, cableado, relación con Rectorado. También es docente en otras carreras de la UNNE. Dejó su mail de contacto al grupo |
| Rectorado de la UNNE | Dueño de los equipos Omada (donados a la facultad), gestión por software de la red WiFi 6, pruebas de velocidad, sede calle Salta |
| Responsable del sistema de asistencia | Lectores de tarjeta y su switch no administrable. No se identificó quién es |
| Especialistas en fibra | Cuevas (ingeniero) y Klein, los dos que fusionan fibra en Corrientes según la encargada. La instalación actual la hizo Klein |
| Gigared | Proveedor del enlace de la red anterior |

El Dpto. Sistemas y el Gabinete Informático figuran en el plano del primer piso, pero no se visitaron ni se habló de ellos.

## 16. Puntos débiles y mejoras posibles

El problema más grave es la falta de redundancia: una sola fibra, un solo gabinete de entrada y sin generador. La columna de mejoras es propuesta mía, salvo donde dice que ya está planeada.

| Punto débil | Evidencia | Mejora posible |
| --- | --- | --- |
| Una sola entrada de fibra, dependiente del nodo Odontología | Audios 1 y 3: cualquier obra en el campus los deja sin servicio | Segundo camino físico de fibra, o usar el enlace de Gigared o Telco como respaldo automático |
| Tramo de fibra aéreo y expuesto sobre el estacionamiento | Audio 3 | Volver a canalizarlo bajo tierra o protegerlo en caño |
| Sin grupo electrógeno; UPS de pocos minutos | Audio 1 | Generador para la sala de máquinas, o UPS de mayor autonomía |
| Todo pasa por un único gabinete | Audio 1: "si hay un problema acá, queda afuera todo" | Separar el rack en dos (ya planeado) con alimentación independiente |
| Cableado desordenado en el rack principal | Fotos 0126, 0134, 0145; ella misma lo reconoce | Prolijar, peinar y etiquetar (ya planeado) |
| Uplinks de cobre entre gabinetes por falta de módulos de fibra | Audio de WhatsApp: "lo ideal sería módulo con módulo, pero no tenemos" | Comprar módulos SFP y tender fibra entre gabinetes |
| Cables entre gabinetes por la fachada, a la intemperie | Fotos 0118, 0131, 0162, 0163, 0167 | Canalizar en caño o bandeja exterior cerrada |
| AP dañados por agua | Foto 0117, audio 3 | Reparar las filtraciones y reubicar o proteger los AP interiores expuestos a humedad |
| Red de oficinas en categoría 5 y WiFi 5 | Audios 1 y 4 | Completar la migración a categoría 6 y WiFi 6 |
| VLAN heredadas con nombres que no reflejan el uso real | Audio 1: "es mentira, no hay docentes ni alumnos" | Redefinir y renombrar las VLAN de planta baja |
| Gestión repartida entre facultad y Rectorado | Audio 4 | Documentar quién administra qué y dar a la facultad una vista de monitoreo de los Omada |
| Switch no administrable para asistencia | Audio 4 | Reemplazarlo por uno administrable |
| Claves de WiFi en un cartel y compartidas por toda la UNNE | Fotos 0109, 0119; audio 4 | Autenticación por usuario (802.1X / portal cautivo) |
| Sin documentación visible de la red del campus | Solo hay hojas de la sede Salta | Armar diagrama de topología e inventario, como los de la sede Salta |
| Equipos comprados sin instalar | Fotos 0135, 0166: edificio nuevo sin terminar | Depende de la obra |

Aspectos positivos que también conviene decir en el informe: switches administrables de capa 3, puertos de 10 Gb en los equipos nuevos, cable categoría 6/6A con conector blindado, UPS online de doble conversión, puesta a tierra con jabalina, sala de máquinas climatizada, AP identificados por nombre y un proyecto de mejora con planos.

## 17. Índice de fotos

Las 58 fotos agrupadas por tema, con el número final del nombre de archivo (IMG-20261113-WA0xxx). La ubicación exacta de varias es inferida.

| Tema | Fotos | Qué muestran | Uso en el informe |
| --- | --- | --- | --- |
| Planos | 0060, 0074, 0107 | Planta baja, primer piso, segundo piso (draw.io), con anotaciones a mano | Base del diagrama de topología |
| Gabinete mural planta baja | 0110, 0160 | Abierto (HP, UniFi, TP-Link JetStream, 2 UPS) y cerrado | Figura de gabinete de distribución |
| Rack principal | 0126, 0134, 0145 | Rack abierto, fibra naranja, cableado desordenado | Figura de sala de máquinas y de punto débil |
| Sala de máquinas | 0148, 0151, 0156, 0157, 0169 | Monitores, PC/servidor, rack visto desde la puerta, cable de puesta a tierra | Figura de monitoreo y puesta a tierra |
| Gabinete de piso con UPS | 0115, 0122, 0150 | Gabinete Gabitel con puerta de vidrio y UPS arriba (probable biblioteca) | Figura de gabinete secundario y UPS |
| AP de techo | 0078, 0079, 0125, 0132, 0133, 0136, 0158, 0164, 0171 | Platos en pasillos, varios con luz azul encendida | Figura de access points |
| AP dañados | 0114, 0117 | Plato colgando de su cable; plato Ubiquiti manchado, en la mano | Figura de punto débil |
| Cable por exterior | 0112, 0118, 0131, 0155, 0162, 0163, 0167, 0170 | Recorrido del UTP por fachada, caja de paso, entrada por la pared | Figura de enlace entre gabinetes |
| Stock | 0135, 0166 | Cajas TP-Link de switches y AP | Figura de equipamiento nuevo |
| Asistencia | 0063, 0111, 0129, 0152 | Lector rojo en la puerta de las aulas 13, 14 y 30 | Figura de sistema de asistencia |
| Cámaras | 0106, 0159 | Cámaras en pasillo, con bandeja portacables | Figura de videovigilancia |
| Sede Salta | 0137, 0168, WhatsApp 11:28 | Hojas con fotos de racks y anotación de VLAN 28 | Ejemplo de VLAN por puerto |
| Cartel de WiFi | 0109, 0119 | Nombres de red y claves | No publicar |
| Contexto del edificio | 0121, 0124, 0139, 0142, 0147, 0149, 0161, 0165 | Pasillos, aulas, sala con micrófonos, ingreso | Opcional |
| Odontología | 0153, 0154 | Hall de la Facultad de Odontología | Ilustrar el nodo del que dependen |

En la foto 0115 se ve a personas reflejadas en el vidrio del gabinete; conviene recortarla antes de usarla.

## 18. Cómo encaja con los trabajos modelo

Los tres trabajos de años anteriores siguen casi la misma estructura, y el material relevado alcanza para cubrirla salvo en direccionamiento, servicios y personal.

| Sección habitual en los modelos | Qué hay para Derecho | Cobertura |
| --- | --- | --- |
| Objetivos del relevamiento | Se redacta; no depende del material | Completa |
| Descripción de la institución y del edificio | Plantas, sectores, medidas de los planos | Completa |
| Topología (diagrama) | Árbol desde Odontología, gabinetes, AP por planta | Completa |
| Infraestructura y cableado | Fibra, UTP 5 y 6/6A, bandejas, tramos exteriores | Completa |
| Equipamiento con fotos | Switches, AP, UPS, gabinetes; pocos modelos exactos | Parcial |
| Red inalámbrica | WiFi 5 y 6, distribución, refuerzos | Completa |
| VLAN y direccionamiento | Nombres de redes y asignación por puerto; sin ID ni subredes | Parcial |
| Proveedores y ancho de banda | UNNE vía Odontología, Gigared, Telco pendiente; sin velocidades | Parcial |
| Servidores y servicios | Un servidor de administración; nada sobre DHCP, DNS, firewall | Débil |
| Energía y respaldo | UPS, sin generador, jabalina, aire | Completa |
| Seguridad | Cámaras y control de asistencia; sin seguridad lógica | Parcial |
| Personal de sistemas | Solo la encargada y el rol de Rectorado | Débil |
| Sugerencias / oportunidades de mejora | Sección 16 | Completa |
| Conclusión | Se redacta | Completa |

Diferencias a tener en cuenta:

- El trabajo del Poder Judicial (19 páginas) es el más completo y tiene índice de figuras, topología en varios niveles y fichas de equipos. Es la mejor plantilla.
- El de Lx Argentina (11 páginas) explica cada concepto de la materia al usarlo (VLAN, troncales 802.1Q, UPS y PDU) y modela la red en Packet Tracer. Es el que mejor cumple la consigna de "aplicar y explicar los conceptos".
- El del IPS (12 páginas) es más corto y se apoya en un diagrama Visio por piso, parecido a lo que permiten los planos draw.io de Derecho.

Lo distintivo del caso Derecho frente a los tres modelos es la convivencia de dos redes en plena migración y la dependencia de otra facultad para la conectividad. Conviene que el informe gire alrededor de eso.
