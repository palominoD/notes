
# Repaso para certificacion HCSS
## vision comercial de los sistemas
## overview
> tenemos certificacion HCSA, HCSP. HCSE, HCSS y Tech labs
> 20 preguntas con un 70% a 30 minutos

## modulo 1
* 2 vertientes principales amplitud (por tipo de infraestructura)
* vertiente 2 por profundidad, que se derive entre los tipos de sistemas que se manejan
* se ofrece covertura, control y consolidacion

### que se hace para tener una eguridad integrativa
> covertura sin depender de entorno
> tener el control, con tar con vita de toda la infraestructura y saber que pasa en ella
> consolidacion, reduce lso costos al reducir los equipos.

### cobertura
> virtual, fisico, microsegmentacion, soluciones de visibilidades
> soluciones de nube, perimetrales, soluciones de data center, de movimiento latera y soluciones de craga de trabajo
> implementacion por modulos para la comodidad.
* solucion de brecha, pre o post
> motores de seguridad

### consolidacion
> analisis de datos atraves de soluciones especificas para determinar las acciness correctas

### funciones principales
> seguridad de red
> itigacion de amenazas
> poteccion de las cargas de trabajo (cloude armour)

### series de NGFW A, E, EP
> todos tiene diferentes motores para la integracion.
> entre mayor storage mayor detalle en los reportes.
> sdwan seguro esta enbebido en el cloud edge.

### protection
> QOS
> conexion vpn donde si es site to site, se puede tener entre 2 configuraciones iguales, agnostico de las marcas
> Reduccion de costo

### NDR 
> se denomina BDS y nos permite tener deteccion de criptomining, ramsonware, botnet,dga, ataques internos y comportamiento sospoechoso.
> analisis de este a oeste, analisis dentro de la red, complementa ya que el NGFW solo vigila norte sur, que sale o entra.
> el sistema NDR reporte logs a el XDR
> NDR, no intrusiva, monitorea el trafico a taves de un port mirror
> soluciona NDR para el analisis forense para determinar y gestionar

### proteccion perimetral y despues a proteccion de nube.
> ngfw norte a sur
#### cloude hide
* solo se implementa en Vware
* tiene la misma teoria que un NDR
* es un software para vmware
* microsegmentacion
* no necesita NSX
* se dimenciona por servidores fisicos y por cantidades de CPU 
* si quieres tener vware y proteccion lateral para micoegmentation, ocupamos CLOUD HIVE

#### cloude armour
* no importa si es nuve publica o privada
* requerimos un agente en el contenedor
* todos los contenedores o host tienen que reportar al armour

### impementacion de zerotrust

### centros de eatencion tecnica 
> mexico, estados unidos y china
> soporte en ingles, espanol y portugues
* trabaja en el cuadrante de visionarios en gartner

## MOdulo 2
> edge proteccion
> cloud protection
> prevention de brechas
> prencion de applicacion 
> manejo central

### NGFW
#### serie A
* l2 to l7, QOS, VPN 
* dos bundles, basico o general (motores o modulos para activar)
* valor real throughput para alto valor de trafico, todos los modleos activados
* hasta 2 TB
* si se usa fibra se deve usar tranceiver.

### ZTNA
> se puede configurara el sistema, y politicas especificas de las cuales debes de cumplir para accesar a los servicios, 
> no se puede conocer el gateway
> minimos privilegios para darle accesoa un usuario conocido

### HSM
* proteccion perimetral
* sd-wan 
* gestion centralizada
* gestion competa de todos los sitioss para despliegues o configuraciones masivas
* manera intelogtete y facil de contolar por consola.

#### serie x
* requeitos de dato moderno, amplio throughput
* equipos grandes
* modulos de puerto

> twin mode (hacer uo de HA en un itio y un twin mode entre diferente localidade)


### NIPS
* serie s
* visibilidad  dentro de la red

