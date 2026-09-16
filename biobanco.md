---
layout: default
title: Biobanco, muestras y alícuotas
---

# 4. Biobanco, muestras y alícuotas

[← Volver al índice](index.md)

El módulo **Biobanco** permite controlar material biológico de forma transversal. Una muestra puede tener un proyecto de origen, estar asociada a un participante y una visita, ocupar una localización física y utilizarse posteriormente en experimentos.

Si tu investigación no utiliza material biológico, puedes omitir este módulo.

## 4.1. Dos formas de trabajar con muestras

Puedes acceder a las muestras desde:

**Proyecto → Muestras**  
Muestra las muestras originadas en ese proyecto y las muestras de otros proyectos que hayan sido asociadas al mismo.

**Biobanco → Muestras**  
Vista global de todas las muestras registradas.

Ambas pantallas trabajan sobre los mismos registros.

---

## 4.2. Indicadores globales del Biobanco

La página global muestra:

- Muestras
- Disponibles
- Reservadas
- Agotadas
- Alícuotas
- Sin ubicación

Estos indicadores sirven para revisar rápidamente el estado del inventario.

---

## 4.3. Tipos de muestra disponibles

RESEARCH OS incluye:

| Tipo |
|---|
| Sangre total |
| Plasma |
| Suero |
| PBMC |
| ADN |
| ARN |
| Tejido |
| Biopsia |
| Orina |
| Saliva |
| Otro |

Al seleccionar **Otro** puedes registrar un tipo personalizado.

## 4.4. Estados de muestra

- Disponible
- Reservada
- En uso
- Parcialmente consumida
- Agotada
- Descartada

El estado se actualiza manualmente según la situación real del material.

---

## 4.5. Crear primero las localizaciones físicas

Si vas a controlar la posición exacta del material, configura antes:

**Biobanco → Localizaciones**

La jerarquía admitida es:

```text
Centro
└── Laboratorio
    └── Congelador
        └── Estante
            └── Rack
                └── Caja
                    └── Posición
```

No es obligatorio llegar hasta Posición. Puedes detener la jerarquía en el nivel que tenga sentido para tu laboratorio.

### Ejemplo

```text
Centro: Facultad de Ciencias de la Salud
└── Laboratorio: Biología Molecular
    └── Congelador: FZ-01
        └── Estante: E2
            └── Rack: R03
                └── Caja: C12
                    └── Posición: B07
```

---

## 4.6. Crear una localización

Abre **+ Nueva localización**.

Campos:

**Tipo**  
Centro, Laboratorio, Congelador, Estante, Rack, Caja o Posición.

**Nombre \***  
Nombre visible.

**Código**  
Opcional. Ejemplo `FZ-01`.

**Padre**  
RESEARCH OS limita las opciones al nivel inmediatamente superior. Un congelador, por ejemplo, debe pertenecer a un laboratorio.

**Temperatura / condición**  
Ejemplo `-80 °C`, `4 °C`, `temperatura ambiente`.

**Localización activa**  
Permite conservar localizaciones históricas sin usarlas para nuevos registros.

**Notas**  
Información adicional.

Pulsa **Guardar localización**.

### Orden recomendado

Crea la jerarquía de arriba hacia abajo:

1. Centro
2. Laboratorio
3. Congelador
4. Estante
5. Rack
6. Caja
7. Posición

---

## 4.7. Editar o eliminar localizaciones

Cada localización puede editarse.

Para eliminarla debes confirmar la acción. La eliminación puede ser rechazada si la localización está siendo utilizada o si rompería la estructura jerárquica. En esos casos, considera marcarla como inactiva.

---

# 4.8. Registrar una muestra

Puedes hacerlo desde:

**Proyecto → Muestras → + Nueva muestra**

o desde:

**Biobanco → Muestras → + Nueva muestra**

En la vista global tendrás que seleccionar primero el proyecto de origen.

### Código

Puedes escribir un código propio o dejarlo vacío para que RESEARCH OS genere un código automático del tipo:

```text
ROS-SMP-000001
```

Si tu protocolo ya utiliza códigos de muestra, suele ser preferible mantener esa convención.

### Tipo de muestra \*

Selecciona el tipo biológico.

### Estado

Indica el estado actual del material.

### Subtipo

Campo libre para mayor detalle, por ejemplo:

- Plasma EDTA
- Tejido tumoral
- Tejido adyacente
- ADN germinal

### Participante

Opcional. Solo aparecen participantes del proyecto de origen.

### Visita

Opcional. Permite indicar en qué visita se obtuvo la muestra.

### Fecha de obtención

Para muestras nuevas viene activada por defecto, pero puede desactivarse.

### Hora de obtención

Campo de texto, por ejemplo `09:30`.

### Cantidad / volumen

Valor numérico no negativo.

### Unidad

Opciones:

- µL
- mL
- mg
- g
- ng
- µg
- unidades
- Otro

### Localización

Selecciona una localización activa. La lista muestra la ruta jerárquica.

### Calidad / observaciones de calidad

Ejemplos:

- RIN 8.2
- hemólisis leve
- concentración 45 ng/µL
- integridad adecuada

### Responsable

Persona responsable de la obtención, recepción o gestión.

### Proyectos asociados adicionales

Este campo es importante. Permite que una misma muestra sea visible en otros proyectos **sin duplicar el registro físico**.

### Notas

Observaciones adicionales.

Pulsa **Registrar muestra**.

---

## 4.9. Proyecto de origen y proyectos asociados

Cada muestra tiene un único **proyecto de origen**.

Puede, además, estar asociada a otros proyectos. En ese caso:

- sigue existiendo una sola muestra física;
- mantiene un solo código e ID interno;
- conserva su localización y cantidad;
- puede aparecer en la pestaña Muestras de varios proyectos;
- RESEARCH OS la etiqueta como **Origen** o **Asociada** según el contexto.

Esto evita la duplicación artificial de material.

---

## 4.10. Buscar y filtrar muestras

En el proyecto puedes filtrar por:

- texto libre: código, subtipo, responsable;
- tipo;
- estado.

En Biobanco global puedes filtrar además por proyecto.

Las tablas muestran información como:

- código;
- proyecto;
- participante;
- visita;
- tipo/subtipo;
- estado;
- cantidad/unidad;
- centro, laboratorio, congelador, estante, rack, caja y posición;
- proyectos asociados;
- número de experimentos;
- número de resultados experimentales.

---

# 4.11. Ficha completa de una muestra

Selecciona una fila. Se abrirán siete pestañas:

1. **Resumen**
2. **Trazabilidad**
3. **Localización**
4. **Alícuotas**
5. **Experimentos**
6. **Resultados experimentales**
7. **Proyectos asociados**

## Resumen

Muestra estado, tipo, número de alícuotas, experimentos, resultados, cantidad, subtipo, responsable, calidad y notas.

Desde **Editar muestra** puedes modificar los campos o eliminarla con confirmación.

## Trazabilidad

Muestra:

- proyecto de origen;
- participante;
- visita;
- fecha/hora de obtención;
- ID interno.

## Localización

Descompone la ruta física por niveles y muestra la ruta completa.

## Experimentos

Lista experimentos que han utilizado la muestra o alguna de sus alícuotas.

## Resultados experimentales

Lista resultados específicamente vinculados a la muestra o a sus alícuotas.

## Proyectos asociados

Muestra el proyecto de origen y los proyectos adicionales.

---

# 4.12. Alícuotas

Una alícuota representa una subdivisión de una muestra principal.

Ejemplo:

```text
Muestra: PLASMA-P001-V0
├── ALQ-01 · 500 µL
├── ALQ-02 · 500 µL
└── ALQ-03 · 250 µL
```

Para crearla:

**Muestra → Alícuotas → + Crear alícuota**

### Campos

- Código de alícuota, opcional. Si se deja vacío se genera `ROS-ALQ...`.
- Estado.
- Cantidad / volumen.
- Unidad.
- Localización.
- Notas.

La alícuota puede tener una ubicación distinta de la muestra principal.

---

## 4.13. Editar o eliminar una alícuota

Selecciona la alícuota de la tabla. Puedes modificar cantidad, estado, localización y notas.

Para eliminarla, marca la confirmación correspondiente.

---

# 4.14. Relación con experimentos

Cuando crees un experimento, RESEARCH OS permite seleccionar como material:

- una muestra completa;
- una alícuota.

Al registrar el uso puedes indicar cantidad, unidad y fecha.

La ficha de muestra mostrará posteriormente qué experimentos la han utilizado.

> **Importante:** en la versión 0.10.1, registrar `100 µL utilizados` dentro de un experimento **no resta automáticamente 100 µL de la cantidad de la muestra o alícuota**. Si necesitas mantener stock exacto, actualiza manualmente la cantidad y/o el estado del material.

---

## 4.15. Buenas prácticas de inventario

### Mantén códigos físicos y digitales alineados

Si el tubo tiene la etiqueta `CRC-P001-PL-01`, utiliza preferiblemente el mismo código en RESEARCH OS.

### Registra la localización con el nivel adecuado

Para pocas muestras puede ser suficiente congelador + caja. Para colecciones grandes, registrar Posición reduce errores.

### Actualiza estados

Cuando una muestra cambia de situación, actualiza su estado:

```text
Disponible → Reservada → En uso → Parcialmente consumida → Agotada
```

No todos los proyectos seguirán exactamente esa secuencia.

### No dupliques registros para reutilización científica

Si una muestra se reutiliza en otro proyecto, utiliza **Proyectos asociados adicionales**.

### Registra el material del experimento

Asociar muestras/alícuotas a experimentos permite reconstruir la cadena de procedencia del resultado.

---

## 4.16. Ejemplo de trazabilidad completa

```text
Proyecto: Biomarcadores CRC
└── Participante: CRC-012
    └── Visita: V0 Basal
        └── Muestra: CRC-012-PLASMA-V0
            ├── Localización: Centro A / Lab 1 / -80 / E2 / R3 / C12 / B07
            └── Alícuota: CRC-012-PL-V0-A1
                └── Experimento: ELISA IL-6
                    └── Resultado: IL-6 = 8.4 pg/mL
```

Este es uno de los usos principales de RESEARCH OS: que el resultado no quede desconectado de la persona, visita y material que lo originaron.

---

**Siguiente capítulo:** [Estudios, experimentos y resultados →](estudios-experimentos.md)
