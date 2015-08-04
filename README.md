# Jetson TK1 Cluster

## Flasheando Jetson TK1

1 - descargar Linux for Tegra
    1.1 - ir a: https://developer.nvidia.com/embedded/linux-tegra
    1.2 - descargar Drive Packages
    1.3 - descargar Sample File System
2 - descomprimir todo
    2.1 - abrir terminal e ir donde se encuentrar los archivos descargados del paso 1
    2.2 - tipear
      sudo tar xpf Tegra124_Linux_R21.4.0_armhf.tbz2
      cd Linux_for_Tegra/rootfs/
      sudo tar xpf ../../Tegra_Linux_Sample-Root-Filesystem_R21.4.0_armhf.tbz2
3 - tipear
  cd ../
  sudo ./apply_binaries.sh
4 - conectar la pc con Jetson TK1 con el cable USB Micro-B
5 - entrar en modo recovery
  5.1 - presionar y no soltar el boton "FORCE RESET" y luego pulsar el boton "RESET"
6 - flashear
  sudo ./flash.sh -S 8GiB Jetson-tk1 mmcblk0p1
7 - esperar
