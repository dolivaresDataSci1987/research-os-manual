---
layout: default
title: Instalación y puesta en marcha
---

# 1. Instalación y puesta en marcha

[← Volver al índice](index.md)

RESEARCH OS puede utilizarse como demo pública o como aplicación local. Para trabajar con un proyecto real debes utilizar la **versión local**, porque es la que guarda la base de datos y los archivos en tu ordenador.

## 1.1. Antes de instalar

Recomendaciones generales:

- Instala RESEARCH OS en un ordenador personal o institucional sobre el que tengas control.
- Mantén suficiente espacio libre para tus documentos, informes, imágenes y resultados.
- Si vas a trabajar con datos sensibles, utiliza una cuenta de usuario protegida por contraseña y, cuando sea posible, cifrado de disco.
- No utilices la demo pública para información real.

La aplicación local incluye el runtime necesario para ejecutar la interfaz. El objetivo de la distribución desktop es que el usuario final no tenga que instalar Python ni ejecutar comandos.

---

## 1.2. Instalación en macOS

RESEARCH OS 0.10.1 dispone de dos compilaciones nativas:

- **Apple Silicon:** para Macs con chip Apple M1, M2, M3, M4 o posteriores compatibles.
- **Intel:** para Macs cuyo procesador sea Intel.

### Cómo saber qué Mac tienes

1. Abre el menú ** Apple**.
2. Selecciona **Acerca de este Mac**.
3. Busca el campo **Chip** o **Procesador**.
4. Si aparece `Apple M...`, utiliza Apple Silicon. Si aparece `Intel`, utiliza la versión Intel.

### Instalación desde el DMG

1. Descarga el archivo `.dmg` correspondiente a tu arquitectura.
2. Haz doble clic en el DMG para montarlo.
3. Se abrirá una ventana que contiene **RESEARCH OS.app** y un acceso a **Applications**.
4. Arrastra **RESEARCH OS.app** a **Applications**.
5. Cuando finalice la copia, abre **Aplicaciones** y ejecuta RESEARCH OS desde allí.
6. Si ya no necesitas el DMG montado, puedes expulsarlo desde Finder.

### Advertencia de seguridad de macOS en la versión actual

La compilación 0.10.1 está firmada de forma técnica para comprobar la integridad del paquete, pero todavía no está notarizada comercialmente por Apple. Por ello, macOS puede advertir que no puede verificar al desarrollador.

Si confías en el instalador recibido y macOS bloquea el primer arranque:

1. Abre **Finder → Aplicaciones**.
2. Haz clic secundario sobre **RESEARCH OS**.
3. Elige **Abrir**.
4. Confirma **Abrir** en el diálogo de macOS.

Según la versión de macOS, también puede ser necesario autorizar la aplicación desde **Ajustes del Sistema → Privacidad y seguridad**.

> Esta advertencia corresponde al estado de distribución de la versión 0.10.1. Una futura distribución comercial notarizada podrá eliminar esta fricción.

---

## 1.3. Uso en Windows

En la versión 0.10.1, Windows se distribuye como un **paquete portable**. Eso significa que no existe todavía un instalador tradicional con asistente `Setup.exe`; la aplicación funciona desde la carpeta descargada.

### Puesta en marcha

1. Descarga el paquete de Windows.
2. Descomprime el ZIP completo en una carpeta estable, por ejemplo `Documentos\RESEARCH OS`.
3. **No ejecutes RESEARCH OS directamente desde dentro del ZIP.** Descomprime primero todo su contenido.
4. Mantén juntos los archivos y subcarpetas incluidos en el paquete.
5. Haz doble clic en **RESEARCH OS.exe**.
6. Espera mientras se inicia el servidor local.
7. Tu navegador se abrirá automáticamente con la interfaz.

Windows puede mostrar una advertencia de editor desconocido en una compilación no firmada comercialmente. Antes de continuar, verifica siempre que el archivo procede del canal oficial desde el que recibiste RESEARCH OS.

### No muevas únicamente el `.exe`

El ejecutable forma parte de un paquete que contiene dependencias y recursos. Si recibes una distribución portable, mueve o copia **la carpeta completa**, no solamente el archivo `RESEARCH OS.exe`.

---

## 1.4. Qué ocurre cuando abres RESEARCH OS

La aplicación desktop realiza automáticamente el siguiente proceso:

1. Comprueba o crea la carpeta local de datos.
2. Fuerza el modo de ejecución `local`.
3. Busca un puerto local disponible, preferentemente el `8501`.
4. Inicia Streamlit únicamente en `127.0.0.1`, es decir, en tu propio ordenador.
5. Espera hasta que el servidor local responde correctamente.
6. Abre automáticamente la interfaz en tu navegador.
7. Mantiene una pequeña ventana de control mientras RESEARCH OS está en ejecución.

La URL suele verse como:

```text
http://127.0.0.1:8501
```

Si el puerto 8501 ya está ocupado, RESEARCH OS puede elegir otro puerto. Eso es normal.

`127.0.0.1` significa **este mismo ordenador**. No es una dirección pública de Internet.

---

## 1.5. Ventana de control de la aplicación local

La distribución desktop muestra una ventana pequeña con tres acciones principales:

### Abrir RESEARCH OS

Vuelve a abrir la interfaz en el navegador si cerraste la pestaña accidentalmente.

### Abrir carpeta de datos

Abre directamente la ubicación en la que RESEARCH OS está guardando la información local.

### Cerrar RESEARCH OS

Detiene correctamente el servidor local y cierra el controlador.

> **Recomendación:** cuando termines de trabajar, utiliza **Cerrar RESEARCH OS**. Cerrar únicamente la pestaña del navegador no equivale necesariamente a detener la aplicación local.

---

## 1.6. Dónde se guardan los datos

En la distribución desktop actual, la ubicación por defecto es:

### Windows

```text
C:\Users\TU_USUARIO\Documents\RESEARCH_OS_DATA\
```

### macOS

```text
/Users/TU_USUARIO/Documents/RESEARCH_OS_DATA/
```

La estructura general es:

```text
RESEARCH_OS_DATA/
├── database/
│   └── research_os.sqlite3
├── projects/
├── imports/
├── exports/
├── backups/
├── trash/
└── logs/
```

### `database/research_os.sqlite3`

Es la base de datos estructurada. Contiene, entre otros, proyectos, participantes, visitas, registros clínicos, muestras, experimentos, agenda y movimientos financieros.

### `projects/`

Contiene el espacio de archivos de cada proyecto. RESEARCH OS crea internamente un directorio para cada proyecto y subcarpetas como:

```text
projects/<ID_INTERNO_DEL_PROYECTO>/
├── clinical/
├── documents/
├── results/
├── attachments/
├── imports/
└── exports/
```

Los nombres internos pueden utilizar identificadores técnicos diferentes del nombre visible del proyecto. **No renombres estas carpetas manualmente.**

### `imports/` y `exports/`

Carpetas reservadas para flujos de importación/exportación local.

### `backups/`

Carpeta preparada para copias de seguridad. En la versión 0.10.1 todavía no existe un sistema completo de backup/restauración desde la interfaz.

### `trash/`

Cuando se elimina un proyecto, su workspace local puede moverse aquí para preservar los archivos fuera del espacio activo.

### `logs/`

Espacio reservado para registros técnicos de ejecución.

---

## 1.7. ¿Puedo cambiar manualmente los archivos de `RESEARCH_OS_DATA`?

En condiciones normales, **no es necesario** y no se recomienda.

Puedes abrir la carpeta para realizar una copia de seguridad completa, pero evita:

- renombrar carpetas internas de proyectos;
- mover archivos almacenados por RESEARCH OS;
- borrar directamente `research_os.sqlite3`;
- editar la base de datos con programas externos;
- copiar solo una parte de la carpeta pensando que es una copia de seguridad completa.

Un documento puede estar registrado en SQLite y almacenado físicamente en el workspace del proyecto. Si mueves únicamente el archivo, la referencia interna puede quedar rota.

---

## 1.8. Primera apertura

En el primer arranque de una instalación local vacía, la aplicación inicializa la base de datos y crea las estructuras necesarias. Después podrás crear tu primer proyecto desde **Proyectos → + Nuevo proyecto**.

Si recibes una distribución que incluye datos de demostración, utiliza esos datos únicamente para aprender el funcionamiento y crea un proyecto separado para tu trabajo real.

---

## 1.9. Cómo cerrar RESEARCH OS correctamente

Al terminar:

1. Guarda cualquier formulario que tengas pendiente.
2. Evita cerrar la aplicación mientras se está subiendo o exportando un archivo.
3. Puedes cerrar la pestaña del navegador.
4. En la ventana de control, pulsa **Cerrar RESEARCH OS**.
5. Espera a que desaparezca la ventana.

Si vas a hacer una copia de seguridad manual, hazla **después de cerrar completamente la aplicación**.

---

## 1.10. Demo pública: qué puedes y qué no puedes hacer

La demo pública tiene una advertencia en la barra lateral indicando **demo pública** y almacenamiento temporal.

Puedes utilizarla para:

- explorar las pantallas;
- abrir COLONOMICS;
- comprender la estructura de participantes, muestras, estudios y experimentos;
- probar filtros y navegación;
- enseñar el funcionamiento del programa con datos sintéticos.

No debes utilizarla para:

- datos reales de pacientes o participantes;
- consentimientos reales;
- historias clínicas;
- PDFs confidenciales;
- documentos de comité de ética con información sensible;
- presupuestos, contratos o facturas reales;
- archivos científicos todavía confidenciales.

---

## 1.11. Comprobación rápida después de instalar

Antes de empezar un proyecto real, verifica que:

- puedes abrir Inicio y Proyectos;
- puedes crear un proyecto de prueba;
- puedes cerrarlo y volver a abrir RESEARCH OS;
- el proyecto sigue apareciendo después de reiniciar;
- la ventana **Abrir carpeta de datos** te lleva a `RESEARCH_OS_DATA`;
- puedes subir y descargar un archivo de prueba no sensible;
- conoces cómo realizar una copia completa de `RESEARCH_OS_DATA`.

Después de esta comprobación puedes eliminar el proyecto de prueba y comenzar tu proyecto real.

---

**Siguiente capítulo:** [Primeros pasos y flujo recomendado →](primeros-pasos.md)
