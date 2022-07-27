# How to compile Qemu
Guia para compilar Qemu en Rocky Linux 9.0

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

## Compilar Qemu

```$ su```

```# pip3 install ninja```

```# nproc```
```# make -j 4```

```# make install```
