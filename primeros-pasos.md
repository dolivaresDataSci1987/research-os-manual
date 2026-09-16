---
layout: default
title: Primeros pasos y flujo recomendado
---

# 2. Primeros pasos y flujo recomendado

[← Volver al índice](index.md)

Este capítulo explica cómo organizar un proyecto desde cero sin necesidad de utilizar todas las funciones de RESEARCH OS desde el primer día.

## 2.1. La idea fundamental: empieza por el proyecto

Casi toda la información de RESEARCH OS tiene contexto de proyecto. Por ello, el punto de partida habitual es:

**Proyectos → + Nuevo proyecto**

Antes de crear registros, conviene decidir al menos:

- nombre del estudio o trabajo;
- acrónimo, si lo tiene;
- investigador/a principal o responsable;
- institución;
- estado inicial;
- fechas previstas;
- si incluirás participantes humanos;
- si manejarás muestras biológicas;
- si registrarás experimentos;
- qué documentación quieres centralizar.

No necesitas tener el protocolo completamente cerrado. Puedes crear el proyecto en estado **Idea** o **Planificado** y completarlo progresivamente.

---

## 2.2. Tres formas habituales de utilizar RESEARCH OS

### A. Trabajo de grado, TFG o proyecto pequeño

Puedes trabajar principalmente con:

```text
Proyecto
├── Equipo
├── Agenda
├── Documentación
├── Informes
└── Exportaciones
```

Si no existen participantes, muestras o experimentos, simplemente no utilices esos módulos.

### B. Maestría, tesis o estudio observacional con participantes

Un flujo razonable es:

```text
Proyecto
├── Participantes
│   ├── Visitas
│   ├── Información clínica
│   └── Estudios Dx y Complementarios
├── Agenda
├── Documentación
├── Finanzas
└── Informes / exportaciones
```

### C. Proyecto biomédico con muestras y laboratorio

Puedes aprovechar la trazabilidad completa:

```text
Proyecto
└── Participante
    └── Visita
        └── Muestra
            └── Alícuota
                └── Experimento
                    └── Resultado experimental
```

RESEARCH OS también permite experimentos vinculados directamente a participantes o resultados agregados cuando no existe una muestra específica.

---

## 2.3. Paso 1 — Crear el proyecto

Ve a **Proyectos** y pulsa **+ Nuevo proyecto**.

Completa como mínimo el **Nombre del proyecto**. El resto puede editarse posteriormente.

Estados disponibles:

| Estado | Uso recomendado |
|---|---|
| Idea | Proyecto todavía conceptual |
| Planificado | Diseño definido pero aún no iniciado |
| En marcha | Trabajo activo |
| Pausado | Interrumpido temporalmente |
| Finalizado | Trabajo concluido |
| Archivado | Fuera del portfolio activo |

El campo **Progreso del proyecto** va de 0 a 100 %. Es un indicador manual; RESEARCH OS no calcula automáticamente el porcentaje en función de tareas o participantes.

También puedes registrar:

- investigador/a principal;
- institución;
- inicio previsto;
- inicio real;
- fin previsto;
- fin real.

Después de crear el proyecto, RESEARCH OS abre su ficha.

---

## 2.4. Paso 2 — Completar el equipo

Ve a:

**Proyecto → Información del proyecto → Equipo**

Añade las personas que participarán en el trabajo. Esto es especialmente útil porque posteriormente pueden aparecer como responsables en la agenda.

Para un proyecto académico pequeño podría ser suficiente registrar:

- estudiante/investigador;
- tutor o director;
- co-tutor;
- colaborador metodológico;
- bioestadístico;
- personal de laboratorio, si procede.

No es necesario añadir personas que no tengan ninguna función operativa relevante.

---

## 2.5. Paso 3 — Definir una estrategia de códigos

Antes de crear participantes o muestras, decide cómo los identificarás.

Ejemplos de participantes:

```text
P001
P002
P003
```

O con prefijo de estudio:

```text
CRC-001
CRC-002
CRC-003
```

Ejemplos de visitas:

```text
V0
V1
V2
```

Ejemplos de categorías de muestras:

```text
Plasma
Suero
ADN
Tejido
```

RESEARCH OS puede generar automáticamente códigos para muestras, alícuotas, estudios Dx, experimentos y resultados cuando sus formularios permiten dejar el código vacío. Para participantes y visitas, define tú el código.

> **Consejo:** no codifiques información sensible dentro del identificador. `P001` es preferible a un código que contenga nombre, documento o fecha de nacimiento.

---

## 2.6. Paso 4 — Crear participantes, si existen

Ve a:

**Proyecto → Participantes → + Nuevo participante**

Para cada participante, el único dato estrictamente necesario en el formulario es el **Código del participante**. Sin embargo, para una buena trazabilidad suele ser conveniente registrar también:

- estado;
- modo de identificación;
- estado de consentimiento;
- sexo, si es una variable pertinente para el estudio;
- año de nacimiento, si corresponde;
- fecha de inclusión;
- notas relevantes no sensibles.

Los nombres y apellidos son opcionales. RESEARCH OS está diseñado para priorizar códigos pseudonimizados.

---

## 2.7. Paso 5 — Registrar visitas

Abre la fila del participante y entra en **Visitas**.

Crea una visita cuando necesites organizar datos longitudinales por momentos del estudio, por ejemplo:

- cribado;
- basal;
- seguimiento a 3 meses;
- seguimiento a 6 meses;
- visita final;
- visita no programada.

Una visita puede contener fecha prevista y fecha real. También puedes definir una ventana temporal.

Si tu proyecto es transversal y tiene una única recogida, una sola visita basal puede ser suficiente.

---

## 2.8. Paso 6 — Registrar información clínica estructurada

Dentro del participante abre **Información clínica**.

Cada registro representa una variable y su valor. Ejemplos:

| Variable | Valor | Unidad | Categoría |
|---|---:|---|---|
| Edad | 46 | años | Demografía |
| IMC | 27.8 | kg/m² | General |
| Diagnóstico | CRC | — | Diagnóstico |
| Hemoglobina | 12.4 | g/dL | Laboratorio |

Puedes asociar el registro a una visita y documentar su fuente.

No utilices el campo de notas como sustituto de datos estructurados cuando posteriormente necesites analizar la información. Si una variable es importante para tu análisis, regístrala de forma consistente.

---

## 2.9. Paso 7 — Preparar el biobanco, si utilizas muestras

Si no trabajas con muestras biológicas, puedes omitir este paso completamente.

Si sí las utilizas, antes de registrar muchas muestras es útil crear la jerarquía física en:

**Biobanco → Localizaciones**

Por ejemplo:

```text
Centro: Universidad X
└── Laboratorio: Laboratorio de Investigación
    └── Congelador: Freezer -80 °C
        └── Estante: E1
            └── Rack: R1
                └── Caja: C1
                    └── Posición: A01
```

Después registra las muestras desde el proyecto o desde Biobanco.

---

## 2.10. Paso 8 — Estudios diagnósticos y complementarios

Utiliza este módulo para pruebas clínicas o diagnósticas relacionadas con un participante, por ejemplo:

- hemograma;
- bioquímica;
- TC/TAC;
- resonancia;
- endoscopia;
- anatomía patológica;
- estudio genético.

Puedes registrar hallazgos y conclusión y adjuntar un PDF o Word del informe.

Esto permite mantener juntos el registro estructurado y el documento de origen.

---

## 2.11. Paso 9 — Experimentos y resultados

Si realizas actividad experimental:

1. Crea el experimento.
2. Define tipo, estado, responsable, plataforma y protocolo.
3. Asocia participantes de forma directa si corresponde.
4. Asocia las muestras o alícuotas utilizadas.
5. Registra cantidad consumida como dato de trazabilidad.
6. Crea uno o varios resultados.
7. Asocia cada resultado al participante y/o material específico cuando sea necesario.
8. Añade archivos de resultados o referencias externas.

Este orden ayuda a que la información tenga contexto científico completo.

---

## 2.12. Paso 10 — Planificar el trabajo

En **Agenda y Cronograma** crea:

- tareas;
- eventos;
- deadlines;
- hitos.

Para cada tarea puedes registrar:

- responsable;
- prioridad;
- progreso;
- horas estimadas;
- dependencias;
- bloques de tiempo planificados;
- tiempo real invertido.

Una forma sencilla de trabajar es revisar la Agenda una vez por semana y actualizar progreso, fechas y horas.

---

## 2.13. Paso 11 — Centralizar documentación

En **Documentación y Finanzas → Documentación**, guarda archivos como:

- protocolo;
- aprobación del comité de ética;
- consentimiento informado;
- plan de análisis;
- presentaciones;
- afiches/posters;
- manuscritos;
- presupuestos;
- facturas;
- correspondencia relevante.

Utiliza categorías y descripciones para encontrarlos posteriormente.

---

## 2.14. Paso 12 — Finanzas, si las necesitas

Para proyectos pequeños sin presupuesto formal puedes omitir el módulo.

Si quieres llevar control económico, el orden recomendado es:

1. Crear una **Fuente de financiación**.
2. Crear las **Partidas presupuestarias**.
3. Registrar **Ingresos**, **Gastos** y **Compromisos**.
4. Asociar justificantes cuando existan.
5. Registrar periódicamente un **corte de saldo real**.

Así podrás comparar presupuesto, movimientos y dinero realmente disponible.

---

## 2.15. Paso 13 — Generar informes y exportar datos

Cuando necesites una entrega:

**Proyecto → Informes**

Puedes crear un informe, elegir sus secciones, añadir narrativa/conclusiones/próximos pasos y descargarlo como:

- PDF;
- DOCX.

También puedes congelar versiones.

Para análisis externo puedes exportar datasets a:

- CSV;
- Excel/XLSX.

Entre los conjuntos exportables se encuentran participantes, visitas, muestras, estudios Dx, experimentos, resultados, finanzas y agenda.

---

## 2.16. Rutina semanal recomendada

Para un estudiante de maestría o doctorado, una rutina simple puede ser:

**Al inicio de la semana**

- revisar deadlines;
- actualizar las tareas;
- reservar bloques de trabajo;
- comprobar documentación pendiente.

**Después de cada sesión de recogida o laboratorio**

- registrar visitas;
- añadir datos clínicos;
- registrar nuevas muestras;
- actualizar estados y cantidades cuando sea necesario;
- registrar experimentos o resultados.

**Al final de la semana**

- registrar horas reales;
- actualizar progreso del proyecto;
- subir documentación nueva;
- revisar que no haya archivos dispersos fuera del sistema;
- cerrar RESEARCH OS y realizar una copia de seguridad periódica.

---

## 2.17. Qué información registrar y cuál no

Un principio útil es: **registra lo que necesites para gestionar, documentar, auditar o analizar tu investigación**.

No conviertas RESEARCH OS en un almacén indiscriminado de información personal. Especialmente con participantes humanos:

- minimiza identificadores directos;
- usa códigos;
- registra solo las variables pertinentes;
- sigue el protocolo aprobado y las políticas de tu institución.

---

## 2.18. Qué hacer si tu proyecto ya está avanzado

No necesitas reconstruir todo el pasado de inmediato.

Puedes migrar progresivamente:

1. Crear el proyecto con su estado actual.
2. Añadir participantes activos o relevantes.
3. Cargar documentación esencial.
4. Introducir agenda futura.
5. Registrar muestras existentes si necesitas control de inventario.
6. Añadir resultados o estudios conforme los vayas utilizando.

Después, si aporta valor, completa datos históricos.

---

## 2.19. Ejemplo mínimo para una tesis clínica

Imagina una tesis con 30 participantes y dos momentos de evaluación.

Una estructura simple sería:

```text
Proyecto: Tesis de Maestría 2026
│
├── Equipo
│   ├── Estudiante
│   └── Tutor
│
├── 30 participantes pseudonimizados
│   ├── V0 · Basal
│   └── V1 · Seguimiento
│
├── Información clínica
│   ├── variables basales
│   └── variables de seguimiento
│
├── Agenda
│   ├── reclutamiento
│   ├── limpieza de datos
│   ├── análisis
│   └── entrega de tesis
│
├── Documentación
│   ├── protocolo
│   ├── ética
│   └── plan de análisis
│
└── Informes / Exportaciones
    └── Excel para análisis estadístico
```

No necesitas utilizar biobanco ni experimentos si no forman parte de la investigación.

---

**Siguiente capítulo:** [Proyectos, equipo y participantes →](proyectos-participantes.md)
