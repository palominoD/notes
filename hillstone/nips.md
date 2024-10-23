# sistema New Intrusion Prevention System
si se hace el intento los primeros 7 dia, se puede optar por la segunda activacion
* entre ma complejo es el sistema mas opciones de ataque e tienen
* auqnue no haya NGFW podemos colocar un IPS 
* varias funciones de NGFW se traslapan con un IPS
* un IPS tiene mayores prestaciones que un NGFW
* trafico cifrado no se puede integrara con otro vendors
* tenemos la opcion de un trafico Bypass para resolver problemas con la red
* capaciodada basica de un sistema WAF
* proteccion durante todo el ciclode  vida de la amenazas, desde l pre hasta el post breach
* bloqueo de ip debido a su reputacion 
* filtrado de anti virus en los IPS
* uso de sanbox
* uso de control dy mitigacion  de servidores de comando y control para botnets
* usando dns sinkhole, mandamos las peticiones a un hoyo negro sin respuesta
* cloud view (tenemso la posibilidad de un solo punto de refeecnai de el estado de salud y seguuridad de los dispositivos, centralizador
* integracion con Isource, reporta el ips para hacer respuestas a observaciones de incidentes
* sistema de reportes para obtener las decicines informadas del presonal encargadod ela seguridad
* reglas ambiguas (any to any) 
* agrupacin de politicas dew una misma indole para una mejor organizacion 
* uso de hsm para centralizacion local de los cambiso y adminitracuion de los dispositivos, sin perder la autonomia en los equipos

* *deploy* en capa 2, aunque se puede tener un despliegue en L3
* podemos hacer un despliegue fuera de ruta, es decir con puerto espejo.
* el bds manipula la dinamic black list, para bloque fqdn, ip o puertos.

## principios de arquitectura 
* compartidos con el firewall
* zonas de interfaces
* tenemos vrSwitch y vrRoute
* uso de politicas
* la zona mgt no tiene salida a internet para tener menor exposicion
* todas las zonas que vive en un mismo vr-* pueden interactuar entre si.
* velocidades de 9600 o 115200
* el puerto es mgt o el puerto 0/0 (para al adminitracion)

## GUI
dashboard, icenter, monitor, log and reprt, configManagement
> port channel
* trabajo primordial en capa 2
* agregamos pares de interfaces, para entrada y salida
* adminitracion con 4 roles (admin, admin solo lectura, operador y auditor)
* el usuario hillstone no se puede eliminar ni cam,biar del rol
* archivos .DAT, reset por hard y por unset all
* update
* si se tiene licensias operativas, una vez que expiran se trabaja con lo que tenemos a al ultima actualizacion
* si son trail, una vez qu expiran se deja inhabilitado por completo el modulo.

## capitulo4 interfaces y rutas
* vWire, layer1 2 inetrfaces como un par de interfaces 

## capitulo5 rules (policy)
* numero de sessiones
* pocisiones
* hit count
* service book, servicios particulares y personalizados
* 65585 ports
* polici asisteance, es para reducir reglas ambiguas
## QOS
* crear pipes y delimitar el uso sobre este
* se puede tener sub pipes, lo cuales reparten el ancho de banda total del pipe
* manejo con el uso de shape, de policy or minitoreo.
* se puede compartri ancho de banda entre sub pipes, pero no entre root pipe

## atack defense
### arp defense
* suplatancion
* envenenamiento
* la asociacion permite esta acciones
* no se aplica en reglas, sino a nivel de zonas, lo que afecta a odS las inetrfaces ligada a esa zona.

### threat protection
* modo log only se le comonoce como ids 
* el sistema IPs se puede aplicar a nivel de zona y de regla, pero la prioridad es la de la regla.
> motores recomendadso el botnet y anti virus
* el antivirus no puede analisar el trafico que este comprimido y contenga clave, 
* detiene las consultas de tcp, dns, y dga
* manejo de listas de exclusion 
### filtro de trafico de perimetro.
* listas de reputacion por IP
* blockeo dinamico de ip, orquestadopor el NDR
* listas negras de servicios
> la diferecnai entre blockeo y drop, 
* block manda un reset para evitar la comunicacion.
* drop no responde y deja sin  respuiesta la peticion.
 
