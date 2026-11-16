# Relevamiento Derecho UNNE — Pendientes a confirmar

Nov 14, 2026 · @Facu

Quedan 7 puntos para confirmar con la encargada de la red y 4 que el grupo puede cerrar solo. El resto del material está en el documento de contexto completo.

## A confirmar con la encargada

Son las contradicciones entre fuentes y los dos datos de servicios que el grupo decidió averiguar.

| #   | Tema                          | Qué dice cada fuente                                                                                                                                    | Qué hay que saber                                                                   | Por qué importa                                                   | Respuesta                                                                                                                                                                              |
| --- | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | VLAN                          | Audio 1: tres VLAN (estudiantes, docentes, personal). Audio 4: "alumnos" y "docentes" en la red anterior; "gestión" e "invitado" en WiFi 6. Notas: tres | Cuántas VLAN hay en total y si existe una de "personal" aparte<br><br>              | Es la sección de segmentación del informe                         | Alumnos<br>Docentes<br>Invitados<br>El personal ocupaba Docentes y Alumnos (mejora a proponer)                                                                                         |
| 2   | Marca de los AP nuevos        | Planos: los AP dicen "Ubiquiti". Racks, audios y cajas en stock: Omada / TP-Link                                                                        | Si los platos WiFi 6 instalados son TP-Link Omada y el rótulo del plano quedó viejo | Define el equipamiento de la red nueva                            | Solo en planta baja quedaron los AP ubiquiti <br>piso 1 y 2 tienen tplink wifi 6. <br><br>(mejora a proponer es que algunos ubiquiti en desuso estaban colocados de todos modos)       |
| 3   | Categoría del cable           | Planos y notas: "UTP 6A". Audios: siempre "6"                                                                                                           | Si el tendido nuevo es 6 o 6A                                                       | Cambia la velocidad máxima que soporta (6A es para 10 Gb a 100 m) | No contamos con esa informacion                                                                                                                                                        |
| 4   | Gabinete mural de planta baja | Foto 0110 y audio de WhatsApp lo muestran; no figura en los planos                                                                                      | De dónde cuelga y a qué AP alimenta                                                 | Falta en el diagrama de topología                                 | FOTOS:<br>110: Ese es el omada que esta en dpto de sistemas en primer piso<br><br><br>115 ,122, 150: Gabinete de biblioteca<br>157: Planta baja con el servidor                        |
| 5   | DHCP, DNS y firewall          | No se mencionan en ninguna fuente                                                                                                                       | Quién los maneja: la facultad, Rectorado o Gigared                                  | Los trabajos modelo tienen una sección de servicios               | Cuando preguntamos sobre estas cosas como ospf, ruteo, manejo de vlans. La respuesta fue "Se maneja por software" . Suponemos que se controla desde el servidor que esa en planta baja |
| 6   | Ancho de banda                | Ninguna fuente da un valor                                                                                                                              | Velocidad del enlace UNNE y del enlace Gigared                                      | Los trabajos modelo lo informan por proveedor                     | Suponemos que 100mbts                                                                                                                                                                  |
| 7   | "Telco"                       | Audio 1: "todavía faltan los de Telco", "de la calle viene el de Telco"                                                                                 | Qué proveedor es y para qué se va a usar                                            | Sería un tercer enlace; opcional                                  | Telco es otro proveedor que estaba ingresando. No tenemos mas informacion. Preferimos no nombrar ya que no tenemos informacion                                                         |
**Todas las respuestas que no sabemos seran preguntadas por mail(Revisar ../Consultas por mail.md)

## Datos aproximados que se usan tal cual

El grupo decidió no seguir indagando en estos puntos. Si van al informe, van marcados como aproximados o "según lo relevado".

| Dato                                                 | Lo que se tiene                                                                 | Origen                             |
| ---------------------------------------------------- | ------------------------------------------------------------------------------- | ---------------------------------- |
| Subred del campus                                    | Suena a "10.40.50", sin máscara                                                 | Audio 4                            |
| Velocidad objetivo                                   | "Llegar a 10", probablemente 10 Gb. Consistente con el switch de puertos 10 GbE | Audio 4, cajas en foto 0135        |
| Interfaces de los switches                           | Fast Ethernet y Gigabit, poco claro                                             | Audio 4                            |
| Sistema de asistencia                                | Nombre inentendible, posiblemente SIU Guaraní                                   | Audio 4                            |
| Qué switch es de qué red en el gabinete mural        | Abajo UNNE, arriba Gigared                                                      | Notas (en el audio no se entiende) |
| Categoría 7 y aplicación de asistencia para docentes | Solo en la transcripción del compañero                                          | Sin confirmar en el audio          |
| AP repartidos "porque salta el voltaje"              | Posible límite de potencia PoE por switch                                       | Notas                              |
| Modelo de los AP nuevos                              | La caja parece decir AXE11000 Quad-Band Wi-Fi 6E                                | Foto 0135, borrosa                 |
| Cantidad de equipos                                  | 16 AP en planos más refuerzos; switches sin contar                              | Planos y fotos                     |
| Alcance del cable                                    | "100 metros, entre 100 y 150"                                                   | Audio 3                            |
| Tramos inaudibles                                    | Entrada a la sala de máquinas; AP apagados y prendidos del segundo piso         | Audios 1 y 2                       |

## A manejar con cuidado en el informe

- **Claves de WiFi.** Las fotos 0109 y 0119 muestran las claves de dos redes. No usar esas fotos ni copiar las claves.
- **Sede calle Salta.** Las hojas de las fotos 0137 y 0168 son de otra sede. Los Cisco 2960 y la VLAN 28 no son del campus; si se usan, es como ejemplo y aclarándolo.
- **Nombres de personas.** En los audios se nombra a la encargada y a dos técnicos de fibra. Los trabajos modelo no nombran personas; conviene referirse a los cargos.
- **Foto 0115.** Se ve a integrantes del grupo reflejados en el vidrio del gabinete; recortar.
- **Inventario.** Los modelos y cantidades son "relevados visualmente", no un inventario completo. Decirlo así.
- **Mejoras propuestas.** Dos ya están planeadas por la facultad (dividir el rack y prolijar el cableado). El resto son propuestas del grupo; distinguirlas.
