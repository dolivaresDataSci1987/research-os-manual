---
layout: default
title: Manual de usuario
---

# RESEARCH OS — Manual de usuario

**Versión documentada: 0.10.1**  
**Ámbito:** investigación en ciencias de la salud y biomedicina  
**Modalidad:** aplicación local-first para Windows y macOS, con una demo pública separada

RESEARCH OS es un entorno para organizar un proyecto de investigación desde una única interfaz: proyecto, equipo, participantes, visitas, información clínica, muestras, estudios diagnósticos y complementarios, experimentos, resultados, agenda, documentación, finanzas, informes, publicaciones y exportaciones.

Este manual está escrito para usuarios finales. No necesitas saber Python, Streamlit, SQL ni programación para utilizar RESEARCH OS.

> **Importante:** la demo pública de Streamlit contiene únicamente datos sintéticos y su almacenamiento es temporal. **No introduzcas datos reales de participantes, pacientes, historias clínicas ni documentación confidencial en la demo pública.** Los proyectos reales deben trabajarse en la versión local.

## Índice del manual

| Capítulo | Contenido |
|---|---|
| [1. Instalación y puesta en marcha](instalacion.md) | Windows, macOS, inicio, cierre y carpeta local de datos |
| [2. Primeros pasos y flujo recomendado](primeros-pasos.md) | Cómo empezar un proyecto desde cero y orden de trabajo recomendado |
| [3. Proyectos, equipo y participantes](proyectos-participantes.md) | Crear proyectos, equipo, participantes, visitas e información clínica |
| [4. Biobanco, muestras y alícuotas](biobanco.md) | Inventario, trazabilidad, localizaciones físicas, muestras y alícuotas |
| [5. Estudios, experimentos y resultados](estudios-experimentos.md) | Estudios Dx, experimentos, material biológico, resultados y archivos |
| [6. Agenda, tareas y gestión del tiempo](agenda.md) | Calendario, tareas, deadlines, hitos, bloques de trabajo y tiempo real |
| [7. Documentación y finanzas](documentacion-finanzas.md) | Archivos del proyecto, financiación, presupuesto, movimientos y saldos |
| [8. Informes, publicaciones y exportaciones](informes-exportaciones.md) | PDF, DOCX, versiones congeladas, outputs científicos, CSV y Excel |
| [9. Datos, privacidad, copias de seguridad y trazabilidad](datos-seguridad.md) | Dónde están los datos, pseudonimización, backups y buenas prácticas |
| [10. Preguntas frecuentes y solución de problemas](faq.md) | Problemas habituales, recuperación, funcionamiento local y límites actuales |
| [11. Glosario](glosario.md) | Conceptos esenciales utilizados por RESEARCH OS |

---

## 1. Cómo está organizado RESEARCH OS

La navegación principal contiene siete áreas:

**Inicio · Proyectos · Biobanco · Estudios Dx y Complementarios · Agenda · Documentación y Finanzas · Informes**

La idea central es que **el proyecto es la unidad de organización principal**. Los datos se relacionan entre sí para mantener trazabilidad:

```text
Proyecto
├── Equipo
├── Participantes
│   ├── Visitas
│   ├── Información clínica
│   ├── Estudios Dx y Complementarios
│   └── Muestras
│       └── Alícuotas
├── Experimentos
│   ├── Participantes
│   ├── Muestras / alícuotas utilizadas
│   └── Resultados experimentales
├── Agenda
├── Documentación
├── Finanzas
├── Informes
└── Publicaciones / outputs científicos
```

Las páginas globales no crean una copia independiente de los datos. Por ejemplo, una muestra que pertenece a un proyecto puede verse tanto dentro de ese proyecto como en **Biobanco**. Un estudio diagnóstico puede verse desde la ficha del participante, desde el proyecto y desde la página global **Estudios Dx y Complementarios**.

## 2. Demo pública y versión local

RESEARCH OS tiene dos contextos de uso distintos.

### Demo pública

La demo pública sirve para explorar la interfaz y entender el flujo de trabajo. Incluye el proyecto de demostración **COLONOMICS** y datos sintéticos o ficticios. El entorno puede reiniciarse y no debe utilizarse como repositorio de investigación real.

### Versión local

La versión local ejecuta la misma interfaz Streamlit en tu propio ordenador. El navegador se conecta a una dirección local, normalmente `http://127.0.0.1:8501`, y los datos se escriben en el propio equipo.

Por defecto, la distribución desktop utiliza:

```text
Documents/
└── RESEARCH_OS_DATA/
    ├── database/
    │   └── research_os.sqlite3
    ├── projects/
    ├── imports/
    ├── exports/
    ├── backups/
    ├── trash/
    └── logs/
```

No necesitas editar estas carpetas manualmente. RESEARCH OS las crea y administra desde la interfaz.

## 3. Inicio rápido: tu primer proyecto en 10 pasos

Si acabas de instalar RESEARCH OS, este es el recorrido más práctico:

1. Entra en **Proyectos** y pulsa **+ Nuevo proyecto**.
2. Completa el nombre, estado, investigador principal, institución, progreso y fechas disponibles.
3. Abre el proyecto y ve a **Información del proyecto → Equipo** para registrar a las personas que participarán.
4. En **Participantes**, crea los códigos de los sujetos. Siempre que sea posible utiliza códigos pseudonimizados.
5. Abre cada participante para registrar **Visitas** e **Información clínica**.
6. Si trabajas con material biológico, define primero las **Localizaciones** en **Biobanco** y después registra las muestras.
7. Añade los **Estudios Dx y Complementarios** que correspondan y adjunta sus informes cuando los tengas.
8. Crea los **Experimentos**, asocia participantes y muestras/alícuotas, y registra los resultados experimentales.
9. Utiliza **Agenda y Cronograma** para tareas, deadlines, reuniones, hitos y horas de trabajo.
10. Guarda documentación y movimientos financieros, y al final genera **Informes**, **Publicaciones** y **Exportaciones**.

No es obligatorio utilizar todos los módulos. Un trabajo de fin de máster pequeño puede utilizar únicamente proyecto, participantes, agenda, documentos e informes. Un proyecto de laboratorio puede añadir biobanco, experimentos y resultados.

## 4. La pantalla Inicio

**Inicio** funciona como panel de control. No es la pantalla principal de edición; su objetivo es ofrecer una visión rápida del estado del trabajo.

Encontrarás:

- **Visión general:** número de proyectos, participantes, muestras, estudios Dx y experimentos.
- **Portfolio de proyectos:** proyectos no archivados, su estado y porcentaje de progreso.
- **Distribución por estado:** gráfico del portfolio según el estado de cada proyecto.
- **Actividad científica:** documentos, resultados experimentales, visitas, información clínica y otras métricas.
- **Agenda y tiempo:** pendientes, elementos en curso, vencidos, próximos siete días y horas registradas.
- **Finanzas:** concedido, recibido, gastado y disponible.

Los números de Inicio se calculan a partir de los registros existentes. Para corregir una métrica, modifica el dato de origen en su módulo correspondiente.

## 5. Principios de uso recomendados

### Un código estable por participante

Utiliza un código que permanezca estable durante todo el estudio, por ejemplo `P001`, `CRC-001` o `Tesis-001`. Evita utilizar nombre, número de documento o teléfono como identificador principal.

### Una muestra física, un registro

No dupliques una misma muestra porque participe en dos proyectos. RESEARCH OS permite asociarla a proyectos adicionales manteniendo un único registro físico y un único proyecto de origen.

### Registra el origen antes que el resultado

Para conservar trazabilidad, el orden ideal es:

```text
Participante → Visita → Muestra → Experimento → Resultado
```

No todos los pasos son obligatorios, pero cuanto más completo sea el contexto, más útil será la trazabilidad.

### Diferencia documento de dato estructurado

Un PDF de laboratorio puede guardarse como archivo, pero si necesitas buscar, filtrar o analizar una variable concreta, registra también esa información como dato estructurado cuando corresponda.

### Congela versiones de los informes

Los informes pueden generarse con datos actuales, pero una **versión congelada** conserva una fotografía del proyecto en un momento concreto. Úsala antes de entregar un informe a un tutor, comité, financiador o colaborador.

## 6. Qué no hace RESEARCH OS automáticamente

Para evitar interpretaciones erróneas, ten presentes estos límites de la versión documentada:

- Registrar consumo de una muestra en un experimento **no descuenta automáticamente** la cantidad restante del biobanco. Actualiza el stock manualmente si necesitas reflejarlo.
- La carpeta `backups` existe, pero la versión 0.10.1 **no incluye todavía un botón de copia de seguridad/restauración dentro de la interfaz**.
- La demo pública no es un repositorio permanente.
- RESEARCH OS no sustituye las obligaciones de comité de ética, consentimiento, seguridad institucional, protección de datos ni buenas prácticas de investigación de tu institución.
- RESEARCH OS organiza investigación; no debe utilizarse como sistema de decisión clínica ni como sustituto de una historia clínica asistencial.

## 7. Convenciones de este manual

Cuando veas una ruta como:

**Proyectos → abrir proyecto → Participantes**

significa que debes entrar en **Proyectos**, seleccionar el proyecto deseado y después elegir la pestaña **Participantes**.

Cuando una tabla permite abrir un elemento, normalmente debes **hacer clic en una fila**. La ficha detallada aparecerá debajo o sustituirá temporalmente la tabla.

Las acciones de borrado suelen exigir marcar antes una casilla de confirmación. Esta protección es intencionada.

---

### ¿Por dónde sigo?

Si acabas de recibir RESEARCH OS, continúa con **[Instalación y puesta en marcha](instalacion.md)**.  
Si ya lo tienes abierto, ve directamente a **[Primeros pasos y flujo recomendado](primeros-pasos.md)**.
