# Informe de Práctica No. 1: Creación y Manipulación de Archivos en Linux

**Nombre:** Josue Moscoso  
**Fecha:** 19 de abril de 2026  
**Asignatura:** Tendencias Tecnológicas

---

## 1. Título
**Creación y Manipulación de Archivos en Sistemas Linux mediante Comandos de Terminal**

### Descripción
Esta práctica proporciona una introducción fundamental a la administración de archivos y directorios en sistemas operativos basados en Linux, utilizando la terminal de comandos como herramienta principal. A través de ejercicios prácticos, el estudiante adquirirá competencias en la navegación, creación, copia, movimiento y eliminación de archivos, consolidando su dominio de los comandos esenciales del shell de Linux.

---

## 2. Tiempo de Duración
**Tiempo estimado:** 45 minutos

---

## 3. Fundamentos

### 3.1 Conceptos Teóricos Fundamentales

El sistema operativo Linux utiliza un modelo jerárquico de organización de archivos basado en la estructura de árbol invertido. Este modelo, contrario a otros sistemas operativos, proporciona una alternativa unificada y coherente para el acceso a archivos, directorios y dispositivos. A continuación se detallan los conceptos clave:

#### **Sistema de Archivos en Linux**
El sistema de archivos Linux sigue el estándar FHS (Filesystem Hierarchy Standard), que define cómo se deben organizar los archivos y directorios en un sistema Unix. La estructura comienza desde el directorio raíz `/`, denominado "root", del cual cuelgan todos los demás directorios. Esta jerarquía permite una organización lógica y eficiente del sistema.

**Figura 3-1. Estructura Jerárquica del Sistema de Archivos Linux**
```
/
├── home/
│   └── usuario/
│       └── Documentos/
├── var/
├── etc/
├── usr/
└── tmp/
```

#### **Tipos de Archivos**
En Linux, todo es considerado un archivo, incluyendo directorios, dispositivos y sockets. Los tipos principales son:

- **Archivos regulares**: Contienen datos como texto, binarios, imágenes, etc.
- **Directorios**: Contenedores lógicos que organizan archivos y otros directorios.
- **Enlaces simbólicos**: Referencias a otros archivos o directorios.
- **Archivos especiales**: Representan dispositivos del sistema.

#### **Redireccionamiento de Flujos de Datos**
El redireccionamiento es un concepto fundamental en Linux que permite modificar el origen (entrada) o destino (salida) de los datos en un comando. Los operadores principales son:

- **`>`**: Redirecciona la salida estándar (stdout) a un archivo, sobrescribiendo su contenido.
- **`>>`**: Redirecciona la salida estándar a un archivo, añadiendo contenido al final sin sobrescribir.
- **`<`**: Redirecciona la entrada estándar (stdin) desde un archivo.
- **`2>`**: Redirecciona el error estándar (stderr).

**Figura 3-2. Esquema de Redireccionamiento de Flujos en Linux**
```
Entrada (stdin)  ← < archivo.txt
      ↓
  COMANDO
      ↓
Salida (stdout)  → > archivo.txt (sobrescribe)
                 → >> archivo.txt (añade)

Error (stderr)   → 2> error.log
```

#### **Operaciones Básicas de Archivos**
Las operaciones fundamentales para manipular archivos incluyen:

- **Creación**: `touch`, `mkdir`, `echo`
- **Lectura**: `cat`, `less`, `more`
- **Copia**: `cp` (con opciones como `-r` para directorios)
- **Movimiento/Renombrado**: `mv`
- **Eliminación**: `rm`, `rmdir`
- **Listado**: `ls` con diversas opciones (`-l`, `-a`, `-h`)

#### **Rutas Absolutas y Relativas**
Existen dos formas de especificar ubicaciones de archivos:

- **Ruta absoluta**: Comienza desde la raíz `/`, ejemplo: `/home/usuario/Documentos/archivo.txt`
- **Ruta relativa**: Se especifica desde el directorio actual, utilizando `.` (directorio actual) y `..` (directorio padre)

### 3.2 Importancia en la Práctica Profesional

El dominio de estos comandos es esencial para cualquier profesional en informática. Los administradores de sistemas Linux, desarrolladores de software, especialistas en DevOps y ingeniero de datos utilizan constantemente estas herramientas. La capacidad de manipular archivos eficientemente desde la terminal aumenta significativamente la productividad en entornos de producción.

**Figura 3-3. Flujo de Trabajo Típico en Administración de Linux**
```
Acceso Terminal → Navegación → Creación → Edición → Copia/Movimiento → Respaldo
```

---

## 4. Conocimientos Previos

Para realizar esta práctica, el estudiante necesita tener claros los siguientes temas:

- **Comandos básicos de Linux**: `cd`, `ls`, `pwd`, `mkdir`, `echo`
- **Manejo de navegador**: Capacidad de buscar documentación y referencias en línea
- **Concepto de terminal o consola**: Comprensión de la interfaz de línea de comandos
- **Sistema operativo Windows/Linux/Mac**: Conocimientos básicos del SO que utiliza
- **Estructura de carpetas**: Entendimiento de cómo se organizan archivos en un sistema
- **Edición de texto básica**: Capacidad de escribir y editar contenido en la terminal
- **Conceptos de rutas de archivos**: Diferenciación entre rutas absolutas y relativas

---

## 5. Objetivos a Alcanzar

Al finalizar esta práctica, el estudiante será capaz de:

1. **Crear estructuras de directorios** complejas mediante comandos de terminal
2. **Manipular archivos** utilizando comandos de copia, movimiento y eliminación
3. **Implementar redireccionamientos de flujo de datos** (`>` y `>>`) para crear y modificar archivos
4. **Utilizar rutas relativas y absolutas** correctamente en la terminal
5. **Gestionar el ciclo completo de creación, copia, movimiento y eliminación** de archivos y directorios
6. **Documentar acciones realizadas** mediante el historial de comandos
7. **Resolver problemas comunes** en manipulación de archivos mediante comandos de Linux

---

## 6. Equipo Necesario

Para realizar esta práctica se requiere:

- **Computador** con sistema operativo Windows 10/11, Linux (cualquier distribución) o macOS
- **Terminal de línea de comandos**: 
  - En Windows: Git Bash, WSL (Windows Subsystem for Linux), o PowerShell
  - En Linux: Terminal nativa
  - En macOS: Terminal nativa
- **Acceso a editor de texto** (nano, vim, vi) o capacidad de crear archivos con `echo` y redireccionamiento
- **Conexión a internet** para consultar documentación (opcional)
- **Permisos de lectura/escritura** en el directorio de trabajo

---

## 7. Material de Apoyo

- [Documentación oficial de Linux](https://linux.die.net/)
- [GNU Bash Manual](https://www.gnu.org/software/bash/manual/)
- [Guía de Asignatura: Tendencias Tecnológicas](link_a_guia)
- [Cheat Sheet de Comandos Linux](https://cheatography.com/davechild/cheat-sheets/linux-command-line/)
- [Manual de redireccionamiento en Bash](https://www.gnu.org/software/bash/manual/html_node/Redirections.html)
- [Tutorial interactivo de Linux](https://www.learnshell.org/)
- [Explicación de permiso de archivos y directorios](https://www.linux.com/training-tutorials/understanding-linux-file-permissions/)

---

## 8. Procedimiento

### Paso 1: Crear la estructura de directorios

Crear un directorio raíz llamado `proyecto_comandos` y organizar tres subdirectorios en su interior.

```bash
mkdir proyecto_comandos
cd proyecto_comandos
mkdir documentos imagenes scripts
```

**Figura 8-1. Estructura de Carpetas Creada**
```
proyecto_comandos/
├── documentos/
├── imagenes/
└── scripts/
```

### Paso 2: Crear archivo de notas en la carpeta documentos

Navegar a la carpeta documentos y crear un archivo `notas.txt` con múltiples líneas de contenido.

```bash
cd documentos
echo -e "Primera nota de la práctica\nSegunda nota: Aprendiendo Linux\nTercera nota: Finalizando edición" > notas.txt
```

Verificar el contenido del archivo:
```bash
cat notas.txt
```

### Paso 3: Copiar el archivo a scripts y renombrarlo

Copiar el archivo `notas.txt` a la carpeta scripts con el nombre `backup_notas.txt`.

```bash
cp notas.txt ../scripts/backup_notas.txt
```

Verificar que la copia se realizó correctamente:
```bash
ls -la ../scripts/
```

### Paso 4: Mover el archivo a la carpeta imágenes

Mover el archivo `backup_notas.txt` desde scripts a imagenes.

```bash
mv ../scripts/backup_notas.txt ../imagenes/
```

Verificar que el movimiento se completó:
```bash
ls -la ../imagenes/
```

### Paso 5: Crear archivo de resumen con redireccionamiento

Crear un archivo `resumen.txt` que contenga el contenido de `notas.txt` usando redireccionamiento.

```bash
cat notas.txt > resumen.txt
```

### Paso 6: Añadir contenido al resumen sin sobrescribir

Agregar una línea de cierre al archivo `resumen.txt` utilizando `>>` (append).

```bash
echo "Línea de cierre del resumen." >> resumen.txt
```

Verificar el contenido final:
```bash
cat resumen.txt
```

### Paso 7: Eliminar archivo

Eliminar el archivo `backup_notas.txt` de la carpeta imagenes.

```bash
rm ../imagenes/backup_notas.txt
```

### Paso 8: Eliminar directorio vacío

Eliminar la carpeta imágenes ahora que está vacía.

```bash
rmdir ../imagenes
```

Verificar la estructura final:
```bash
cd ..
ls -la
```

**Figura 8-2. Estructura Final del Proyecto (max 800px)**
```
proyecto_comandos/
├── documentos/
│   ├── notas.txt
│   └── resumen.txt
└── scripts/
```

---

## 9. Resultados Esperados

### 9.1 Archivos Creados

Al completar la práctica, se deben observar los siguientes resultados:

**Figura 9-1. Contenido del archivo notas.txt**
```
Primera nota de la práctica
Segunda nota: Aprendiendo Linux
Tercera nota: Finalizando edición
```

**Figura 9-2. Contenido del archivo resumen.txt**
```
Primera nota de la práctica
Segunda nota: Aprendiendo Linux
Tercera nota: Finalizando edición
Línea de cierre del resumen.
```

### 9.2 Verificación de Estructura Final

Ejecutar el comando `tree proyecto_comandos` o `ls -R proyecto_comandos` debe mostrar:

```
proyecto_comandos/
├── documentos
│   ├── notas.txt
│   └── resumen.txt
└── scripts
```

### 9.3 Evidencia de Historial de Comandos

Ejecutar `history` para verificar el registro de todos los comandos utilizados durante la práctica:

```bash
history | tail -20
```

Los resultados demuestran que se han alcanzado todos los objetivos:
- ✓ Estructura de directorios creada correctamente
- ✓ Archivos manipulados (creados, copiados, movidos)
- ✓ Redireccionamiento de flujos implementado
- ✓ Eliminación de archivos y directorios completada
- ✓ Historial de comandos documentado

---
##imagenes y links
<img width="921" height="803" alt="image" src="https://github.com/user-attachments/assets/a7d78240-7f25-4d73-8878-1e670f9ebd7b" />
<img width="921" height="803" alt="image" src="https://github.com/user-attachments/assets/5929d8cc-759e-452b-b26b-e008abca16f1" />
https://youtube.com/shorts/h8wN_BC4ALA?si=ZdeaBtKDh_eI7CEC



## 10. Bibliografía

Aman, S., Love, R., y Venkatesan, S. (2012). *Linux System Administration*. Packt Publishing.

Free Software Foundation. (2021). *GNU Bash Manual*. Recuperado de https://www.gnu.org/software/bash/manual/

Kerrisk, M. (2010). *The Linux Programming Interface: A Linux and UNIX System Programming Handbook*. No Starch Press.

Negus, C. (2015). *Linux Bible* (9ª ed.). John Wiley & Sons, Inc.

Raymond, E. S. (2004). *The Art of Unix Programming*. Addison-Wesley.

The Linux Foundation. (2023). *Filesystem Hierarchy Standard*. Recuperado de https://refspecs.linuxfoundation.org/FHS_3.0/fhs-3.0.pdf

Upton, E., y Halfacree, G. (2016). *The Official Raspberry Pi Handbook*. Raspberry Pi Press.

Ward, B. (2014). *How Linux Works: What Every Superuser Should Know* (2ª ed.). No Starch Press.
