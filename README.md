
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
- Descripción: Obtener IP y comprobar conexión.ç


