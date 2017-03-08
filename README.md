# RETO_20_3_2017_ANM

Este repositorio contiene informacion para la instalacion del OpenDataBus sin el uso de los scripts de Vagrant/Ansible. Esta actividad esta planteada como un ejercicio a realizar en dos semanas. Implica la instalacion de VirtualBox, Docker y Rancher y require aprender alguno de los conceptos basicos de estas tres herramientas.

Pasos:

1 - Instalacion de Oracle Virtual Box. Seguir las instrucciones en https://www.virtualbox.org/manual/ch01.html#intro-installing, los "extension packs" son opcionales.

2 - Creacion de una maquina virtual con Ubuntu Server 14 (64 bits). Descargar de http://releases.ubuntu.com/14.04/. Instalar el OpenSSH server.

3 - Preferiblemente configurar esa maquina virtual con el primer interfaz de red tipo NAT y el segundo "Red solo anfitrion".

4 - Instalar Docker en esa maquina virtual. Seguir las instrucciones en https://docs.docker.com/engine/installation/linux/ubuntu/

5 - Instalar Rancher https://docs.rancher.com/rancher/v1.5/en/installing-rancher/installing-server/#single-container

6 - Instalar OpenDataBus

6.1 - Se accede a http://laipdelamaquina:8080 y se crea un usuario en Rancher (Admin->Access Control y Local Authentication)

6.2 - Se agrega un host a rancher (Infrastructure->Hosts Add Host)

6.3 - Se agrega el catalogo (Admin->Settings y Add Catalog) la url del catalogo es https://open-data-bus:xxxxxx@bitbucket.org/open-data-bus/open-data-catalog

6.4 - Se agrega el registry (Infrastructure->Registries y Add Registry y tipo Custom) la  url del registro es ec2-35-157-174-83.eu-central-1.compute.amazonaws.com

6.5 - Se agregan los certificados (pedir a German Blanco por correo)

6.6 - Ir a Catalog-> El nombre que hayais puesto ... Seleccionar CoreDemo Details y Launch

6.7 - Lanzar un Zeppelin o Jupyter del catalogo contra el CoreDemo
