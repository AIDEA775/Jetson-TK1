# Jetson TK1 Cluster

## Flasheando Jetson TK1

#####1 - descargar Linux for Tegra

    1.1 - ir a: https://developer.nvidia.com/embedded/linux-tegra
    
    1.2 - descargar Drive Packages
    
    1.3 - descargar Sample File System

#####2 - descomprimir todo

2.1 - abrir terminal e ir donde se encuentrar los archivos descargados del paso 1
    
2.2 - tipear

    sudo tar xpf Tegra124_Linux_R21.4.0_armhf.tbz2
      
    cd Linux_for_Tegra/rootfs/

    sudo tar xpf ../../Tegra_Linux_Sample-Root-Filesystem_R21.4.0_armhf.tbz2
      
#####3 - tipear

    cd ../

    sudo ./apply_binaries.sh
  
#####4 - conectar la pc con Jetson TK1 con el cable USB Micro-B

#####5 - entrar en modo recovery

    presionar y no soltar el boton "FORCE RESET" y luego pulsar el boton "RESET"
  
#####6 - flashear

    sudo ./flash.sh -S 14580MiB jetson-tk1 mmcblk0p1
  
#####7 - esperar


## Accediendo por ssh sin router

    http://elinux.org/Jetson/Remote_Access#Hard_method:_Manually_setting_up_a_DHCP_server

Nota: pude usar comandos (e.g. sudo apt-get update) e iniciar aplicaciones graficas (e.g. nautilus) pero no pude ejecutar algun programa CUDA o OpenGL

Nota2: para cambiar de una Jetson a otra

    matar Network Manager:  sudo pkill NetworkManager
    
    restablecer server dhcp:  sudo /etc/init.d/dnsmasq restart
    
    probrar con ping: ping tegra-ubuntu


## Log

4 ago 2015 - las 3 Jetson TK1 fueron flasheadas

6 ago 2015 - actualizado los 3 ubuntus a lo ultimo ultimo (apt-get upgrade)

6 ago 2015 - pegadas las patitas con poxipol

7 ago 2015 - cables de red desgastados con amoladora de banco :D

10 ago 2015 - configuradas las direcciones IP y definido el nodo maestro

10 ago 2015 - ssh login sin clave 
