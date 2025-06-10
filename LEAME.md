# Manual de instalación del Spanish Pathogen Portal

## Instalar dependencias

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
CGO_ENABLED=1 go install -tags extended,withdeploy github.com/gohugoio/hugo@latest
```

## Instalar la aplicación

1. Clonar el repo de Github

```bash
git clone --recursive https://github.com/BU-ISCIII/spanish-pathogens-portal.git
```

2. Comprobar que está bien instalado

```bash
cd node-pathogens-portal
sudo /opt/go/bin/hugo serve --baseURL http://dpathogen.isciiides.es --port 80 --bind 172.20.10.33
```

Si todo va bien saldra este mensaje:

```bash
Start building sites … 
hugo v0.147.6-0a5fd8ebb8e2ca798515e8c564c14e32db3b4127 linux/amd64 BuildDate=2025-05-27T11:17:16Z VendorInfo=gohugoio
........
........
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://dpathogen.isciiides.es:80/ (bind address 172.20.10.33)
Press Ctrl+C to stop
```

3. Copiar la carpeta public generada por Hugo en la carpeta html de apache

```bash
sudo cp -r /opt/node-pathogens-portal/public /var/www/html
```