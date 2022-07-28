# Guia de compilación de Qemu Rocky Linux 9 Workstation
Guia para compilar Qemu en un clonico binario RHEL 9.

## 1. Instalar las dependencias

```$ sudo dnf install python3 python3-pip pkgconf-pkg-config glib2-devel libmount-devel pixman-devel lzo-devel gtk3-devel```

## 2. Crear un directorio para alojar el codigo a compilar

```$ mkdir sources```

```$ cd sources```

## 3. Descargar y descomprimir archivo *.tar.xz

```$ wget https://download.qemu.org/qemu-7.0.0.tar.xz```

```$ tar Jxvf qemu-7.0.0.tar.xz```

```$ cd qemu-7.0.0```

## Configurar parámetros necesarios

```$ ./configure --help```

```$ ./configure --prefix=/opt/qemu --target-list=x86_64-softmmu --enable-gtk```

## Entrar en modo superusuario e instalar ninja

```$ su```

```# pip3 install ninja```

## Verificar núcleos disponibles para compilar y compilación con Make

```# nproc```

```# make -j 4```

```# make install```
