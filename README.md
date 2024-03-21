# AWS-EC2-ngnix
Nginx sobre Amazon EC2
## Bloqueo de direcciones IP
Teniendo una instancia de EC2 en funcionamiento podemos acceder a ella a través de SSH.
## Paso 1: Conectarse a tu instancia de EC2

Utiliza tu cliente SSH favorito para conectarte a tu instancia de EC2. Por ejemplo:


`ssh -i tu-llave.pem usuario@tu-direccion-ip-publica`

## Paso 2: Instalar Nginx

Primero, actualiza los repositorios de paquetes:

`sudo apt update`


Luego, instala Nginx:

`sudo apt install nginx`


## Paso 3: Agregar módulos adicionales

Existen diferentes módulos adicionales que puedes agregar a Nginx según tus necesidades específicas. Aquí te mostraré cómo agregar algunos ejemplos comunes:

### ·3.1: Agregar el módulo ngx_http_geoip_module

Este módulo permite la resolución de direcciones IP a ubicaciones geográficas. Para instalarlo:

`sudo apt install nginx-extras`


Luego, puedes habilitar el módulo agregando la configuración adecuada en tus archivos de configuración de Nginx.

### ·3.2: Agregar el módulo ngx_http_ssl_module

Este módulo es útil si deseas habilitar el soporte SSL/TLS en tu servidor Nginx. Sin embargo, en la mayoría de los casos, este módulo ya viene incluido con la instalación predeterminada de Nginx.

## Paso 4: Configurar los módulos

Después de instalar los módulos, es posible que necesites configurarlos según tus necesidades. Esto puede incluir ajustes en el archivo de configuración de Nginx (`nginx.conf`) o en archivos de configuración específicos para cada sitio (`/etc/nginx/sites-available/*`).

## Paso 5: Reiniciar Nginx

Una vez que hayas instalado y configurado los módulos según tus necesidades, reinicia Nginx para que los cambios surtan efecto:

`sudo systemctl restart nginx`

## Paso 6: Verificar el funcionamiento

Puedes verificar que Nginx se esté ejecutando correctamente y que los módulos adicionales estén funcionando según lo esperado visitando la dirección IP pública de tu instancia de EC2 en un navegador web y realizando pruebas específicas según los módulos que hayas instalado.
