---
layout: default
title: Estudios, experimentos y resultados
---

# 5. Estudios, experimentos y resultados

[← Volver al índice](index.md)

Este capítulo describe dos áreas relacionadas pero conceptualmente diferentes:

- **Estudios Dx y Complementarios:** pruebas clínicas o diagnósticas realizadas a un participante.
- **Experimentos y resultados:** actividad experimental o analítica del proyecto, vinculable a participantes, muestras y alícuotas.

---

# 5.1. Estudios Dx y Complementarios

Puedes acceder a estos estudios desde tres lugares:

1. **Participante → Estudios Dx y Complementarios**: solo los estudios de esa persona.
2. **Proyecto → Estudios Dx y Complementarios**: todos los estudios del proyecto.
3. **Menú global → Estudios Dx y Complementarios**: visión transversal de todos los proyectos.

Los tres accesos trabajan sobre el mismo registro.

## 5.2. Cuándo utilizar este módulo

Ejemplos:

- análisis de laboratorio;
- hemograma;
- bioquímica;
- coagulación;
- microbiología;
- radiografía;
- ecografía;
- TC/TAC;
- resonancia magnética;
- PET/PET-TC;
- electrocardiograma;
- ecocardiograma;
- endoscopia;
- anatomía patológica;
- estudio genético o molecular.

Si el dato que quieres registrar es una simple variable clínica, puede ser más apropiado **Información clínica**. Si se trata de una prueba o estudio con entidad propia, informe, fecha, centro y conclusión, utiliza **Estudios Dx y Complementarios**.

---

## 5.3. Categorías disponibles

- Laboratorio
- Imagen
- Cardiología
- Funcional
- Endoscopia
- Anatomía patológica
- Genética / molecular
- Otro

## 5.4. Estados disponibles

- Solicitado
- Programado
- Realizado
- Pendiente de informe
- Informado
- Cancelado

Esto permite seguir el ciclo completo desde que se solicita la prueba hasta que existe un informe final.

---

## 5.5. Crear un estudio

Desde un participante:

**Participante → Estudios Dx y Complementarios → + Nuevo estudio**

Desde el proyecto:

**Proyecto → Estudios Dx y Complementarios → + Nuevo estudio**

En la vista de proyecto debes elegir primero el participante.

### Campos

**Código**  
Opcional. Si se deja vacío, RESEARCH OS genera un código automático `ROS-DX-...`.

**Categoría \***  
Selecciona la familia del estudio.

**Tipo de estudio \***  
La lista incluye pruebas frecuentes. Si eliges `Otro`, puedes indicar un tipo personalizado.

**Título / descripción corta \***  
Ejemplo: `Colonoscopia basal`, `TC toracoabdominal`, `Hemograma V1`.

**Estado**  
Sitúa el estudio dentro de su ciclo de trabajo.

**Fecha del estudio**  
Opcional.

**Visita**  
Opcional. Permite relacionar el estudio con una visita concreta del participante.

**Centro / laboratorio / proveedor**  
Lugar o entidad que realizó la prueba.

**Hallazgos / resumen**  
Contenido clínico o técnico relevante.

**Conclusión / impresión diagnóstica**  
Conclusión final del estudio.

**Notas**  
Información adicional de gestión.

Pulsa **Guardar estudio**.

---

## 5.6. Abrir la ficha del estudio

Selecciona una fila de la tabla. La ficha se divide en:

1. **Resumen**
2. **Informe clínico**
3. **Archivos**
4. **Gestión**

### Resumen

Muestra estado, categoría, participante, número de archivos, proyecto, visita, fecha y centro/proveedor.

### Informe clínico

Muestra los campos de hallazgos, conclusión y notas.

### Archivos

Permite guardar el documento original del estudio.

### Gestión

Permite editar o eliminar el registro.

---

## 5.7. Adjuntar un informe

En **Archivos → + Adjuntar informe** puedes subir:

- `.pdf`
- `.doc`
- `.docx`

También puedes añadir una descripción.

Después de guardar, el archivo aparece en una tabla con nombre, tipo, tamaño, descripción y fecha.

Selecciona el archivo para:

- descargarlo;
- eliminarlo con confirmación.

> Eliminar el estudio elimina también los informes PDF/Word almacenados dentro de RESEARCH OS para ese estudio.

---

## 5.8. Vista global de Estudios Dx

La página global muestra indicadores de:

- número de estudios;
- informados;
- pendientes de informe;
- informes adjuntos.

Filtros disponibles:

- búsqueda;
- proyecto;
- categoría;
- estado.

Esta vista es útil para detectar pruebas pendientes o revisar el conjunto de un portfolio.

---

# 5.9. Experimentos

Los experimentos se crean dentro de un proyecto:

**Proyecto → Experimentos**

Un experimento puede relacionarse con:

- uno o varios participantes;
- una o varias muestras;
- una o varias alícuotas;
- uno o varios resultados experimentales.

## 5.10. Tipos de experimento

- ELISA
- PCR / qPCR
- Secuenciación
- Citometría de flujo
- Western blot
- Cultivo celular
- Microscopía
- Proteómica
- Metabolómica
- Inmunohistoquímica
- Otro

## 5.11. Estados de experimento

- Planificado
- Preparación
- En curso
- Finalizado
- Fallido
- Cancelado

---

## 5.12. Crear un experimento

Abre **+ Nuevo experimento**.

### Campos

**Código**  
Opcional. Si no introduces uno, RESEARCH OS genera un código automático.

**Nombre / título \***  
Describe claramente el ensayo.

**Tipo \***  
Selecciona el tipo o utiliza `Otro`.

**Estado**  
Situación del experimento.

**Fecha del experimento**  
Opcional.

**Responsable**  
Persona que ejecuta o supervisa.

**Plataforma / equipo**  
Ejemplo: `Illumina NextSeq`, `LightCycler 480`, `BD FACSCanto`.

**Lote de reactivos**  
Campo útil para trazabilidad.

**Protocolo / metodología**  
Descripción del método, versión de SOP o pasos clave.

**Notas**  
Observaciones adicionales.

Pulsa **Guardar experimento**.

La interfaz indicará que puedes abrirlo posteriormente para asociar participantes y material biológico.

---

## 5.13. Buscar experimentos

La tabla permite filtrar por:

- búsqueda por código, nombre o responsable;
- estado;
- tipo.

Columnas relevantes:

- código;
- experimento;
- tipo;
- estado;
- fecha;
- responsable;
- plataforma;
- material biológico;
- participantes;
- número de resultados.

Selecciona una fila para abrir la ficha completa.

---

# 5.14. Ficha del experimento

La ficha tiene seis pestañas:

1. **Resumen**
2. **Participantes**
3. **Material biológico**
4. **Protocolo / metodología**
5. **Resultados**
6. **Gestión**

## Resumen

Muestra estado, tipo, número de participantes, materiales y resultados, además de responsable, plataforma y notas.

Desde **Editar experimento** puedes modificar su información.

---

## 5.15. Asociar participantes

En **Participantes** existen dos formas de relación.

### Asociación directa

Selecciona manualmente los participantes que forman parte del experimento.

Esto es útil cuando:

- el experimento es clínico o funcional;
- todavía no existe una muestra asociada;
- quieres declarar explícitamente el sujeto relacionado.

### Asociación derivada del material

Si una muestra o alícuota pertenece a un participante y se utiliza en el experimento, RESEARCH OS puede derivar automáticamente esa asociación.

La interfaz distingue estas asociaciones. Las derivadas del material no se eliminan desde el editor de asociaciones directas; debes modificar el material del experimento si quieres cambiar esa relación.

---

# 5.16. Asociar muestras o alícuotas

Ve a:

**Experimento → Material biológico → + Asociar muestra o alícuota**

Las opciones incluyen material del proyecto y muestras asociadas disponibles en su contexto.

Campos:

- Material
- Cantidad utilizada
- Unidad
- Fecha de uso
- Notas

Pulsa **Asociar material**.

Después aparece una tabla con:

- tipo: Muestra o Alícuota;
- código;
- muestra de origen;
- participante;
- cantidad usada;
- unidad;
- fecha;
- notas.

Selecciona una fila para editar el uso o desasociar el material.

> Registrar una cantidad utilizada **no modifica automáticamente el stock** de la muestra. Si necesitas reflejar la cantidad restante, actualiza la muestra/alícuota en Biobanco.

---

## 5.17. Protocolo y metodología

La pestaña **Protocolo / metodología** muestra:

- plataforma/equipo;
- lote de reactivos;
- protocolo/metodología.

Utiliza este espacio para dejar un registro comprensible de cómo se obtuvo el resultado. Para protocolos completos o SOP extensos, puedes además guardar el archivo en **Documentación**.

---

# 5.18. Resultados experimentales

Ve a:

**Experimento → Resultados → + Nuevo resultado**

Un experimento puede producir múltiples resultados.

## 5.19. Campos de un resultado

**Código**  
Opcional. Se genera automáticamente si se deja vacío.

**Variable / resultado \***  
Ejemplos: `IL-6`, `Ct GAPDH`, `Expresión relativa`, `Mutación KRAS`, `Reads mapeados`.

**Valor**  
Puede ser numérico o textual según el tipo de resultado.

**Unidad**  
Opcional.

**Fecha del resultado**  
Opcional.

**Validación**

- Pendiente
- Validado
- Rechazado
- Repetir

**Validado por**  
Persona que revisó/validó.

**Notas**  
Contexto adicional.

Pulsa **Guardar resultado**.

---

# 5.20. Ficha del resultado

La ficha se divide en:

1. **Resumen**
2. **Origen y trazabilidad**
3. **Archivos**
4. **Gestión**

## Resumen

Muestra:

- estado de validación;
- variable;
- valor;
- participante;
- número de archivos;
- muestra/alícuota;
- unidad;
- fecha;
- validador;
- notas.

---

## 5.21. Asociar el resultado a participante y material

En **Origen y trazabilidad** puedes definir un contexto específico.

RESEARCH OS permite tres situaciones principales:

### Material específico

El resultado corresponde a una muestra o alícuota concreta utilizada en el experimento.

### Participante específico

El resultado está vinculado a una persona pero no a un material concreto.

### Agregado / sin asociación específica

El resultado representa una métrica global del experimento.

Para asociar:

1. Selecciona el participante, si corresponde.
2. Selecciona una muestra/alícuota del experimento, si corresponde.
3. Pulsa **Guardar asociación**.

Si el material seleccionado ya tiene un participante conocido, RESEARCH OS comprueba la coherencia entre ambos.

---

# 5.22. Archivos de resultados

En **Archivos → + Añadir archivo / referencia** existen dos modos.

## Subir archivo

El archivo se copia dentro del workspace local de RESEARCH OS.

Ejemplos:

- PDF de análisis;
- imagen;
- tabla de resultados;
- archivo procesado;
- informe bioinformático.

Añade opcionalmente una descripción.

## Ruta externa

En lugar de copiar un archivo grande, puedes guardar una referencia a una ruta externa, por ejemplo:

```text
/Datos/secuenciacion/run_01/sample.fastq.gz
```

O en Windows:

```text
D:\Datos\run_01\sample.fastq.gz
```

En este caso RESEARCH OS conserva la referencia textual, **no copia el archivo**.

Esto puede ser útil para FASTQ, BAM, imágenes o datasets muy pesados.

> Una ruta externa puede dejar de funcionar si el archivo se mueve o si abres RESEARCH OS en otro ordenador donde esa ruta no existe.

---

## 5.23. Eliminar resultados y experimentos

### Eliminar un resultado

La interfaz advierte que la eliminación borra también los archivos copiados dentro de RESEARCH OS asociados a ese resultado.

### Eliminar un experimento

La eliminación borra:

- el experimento;
- sus resultados;
- los archivos asociados a esos resultados.

Las muestras y alícuotas utilizadas **se conservan** en Biobanco.

Utiliza estas acciones con cuidado y realiza copias de seguridad periódicas.

---

## 5.24. Ejemplo de flujo experimental

```text
Participante P014
└── Visita V0
    └── Muestra ARN-P014-V0
        └── Experimento RNA-seq-01
            ├── Responsable: Investigador A
            ├── Plataforma: Secuenciador X
            ├── Material usado: 1 µg ARN
            └── Resultados
                ├── QC: Aprobado
                ├── Reads mapeados: 94 %
                └── Informe bioinformático.pdf
```

La ventaja de esta estructura es que puedes navegar desde el participante o la muestra hacia el experimento y sus resultados sin perder el origen biológico.

---

**Siguiente capítulo:** [Agenda, tareas y gestión del tiempo →](agenda.md)
