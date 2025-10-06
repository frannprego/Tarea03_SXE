
# Práctica Docker Alpine

## 1. Descargar la imagen Alpine
- Comando:
  ```bash
  docker pull alpine
- Descripción: Descarga la imagen sin arrancarla.

## 2. Crear contenedor sin nombre
- Comando:
  ```bash
  docker create alpine
- Descripción: Crea un contenedor pero no lo arranca

## 3. Crear contenedor dam_alp1
- Comando:
  ```bash
   docker run -it --name dam_alp1 alpine sh
- Descripción: Crea y accede al contenedor.

## 4. Comprobar ip y ping a google
- Comando:
  ```bash
    ip addr
- Comando ping:
  ```bash
  ping -c 4 google.com
- Descripción: Obtener IP y comprobar conexión.

## 5. Crear contenedor dam_alp2 y ping entre contenedores
- Comandos:
  ```bash
  docker run -it --name dam_alp2 alpine /bin/sh
  apk add iproute2 iputils
  docker exec dam_alp1 ip addr show eth0
  ping -c 4 <IP_dam_alp1>
- Se crea un segundo contenedor y se instala ping.
- Con la IP de dam_alp1, hacemos ping desde dam_alp2.
- Los contenedores se pueden comunicar porque están en la misma red

## 6. Sal del terminal, ¿qué ocurre con el contenedor?
- Comando:
   ```bash
     exit
- Descripción: El contenedor se detiene, pero no se elimina.

## ## 7. Espacio en disco
- Comando:
    ```bash
    docker system df
 - Descripción: Muestra la memoria ocupada en disco.

## Uso de RAM
- Comando:
  ```bash
    docker stats
- Descripción: Muestra el uso de RAM y CPU de los contenedores.



