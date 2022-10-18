
Configuración y explicación ALPINE Diego Varela



_1. Volumen por separado de la configuración_
Creamos "nuevo_volumen" que es el volumen que va a tener nuestro alpine.



_2. Red propia interna para todos los contenedores_

En docker-compose, vamos a network y le añadimos la subred "Red_Practica_DNS"



_3. ip fija en el servidor_
Le damos la ip fija en docker-compose.yml. 

		10.1.0.90


_4. Configurar Forwarders_
Le configuramos los Forwaders en named.conf.options añadiendo los mismos:
8.8.8.8
8.8.4.4
1.1.1.1



_5. Crear Zona propia_

Para añadir una nueva zona me dirijo a config, posteriormente a named.conf.local y añadimos las zonas.


_6. Registros a configurar: NS, A, CNAME, TXT, SOA_

En zonas,accedemos a db.asircastelao.int y le añadimos la zona ns.DiegoV_DNS.int



_7. Cliente con herramientas de red_

Para añadir el cliente nos dirijimos a docker-compose.yml y añadimos el cliente en:
container_name: asir_cliente


