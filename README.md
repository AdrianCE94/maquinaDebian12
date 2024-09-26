# maquinaDebian12
Preparación de una maquina con su configuración personalizada

# Requisitos para Preparar una Máquina Virtual con Debian 12

## 1. Requisitos Generales

Antes de comenzar, asegúrate de cumplir con los siguientes requisitos en tu sistema operativo base:

### 1.1 Hardware Recomendado
- **Procesador**: Intel/AMD con soporte de virtualización (habilitado en la BIOS/UEFI).
- **RAM**: Al menos 4 GB (recomendado 8 GB o más).
- **Almacenamiento**: Espacio disponible de al menos 25 GB para la máquina virtual.
- **Conexión a Internet**: Para descargar las ISOs y actualizar el sistema operativo.

## 2. Instalación de VirtualBox según el Sistema Operativo Host

### 2.1 Windows 11
1. Descarga la última versión de VirtualBox desde [https://www.virtualbox.org](https://www.virtualbox.org/wiki/Downloads).
2. Ejecuta el instalador y sigue los pasos predeterminados.
3. Instala el **Extension Pack** para soporte adicional de dispositivos USB, RDP, etc.
   - Descárgalo desde la misma página de VirtualBox.
   - Ve a `Archivo > Preferencias > Extensiones` y añade el **Extension Pack**.

### 2.2 macOS
1. Descarga VirtualBox para macOS desde [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads).
2. Ejecuta el instalador y sigue las instrucciones.
3. **(Opcional)**: Instala el **Extension Pack** siguiendo los mismos pasos que en Windows.

### 2.3 Linux (Ubuntu/Debian)
1. Añade el repositorio oficial de VirtualBox:
   ```bash
   sudo apt update
   sudo apt install virtualbox
   sudo apt install virtualbox-ext-pack

## 3. Descarga de Debian 12 (64 bits)

1. Visita el sitio oficial de Debian: https://www.debian.org/index.es.html

2. **Descarga la ISO del DVD**:
   - Para una instalación completa sin requerir una conexión a Internet, elige la imagen **DVD**.
   - Haz clic en el enlace de descarga del primer DVD (DVD-1) que contiene los paquetes necesarios para la instalación básica.

   - **URL directa**: https://cdimage.debian.org/debian-cd/current/amd64/iso-dvd/
   
     ![isoDebian](imgs/image.png)
     

   - **Tamaño del archivo**: Alrededor de 4GB

---

Asegúrate de que la imagen ISO descargada esté completa antes de continuar con la creación de la máquina virtual.

## 4. Requisitos de Instalación de Debian 12

![requires](image2.png)

## 4.3 Requisitos de Recursos Asignados a la Máquina Virtual

Para optimizar el rendimiento durante la instalación de Debian 12, se han asignado los siguientes recursos a la máquina virtual:

- **RAM Asignada**: 5000 MB (5 GB)
  - **Nota**: Aunque 4500 MB (4.5 GB) es suficiente, se ha asignado 5000 MB para acelerar el proceso de instalación.

- **Procesadores Asignados**: 4 núcleos
  - **Nota**: Aunque 2 núcleos (procesadores) son suficientes, se han asignado 4 núcleos para mejorar la velocidad de instalación.
  - **Nota**: Si tu sistema tiene menos núcleos, asigna solo los disponibles.
  
- **Almacenamiento Asignado**: En mi caso he asignado 40gb de almacenamiento dinámico.
  - **Nota**: El almacenamiento dinámico es una característica que permite que el tamaño del disco virtual crezca a medida que se necesite, hasta un tamaño máximo que se haya especificado al crear el disco.
- **Adaptador de Red**: adaptador puente.
  - **Nota**: El adaptador de red en modo puente permite que la máquina virtual se comunique directamente con la red física, obteniendo una dirección IP de la misma subred que el host.(mas adelante configuraremos la red en la maquina virtualen el propio debian12)
---

Estos recursos ayudarán a garantizar que la instalación de Debian 12 se realice de manera eficiente y rápida.

![vb](image3.png)