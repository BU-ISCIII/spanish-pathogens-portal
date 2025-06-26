## Manual de despliegue del portal en producción

Este documento describe los pasos para instalar el portal en el servidor web desde el fichero proporcionado en GitLab.

- [Manual de despliegue del portal en producción](#manual-de-despliegue-del-portal-en-producción)
  - [1. Descargar el archivo desde GitLab](#1-descargar-el-archivo-desde-gitlab)
  - [2. Descomprimir el contenido en `/var/www/html`](#2-descomprimir-el-contenido-en-varwwwhtml)
  - [3. Establecer permisos seguros](#3-establecer-permisos-seguros)
  - [4. Configurar el VirtualHost de Apache](#4-configurar-el-virtualhost-de-apache)
  - [Verificación](#verificación)

### 1. Descargar el archivo desde GitLab

Descargar el paquete comprimido desde la siguiente URL (requiere sesión activa en GitLab): https://gitlab.isciii.es/-/project/259/uploads/b795438b82f58d5ec6187e6195acf86e/public.tar.gz, y copiarlo al servidor.

### 2. Descomprimir el contenido en `/var/www/html`

```bash
sudo mkdir -p /var/www/html/pathogens_portal_public
sudo tar -xzf public.tar.gz -C /var/www/html/pathogens_portal_public --strip-components=1
sudo rm -rf public.tar.gz
```

Esto dejará los archivos estáticos del portal en:

```bash
/var/www/html/pathogens_portal_public
```

### 3. Establecer permisos seguros

Se recomienda configurar los permisos de forma que:

- Los archivos sean legibles por el servidor web (por ejemplo, `apache` o `www-data`)
- No se permita escritura

```bash
sudo chown -R apache:apache /var/www/html/pathogens_portal_public
sudo find /var/www/html/pathogens_portal_public -type d -exec chmod 750 {} \;
sudo find /var/www/html/pathogens_portal_public -type f -exec chmod 640 {} \;
```

### 4. Configurar el VirtualHost de Apache

Crear un archivo de configuración, por ejemplo `/etc/httpd/conf.d/pathogens_portal.conf`:

```apache
<VirtualHost *:80>
 
    ServerAdmin sistemas@isciii.es
    ServerName pathogensportal.isciiides.es
    DocumentRoot /var/www/html/pathogens_portal_public
 
    <Directory /var/www/html/pathogens_portal_public>
        Options Indexes FollowSymLinks
        AllowOverride None
        Require all granted
    </Directory>
 
    ErrorLog logs/pathogens_portal.pre.isciiides.es-apache.error.log.log
    CustomLog logs/pathogens_portalpre.isciiides.es-apache.access.log combined
 
</VirtualHost>
```

Reiniciar Apache para aplicar los cambios:

```bash
sudo systemctl restart httpd
```

### Verificación

Abrir en el navegador:

```bash
http://pathogensportal.isciiides.es/
```

Debería mostrarse el portal estático desplegado correctamente.
