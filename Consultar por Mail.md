# Consultas por mail a la encargada de la red

Cada pregunta tiene debajo un **Supuesto**: lo que asumimos a partir de lo relevado y de lo visto en la cátedra, mientras no haya respuesta. Si responde, se reemplaza el supuesto por el dato real.

## Principales

1. **VLAN:** ¿Qué VLAN existen y qué número (ID) tiene cada una? (alumnos, docentes, gestión, invitado, personal/administración). ¿Hay una VLAN de gestión para los equipos de red?
   > **Supuesto:** tres VLAN de usuarios: **Docentes** (en WiFi 6 se llama "gestión"), **Alumnos** e **Invitados**. El personal administrativo no tiene VLAN propia y usa la de docentes o la de alumnos (lo dijo en el audio 1). Además suponemos una VLAN de gestión para los switches y AP, que es lo habitual en equipos administrables. Los ID no los sabemos; en el informe usamos de ejemplo 10 = Docentes, 20 = Alumnos, 30 = Invitados, 99 = Gestión, aclarando que son ilustrativos.

2. **DHCP:** ¿Quién entrega las direcciones IP: el switch de capa 3, el servidor de la facultad, Rectorado o Gigared?
   > **Supuesto:** en la red UNNE, el **switch de capa 3** del gabinete principal, con un pool por VLAN. Si el DHCP estuviera en Rectorado, el switch haría de relay (`ip helper-address`). En la red Gigared, el equipo de borde de Gigared / UniFi entrega sus propias direcciones.

3. **DNS:** ¿Qué servidores DNS usan los equipos: de la UNNE, de Gigared o públicos (8.8.8.8 / 1.1.1.1)?
   > **Supuesto:** el DNS lo informa el mismo DHCP. En la red UNNE, **DNS primario de la UNNE (Rectorado)** y uno público como secundario (8.8.8.8 o 1.1.1.1). En la red Gigared, los DNS del proveedor. La facultad no tiene DNS propio (no se vio ningún servidor para eso).

4. **Firewall y NAT:** ¿Hay firewall? ¿Lo administra la facultad o Rectorado? ¿Dónde se hace el NAT hacia Internet? ¿Se filtra contenido o puertos?
   > **Supuesto:** como mínimo, un **firewall perimetral centralizado en Rectorado**, en la salida a Internet de toda la UNNE, que hace el **NAT/PAT** de las direcciones privadas. En la facultad no hay firewall dedicado: la seguridad interna son las VLAN y, como mucho, ACL en el switch de capa 3. En la red Gigared, el router del proveedor hace NAT y un filtrado básico.

5. **Ruteo entre VLAN:** ¿Dónde se rutea entre VLAN: en el switch de capa 3 de la facultad o en Rectorado? ¿Usan ruteo estático u OSPF hacia la red de la UNNE?
   > **Supuesto:** el **ruteo entre VLAN lo hace el switch de capa 3** con interfaces SVI (una por VLAN), que es lo que respondió ("con los switches de capa 3 y software"). Hacia la red de la UNNE, una **ruta estática por defecto** hacia el nodo de Odontología. Un protocolo dinámico como OSPF tendría sentido en el backbone de la UNNE, pero no lo podemos afirmar.

6. **Velocidad:** ¿Cuál es el ancho de banda actual del enlace UNNE y del de Gigared, y cuál es la velocidad que buscan alcanzar? (en el audio se entiende "llegar a 10", ¿10 Gb?)
   > **Supuesto:** enlace interno de fibra con Odontología a **1 Gbps**, con **objetivo de 10 Gbps** (coincide con los switches TP-Link de puertos 10 GbE y con el cable 6/6A). El acceso a Internet que llega a cada usuario es menor y no lo conocemos; Gigared, un plan comercial de **unos 100 Mbps** (el valor que ya veníamos usando). Todo marcado como estimado.

## Opcionales

7. **Direccionamiento:** ¿Qué subred y máscara usa cada VLAN? ¿La "10.40.50" es la de la facultad?
   > **Supuesto:** direcciones privadas de clase A (RFC 1918) dentro de la red de la UNNE. Tomamos **10.40.50.0/24** como la subred de la facultad y, para el resto de las VLAN, una /24 por VLAN (254 hosts). Para Invitados/Alumnos podría hacer falta una /23 o más grande por la cantidad de estudiantes en eventos.

8. **Troncales:** ¿Los enlaces entre gabinetes son troncales 802.1Q? ¿Cuál es la VLAN nativa?
   > **Supuesto:** sí, los uplinks entre gabinetes son **troncales 802.1Q**, porque las mismas VLAN aparecen en todos los pisos. Los puertos hacia los AP también son troncales, porque cada AP emite varias redes (cada SSID va a su VLAN). VLAN nativa: la **1, por defecto**; lo recomendable sería cambiarla por una sin uso (mejora a proponer).

9. **Aislamiento:** ¿La red de invitados está aislada de la administrativa? ¿Hay ACL entre VLAN?
   > **Supuesto:** las VLAN separan el tráfico a nivel 2, pero al rutear el switch de capa 3 se comunicarían entre sí salvo que haya **ACL**. Suponemos como mínimo una ACL que impide que Invitados llegue a la VLAN de gestión de los equipos, y aislamiento de clientes en el WiFi de invitados (función típica de los controladores Omada/UniFi).

10. **Seguridad WiFi:** ¿Usan WPA2/WPA3 con clave compartida, 802.1X o portal cautivo?
    > **Supuesto:** **WPA2-Personal (PSK)**, o WPA2/WPA3 mixto. Hay un cartel con las claves y la clave es la misma en toda la UNNE, así que no hay autenticación por usuario (sin 802.1X ni portal cautivo). Mejora a proponer: 802.1X con usuario institucional.

11. **Controlador Omada:** ¿Los Omada se gestionan desde un controlador en la nube, en Rectorado o por software local?
    > **Supuesto:** **controlador por software centralizado en Rectorado** (Omada Software Controller o Cloud). Encaja con que la red tenga el mismo SSID y la misma clave en todas las facultades y con que los equipos los gestione Rectorado. No hay controladora física (WLC), como respondió en el audio 4.

12. **Monitoreo:** ¿Qué software administra los Ubiquiti (¿UniFi Network?)? ¿Usan SNMP u otra herramienta de monitoreo?
    > **Supuesto:** el servidor Linux de la sala de máquinas corre la **UniFi Network Application**, el controlador de Ubiquiti. Ahí se ven los AP por nombre y cuáles están caídos, que es lo que mostraban los monitores. No suponemos SNMP ni otra herramienta aparte.

13. **Proveedores y respaldo:** ¿Hoy funcionan solo con UNNE y Gigared o ya está Telco? Si se corta la fibra de Odontología, ¿pasan a Gigared automáticamente o a mano?
    > **Supuesto:** hoy funcionan con **UNNE y Gigared**; Telco todavía no está instalado. **No hay respaldo automático**: son dos redes separadas, con equipos y WiFi distintos. Si se corta la fibra de Odontología, los usuarios tienen que conectarse a mano a la red de Gigared. Mejora a proponer: failover automático.

14. **Otros sistemas:** ¿Las cámaras y los lectores de asistencia tienen VLAN propia?
    > **Supuesto:** **no tienen VLAN propia.** Los lectores de asistencia cuelgan de un switch no administrable, que no maneja VLAN, y llegan a la red por un puerto de acceso de algún switch. Las cámaras, con su grabador en la sala de máquinas, estarían en la red administrativa. Mejora a proponer: una VLAN para cámaras y otra para asistencia.

15. **Redundancia:** ¿Usan Spanning Tree o hay enlaces redundantes entre switches?
    > **Supuesto:** **STP/RSTP activo por defecto** en los switches administrables, pero como la topología es un árbol sin enlaces redundantes, no bloquea ningún puerto. Sirve solo de protección ante un bucle accidental. No hay agregación de enlaces.

16. **IP fijas:** ¿Hay IP fijas o reservas para el servidor, impresoras o cámaras?
    > **Supuesto:** **IP fija** para el servidor, los switches (en la VLAN de gestión), el grabador de cámaras y las impresoras, o reservas por MAC en el DHCP. Todos los usuarios toman IP dinámica.
