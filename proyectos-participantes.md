---
layout: default
title: Proyectos, equipo y participantes
---

# 3. Proyectos, equipo y participantes

[← Volver al índice](index.md)

Este capítulo explica el núcleo organizativo de RESEARCH OS: el proyecto, su equipo y la ficha longitudinal de cada participante.

## 3.1. Página Proyectos

En el menú lateral selecciona **Proyectos**.

La vista principal incluye:

- buscador por nombre, acrónimo, institución o investigador principal;
- casilla **Mostrar archivados**;
- botón **+ Nuevo proyecto**;
- una tarjeta por proyecto con estado, progreso y métricas principales.

En cada tarjeta puedes ver información resumida como participantes, muestras, estudios Dx, experimentos, documentos, agenda, informes y dinero disponible.

Pulsa **Abrir** para entrar en un proyecto.

---

## 3.2. Crear un proyecto

Pulsa **+ Nuevo proyecto**.

### Campos

**Nombre del proyecto \***  
Obligatorio. Utiliza un nombre suficientemente descriptivo.

**Acrónimo**  
Opcional. Útil para identificar proyectos con nombres largos.

**Descripción**  
Resumen del objetivo o alcance.

**Estado**  
Valores disponibles: `Idea`, `Planificado`, `En marcha`, `Pausado`, `Finalizado`, `Archivado`.

**Progreso del proyecto**  
Porcentaje manual entre 0 y 100.

**Investigador/a principal**  
Nombre del responsable científico principal.

**Institución**  
Universidad, hospital, centro, laboratorio u organización.

**Inicio previsto / Inicio real / Fin previsto / Fin real**  
Cada fecha es opcional y se activa mediante su casilla correspondiente.

Pulsa **Crear proyecto**. El nuevo proyecto aparecerá en el portfolio y RESEARCH OS creará su workspace local.

---

## 3.3. Ficha del proyecto

Al abrir un proyecto encontrarás nueve pestañas:

1. **Resumen**
2. **Información del proyecto**
3. **Participantes**
4. **Muestras**
5. **Estudios Dx y Complementarios**
6. **Experimentos**
7. **Agenda y Cronograma**
8. **Informes**
9. **Documentación y Finanzas**

### Resumen

La pestaña Resumen concentra métricas de:

- investigador principal e institución;
- equipo;
- participantes;
- visitas;
- datos clínicos;
- muestras de origen y asociadas;
- estudios Dx e informes adjuntos;
- experimentos;
- documentos;
- tareas pendientes, en curso y vencidas;
- horas registradas;
- informes y outputs científicos;
- financiación concedida, recibida, gastada, comprometida y disponible.

Esta vista es especialmente útil para revisiones periódicas del proyecto.

---

## 3.4. Editar los datos generales

Ve a:

**Información del proyecto → Datos generales**

El formulario contiene los mismos campos utilizados al crear el proyecto. Modifica lo necesario y pulsa **Guardar cambios**.

El porcentaje de progreso debe actualizarse manualmente. Puedes utilizar un criterio propio, pero conviene ser consistente durante toda la investigación.

---

## 3.5. Gestionar el equipo

Ve a:

**Información del proyecto → Equipo**

La pantalla muestra el número total de miembros y cuántos están activos.

### Añadir un miembro

Abre **+ Añadir miembro**.

Campos disponibles:

- Nombre \*
- Apellidos \*
- Rol \*
- Rol personalizado si seleccionas `Otro`
- Email
- Teléfono
- Institución
- Departamento / unidad
- ORCID
- Funciones / contribución en el proyecto
- Notas
- Miembro activo

Roles predefinidos:

| Rol |
|---|
| Investigador/a principal |
| Co-investigador/a |
| Investigador/a |
| Coordinador/a de proyecto |
| Data manager |
| Bioestadístico/a |
| Técnico/a de laboratorio |
| Enfermería |
| Monitor/a |
| Colaborador/a |
| Otro |

Pulsa **Añadir al equipo**.

### Editar un miembro

1. Localiza la persona.
2. Pulsa **Editar**.
3. Modifica los datos.
4. Pulsa **Guardar cambios**.

### Miembros inactivos

Puedes mantener a una persona registrada y desmarcar **Miembro activo** cuando ya no participe. La casilla **Mostrar miembros inactivos** permite incluirlos o excluirlos de la vista.

### Eliminar miembro

Marca **Confirmar baja** y pulsa **Eliminar**.

Si solo quieres conservar la historia de participación, normalmente es preferible marcarlo como inactivo en vez de eliminarlo.

---

## 3.6. Gestión del proyecto: archivar y eliminar

Ve a:

**Información del proyecto → Gestión**

### Archivar

Pulsa **Archivar proyecto** para retirarlo del portfolio activo sin borrar sus datos.

Los proyectos archivados pueden volver a encontrarse activando **Mostrar archivados** en la lista de Proyectos. También puedes cambiar el estado desde Datos generales.

### Eliminar

La eliminación requiere marcar una confirmación antes de pulsar **Eliminar definitivamente**.

RESEARCH OS advierte que:

- se elimina el registro y sus datos dependientes;
- si existen muestras cuyo proyecto de origen es el proyecto que intentas eliminar, la operación puede bloquearse para preservar la trazabilidad;
- la carpeta local del proyecto se mueve a `trash`.

> Para proyectos reales, **archivar suele ser más seguro que eliminar**.

---

# 3.7. Participantes

Ve a:

**Proyecto → Participantes**

La página muestra una tabla maestra. Puedes buscar por código, ID externo o estado y filtrar por estado.

Si existen más de 25 participantes, la tabla se pagina.

Columnas principales:

- Código
- ID externo
- Estado
- Consentimiento
- Identificación
- Sexo
- Año de nacimiento
- Inclusión
- Número de visitas
- Número de muestras
- Número de experimentos
- Número de estudios Dx

Haz clic en una fila para abrir la ficha completa.

---

## 3.8. Crear un participante

Pulsa **+ Nuevo participante**.

### Código del participante \*

Es obligatorio y debe ser único dentro del proyecto.

Recomendado:

```text
P001
P002
P003
```

Evita:

```text
JUAN-PEREZ-1980
CI-1234567
```

### ID externo / código de origen

Opcional. Puede servir para relacionar RESEARCH OS con otro sistema, siempre respetando la política de datos.

La propia interfaz recuerda evitar identificadores personales innecesarios.

### Estado

Opciones:

| Estado | Interpretación habitual |
|---|---|
| Candidato | Evaluado pero aún no incluido |
| Incluido | Ya forma parte del estudio |
| Seguimiento | En seguimiento activo |
| Retirado | Ha salido del estudio |
| Completado | Ha completado el protocolo |

### Modo de identificación

- **Pseudonimizado:** existe una clave separada que podría permitir reidentificación autorizada.
- **Anonimizado:** el registro no pretende conservar una relación identificable.
- **Identificable:** se conservan datos identificativos directos.

RESEARCH OS prioriza el uso de códigos pseudonimizados.

### Consentimiento

Opciones:

- Pendiente
- Firmado
- No procede
- Retirado

Este campo organiza el estado del consentimiento, pero no sustituye el documento original ni los procedimientos exigidos por tu protocolo.

### Nombre y apellidos

Son opcionales. Regístralos únicamente cuando el protocolo y la política de protección de datos lo permitan y exista una razón real para hacerlo.

### Sexo

Opciones actuales:

- No especificado
- Femenino
- Masculino
- Intersexual
- Otro

### Año de nacimiento

Opcional. Debe ser un año válido.

### Fecha de inclusión

Activa **Registrar fecha de inclusión** para guardarla.

### Notas

Utilízalas para observaciones breves relacionadas con la gestión. Evita introducir información sensible innecesaria.

Pulsa **Guardar**.

---

## 3.9. Ficha longitudinal del participante

Al seleccionar un participante se abre una ficha con seis pestañas:

1. **Resumen**
2. **Información clínica**
3. **Visitas**
4. **Muestras**
5. **Estudios Dx y Complementarios**
6. **Experimentos**

### Resumen

Muestra:

- estado;
- número de visitas;
- número de muestras;
- número de datos clínicos;
- estudios Dx;
- experimentos;
- código;
- ID externo;
- modo de identificación;
- consentimiento;
- sexo;
- año de nacimiento;
- fecha de inclusión;
- notas.

Desde **Editar participante** puedes actualizar los datos o eliminar el participante.

---

# 3.10. Visitas

Abre:

**Participante → Visitas**

### Crear visita

Pulsa **+ Añadir visita**.

Campos:

**Código de visita \***  
Debe ser único para ese participante.

**Estado**

- Planificada
- Completada
- Cancelada
- No realizada

**Tipo de visita**

- Cribado
- Basal
- Seguimiento
- Final
- No programada
- Otro

Si seleccionas **Otro**, puedes definir un tipo personalizado.

**Fecha prevista**  
Opcional.

**Fecha real**  
Opcional.

**Ventana de visita**  
Permite definir inicio y fin aceptables de la ventana.

**Notas**  
Observaciones de gestión.

Pulsa **Guardar visita**.

### Editar visita

Selecciona la fila en la tabla. Se abrirá el formulario de edición.

### Eliminar visita

Marca la confirmación y pulsa **Eliminar visita**.

Los datos clínicos vinculados a la visita **se conservan**, pero quedan sin esa asociación de visita.

---

# 3.11. Información clínica

Abre:

**Participante → Información clínica**

Cada fila representa un dato estructurado.

### Añadir un dato clínico

Abre **+ Añadir dato clínico**.

Campos:

**Variable clínica \***  
Ejemplos: `Edad`, `Hemoglobina`, `Diagnóstico`, `Presión arterial sistólica`.

**Valor \***  
El valor se guarda como contenido del registro.

**Categoría**

- General
- Demografía
- Antecedentes
- Diagnóstico
- Tratamiento
- Laboratorio
- Signos vitales
- Escalas
- Otro

Si eliges Otro puedes utilizar una categoría personalizada.

**Unidad**  
Ejemplos: `mg/dL`, `mmHg`, `kg`, `años`.

**Fuente**  
Ejemplos: `eCRF`, `historia clínica`, `laboratorio`, `cuestionario`.

**Visita asociada**  
Opcional. Selecciona una de las visitas del participante.

**Fecha del dato**  
Opcional.

**Notas**  
Contexto adicional.

### Buenas prácticas para datos clínicos

Mantén nombres de variables consistentes. No mezcles, por ejemplo:

```text
Hemoglobina
Hb
HGB
```

si todos significan lo mismo y luego quieres analizarlos juntos.

Asimismo, mantén una convención de unidades estable.

### Editar o eliminar

Selecciona una fila. El formulario permite editarla. Para borrar, activa **Confirmar eliminación** y pulsa **Eliminar registro**.

---

## 3.12. Acceso a muestras, Dx y experimentos desde el participante

La ficha del participante sirve como una vista longitudinal:

### Muestras

Muestra únicamente las muestras relacionadas con ese participante. Al seleccionar una, puedes abrir su ficha completa.

### Estudios Dx y Complementarios

Permite crear y revisar pruebas diagnósticas del participante.

### Experimentos

Muestra experimentos asociados directamente al participante o derivados del uso de sus muestras/alícuotas.

Esto permite responder rápidamente preguntas como:

- ¿Qué visitas tiene este participante?
- ¿Qué muestras se obtuvieron?
- ¿Qué pruebas diagnósticas existen?
- ¿En qué experimentos se utilizaron sus muestras?

---

## 3.13. Eliminar un participante con muestras

Si intentas eliminar un participante que tiene muestras, la interfaz avisa de que las muestras **se conservarán y quedarán desvinculadas**.

Esto está pensado para evitar que la eliminación administrativa de una persona destruya accidentalmente el registro físico de material biológico.

Antes de eliminar un participante real, revisa las implicaciones científicas y documentales. En muchos proyectos puede ser más adecuado cambiar su estado a **Retirado** o **Completado**.

---

## 3.14. Flujo recomendado para estudios longitudinales

Para cada nuevo participante:

```text
1. Crear participante
2. Registrar consentimiento / estado
3. Crear visita basal
4. Registrar datos clínicos basales
5. Registrar muestras de la visita, si existen
6. Añadir estudios Dx, si existen
7. Crear próximas visitas
8. Repetir el proceso en seguimientos
```

Con este enfoque, RESEARCH OS puede utilizarse como una ficha longitudinal de investigación sin convertir la interfaz en una historia clínica asistencial.

---

**Siguiente capítulo:** [Biobanco, muestras y alícuotas →](biobanco.md)
