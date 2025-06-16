# Manual de instalación del Spanish Pathogen Portal

## Instalar dependencias (requiere permisos de admin)

1. Instalar Go y Git

```bash
sudo yum install go git gcc gcc-c++
```

2. Configurar Go

```bash
sudo mkdir -p /opt/go/bin 
sudo go env -w GOBIN=/opt/go/bin
sudo go env -w GOPATH=/opt/go
```

3. Compilar HUGO

```bash
sudo CGO_ENABLED=1 go install -tags extended,withdeploy github.com/gohugoio/hugo@latest
```

## Instalar la aplicación

1. Clonar el repo de Github

```bash
cd /opt/
sudo git clone --recursive https://gitlab.isciii.es/BU-ISCIII/spanish-pathogens-portal.git
```

2. Comprobar que está bien instalado y generar carpeta public

```bash
cd spanish-pathogens-portal
# Borrar carpeta public si existe
sudo systemctl stop httpd
rm -rf public
sudo /opt/go/bin/hugo serve --baseURL http://dpathogen.isciiides.es --port 80 --bind 172.20.10.33
```

Si todo va bien saldra este mensaje:

```bash
Start building sites … 
hugo v0.147.6-0a5fd8ebb8e2ca798515e8c564c14e32db3b4127 linux/amd64 BuildDate=2025-05-27T11:17:16Z VendorInfo=gohugoio
........
........
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://pathogenportal.isciiides.es:80/ (bind address 172.20.10.33)
Press Ctrl+C to stop
```

y se habrá creado una carpeta que se llama `public`.

3. Copiar la carpeta public generada por Hugo en la carpeta html de apache

```bash
sudo systemctl start httpd
sudo cp -r /opt/spanish-pathogens-portal/public/* /var/www/html
sudo systemctl restart httpd
```
