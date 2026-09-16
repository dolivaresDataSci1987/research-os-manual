---
layout: default
title: Preguntas frecuentes y solución de problemas
---

# 10. Preguntas frecuentes y solución de problemas

[← Volver al índice](index.md)

## 10.1. ¿Necesito Internet para utilizar RESEARCH OS localmente?

No para el funcionamiento básico de la aplicación local. La interfaz se ejecuta en tu propio ordenador y el navegador se conecta a `127.0.0.1`.

Sí puedes necesitar Internet para otras actividades externas, como abrir un enlace web, consultar una publicación o descargar/actualizar software.

---

## 10.2. ¿Necesito tener Python instalado?

La distribución desktop está diseñada para incluir el runtime necesario. El usuario final no debería tener que instalar Python ni ejecutar `streamlit run`.

---

## 10.3. Se ha abierto una página en el navegador. ¿Eso significa que mis datos están en Internet?

No necesariamente. En la versión local, la dirección es normalmente:

```text
http://127.0.0.1:8501
```

`127.0.0.1` es la propia máquina. El navegador actúa como interfaz de una aplicación que está corriendo localmente.

Comprueba también que la barra lateral muestre el modo **local-first**, no **demo pública**.

---

## 10.4. ¿Dónde están mis datos?

Por defecto, la distribución desktop utiliza:

```text
Documents/RESEARCH_OS_DATA/
```

Dentro encontrarás la base de datos y los espacios de archivos de los proyectos.

Utiliza el botón **Abrir carpeta de datos** de la ventana de control para localizarla.

---

## 10.5. Cerré la pestaña del navegador. ¿Perdí mi trabajo?

No. Si el servidor local continúa abierto, puedes utilizar **Abrir RESEARCH OS** en la ventana de control.

Los registros que ya habías guardado permanecen en la base de datos.

Los cambios que estuvieran escritos en un formulario pero todavía no enviados mediante su botón de Guardar pueden perderse al cerrar o recargar la página.

---

## 10.6. ¿Cómo cierro correctamente la aplicación?

Utiliza **Cerrar RESEARCH OS** en la ventana de control desktop.

Cerrar solamente la pestaña del navegador puede dejar el servidor local activo.

---

## 10.7. La URL no usa el puerto 8501. ¿Es un error?

No necesariamente. Si el puerto 8501 estaba ocupado, el launcher busca otro puerto local disponible.

Mientras la dirección siga siendo local (`127.0.0.1`), la aplicación puede funcionar con normalidad.

---

## 10.8. macOS dice que no puede verificar al desarrollador

La versión 0.10.1 todavía no está notarizada comercialmente por Apple.

Si el archivo procede de tu canal oficial de distribución:

1. Abre Finder → Aplicaciones.
2. Haz clic secundario sobre RESEARCH OS.
3. Pulsa **Abrir**.
4. Confirma de nuevo.

En algunas versiones de macOS puede ser necesario revisar **Ajustes del Sistema → Privacidad y seguridad**.

---

## 10.9. Windows muestra una advertencia al ejecutar el programa

Las versiones no firmadas comercialmente pueden aparecer como editor desconocido. Comprueba que el archivo procede del canal oficial y que has descomprimido completamente el paquete.

La versión 0.10.1 de Windows es portable; todavía no es el instalador comercial definitivo.

---

## 10.10. Moví solamente `RESEARCH OS.exe` y ya no funciona

En una distribución portable debes mantener la carpeta completa. El ejecutable puede depender de otros archivos incluidos en el paquete.

Vuelve a descomprimir el paquete original completo y ejecuta RESEARCH OS desde esa carpeta.

---

## 10.11. ¿Puedo mover `RESEARCH_OS_DATA` mientras la app está abierta?

No es recomendable. Cierra RESEARCH OS antes de copiar, mover, restaurar o manipular la carpeta de datos.

---

## 10.12. ¿Cómo hago una copia de seguridad?

Con la versión actual:

1. Cierra RESEARCH OS.
2. Copia la carpeta completa `RESEARCH_OS_DATA`.
3. Guarda la copia en un destino seguro.
4. Añade una fecha al nombre de la copia.

No copies únicamente `research_os.sqlite3`, porque los archivos de proyecto se almacenan también en el filesystem.

---

## 10.13. ¿Puedo guardar `RESEARCH_OS_DATA` en Dropbox, OneDrive o Google Drive y abrirlo en varios equipos?

No se recomienda utilizar la misma base SQLite de manera simultánea desde varios equipos mediante sincronización de carpetas. Puede generar conflictos o pérdida de cambios.

Para la versión actual, considera el workspace como una fuente de verdad local única y utiliza servicios aprobados solo para copias de seguridad cuando sea apropiado.

---

## 10.14. Creé un proyecto pero no aparece en Inicio

Comprueba:

- que se guardó correctamente;
- que no está archivado;
- que estás utilizando la misma carpeta local de datos;
- que no abriste accidentalmente la demo pública en otra pestaña.

La vista Inicio normalmente muestra proyectos no archivados en el portfolio.

---

## 10.15. No veo un proyecto archivado

En **Proyectos**, activa **Mostrar archivados**.

También puedes cambiar su estado si necesitas devolverlo al portfolio activo.

---

## 10.16. ¿Cómo cambio el progreso del proyecto?

Ve a:

**Proyecto → Información del proyecto → Datos generales**

Mueve el control de progreso y guarda los cambios.

El progreso del proyecto es manual y no se calcula automáticamente a partir de las tareas.

---

## 10.17. No puedo seleccionar una persona como responsable de una tarea

Primero debes registrarla en:

**Proyecto → Información del proyecto → Equipo**

Después aparecerá entre los responsables disponibles en Agenda.

---

## 10.18. No puedo crear una visita

Comprueba que:

- existe el participante;
- el código de visita no está vacío;
- no existe ya una visita con el mismo código para ese participante;
- la ventana de visita no tiene fecha inicial posterior a la final.

---

## 10.19. No puedo crear un participante con un código determinado

El código debe ser único dentro del proyecto. `P001` y una variante equivalente ya existente pueden provocar conflicto.

Utiliza otro código o edita el participante ya registrado.

---

## 10.20. Eliminé una visita. ¿Qué ocurre con los datos clínicos?

Los datos clínicos vinculados se conservan, pero quedan sin la asociación de esa visita.

---

## 10.21. Eliminé un participante. ¿Qué ocurre con sus muestras?

Si existen muestras, la interfaz advierte que se conservarán y quedarán desvinculadas del participante.

Antes de eliminar personas de un estudio real, considera si es más adecuado cambiar el estado a **Retirado** o **Completado**.

---

## 10.22. ¿Puedo usar nombre y apellido del participante?

Técnicamente sí, porque son campos opcionales. Sin embargo, utilízalos únicamente cuando tu protocolo, consentimiento y política institucional lo permitan.

RESEARCH OS prioriza códigos pseudonimizados.

---

## 10.23. ¿Cómo registro una muestra sin participante?

En el formulario de muestra selecciona **— Sin participante —**.

Esto puede ser útil para controles, estándares u otro material no vinculado a una persona.

---

## 10.24. ¿Cómo registro una muestra sin saber todavía su ubicación?

Selecciona **— Sin ubicación —**.

La muestra contará dentro del indicador global **Sin ubicación**. Puedes editarla después para asignar su posición física.

---

## 10.25. No aparece una localización en el formulario de muestra

Comprueba que la localización esté marcada como activa. La selección de muestras utiliza localizaciones activas.

También revisa que la jerarquía haya sido creada correctamente.

---

## 10.26. ¿Puedo asociar la misma muestra a dos proyectos?

Sí. Una muestra mantiene un solo proyecto de origen y puede tener proyectos asociados adicionales.

No se duplica físicamente el registro.

---

## 10.27. Registré consumo de muestra en un experimento y la cantidad no cambió

Es el comportamiento actual. RESEARCH OS registra la cantidad utilizada como dato de trazabilidad, pero **no descuenta automáticamente el stock**.

Actualiza manualmente cantidad y estado de la muestra/alícuota si necesitas reflejar el inventario restante.

---

## 10.28. ¿Cómo sé qué experimentos han utilizado una muestra?

Abre:

**Muestra → Experimentos**

La ficha muestra experimentos que utilizaron la muestra o cualquiera de sus alícuotas.

---

## 10.29. ¿Por qué un participante aparece asociado a un experimento aunque no lo seleccioné manualmente?

Puede tratarse de una **asociación derivada del material biológico**. Si el experimento utiliza una muestra que pertenece a ese participante, RESEARCH OS puede derivar la relación automáticamente.

---

## 10.30. No puedo quitar una asociación derivada de participante

Las asociaciones derivadas no se eliminan desde la lista de participantes directos. Modifica la asociación del material biológico que provoca esa relación.

---

## 10.31. ¿Un resultado experimental necesita siempre una muestra?

No. Puede tener:

- material específico;
- participante específico;
- contexto agregado/sin asociación específica.

Elige el nivel de trazabilidad que represente correctamente el resultado.

---

## 10.32. No puedo asociar un resultado a una muestra que no aparece

La selección de material del resultado se basa en los materiales asociados al experimento. Primero asocia la muestra o alícuota en:

**Experimento → Material biológico**

Después vuelve al resultado.

---

## 10.33. ¿Puedo guardar archivos muy grandes como resultados?

RESEARCH OS permite subir archivos, pero para datasets muy pesados puede ser más conveniente utilizar **Ruta externa** y conservar el archivo en una ubicación gestionada específicamente para datos grandes.

Recuerda que una ruta externa no se copia ni se incluye automáticamente en el backup de `RESEARCH_OS_DATA`.

---

## 10.34. ¿Cómo adjunto un informe diagnóstico?

Abre el estudio y ve a:

**Archivos → + Adjuntar informe**

Los adjuntos de estudios Dx aceptan PDF, DOC y DOCX.

---

## 10.35. ¿Puedo subir una factura y asociarla a un gasto?

Sí.

1. Sube la factura en **Documentación**, preferentemente como `Factura / Justificante`.
2. Ve a **Finanzas → Movimientos**.
3. Crea o edita el gasto.
4. Selecciona la factura en **Documento / justificante asociado**.

---

## 10.36. ¿Los gastos se introducen con signo negativo?

No. Los importes se registran como positivos. El campo **Tipo** determina el efecto contable.

Ejemplo correcto:

```text
Tipo: Gasto
Importe: 500000
```

---

## 10.37. ¿Por qué el dinero “disponible” no coincide con mi cuenta bancaria?

RESEARCH OS calcula el resumen a partir de la financiación y movimientos registrados. Si existe una diferencia con el saldo real, comprueba:

- ingresos no registrados;
- gastos pendientes de registrar;
- compromisos;
- devoluciones;
- ajustes;
- moneda utilizada.

Puedes registrar un **corte de saldo real** en Evolución financiera para documentar cuánto dinero había realmente en una fecha concreta.

---

## 10.38. Arrastré una tarea en el calendario. ¿Qué cambió?

Para tareas, arrastrar el elemento actualiza su fecha objetivo/deadline. Para eventos puede actualizar fechas y horarios. Para bloques de trabajo actualiza su programación.

Abre la ficha después si quieres comprobar el resultado.

---

## 10.39. ¿Cuál es la diferencia entre horas estimadas, planificadas y registradas?

- **Estimadas:** esfuerzo total que crees necesario.
- **Planificadas:** horas reservadas en bloques de calendario.
- **Registradas:** horas que realmente trabajaste.

---

## 10.40. ¿Cómo genero un informe en PDF?

1. Ve a **Proyecto → Informes**.
2. Crea un informe.
3. Ábrelo desde la tabla.
4. En **Contenido y exportación**, pulsa **Descargar PDF**.

---

## 10.41. ¿Qué es una versión congelada de un informe?

Es una fotografía de los datos del proyecto en un momento determinado.

Utilízala para conservar exactamente el contexto de una entrega aunque el proyecto siga cambiando después.

---

## 10.42. ¿Puedo exportar datos a Excel?

Sí. En **Informes → Exportaciones** selecciona el dataset y pulsa **Descargar Excel**.

También existe CSV.

---

## 10.43. Modifiqué el Excel exportado. ¿Se actualiza RESEARCH OS?

No. Las exportaciones son copias independientes y no modifican la base de datos.

---

## 10.44. ¿Puedo utilizar RESEARCH OS con un proyecto sin participantes?

Sí. Puedes utilizar únicamente proyecto, equipo, agenda, documentación, finanzas, informes y publicaciones.

---

## 10.45. ¿Puedo utilizar RESEARCH OS sin biobanco?

Sí. Los módulos son complementarios. Una tesis clínica o de revisión/proyecto puede no necesitar muestras.

---

## 10.46. ¿RESEARCH OS sustituye REDCap, una historia clínica o un sistema institucional?

RESEARCH OS es una plataforma de gestión de investigación. La idoneidad de cada herramienta depende del estudio y de las exigencias institucionales.

No debe utilizarse como sustituto de una historia clínica asistencial ni para decisiones clínicas. Si tu institución exige un sistema específico para captura regulada, consentimiento o datos clínicos, debes seguir esas exigencias.

---

## 10.47. ¿Qué hago si la aplicación no inicia?

Prueba, en este orden:

1. Cierra cualquier instancia anterior.
2. Reinicia el ordenador.
3. En Windows, verifica que descomprimiste el paquete completo.
4. En macOS, confirma que instalaste la versión correcta: Apple Silicon o Intel.
5. Verifica que el sistema de seguridad no haya bloqueado la aplicación.
6. Comprueba que tienes permiso de escritura en `Documents`.
7. No borres `RESEARCH_OS_DATA` para “arreglar” el problema: contiene tus datos.
8. Si necesitas soporte, conserva una descripción exacta de qué ocurre y cualquier mensaje de error.

---

## 10.48. La aplicación abre, pero mis proyectos han desaparecido

Antes de crear nada nuevo:

1. Comprueba si estás en demo pública o local.
2. Pulsa **Abrir carpeta de datos**.
3. Comprueba que estás utilizando la carpeta `RESEARCH_OS_DATA` habitual.
4. Busca si existe una copia anterior o si cambió la cuenta de usuario del ordenador.
5. No reemplaces archivos hasta haber identificado la causa.

Si tienes backup, conserva tanto la carpeta actual como la copia antes de restaurar.

---

## 10.49. ¿Puedo editar directamente `research_os.sqlite3`?

No se recomienda. Utiliza la interfaz de RESEARCH OS.

La edición manual puede romper relaciones o dejar la base de datos en un estado incoherente.

---

## 10.50. ¿Qué debo incluir al pedir soporte?

Sin enviar datos sensibles, describe:

- sistema operativo y versión;
- versión de RESEARCH OS;
- pantalla/módulo donde ocurre;
- pasos exactos para reproducirlo;
- texto del error;
- si ocurre siempre o solo con un proyecto;
- captura de pantalla anonimizada, si es posible.

No envíes bases de datos reales, historias clínicas o documentación confidencial por canales no autorizados.

---

**Siguiente capítulo:** [Glosario →](glosario.md)
