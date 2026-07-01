# Laboratorio NAT y ACL

## Objetivo

Configurar un router (`Router_FW`) con tres redes conectadas (Interna, DMZ y Externa), aplicando:

- **NAT** para ocultar las IPs privadas y publicar un servidor web de la DMZ hacia Internet.
- **ACLs** para controlar qué tráfico puede pasar entre las redes (por ejemplo, evitar que la DMZ acceda a la red Interna).

## Topología

- **Red Interna** (192.168.1.0/24): PCs de usuarios.
- **DMZ** (192.168.2.0/24): servidor web público.
- **Red Externa** (192.168.3.0/24): representa Internet.

## Contenido del repositorio

- `topologia.pka` → archivo de Packet Tracer con la red simulada.
- `README.md` → este documento.

## Qué se logró

1. El servidor web de la DMZ es accesible desde la red Externa solo por el puerto 80 (HTTP).
2. La red Interna puede navegar hacia Internet y consultar el servidor de la DMZ.
3. La DMZ no puede iniciar conexiones hacia la red Interna, protegiendo la red interna en caso de que el servidor sea comprometido.
