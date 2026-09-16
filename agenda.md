---
layout: default
title: Agenda, tareas y gestión del tiempo
---

# 6. Agenda, tareas y gestión del tiempo

[← Volver al índice](index.md)

El módulo **Agenda** combina calendario, tareas, eventos, deadlines, hitos, planificación horaria y registro de tiempo real. Puede utilizarse dentro de un proyecto o desde la vista global.

## 6.1. Dos vistas de Agenda

### Agenda del proyecto

Ruta:

**Proyecto → Agenda y Cronograma**

Muestra únicamente los elementos del proyecto abierto.

### Agenda global

Ruta:

**Menú lateral → Agenda**

Permite revisar todos los proyectos o filtrar uno concreto.

---

## 6.2. Tipos de elemento

RESEARCH OS utiliza cuatro tipos:

| Tipo | Uso habitual |
|---|---|
| Tarea | Trabajo que debe ejecutarse y cuyo progreso puede medirse |
| Evento | Reunión, sesión, presentación, actividad con horario o lugar |
| Deadline | Fecha límite externa o interna |
| Hito | Punto importante del proyecto, como cierre de reclutamiento |

## 6.3. Estados

- Pendiente
- En curso
- Bloqueada
- Completada
- Cancelada

## 6.4. Prioridades

- Baja
- Media
- Alta
- Crítica

---

# 6.5. El calendario

El calendario puede visualizarse por:

- **Mes**
- **Semana**
- **Día**

La semana comienza en lunes y la vista horaria cubre aproximadamente de 06:00 a 22:00.

Puedes:

- navegar con **Hoy**, anterior y siguiente;
- hacer clic en una fecha;
- seleccionar un intervalo;
- hacer clic en un elemento existente;
- arrastrar elementos y bloques de trabajo para reprogramarlos.

> Cuando arrastras un elemento, RESEARCH OS actualiza su fecha. Revisa después la ficha si el cambio afecta a otros campos o dependencias.

---

## 6.6. Crear rápidamente desde el calendario

Haz clic en una fecha o selecciona un intervalo y abre **➕ Añadir al calendario**.

Si estás en la Agenda global, primero selecciona el proyecto.

Campos disponibles:

- Tipo
- Título \*
- Prioridad
- Responsable
- Fase
- Fecha / inicio
- Fin / fecha objetivo o Deadline
- Hora de inicio y fin para eventos y tareas
- Tiempo estimado para tareas
- Descripción / notas
- Lugar / enlace para eventos

Pulsa **Crear**.

### Creación rápida de una tarea con horario

Si al crear una tarea indicas hora de inicio y hora de fin, RESEARCH OS crea también un **bloque de trabajo planificado** en esa fecha.

Ejemplo:

```text
Tarea: Revisar base de datos
Fecha: 20/09/2026
Desde: 09:00
Hasta: 11:00
```

Resultado:

- una tarea con su deadline;
- un bloque de 2 horas reservado en calendario.

---

# 6.7. Crear y gestionar tareas

Debajo del calendario abre la pestaña **Tareas**.

Pulsa **+ Crear tarea**.

La ficha completa permite registrar:

- título;
- estado;
- prioridad;
- fase / paquete de trabajo;
- descripción;
- inicio planificado;
- fin / deadline;
- inicio real;
- fecha completada;
- responsable;
- progreso de 0 a 100 %;
- horas estimadas;
- hora de inicio y fin;
- lugar/enlace;
- dependencias;
- notas.

Aunque el formulario general muestra varios campos, utiliza solo los que tengan sentido para la tarea.

---

## 6.8. Responsable de una tarea

Los responsables se seleccionan entre los miembros registrados en:

**Proyecto → Información del proyecto → Equipo**

Si una persona no aparece, añádela primero al equipo.

---

## 6.9. Fase o paquete de trabajo

El campo **Fase / paquete de trabajo** es libre.

Ejemplos:

```text
Diseño
Reclutamiento
Laboratorio
Análisis estadístico
Redacción
WP1
WP2
```

Utilizar nombres consistentes facilita interpretar el calendario y las tablas.

---

## 6.10. Dependencias

Una tarea puede indicar que depende de otro elemento del proyecto.

Ejemplo:

```text
Cerrar base de datos
    ↓
Realizar análisis final
    ↓
Redactar resultados
```

En el formulario selecciona los elementos en **Depende de**.

Las dependencias sirven para documentar el orden lógico. La versión actual no pretende sustituir un motor avanzado de planificación de proyectos.

---

# 6.11. Ficha de una tarea

Selecciona una tarea en la tabla o haz clic en ella desde el calendario.

La cabecera muestra:

- estado;
- horas estimadas;
- horas planificadas;
- horas registradas;
- progreso;
- responsable;
- fase;
- deadline;
- prioridad;
- dependencias.

Para las tareas aparecen pestañas de:

1. **Resumen**
2. **Planificación**
3. **Tiempo real**
4. **Gestión**

---

# 6.12. Planificar bloques de trabajo

Un bloque representa tiempo que has reservado para trabajar en una tarea.

Desde la ficha de tarea:

**Planificación → + Planificar tiempo**

O desde:

**Agenda → Gestión del tiempo → Planificar tiempo**

Campos:

- tarea;
- persona;
- fecha;
- desde;
- hasta;
- notas.

Las horas se calculan a partir del intervalo.

Ejemplo:

```text
Tarea: Análisis descriptivo
Fecha: 22/09/2026
Desde: 14:00
Hasta: 16:30
Planificado: 2.5 h
```

La hora final debe ser posterior a la inicial y el formato esperado es `HH:MM`.

El bloque aparece en el calendario y puede arrastrarse para reprogramarlo.

---

## 6.13. Registrar tiempo real

Planificar no es lo mismo que registrar lo que realmente hiciste.

Abre:

**Tarea → Tiempo real → + Registrar trabajo realizado**

o:

**Agenda → Gestión del tiempo → Registrar tiempo real**

Campos:

- elemento;
- persona;
- fecha;
- horas reales;
- notas del trabajo realizado.

Las horas pueden introducirse en incrementos de 0,25 h.

Ejemplo:

```text
Fecha: 22/09/2026
Horas reales: 3.25
Notas: Limpieza final y análisis descriptivo
```

---

## 6.14. Estimado, planificado y registrado

RESEARCH OS diferencia tres conceptos:

### Estimado

Cuánto crees que debería requerir la tarea en total.

### Planificado

Cuántas horas has reservado en bloques de calendario.

### Registrado

Cuántas horas reales has declarado después de trabajar.

Ejemplo:

```text
Estimado: 8 h
Planificado: 6 h
Registrado: 7.5 h
```

Esto permite detectar tareas subestimadas o trabajo todavía sin planificar.

---

## 6.15. Resumen semanal

En **Gestión del tiempo** aparece la semana actual con:

- horas planificadas;
- horas registradas;
- pendiente planificado;
- tareas vencidas.

Si existen registros por persona, también se muestra la carga por miembro del equipo.

Esto puede utilizarse para una revisión semanal de tesis o de proyecto.

---

# 6.16. Eventos

Utiliza **Evento** para:

- reuniones con tutor;
- reuniones de equipo;
- presentaciones;
- sesiones de laboratorio;
- congresos;
- entrevistas;
- sesiones de recogida de datos.

Un evento puede incluir:

- fecha de inicio y fin;
- hora de inicio y fin;
- responsable;
- prioridad;
- fase;
- lugar o enlace;
- notas.

Ejemplo:

```text
Reunión de seguimiento de tesis
25/09/2026
15:00–16:00
Lugar: Google Meet
```

---

# 6.17. Deadlines

Utiliza **Deadline** para fechas límite concretas:

- entrega de protocolo;
- envío a comité de ética;
- cierre de convocatoria;
- entrega de trabajo final;
- envío de manuscrito;
- fecha de informe al financiador.

La pestaña **Deadlines e hitos** separa próximas fechas y puede mostrar deadlines vencidos.

---

# 6.18. Hitos

Un hito representa un acontecimiento relevante del proyecto, aunque no sea una tarea de varias horas.

Ejemplos:

- aprobación ética;
- primer participante incluido;
- 50 % de reclutamiento;
- cierre de reclutamiento;
- base de datos congelada;
- análisis final completado;
- tesis defendida.

---

## 6.19. Tareas vencidas

Una tarea se considera vencida cuando tiene una fecha límite anterior a hoy y su estado no es `Completada` ni `Cancelada`.

Revisa periódicamente el indicador **Vencidas**.

Cuando una tarea se complete:

- cambia el estado a **Completada**;
- ajusta el progreso a 100 %;
- registra fecha completada si quieres mantener una historia temporal.

---

## 6.20. Agenda global

La Agenda global permite filtrar por:

- proyecto;
- estado;
- tipo;
- texto de búsqueda.

Si seleccionas **Todos los proyectos**, puedes ver el calendario conjunto y una tabla de tiempo semanal por proyecto.

Para crear bloques de trabajo o registrar tiempo con herramientas completas, selecciona un proyecto específico.

---

## 6.21. Flujo semanal recomendado para estudiantes

### Lunes

- abrir Agenda;
- revisar deadlines;
- elegir 3–5 tareas prioritarias;
- asignar horas estimadas;
- bloquear tiempo en calendario.

### Durante la semana

- mover bloques si cambia la planificación;
- actualizar estado y progreso;
- registrar incidencias en notas.

### Viernes

- registrar las horas reales;
- marcar tareas completadas;
- revisar tareas vencidas;
- preparar la semana siguiente.

Esto convierte RESEARCH OS en un sistema de trabajo, no solo en un almacén de información.

---

## 6.22. Ejemplo de cronograma de una tesis

```text
Hito       Aprobación del protocolo          01/10
Tarea      Preparar base de datos             01/10–05/10
Tarea      Reclutamiento                      06/10–15/12
Evento     Reunión con tutor                   cada 2 semanas
Deadline   Cierre de reclutamiento             15/12
Tarea      Limpieza de datos                  16/12–22/12
Hito       Base de datos congelada             22/12
Tarea      Análisis estadístico               23/12–10/01
Tarea      Redacción de resultados            11/01–20/01
Deadline   Entrega de tesis                    31/01
```

---

## 6.23. Eliminar elementos y registros de tiempo

La ficha de cada elemento permite eliminarlo tras confirmación.

También puedes eliminar:

- bloques de trabajo planificados;
- registros de tiempo real.

Antes de borrar un elemento con historia de trabajo, considera si es mejor cambiarlo a **Cancelada** para conservar el registro de planificación.

---

**Siguiente capítulo:** [Documentación y finanzas →](documentacion-finanzas.md)
