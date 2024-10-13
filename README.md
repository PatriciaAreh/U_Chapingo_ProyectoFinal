# PROYECTO FINAL- Análisis de la evolución en la Universidad Autónoma Chapingo.

## Introducción
Este repositorio contiene el análisis y visualización de datos de los registros de alumnos de la Universidad Autónoma Chapingo, desde 2006 hasta 2021. El proyecto incluye la selección, limpieza y preparación de una base de datos con más de 148,000 registros, así como análisis exploratorio y predicciones a futuro.
La Universidad Autónoma Chapingo es una de las principales instituciones de educación superior en México, especializada en ciencias agrícolas y forestales. Este estudio busca identificar patrones de crecimiento en la matrícula de estudiantes, así como proyecciones para los próximos 10 años, con el objetivo de apoyar la toma de decisiones estratégicas para la oferta académica de la universidad.
## 1.- Selección y Justificación de la base de datos.
- Búsqueda de la base de datos
  Los integrantes realizamos una búsqueda individual en diversas fuentes de bases de datos. Tras analizar las propuestas, a través de una sesión virtual, se acordó por unanimidad utilizar la base de datos que contiene los registros de alumnos en la Universidad de Chapingo.
- Justificación de la selección
- La exploración al vuelo de los datos contenidos en la propuesta nos pareció completa, con los criterios necesarios y suficientes, lo que nos permitirá explorar y analizar las distintas hipótesis -que se describen más a detalle en los puntos 3 y 4 (Análisis exploratorio y Visualización de Datos).  Con lo anterior, acordamos que: contiene un cúmulo lo suficientemente grande para ejercitar el manejo de grandes cantidades de registros (metadatos) y con las suficientes variables que nos brindaran bastas alternativas para indagar.
## 2.- Preparación y limpieza de datos. 
- Resumen de los datos
  Es una base de datos de la universidad de Chapingo, con 148,431 datos, que recopila información del número de alumnos matriculados en los diferentes niveles que tienen disponibles en su programa académico; estos comprenden desde propedéutico hasta doctorado, en los años 2006 al 2021 en sus distintas unidades académicas.
Las columnas muestran información del año de ingreso, género del alumno, a que grado ingresan, edad, nivel académico, categoría (becados, externos, media beca…) Unidad académica, sede, programa educativo, nacionalidad, estado de procedencia, lengua indígena y número de alumnos.
- Limpieza de datos
  En primera instancia, detectamos la ausencia de ciertas especificaciones en la columna de nacimiento, por lo que se consideraron incompletos. 
En el campo de lengua indígena sólo en caso afirmativo había información, aunado al tipo de lengua se trataba. Aunado a esto, encontramos que existían registros que no eran individuales, sino de 2 o más con respecto al número de alumnos. 
Por tanto, la corrección para esta situación fue, registrar uno solo con esas características. Se encontraron 264 registros en esa situación, que totalizan 556 alumnos, por lo que la limpieza da un total de 292 alumnos, que representan el 0.1963% del total de 148,722, por lo que esta limpieza no afecta la integridad ni es representativo del total.
Para el caso de las columnas de “Lengua indígena” y “fecha de nacimiento”, se rellenaron las celdas vacías con los datos “Null” y “N/A”, sin embargo, estas variables no formaron parte del análisis posterior. 
Por último, en el campo de nivel educativo, fueron reclasificados los datos de las maestrías que estaban en nivel doctorado a “Maestrías”, así mismo el programa propedéutico al ser parte de la preparación para el “medio superior” se englobó en un solo nivel de medio superior.
