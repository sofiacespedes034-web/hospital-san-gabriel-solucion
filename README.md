# Hospital San Gabriel: análisis de registros clínicos simulados

**Estudiante:** Karen Sofia Duarte Cespedes  
**Código:** 01260181080  
**Herramienta de análisis:** Microsoft Excel  
**Tipo de información:** Datos ficticios para fines académicos

## 1. Objetivo del proyecto

Organizar, revisar y analizar una base de 20 registros clínicos simulados para calcular indicadores descriptivos, identificar inconsistencias y reflexionar sobre la calidad y la privacidad de los datos sanitarios. El ejercicio es académico y no está destinado a apoyar decisiones clínicas reales.

## 2. Diccionario de datos

| Campo | Descripción | Tipo/formato esperado |
|---|---|---|
| `codigo` | Identificador ficticio del registro (P001–P020). | Texto |
| `Edad` | Edad simulada del paciente, expresada en años. | Número entero |
| `sexo` | Categoría registrada para el sexo (`F` o `M`). | Texto categórico |
| `Fecha de consulta` | Fecha simulada de la consulta. | Fecha (`dd/mm/aaaa`) |
| `Motivo` | Motivo de consulta registrado. | Texto |
| `temperatura (°C)` | Temperatura corporal registrada. | Número decimal en °C |
| `frecuencia cardíaca (lpm)` | Frecuencia cardíaca en latidos por minuto. | Número |
| `saturación de oxígeno (%)` | Saturación de oxígeno registrada. | Porcentaje; puede estar vacío si falta el dato |
| `diagnóstico simulado` | Diagnóstico ficticio asociado al registro. | Texto |
| `estado de atención` | Estado administrativo de la atención: finalizada, en atención o pendiente. | Texto categórico |

## 3. Proceso de limpieza y validación

1. Se revisó la estructura de los archivos de entrada y se identificaron 20 registros individuales, con códigos P001 a P020.
2. Se distinguieron los registros clínicos de las filas vacías, los indicadores agregados y la información auxiliar para gráficas que aparecen al final del archivo.
3. Se detectaron encabezados con espacios y signos sobrantes; deben normalizarse para facilitar el uso de fórmulas y filtros.
4. Se identificó el uso de coma decimal en la temperatura. Antes de calcular promedios, los valores deben convertirse a números sin alterar su magnitud.
5. Se verificaron los campos incompletos. El registro P016 no tiene saturación de oxígeno; se conserva como dato faltante y no se imputa un valor inventado.
6. Se revisaron las categorías de estado de atención y se señaló que la etiqueta “paciente” usada en el resumen no coincide con “Pendiente” en los registros individuales.
7. Se observó que el archivo que tiene extensión `.xlsx` posee contenido de texto delimitado por punto y coma, igual que el CSV. Para utilizarlo como libro de Excel, debe importarse correctamente y guardarse de nuevo en formato `.xlsx`.

## 4. Indicadores reportados

El análisis contempla los siguientes siete indicadores:

1. Total de pacientes: 20.
2. Edad promedio: 43 años.
3. Temperatura promedio: aproximadamente 37,15 °C.
4. Distribución por sexo: 10 F y 10 M.
5. Estado de atención: 9 finalizados, 7 en atención y 4 pendientes.
6. Saturación mínima registrada: 91 %.
7. Registros incompletos: 1, correspondiente a P016 por ausencia de saturación de oxígeno.

Los resultados describen únicamente los registros simulados disponibles. No deben interpretarse como estadísticas de un hospital real ni como recomendaciones diagnósticas.

## 5. Archivos entregados

- `README.md`: objetivo, diccionario de datos, proceso de limpieza, indicadores, archivos y declaración sobre la naturaleza ficticia de los datos.
- `analisis.md`: interpretación de los siete indicadores, descripción de las inconsistencias y reflexión sobre privacidad clínica.
- `Base_Datos_Hospital..csv`: archivo de datos de entrada delimitado por punto y coma.
- `Base_Datos_Hospital (1)(1).xlsx`: archivo recibido con extensión `.xlsx`, cuyo contenido debe importarse o guardarse nuevamente como libro de Excel válido antes de tratarlo como tal.

## 6. Declaración de datos ficticios

Todos los registros y datos clínicos de este proyecto son **ficticios y se utilizan exclusivamente con fines académicos**. No representan pacientes reales ni deben emplearse para atención médica, diagnóstico, investigación clínica real o toma de decisiones institucionales. Los resultados son descriptivos de esta base simulada y pueden depender de la calidad y completitud de los datos proporcionados.
