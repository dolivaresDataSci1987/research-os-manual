---
layout: default
title: Datos, privacidad, copias de seguridad y trazabilidad
---

# 9. Datos, privacidad, copias de seguridad y trazabilidad

[← Volver al índice](index.md)

RESEARCH OS está diseñado con una arquitectura **local-first**: en la distribución desktop, la base de datos y los archivos del proyecto se guardan en el ordenador del usuario. Esta arquitectura reduce la dependencia de una nube central, pero también hace que la protección y las copias de seguridad del equipo local sean importantes.

> Este capítulo describe buenas prácticas de uso. RESEARCH OS no sustituye las políticas de seguridad, protección de datos, comité de ética o gobierno de datos de tu institución.

---

## 9.1. Demo pública frente a datos reales

### Demo pública

- utiliza datos sintéticos/ficticios;
- puede reiniciarse;
- el almacenamiento es temporal;
- sirve para aprendizaje y demostración.

**No introduzcas información real sensible en la demo pública.**

### Versión local

- se ejecuta en tu propio ordenador;
- la interfaz se abre en el navegador mediante `127.0.0.1`;
- utiliza una base SQLite local;
- almacena documentos y adjuntos en el filesystem local del proyecto.

Para investigación real, utiliza la distribución local y aplica las medidas de seguridad exigidas por tu institución.

---

# 9.2. Carpeta `RESEARCH_OS_DATA`

La distribución desktop utiliza por defecto:

```text
Documents/RESEARCH_OS_DATA/
```

Estructura principal:

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

### Dos componentes deben mantenerse juntos

**Base de datos SQLite**  
Contiene la información estructurada y relaciones.

**Archivos de proyectos**  
Contienen documentos y adjuntos copiados al workspace.

Por eso una copia de seguridad completa debe incluir **toda la carpeta `RESEARCH_OS_DATA`**, no solo el archivo SQLite.

---

# 9.3. Qué significa local-first

Local-first significa que la instalación desktop prioriza el almacenamiento local como fuente de verdad.

No significa automáticamente que:

- el ordenador esté cifrado;
- exista una copia de seguridad externa;
- cualquier dato sea legalmente apropiado para almacenar;
- el usuario pueda ignorar su protocolo o normativa;
- la aplicación sustituya controles institucionales.

La seguridad final depende también del equipo, sistema operativo, cuentas de usuario, copias, permisos y prácticas del investigador.

---

# 9.4. Pseudonimización y minimización de datos

El formulario de participante ofrece:

- Pseudonimizado
- Anonimizado
- Identificable

RESEARCH OS prioriza códigos pseudonimizados y hace opcionales nombre y apellidos.

### Práctica recomendada

En lugar de:

```text
Nombre: Juan Pérez
Documento: 1234567
```

utiliza, cuando el protocolo lo permita:

```text
Código: P017
Modo: Pseudonimizado
```

Si necesitas una tabla que relacione `P017` con una identidad real, considera mantener esa clave separada y protegida según el plan de gestión de datos de tu estudio.

### Minimización

No registres una variable personal simplemente porque existe un campo disponible. Pregúntate:

- ¿la necesito para el objetivo científico?
- ¿está contemplada en el protocolo?
- ¿estoy autorizado a almacenarla?
- ¿podría utilizar una versión menos identificable?

---

# 9.5. Protección del ordenador

Para proyectos reales con información sensible, considera como mínimo:

- contraseña robusta de inicio de sesión;
- bloqueo automático de pantalla;
- cifrado del disco cuando esté disponible;
- actualizaciones del sistema operativo;
- antivirus/seguridad apropiada a tu entorno;
- no compartir la cuenta del sistema operativo;
- no dejar el equipo desatendido desbloqueado;
- evitar copiar datos sensibles a dispositivos no controlados.

En macOS, FileVault puede proporcionar cifrado del disco. En Windows, la disponibilidad de BitLocker u otras opciones depende de la edición y configuración del sistema. Sigue siempre la política de tu institución.

---

# 9.6. Copia de seguridad manual completa

La versión 0.10.1 crea una carpeta `backups`, pero todavía no incluye un flujo completo de backup/restauración desde la interfaz.

La forma más segura de hacer una copia manual es copiar **todo `RESEARCH_OS_DATA` con RESEARCH OS cerrado**.

### Procedimiento recomendado

1. Termina de guardar formularios o archivos.
2. Cierra la pestaña de RESEARCH OS si quieres.
3. En la ventana de control, pulsa **Cerrar RESEARCH OS**.
4. Comprueba que la aplicación se ha detenido.
5. Localiza `Documents/RESEARCH_OS_DATA`.
6. Copia la carpeta completa.
7. Renombra la copia con fecha y hora.
8. Guarda la copia en un destino seguro.

Ejemplo:

```text
RESEARCH_OS_BACKUP_2026-09-30/
RESEARCH_OS_BACKUP_2026-10-31/
```

### Por qué cerrar antes

Copiar una base SQLite mientras está siendo modificada puede producir una copia inconsistente. Cerrar RESEARCH OS reduce ese riesgo y también asegura que los archivos adjuntos estén completamente escritos.

---

## 9.7. Dónde guardar las copias

Depende de las normas de tu institución y de la sensibilidad de los datos.

Posibles destinos:

- disco externo cifrado;
- servidor institucional;
- NAS institucional;
- almacenamiento corporativo autorizado;
- servicio cloud aprobado por tu organización.

No asumas que cualquier nube personal es adecuada para datos de investigación sensibles.

---

## 9.8. Regla 3-2-1 como referencia

Para información importante puede ser útil aplicar una estrategia similar a:

- 3 copias de los datos;
- 2 soportes distintos;
- 1 copia fuera del equipo principal.

Adáptala a las exigencias de tu institución y presupuesto.

---

# 9.9. Restauración manual

La versión actual no tiene un botón de restauración. Si necesitas recuperar una copia:

1. Cierra RESEARCH OS completamente.
2. Conserva la carpeta actual por si fuera necesaria para diagnóstico.
3. Identifica una copia completa y conocida como válida.
4. Restaura la carpeta completa `RESEARCH_OS_DATA` de manera coherente.
5. Abre RESEARCH OS.
6. Comprueba proyectos, participantes y archivos importantes.

Evita mezclar manualmente una base SQLite de una fecha con carpetas `projects/` de otra fecha salvo que sepas exactamente qué relaciones estás reconstruyendo.

---

# 9.10. No uses simultáneamente la misma carpeta desde varios ordenadores

SQLite y el diseño actual están pensados principalmente para un uso local individual.

No recomendamos colocar `RESEARCH_OS_DATA` en una carpeta sincronizada y abrir simultáneamente la misma base de datos desde dos ordenadores.

Riesgos:

- conflictos de sincronización;
- copias duplicadas de SQLite;
- pérdida de cambios;
- corrupción de datos;
- rutas externas inconsistentes.

Para la versión documentada, trata cada workspace local como una única fuente de verdad activa.

---

# 9.11. Archivos externos en resultados

Los resultados experimentales permiten registrar una **Ruta externa**.

Ejemplo:

```text
D:\Sequencing\Run_2026_10\sample_01.fastq.gz
```

Esto no copia el archivo. Solo guarda la referencia.

Por tanto:

- la ruta puede romperse si mueves el archivo;
- otro ordenador puede no tener la misma ruta;
- una copia de `RESEARCH_OS_DATA` no incluye automáticamente el archivo externo.

Si un archivo externo es crítico, documenta también dónde y cómo se respalda.

---

# 9.12. Trazabilidad científica

Una fortaleza del modelo de RESEARCH OS es conectar entidades.

Cadena ideal:

```text
Proyecto
→ Participante
→ Visita
→ Muestra / Alícuota
→ Experimento
→ Resultado
```

Un resultado puede así responder:

- ¿de qué experimento procede?
- ¿qué material se utilizó?
- ¿de qué muestra madre procede la alícuota?
- ¿a qué participante pertenece?
- ¿en qué visita se obtuvo?
- ¿a qué proyecto pertenece?

No todos los proyectos necesitan toda la cadena, pero registrar contexto mejora la reproducibilidad y revisión posterior.

---

## 9.13. Trazabilidad documental

Además de datos científicos, RESEARCH OS permite relacionar:

```text
Movimiento financiero → Factura / justificante
Publicación → Documento del manuscrito
Estudio Dx → Informe PDF/Word
Resultado → Archivo / referencia externa
```

Utiliza estas relaciones cuando aporten contexto y eviten búsquedas manuales en carpetas separadas.

---

# 9.14. Eliminación frente a conservación histórica

Antes de borrar un registro, pregúntate si realmente debe desaparecer.

Alternativas:

- Proyecto: **Archivar** en lugar de eliminar.
- Participante: cambiar a **Retirado** o **Completado**.
- Tarea: cambiar a **Cancelada**.
- Miembro: marcarlo como **inactivo**.
- Estudio/experimento: utilizar estados de cancelación o fallo cuando representen mejor lo ocurrido.

Eliminar es apropiado para errores reales, pruebas o información que deba retirarse según tu política. Para historia científica, un cambio de estado suele conservar más contexto.

---

# 9.15. Qué ocurre con algunas eliminaciones

### Participante

Si tiene muestras, la interfaz informa de que las muestras se conservarán y quedarán desvinculadas.

### Visita

Los datos clínicos asociados se conservan sin la relación a la visita.

### Estudio Dx

Eliminarlo elimina también sus informes almacenados dentro de RESEARCH OS.

### Experimento

Eliminarlo elimina resultados y archivos asociados, pero conserva el material biológico.

### Resultado

Eliminarlo elimina también sus archivos locales asociados.

### Proyecto

Puede estar bloqueado si tiene muestras de origen. La carpeta del proyecto puede moverse a `trash` durante la eliminación.

---

# 9.16. Datos identificables

RESEARCH OS permite registrar nombre y apellidos opcionalmente, pero la posibilidad técnica no implica que debas hacerlo.

Antes de utilizar datos identificables:

- revisa el protocolo;
- revisa el consentimiento;
- revisa la base jurídica y políticas aplicables;
- revisa las normas de tu institución;
- limita el acceso físico y lógico al equipo.

Para la mayoría de análisis y gestión de una tesis, un código pseudonimizado suele ser suficiente.

---

# 9.17. Exportaciones y privacidad

Cuando descargas un CSV o Excel, ese archivo sale del entorno controlado de RESEARCH OS y pasa a ser un archivo independiente.

Por tanto:

- evita enviarlo por canales no autorizados;
- protege el archivo si contiene datos sensibles;
- controla dónde se guarda;
- elimina copias innecesarias;
- utiliza datasets pseudonimizados cuando sea posible.

Lo mismo aplica a PDF, DOCX y documentos descargados.

---

# 9.18. RESEARCH OS no es una historia clínica asistencial

RESEARCH OS está pensado para gestión de investigación. No debe considerarse un sistema de historia clínica, prescripción, monitorización asistencial o decisión diagnóstica.

Los campos de información clínica y estudios Dx sirven para documentar datos de investigación, no para sustituir los sistemas clínicos oficiales.

---

# 9.19. Checklist antes de usar datos reales

Antes de empezar un estudio real, verifica:

- que estás usando la versión local;
- que el ordenador está protegido;
- que conoces dónde se guarda `RESEARCH_OS_DATA`;
- que tienes un plan de backup;
- que has definido códigos pseudonimizados;
- que sabes qué datos estás autorizado a registrar;
- que tienes claro quién puede acceder al ordenador;
- que tus exportaciones también serán protegidas;
- que no utilizarás la demo pública para información real.

---

# 9.20. Checklist mensual de mantenimiento

Una vez al mes, como mínimo en proyectos activos:

1. Cierra correctamente RESEARCH OS.
2. Haz una copia completa de `RESEARCH_OS_DATA`.
3. Comprueba que puedes abrir la copia o que el soporte existe y es accesible.
4. Revisa documentos esenciales.
5. Revisa participantes retirados/completados.
6. Revisa muestras sin ubicación.
7. Revisa tareas vencidas.
8. Revisa resultados pendientes de validación.
9. Revisa estudios pendientes de informe.
10. Documenta cualquier incidencia importante.

---

**Siguiente capítulo:** [Preguntas frecuentes y solución de problemas →](faq.md)
