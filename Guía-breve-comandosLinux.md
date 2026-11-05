# Guía práctica de comandos basicos en Linux
## Índice
* [1. Introducción](#1-introducción)
* [2. Requisitos Previos](#2-requisitos-previos)
* [3. Comandos por Categoría](#3-comandos-por-categoría)
* [4. Ejemplo Paso a Paso](#4-ejemplo-paso-a-paso)
* [5. Recursos Adicionales](#5-recursos-adicionales)
* [6. Diagnóstico de Red](#6-diagnóstico-de-red)
* [7. Gestión de Usuarios y Permisos](#7-gestión-de-usuarios-y-permisos)

---
## 1. Introducción
La ***línea de comandos*** o ***terminal de Linux*** es una herramienta fundamental en el entorno informático para interactuar directamente con el sistema operativo sin necesidad de una interfaz gráfica.
>A través de la terminal se pueden gestionar archivos, administrar usuarios y configurar servicios de forma eficiente.
---
## 2. Requisitos Previos
Para llevar a cabo las prácticas explicadas en esta guía es necesario contar con:
* **Sistema Operativo:** Una distribución basada en Linux (*Ubuntu, Debian, Fedora*) o una máquina virtual (*VirtualBox, VMware*).
* **Terminal:** Acceso a la interfaz de línea de comandos (se abre con `Ctrl + Alt + T` en entornos gráficos).
* **Permisos:** Usuario con privilegios de administración (`sudo`) para ejecutar comandos del sistema.
* **Editor de texto:** Visual Studio Code o un editor por consola como `nano` para la edición de archivos.

## 3. Comandos por Categoría
**A. Navegación por el sistema de archivos**
    Permite conocer la ubicación actual dentro del árbol de directorios y desplazarse entre carpetas:
  ```bash
  pwd # Print Working Directory
  ls  # List
  cd  # Change Directory
  ```
| Comando | ¿Qué hace? | E.j de Uso |
| :---: | :---: | :---: |
| pwd | Muestra la ruta absoluta del directorio en el que te encuentras actualmente | Comprobar en qué carpeta te encuentras actualmente | 
| ls | Muestra la lista de archivos y subcarpetas dentro del directorio actual | Listar los archivos y carpetas del directorio actual |
| cd | Cambia el directorio de trabajo a la ruta especifica seleccionada | Cambiar de directorio para entrar en la carpeta "Documentos" |

**B. Gestión y manioukación de documentos**
Permite crear, mover, copiar y eliminar archivos o carpetas:
 ```bash
  mkdir # Make Directory
  cp  # Copy
  mv  # Change Directory
  rm # Remove
  cat # Concatenate
```
| Comando | ¿Qué hace? | E.j de Uso |
| :---: | :---: | :---: |
| mkdir | Crea una carpeta en la ruta indicada | Crea una nueva carpeta llamada ``proyectos`` | 
| cp | Copia archivos o directorios de un origen a un destino | Copia notas.txt creando un duplicado llamado copia.txt (``cp notas.txt copia.txt``) |
| mv | Mueve un archivo o carpeta a otra ubicación | Mueve notas.txt a la carpeta /tmp/ (o lo renombra si indicas otro nombre)(``mv notas.txt /tmp/`` |
| rm | Elimina archivos de forma permanente | Elimina la carpeta proyectos y todo su contenido de forma permanente (``rm -r proyectos``) |
| cat | Muestra el contenido completo de un archivo directamente en la terminal | Muestra en pantalla el texto que contiene el archivo notas.txt (``cat notas.txt``)

**C. Permisos y administración del sistema**
Instrucciones para gestionar privilegios y mantener la terminal limpia:
  ```bash
  sudo # Superuser Do
  clear  
  history
  ```
| Comando | ¿Qué hace? | E.j de Uso |
| :---: | :---: | :---: |
| sudo | Anteponer este comando ejecuta la instrucción con privilegios de administrador (root) | Ejecuta la actualización de paquetes con permisos de administrador (root)(``sudo apt update``) | 
| clear | Limpia todo el texto visible en la pantalla de la terminal | Borrar todo el texto visible en la pantalla para dejar la terminal limpia |
| history | Muestra la lista de comandos ejecutados recientemente en la sesión actual | Despliega la lista numerada de los últimos comandos ejecutados en la sesión |
|

---

## 4. Ejemplo Paso a Paso
En el siguiente procedimiento se muestra el flujo habitual de trabajo en la terminal:
1. ***Verifica el directorio inicial***:
Ejecutar ``pwd`` para confirmar en qué carpeta del sistema se empieza a trabajar.

2. ***Crear y acceder a un entorno de prueba***:
Ejecutar ``mkdir mi_proyecto`` para crear una carpeta y luego ``cd mi_proyecto`` para entrar en ella.

3. ***Crear y comprobar un archivo:***
Ejecutar ``touch notas.txt`` para generar un documento y luego comprobar que existe ``ls -l``.

4. ***Escribir y verificar datos***
Añadir contenido al archivo y revisarlo ejecutando ``cat notas.txt``.


![](https://victorhckinthefreeworld.com/wp-content/uploads/2014/06/consola-linux-tux.jpg)

---
## 5. Recursos Adicionales
* [Documentación Oficial de Ubuntu](https://help.ubuntu.com/)
* [Manual de Comandos Linux](https://www.freecodecamp.org/espanol/news/comandos-de-linux/)
* [Tutoriales de Linux](https://youtu.be/L906Kti3gzE?si=eIHoVe9mRZQIiC9g)

---
## 6. Diagnóstico de Red
Comandos básicos para verificar el estado de la conexión y las interfaces en Linux:
* **ip addr**: Muestra las direcciones IP y la configuración de las interfaces de red.
* **ping -c 4 8.8.8.8**: Envía paquetes ICMP para comprobar la conectividad con internet.

---
## 7. Gestión de Usuarios y Permisos
Administrar usuarios y permisos es clave para mantener la seguridad en sistemas Linux:
* `whoami`: Muestra el nombre del usuario con el que has iniciado sesión actual.
* `chmod 755 archivo`: Cambia los permisos para que solo el propietario pueda modificarlo.
---
## Información del proyecto
**Esta documentación se ha elaborado utilizando Markdown.
El control de versiones se realiza mediante Git
y el repositorio remoto se encuentra alojado en GitHub.**
---
## Próximas mejoras
1. Crear un proyecto personal
2. Mejorar el proyecto actual
3. Compartir las fuentes
