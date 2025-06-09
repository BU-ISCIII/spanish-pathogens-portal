# Instalation manual

## Content

- [Instalation manual](#instalation-manual)
  - [Content](#content)
  - [Install Hugo](#install-hugo)
    - [Ubuntu](#ubuntu)
      - [Last github release deb file](#last-github-release-deb-file)
    - [Using snap](#using-snap)
  - [Install githu](#install-githu)
  - [Setup](#setup)
  - [Hosting](#hosting)

## Install Hugo

### Ubuntu

#### Last github release deb file

- `Hugo v0.139` or higher (see [here](https://gohugo.io/installation/) for Hugo installation)

```bash
wget https://github.com/gohugoio/hugo/releases/download/v0.147.6/hugo_0.147.6_linux-amd64.deb
sudo dpkg -i hugo_0.147.6_linux-amd64.deb
```

### Using snap

```bash
sudo apt update -y && sudo apt dist-upgrade -y
sudo apt install snapd
snap install hugo
```

## Install githu

```bash
sudo apt-get install github
```

## Setup

The following steps are for a quick setup/starting guide.

1) Clone this repository to your computer using the following command in a terminal ([demo video](https://youtu.be/671ij1kB2EU))

    ```bash
    git clone --recursive git@github.com:BU-ISCIII/node-pathogens-portal.git
    ```

    **Note** the `--recursive` mentioned in the command is **important to include** in the command.

2) Change into the downloaded repository

    ```bash
    cd node-pathogens-portal.git
    ```

3) Start `hugo` and see if works as expected ([demo video](https://youtu.be/L4cLXx90dJI))

    ```bash
    hugo serve
    ```

    If everything is good, you should see output similar to what mentioned below

    ```bash
    Start building sites … 
    hugo v0.147.6-0a5fd8ebb8e2ca798515e8c564c14e32db3b4127 linux/amd64 BuildDate=2025-05-27T11:17:16Z VendorInfo=gohugoio
    ........
    ........
    Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
    Web Server is available at http://localhost:1313/ (bind address 127.0.0.1) 
    Press Ctrl+C to stop
    ```

4) Open a browser and typr the URL `http://localhost:1313/`. You will see the bare minimum website with example content.

## Hosting

Hosting means getting the content to the internet, this can be done in different ways. Contact your university/group IT team regarding this, as there can be organisational policies/regulations on this.
