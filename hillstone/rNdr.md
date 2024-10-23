# Repaso de Certificacion HCSA-NDR
## Capitulo 1 
*minuto 17.35*
* El NDR existe debido a la nesecidad de ver el trafico interno y protegernos de amenazas con movimiento laterales
* podemos ver la fuga de informacion desde el interior
* Controla, dando visibilidad de lo que el NGFW y otras soluciones no alcanzan a ver
* malware, zero-day and APT
* expancion de manera lateral
* rol mas estrategico comparado con un NGFW
* Motores a destacar *ML* basado en analisis de comportamiento, revela comportamiento sospechoso de los ususarios
* manejo de trafico cifrado atravez de algoritmos para obtener una aproximacion del trafico 
	basado en un puntaje de que tan grande es la amenaza que representa.
	no rompe el cifrado de los archivos
* cumplimiento basico de WAF
	DDoS
	injection attack
	cross-site attack
	HTTP attack
* deception technology (Honeypot)
* sysmon server
	Es para windows y sirve para conentrar logs de endpoints, para tener el estado presente en el BDS
* se puede ver el nivel de amenaza de cada apliacion, basado en que tanto exponemos nuestra red al hacer uso del servicio.
* visibilidad de la topologia en la red de quien y con que interactua un end point
* Basado en el marco de Mitre attack
* Integracion con NIPS y NGFW, alimenta el sistema para que se pueden remediar y detener los traficos malisiosos por el BDS
* integracion con Isource (XDR) 
* mejoras del los ultimos BDS es disco SSD y mayor capacidada de interfaces por caja.
### topologias
*despliegue* puerto espejo

## Capitulo 2
* acceso por SSH, cable serial y acceso web
* hard reset or unset all 
* el BDS lanza una alerta antes de 30 dias de que terminen las licencias.
* podemos mantener 10 respaldos en la caja de las configuraciones del sistema
* la licencia platform es obigatoria para poder el resto de licencias.

## Capitulo 3
### zonas
* agrupamiento logico de interfaces
* zona TAP trabajo principal de analisis

## Capitulo 4
* configurar en zona TAP
* ligar la zona a una interface
* integracion con Isource 
> activar el check de applications identification 
* en la zona se deben activar todos los motores disponibles, salvo que se pida lo contrario
* antivirus requiere reinicio de equipo para aplicar
* el antivirus con templates predefinidos
* el antivirus penetra hasta 5 capas de compresion, mientras no tenga password
> el BDs hace adquision y  analisis de trafico a nivel de zona, no hay reglas ni politicas 
* toma como parametro los valores de  los CV de MITTRE
* mayor cantidad de firmas que un NGFW 
* IDS basado en firmas, proteccion de HTTP y DNS.
* ataques de DNS ()
### antispam
* proteccion por protocolo
### botnet and Comand Control Detection
* manejo por Botnet
* intalacion de malware para comando y control del equipo
* en comando y control detection podemos verificar las conexion por la reputacion y por como se llevan acabo
#### protocolos
* dns
* tcp
* http 
* dga
### sandbox
* basado en nube para detection, 
* soporte de diferentes formatos de archivos
* nesesita un reboot despues de aplicar la licencia.
### Deception
* honeypot
* asociado a una interface
* se crea un servidor
* se liga a una ip y a un puerto
### ABD
* basado en aprendizaje, para detectar el comportamiento anormal
* basado en base line
* umbrales a configurar
* generico o especifico
### web attack
* waf de baja capacidad
* servidores web
* nesesita un reboot despues de aplicar licencias
* reporte de ataques 
### Advance Threat detection
si pasamos el nivel de servers posibles o de end points
	 la herramienta deja de ver los que estan fuera del rango posible para monitorear
## capitulo 5
* amenazas
	detetion basado en varios motores
	ML y Big data
* motor de corelacion del BDS funciona dandonos la vista de como es que se pudo crear un movimiento lateral, determinar el paciente 0
* hot threat intelligent (NTI) no disponible en mexico
*el dispositivo nos muestra muchos logs de amenazas en la red*
* sandbox, colaboracion global
* escala de 0 a 100
* verificar los indicadores de compromiso con un tercero 
* toda la informacion permite saber mas acerca del sistema y tomar la mejor decision.
* categoria
	no confirmado
	ignorar
	falso positivo
	confirmar
	fixed
* exportacion de reportes
* sysmon (maquina virtual que recopila informacion) integrable con Isource

## capitulo 6
* linkage con NGFW or NIPS
* conect whit cloud view
* conect to Isource 
* threat trade server (no disponible en mexico) 
* linkage
	conexion atraves de protocolos seguros, IP directa, puerto y credenciales
	crear un usuario (recomendado unico) para administrar que modificaciones hara el BDS en el firewall para el bloqueo de las amenazas
minuto 3.54.59
* hillstone black list dinamic
* tipos de bloque manual y por reglas *and & or*

## Capitulo 7
* monitoreo, minimo de 7 dias y recomendado de 30
* alertamiento por umbrales
* usar templates y podemos usar tareas para que envie reportes
* logs de amenazas, de red, de evento, de sesion, de configuracion, sandbox
