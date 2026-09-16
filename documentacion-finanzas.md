---
layout: default
title: Documentación y finanzas
---

# 7. Documentación y finanzas

[← Volver al índice](index.md)

RESEARCH OS reúne la gestión documental y financiera en una misma sección. Puedes trabajar dentro de un proyecto o consultar una vista transversal desde el menú global.

---

# 7.1. Documentación

Accesos:

- **Proyecto → Documentación y Finanzas → Documentación**
- **Menú lateral → Documentación y Finanzas → Documentación**

En modo local, los archivos guardados desde la interfaz se almacenan dentro del workspace privado del proyecto y su información se registra en la base de datos.

## 7.2. Qué documentos puedes guardar

RESEARCH OS permite subir archivos de forma general. Las categorías disponibles son:

| Categoría |
|---|
| Protocolo |
| Comité de ética |
| Enmienda |
| Consentimiento informado |
| Consentimiento |
| CRF / eCRF |
| SOP / Procedimiento |
| Contrato |
| Financiación / Concesión |
| Financiación |
| Factura / Justificante |
| Presupuesto / Oferta |
| Orden de compra |
| Plan de gestión de datos |
| Plan de análisis |
| Informe |
| Afiches / Posters |
| Presentación |
| Manuscrito / Publicación |
| Correspondencia |
| Otro |

No es necesario utilizar todas las categorías.

---

## 7.3. Subir un documento

Ve a **Documentación del proyecto → + Subir documento**.

1. Selecciona el archivo.
2. Elige una categoría.
3. Añade una descripción o notas, si lo necesitas.
4. Pulsa **Guardar documento**.

La tabla mostrará:

- archivo;
- categoría;
- tamaño;
- descripción;
- fecha/hora de incorporación.

### Recomendación para nombres

Antes de subir un documento, utiliza nombres comprensibles, por ejemplo:

```text
Protocolo_v2_2026-09-10.pdf
Aprobacion_Comite_Etica_2026-10-03.pdf
Plan_Analisis_v1.docx
Factura_Reactivos_2026-11-15.pdf
```

Aunque RESEARCH OS mantiene el nombre original visible, internamente puede almacenar el archivo con un nombre técnico para evitar colisiones.

---

## 7.4. Buscar y filtrar documentación

Dentro de un proyecto puedes:

- buscar por nombre, categoría o descripción;
- filtrar por categoría.

En la vista global puedes además filtrar por proyecto.

Selecciona una fila para abrir sus acciones.

---

## 7.5. Descargar, editar metadatos o eliminar

Al seleccionar un documento:

### Descargar

Pulsa **Descargar** para recuperar el archivo almacenado.

### Editar metadatos

Puedes cambiar:

- categoría;
- descripción / notas.

El contenido del archivo no se modifica.

### Eliminar documento

Marca **Confirmar eliminación** y pulsa **Eliminar documento**.

La eliminación retira el registro y el archivo almacenado. Para documentos importantes de un proyecto real, realiza copias de seguridad periódicas.

---

## 7.6. Diferencia entre Documentación y archivos de otros módulos

RESEARCH OS tiene varios lugares para archivos porque cada uno tiene un propósito distinto:

- **Documentación:** documentos generales del proyecto.
- **Estudios Dx → Archivos:** informe clínico de un estudio diagnóstico concreto.
- **Resultados experimentales → Archivos:** archivos que pertenecen a un resultado experimental concreto.
- **Publicaciones:** pueden enlazarse a un documento previamente guardado en Documentación.

Ejemplo:

```text
Aprobación comité ética        → Documentación
Informe de anatomía patológica → Estudio Dx
Informe de RNA-seq             → Resultado experimental
Manuscrito final               → Documentación + registro de Publicación
```

---

# 7.7. Finanzas

Accede desde:

**Proyecto → Documentación y Finanzas → Finanzas**

La gestión financiera se divide en cinco pestañas:

1. **Resumen financiero**
2. **Movimientos**
3. **Presupuesto**
4. **Fuentes de financiación**
5. **Evolución financiera**

La vista global permite comparar proyectos y abrir las finanzas detalladas de uno de ellos.

---

## 7.8. Monedas disponibles

La interfaz incluye:

- EUR
- USD
- GBP
- PYG
- BRL
- ARS

Para proyectos en Paraguay puedes utilizar **PYG**.

> Conviene mantener una moneda principal coherente dentro de cada proyecto. La versión actual no funciona como un sistema avanzado de conversión automática de divisas.

---

# 7.9. Fuentes de financiación

Aunque en la interfaz aparecen después de otras pestañas, conceptualmente suele ser útil crearlas primero.

Ve a:

**Fuentes de financiación → + Añadir fuente**

Campos:

**Fuente / convocatoria \***  
Nombre de la financiación.

**Entidad financiadora**  
Universidad, agencia, hospital, empresa, fondos propios, etc.

**Importe concedido**  
Cantidad total concedida.

**Moneda**  
Selecciona el código correspondiente.

**Código / referencia**  
Número de proyecto, convocatoria o referencia.

**Fecha de concesión**  
Opcional.

**Inicio / Fin**  
Periodo de financiación, opcional.

**Notas**  
Condiciones o información relevante.

Pulsa **Guardar**.

### Ejemplo

```text
Fuente: Fondo de investigación de la Universidad
Financiador: Universidad X
Importe concedido: 15.000.000 PYG
Referencia: INV-2026-014
```

---

# 7.10. Presupuesto

Ve a:

**Presupuesto → + Añadir partida**

Cada partida define una cantidad planificada.

Campos:

- Partida \*
- Presupuesto
- Moneda
- Notas

Ejemplo:

| Partida | Presupuesto |
|---|---:|
| Reactivos | 5.000.000 PYG |
| Impresiones y material | 1.000.000 PYG |
| Análisis externo | 3.000.000 PYG |
| Viajes | 2.000.000 PYG |

La tabla muestra posteriormente presupuestado, gastado, comprometido y disponible.

---

# 7.11. Movimientos financieros

Ve a:

**Movimientos → + Registrar movimiento**

Tipos disponibles:

- Ingreso
- Gasto
- Compromiso
- Liberación compromiso
- Devolución
- Ajuste +
- Ajuste -

### Regla importante sobre los importes

**Introduce siempre el importe como número positivo.** El tipo del movimiento determina su efecto contable.

No escribas `-500000` para un gasto de 500.000 PYG. Registra:

```text
Tipo: Gasto
Importe: 500000
```

---

## 7.12. Campos de un movimiento

**Fecha \***  
Fecha del movimiento.

**Tipo \***  
Ingreso, gasto, compromiso, etc.

**Categoría**

- Personal
- Equipamiento
- Reactivos
- Consumibles
- Servicios externos
- Viajes
- Publicaciones
- Software
- Formación
- Infraestructura
- Financiación
- Otros

**Concepto \***  
Descripción breve y clara.

**Importe \***  
Cantidad positiva.

**Moneda**

**Proveedor / pagador**  
Contraparte.

**Fuente de financiación**  
Opcional. Permite vincular el movimiento a una fuente registrada.

**Partida presupuestaria**  
Opcional.

**Documento / justificante asociado**  
Opcional. La lista se alimenta de Documentación del proyecto.

**Referencia / factura / PO**  
Número de factura, orden, recibo, etc.

**Notas**

---

## 7.13. Ejemplo de gasto con justificante

Primero sube:

```text
Factura_Reactivos_001.pdf
Categoría: Factura / Justificante
```

Después crea el movimiento:

```text
Fecha: 12/10/2026
Tipo: Gasto
Categoría: Reactivos
Concepto: Kit ELISA
Importe: 1.250.000
Moneda: PYG
Proveedor: Proveedor X
Partida: Reactivos
Justificante: Factura_Reactivos_001.pdf
Referencia: FAC-001
```

Así el registro contable queda conectado con el documento.

---

## 7.14. Compromisos

Utiliza **Compromiso** cuando un gasto está previsto/comprometido pero todavía no se ha materializado como gasto definitivo.

Ejemplo:

```text
Compra aprobada de reactivos: 2.000.000 PYG
Tipo: Compromiso
```

Si posteriormente necesitas liberar ese compromiso, utiliza **Liberación compromiso** según tu flujo de gestión.

---

# 7.15. Resumen financiero

La primera pestaña muestra:

- **Concedido**
- **Recibido**
- **Gastado**
- **Comprometido**
- **Disponible**
- **Presupuestado**

Cuando existen fondos recibidos, aparece también el porcentaje de ejecución sobre los fondos recibidos.

Si existen partidas presupuestarias, se muestra una tabla de ejecución por partida.

---

# 7.16. Evolución financiera

Los movimientos contables no siempre reflejan exactamente el saldo bancario o efectivo disponible en una fecha concreta. Para documentar esa realidad, RESEARCH OS permite registrar **cortes de saldo**.

Ve a:

**Evolución financiera → + Registrar / actualizar corte de saldo**

Campos:

- Fecha
- Saldo real
- Moneda
- Notas

Ejemplo:

```text
31/10/2026 · 8.450.000 PYG
30/11/2026 · 6.980.000 PYG
31/12/2026 · 5.100.000 PYG
```

RESEARCH OS muestra una gráfica temporal y una tabla de estos cortes.

Esto sirve para comparar la contabilidad registrada con la cantidad realmente disponible en fechas de referencia.

---

## 7.17. Editar y eliminar datos financieros

Las tablas de fuentes, presupuesto y movimientos permiten seleccionar una fila para editarla.

La eliminación requiere confirmación.

Los cortes de saldo también pueden eliminarse desde su tabla.

Para conservar una historia financiera fiable, evita borrar movimientos únicamente para “corregir” una cifra sin entender qué ocurrió. Cuando corresponda, puede ser preferible utilizar ajustes o documentar la corrección en notas.

---

## 7.18. Vista global de finanzas

En:

**Menú → Documentación y Finanzas → Finanzas**

aparece una tabla con una fila por proyecto:

- concedido;
- recibido;
- gastado;
- comprometido;
- disponible;
- presupuestado;
- moneda.

Después puedes seleccionar un proyecto y abrir debajo todas sus pestañas financieras.

---

## 7.19. Uso simplificado para una tesis

No necesitas convertir RESEARCH OS en un software contable completo.

Para una tesis de maestría, puede bastar con:

1. Registrar la financiación o fondos propios.
2. Crear 3–5 partidas.
3. Registrar gastos relevantes.
4. Adjuntar facturas importantes.
5. Revisar el disponible.

Si el proyecto no tiene presupuesto, ignora el módulo financiero.

---

## 7.20. Buenas prácticas documentales y financieras

- Sube documentos con nombres comprensibles.
- Añade categoría y descripción.
- No guardes información personal innecesaria.
- Vincula facturas con movimientos cuando sea útil.
- Registra importes positivos y deja que el tipo determine el efecto.
- Evita mezclar monedas sin una convención clara.
- Realiza backups completos de `RESEARCH_OS_DATA`.
- Para obligaciones fiscales, contables o institucionales, utiliza los sistemas oficiales exigidos; RESEARCH OS sirve como herramienta de gestión del proyecto.

---

**Siguiente capítulo:** [Informes, publicaciones y exportaciones →](informes-exportaciones.md)
