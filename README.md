# Guia de compilación de Qemu Rocky Linux 9 Workstation
Guia para compilar Qemu en un clonico binario RHEL 9.

Esta compilación es para emulación de máquinas x86_64, con interfaz GTK.

## 1. Instalar Herramientas de desarrollo y dependencias

```# su```

```# dnf groupinstall "Herramientas de desarrollo"```

```# dnf install python3 python3-pip pkgconf-pkg-config glib2-devel libmount-devel pixman-devel lzo-devel gtk3-devel```

## 2. Ir al directorio para alojar el codigo

```$ cd /usr/local/src```

## 3. Descargar y descomprimir archivo *.tar.xz

```$ wget https://download.qemu.org/qemu-7.0.0.tar.xz```

```$ tar Jxvf qemu-7.0.0.tar.xz```

```$ cd qemu-7.0.0```

## Configurar parámetros necesarios

```# pip3 install ninja```

```$ ./configure --help```

```$ ./configure --target-list=x86_64-softmmu,i386-softmmu --enable-gtk```

## Verificar núcleos disponibles para compilar y compilación con Make

```# nproc```

```# make -j <nproc>```

```# make install```
