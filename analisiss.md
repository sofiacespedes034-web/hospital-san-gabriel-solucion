# Análisis de registros clínicos simulados

**Estudiante:** Karen Sofia Duarte Cespedes  
**Código:** 01260181080  
**Proyecto:** Hospital San Gabriel  
**Herramienta:** Microsoft Excel  
**Tipo de datos:** Registros clínicos ficticios con fines académicos

## 1. Interpretación de los siete indicadores

### 1. Total de pacientes
Se identificaron **20 registros de pacientes**, correspondientes a los códigos P001–P020. Este total debe calcularse contando únicamente los registros individuales y excluyendo las filas vacías y el bloque de resumen que aparece al final del archivo.

### 2. Edad promedio
La edad promedio es de **43 años**. La base contiene pacientes adultos de distintas edades; por tanto, el promedio sirve como descripción general, pero no representa por sí solo las necesidades de cada grupo etario.

### 3. Temperatura promedio
La temperatura promedio registrada es de aproximadamente **37,15 °C**. Aunque el promedio está cerca del rango habitual, hay registros individuales elevados, como 38,1 °C y 38,5 °C. El promedio no debe utilizarse para descartar alteraciones en pacientes específicos.

### 4. Distribución por sexo
Se registraron **10 pacientes con sexo F y 10 con sexo M**, equivalentes al 50 % para cada categoría. La distribución está equilibrada en esta muestra, aunque no permite generalizar resultados a una población real.

### 5. Estado de atención
Los estados registrados son: **9 finalizados**, **7 en atención** y **4 pendientes**. Esto indica que 45 % de los casos figura como finalizado, 35 % continúa en atención y 20 % está pendiente. Conviene revisar periódicamente los casos pendientes y en atención para mantener actualizado el seguimiento administrativo.

### 6. Saturación mínima de oxígeno
La saturación mínima registrada es **91 %**. Este valor merece revisión clínica en el contexto del paciente y de la calidad de la medición; no debe interpretarse de forma aislada ni utilizarse como diagnóstico automático. La base incluye un registro sin dato de saturación, por lo que el indicador se calculó con los valores disponibles.

### 7. Registros incompletos
Se identificó **1 registro clínico incompleto** entre los 20 pacientes: el registro **P016** no contiene el valor de saturación de oxígeno. Esto corresponde al 5 % de los registros. El dato faltante debe verificarse en la fuente original o marcarse como no disponible; no se debe inventar ni reemplazar por un valor supuesto.

## 2. Inconsistencias y aspectos de calidad detectados

- **Dato faltante:** el registro P016 no tiene saturación de oxígeno.
- **Formato numérico:** la temperatura usa coma decimal (por ejemplo, `36,8`), por lo que debe convertirse de manera consistente antes de realizar cálculos.
- **Encabezados con espacios y signos adicionales:** algunos nombres de columnas contienen espacios al inicio o al final y puntuación sobrante. Esto puede dificultar las fórmulas, filtros y análisis.
- **Filas que no son registros clínicos:** después de los 20 pacientes aparecen filas vacías, un bloque de indicadores y datos para gráficas. Si se incluyen en los cálculos, pueden alterar los resultados o generar errores.
- **Etiqueta de estado ambigua en el resumen:** el bloque final usa la expresión “cantidad de estado de atención paciente” para los cuatro casos que en los registros individuales figuran como “Pendiente”. Conviene corregir la etiqueta para que coincida con la categoría real.
- **Archivo con extensión no coincidente:** el archivo llamado `.xlsx` contiene el mismo contenido de texto delimitado por punto y coma que el CSV, no un libro de Excel válido. Debe abrirse/importarse como texto delimitado o guardarse nuevamente desde Excel como un archivo `.xlsx` real.
- **Criterio de análisis:** los diagnósticos y datos son simulados. Los indicadores describen esta base de práctica y no permiten inferir diagnósticos reales ni conclusiones clínicas generales.

## 3. Recomendaciones de limpieza

1. Conservar únicamente las 20 filas identificadas con códigos P001–P020 para el análisis.
2. Normalizar los encabezados, quitando espacios y signos sobrantes.
3. Convertir edad, temperatura y frecuencia cardíaca a valores numéricos; manejar la coma decimal correctamente.
4. Convertir la saturación porcentual a un campo numérico y mantener el valor faltante como vacío o “No registrado”.
5. Estandarizar las categorías de sexo y estado de atención.
6. Separar los registros individuales de las tablas de resumen y los datos usados para gráficas.
7. Verificar los cálculos en Excel y documentar cualquier dato que siga pendiente de validación.

## 4. Reflexión sobre la privacidad clínica

La privacidad clínica es esencial porque los datos de salud pueden revelar información personal y afectar la dignidad, la seguridad y los derechos de los pacientes. Aunque esta actividad utiliza registros ficticios, permite reconocer la importancia de limitar el acceso a la información, utilizar los datos solo para el propósito autorizado y evitar compartir archivos con personas que no participan en el trabajo. En una institución real, sería necesario aplicar controles de acceso, proteger los archivos con medidas de seguridad, evitar divulgar identificadores y cumplir las normas de protección de datos personales. También es importante revisar la información antes de publicarla y reportar cualquier error o acceso no autorizado. El manejo responsable de los datos fortalece la confianza entre pacientes y personal sanitario y reduce el riesgo de uso indebido.

