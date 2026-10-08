# Pi hole Bloqueador de anuncion es la red

## Indice

- [1. Que es Pi-hole](#1-que-es-pi-hole.)
  - [1.2 Requerimientos](#12-requerimientos)
- [2. Instalación](#2-instalación)

## 1. Que es Pi-hole

![Imagen pi-hole](https://wp-cdn.pi-hole.net/wp-content/uploads/2016/12/Vortex-R.png)
Pi hole es un sistema de filtado de ip el cual reside en la capa de la [DNS](https://en.wikipedia.org/wiki/DNS_sinkhole) Permitiendo un bloque a nivel de red y lo mas inportante de codigo libre y gratuito.

### 1.2 Requerimientos

- Hardware
  - 2GB de espacio siendo recomendado 4GB
  - 512 MB de RAM
- Software
  - Cualquier sistema con systemd o sysvinit
- Sistemas Operativos
  - Alpine
  - Armbian OS
  - Debian
  - CentOS Stream
  - Fedora
  - Raspberry PI OS
  - Ubuntu
- Direciones ip
  - Necesidad de direcion IP statica
- Ports
  - 53 TCP/UDP
  - 67 IPv4 UDP
  - 547 IPv6 UDP
  - 80 TCP
  - 443 TCP
  - 123 UDP

_Pi-hole puede ser soportado por mas sistemas operativos pero no es soportado de forma nativa_

## 2. Instalación

Para instalar Pi-hole se puede realizar de forma automatizada con un simple comando :

```
curl -sSL https://install.pi-hole.net | bash
```

O la alternativa de un repositorio clon

```
git clone --depth 1 https://github.com/pi-hole/pi-hole.git Pi-hole
cd "Pi-hole/automated install/"
sudo bash basic-install.sh
```

O la instalacion con docker en la cual no profundizare la [documentacion oficial de docker](https://docs.pi-hole.net/docker/)

## 3. Post-Install

### IMPORTANTE ESTES PASOS PUEDEN DEJARTE SIN ACCESO A INTERNET

De forma por defecto Pi-hole no sera usado por tu red para ello configuraremos nuestro ruter personal para usarlo como dns por defecto tambien podriamos configurar a Pi-hole como cliente DHCP si tu ruter no lo permite

[Para configurar Pi-Hole como DNS](https://discourse.pi-hole.net/t/how-do-i-configure-my-devices-to-use-pi-hole-as-their-dns-server/245)

[Para configurar Pi-Hole como DHCP](https://discourse.pi-hole.net/t/how-do-i-use-pi-holes-built-in-dhcp-server-and-why-would-i-want-to/3026)
