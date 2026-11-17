# Consultas por mail a la encargada de la red

## Principales

1. **VLAN:** ¿Qué VLAN existen y qué número (ID) tiene cada una? (alumnos, docentes, gestión, invitado, personal/administración). ¿Hay una VLAN de gestión para los equipos de red?
2. **DHCP:** ¿Quién entrega las direcciones IP: el switch de capa 3, el servidor de la facultad, Rectorado o Gigared?
3. **DNS:** ¿Qué servidores DNS usan los equipos: de la UNNE, de Gigared o públicos (8.8.8.8 / 1.1.1.1)?
4. **Firewall y NAT:** ¿Hay firewall? ¿Lo administra la facultad o Rectorado? ¿Dónde se hace el NAT hacia Internet? ¿Se filtra contenido o puertos?
5. **Ruteo entre VLAN:** ¿Dónde se rutea entre VLAN: en el switch de capa 3 de la facultad o en Rectorado? ¿Usan ruteo estático u OSPF hacia la red de la UNNE?
6. **Velocidad:** ¿Cuál es el ancho de banda actual del enlace UNNE y del de Gigared, y cuál es la velocidad que buscan alcanzar? (en el audio se entiende "llegar a 10", ¿10 Gb?)

## Opcionales

7. **Direccionamiento:** ¿Qué subred y máscara usa cada VLAN? ¿La "10.40.50" es la de la facultad?
8. **Troncales:** ¿Los enlaces entre gabinetes son troncales 802.1Q? ¿Cuál es la VLAN nativa?
9. **Aislamiento:** ¿La red de invitados está aislada de la administrativa? ¿Hay ACL entre VLAN?
10. **Seguridad WiFi:** ¿Usan WPA2/WPA3 con clave compartida, 802.1X o portal cautivo?
11. **Controlador Omada:** ¿Los Omada se gestionan desde un controlador en la nube, en Rectorado o por software local?
12. **Monitoreo:** ¿Qué software administra los Ubiquiti (¿UniFi Network?)? ¿Usan SNMP u otra herramienta de monitoreo?
13. **Proveedores y respaldo:** ¿Hoy funcionan solo con UNNE y Gigared o ya está Telco? Si se corta la fibra de Odontología, ¿pasan a Gigared automáticamente o a mano?
14. **Otros sistemas:** ¿Las cámaras y los lectores de asistencia tienen VLAN propia?
15. **Redundancia:** ¿Usan Spanning Tree o hay enlaces redundantes entre switches?
16. **IP fijas:** ¿Hay IP fijas o reservas para el servidor, impresoras o cámaras?
