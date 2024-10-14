# PROYECTO FINAL- Análisis de la evolución en la Universidad Autónoma Chapingo.

## Introducción
Este repositorio contiene el análisis y visualización de datos de los registros de alumnos de la Universidad Autónoma Chapingo, desde 2006 hasta 2021. El proyecto incluye la selección, limpieza y preparación de una base de datos con más de 148,000 registros, así como análisis exploratorio y predicciones a futuro.
La Universidad Autónoma Chapingo es una de las principales instituciones de educación superior en México, especializada en ciencias agrícolas y forestales. Este estudio busca identificar patrones de crecimiento en la matrícula de estudiantes, así como proyecciones para los próximos 10 años, con el objetivo de apoyar la toma de decisiones estratégicas para la oferta académica de la universidad.

## 1.- Selección y Justificación de la base de datos.
- Búsqueda de la base de datos: Los integrantes realizamos una búsqueda individual en diversas fuentes de bases de datos. Tras analizar las propuestas, a través de una sesión virtual, se acordó por unanimidad utilizar la base de datos que contiene los registros de alumnos en la Universidad de Chapingo.
- Justificación de la selección: La exploración al vuelo de los datos contenidos en la propuesta nos pareció completa, con los criterios necesarios y suficientes, lo que nos permitirá explorar y analizar las distintas hipótesis -que se describen más a detalle en los puntos 3 y 4 (Análisis exploratorio y Visualización de Datos).  Con lo anterior, acordamos que: contiene un cúmulo lo suficientemente grande para ejercitar el manejo de grandes cantidades de registros (metadatos) y con las suficientes variables que nos brindaran bastas alternativas para indagar.

## 2.- Preparación y limpieza de datos. 
- Resumen de los datos: Es una base de datos de la universidad de Chapingo, con 148,431 datos, que recopila información del número de alumnos matriculados en los diferentes niveles que tienen disponibles en su programa académico; estos comprenden desde propedéutico hasta doctorado, en los años 2006 al 2021 en sus distintas unidades académicas.
Las columnas muestran información del año de ingreso, género del alumno, a que grado ingresan, edad, nivel académico, categoría (becados, externos, media beca…) Unidad académica, sede, programa educativo, nacionalidad, estado de procedencia, lengua indígena y número de alumnos.
- Limpieza de datos: En primera instancia, detectamos la ausencia de ciertas especificaciones en la columna de nacimiento, por lo que se consideraron incompletos. 
En el campo de lengua indígena sólo en caso afirmativo había información, aunado al tipo de lengua se trataba. Aunado a esto, encontramos que existían registros que no eran individuales, sino de 2 o más con respecto al número de alumnos. 
Por tanto, la corrección para esta situación fue, registrar uno solo con esas características. Se encontraron 264 registros en esa situación, que totalizan 556 alumnos, por lo que la limpieza da un total de 292 alumnos, que representan el 0.1963% del total de 148,722, por lo que esta limpieza no afecta la integridad ni es representativo del total.
Para el caso de las columnas de “Lengua indígena” y “fecha de nacimiento”, se rellenaron las celdas vacías con los datos “Null” y “N/A”, sin embargo, estas variables no formaron parte del análisis posterior. 
Por último, en el campo de nivel educativo, fueron reclasificados los datos de las maestrías que estaban en nivel doctorado a “Maestrías”, así mismo el programa propedéutico al ser parte de la preparación para el “medio superior” se englobó en un solo nivel de medio superior.

## 3.- Análisis exploratorio de datos.  
- El análisis exploratorio de la edad de los alumnos fue realizado utilizando R, con el objetivo de comprender la distribución de esta variable en el conjunto de datos y detectar posibles patrones, tendencias y anomalías que pudieran influir en el comportamiento general de la muestra. 
IMAGEN
Los resultados obtenidos indican que la media de la edad de los estudiantes es de 19 años, mientras que la mediana es de 19 años, lo cual sugiere que la mayoría de los alumnos presentan edades cercanas a este valor los cuales se encuentran concentrados en el nivel educativo: Media Superior y Licenciatura.
La desviación estándar de 4.496006 refleja una dispersión moderada en la edad, indicando que las edades de los estudiantes no están significativamente dispersas respecto al promedio. Además, el resumen de los datos muestra que la edad mínima es de 0 años y la máxima de 73 años, mientras que el primer cuartil es de 17 años y el tercer cuartil es de 21 años, proporcionando una visión más detallada de la distribución de edades en el grupo analizado.
La presencia del valor mínimo de 0 se debe, en gran medida, a un error en la etapa de limpieza de datos, más que a un problema propio de R. En este caso, el valor de 0 probablemente provino de una fila que se omitió eliminar en Excel, y R simplemente identificó y reportó dicho valor como el mínimo.
Sin embargo, este valor no tuvo un impacto significativo en el análisis, ya que no afectó de manera sustancial los resultados generales ni la interpretación de la distribución de edades.

## 4.- Visualización de datos. 
- Objetivo del estudio:
Identificar el nivel educativo, sede y programa educativo con mayor crecimiento en la matrícula de estudiantes, a través del análisis y visualización de los datos a lo largo del tiempo, para realizar una predicción de los próximos 10 años que nos permita estimar la demanda futura la cual permitirá apoyar la toma de decisiones estratégicas en materia de oferta académica.
- Hipótesis: 
  1.- Los años con menor número de alumnos matriculados fueron los años de la pandemia (2020-2021) en comparación a los años anteriores.
  2.- El programa con mayor demanda es la licenciatura agrícola y los de menor demanda serán los de Maestría y doctorado, en los cuales se necesita una estrategia para promocionarlos.
  3.- El alumno está repartido equitativamente en todas las sedes y niveles educativos.
- Plan de desarrollo: 
Como se describió anteriormente, la etapa inicial consistió en la limpieza exhaustiva de datos en Excel, con el objetivo de garantizar la calidad y confiabilidad de la información. Para ello, se establecieron cuatro sencillos pero contundentes criterios:
-     Identificación y eliminación de datos nulos en variables significativas.
-     Corrección de valores atípicos fuera de un rango razonable.
-     Eliminación de valores duplicados en el alumnado.
-      Verificación de la consistencia en los datos, asegurando que cada registro pertenezca a la categoría
En seguida, se realizó un análisis exploratorio de los datos utilizando R, que incluyó la visualización del efecto de la pandemia. 
Para ello, se utilizó un gráfico lineal que muestra el número de alumnos ingresados por año, con la posibilidad de filtrar por género. Además, se desarrolló un gráfico circular para mostrar cuáles son los niveles con más ingresos, y se realizó un análisis más específico para identificar los programas educativos más concurridos por nivel. 
Por último, se utilizó un visualizador de datos como Tableau o Power BI, para facilitar la comprensión de la información y así llegar a conclusiones significativas. Se espera que este proceso de análisis, permita identificar tendencias clave y objetivos estratégicos.

##Resultados:
- Gráfico lineal: Alumnos matriculados por año:
En este gráfico se puede visualizar que al contrario de lo que se pensaba, el número de alumnos fue en incremento gradual desde el año 2006 hasta el año 2021, por lo que no se vio afectado por el inicio de la pandemia en el año 2020-2021, años en los que se registró la mayor cantidad de alumnos matriculados (10,807 y 11.199) respectivamente. Con un promedio de 9,277 alumnos inscritos.
IMAGEN
Por lo que podemos observar que incluso no hubo un cambio significativo al tener un evento adverso como lo fue la pandemia.
Gráfico circular: Número de ingresos por niveles:
En este segundo gráfico se puede observar el número de ingresos en nuestros distintos niveles académicos.
Licenciatura (51.8%): Es la categoría más representativa, lo que sugiere que más de la mitad de los alumnos inscritos están en programas de licenciatura. Esto podría indicar una fuerte preferencia o necesidad de obtener este grado académico en la población estudiantil.
Medio Superior (42.5%): Este grupo también es significativo, indicando que una gran parte de los estudiantes está en el nivel de preparatoria o bachillerato.
Para los niveles de Maestría (3.7%) y Doctorado (2.1%) sugiere que estos niveles académicos aún no son una opción popular o accesible para muchos. Los programas de maestría y doctorado suelen requerir más tiempo y recursos, lo que puede limitar la cantidad de estudiantes que se inscriben.
- Gráfico de barras: Programa educativo.
Este gráfico de barras permite realizar una selección por nivel y programa educativo, proporcionando una visión detallada de la demanda de cada uno. Al analizar los programas con mayor número de estudiantes, se observa que el nivel educativo con la mayor demanda es la licenciatura. 
Dentro de este nivel, se destacan varios programas académicos, siendo el más solicitado el de Ingeniero Agrónomo Especialista en Parasitología Agrícola, seguido por el programa de Ingeniería Agroindustrial,en el resto de los programas se observa una gran dispersión por parte del alumnado. 
IMAGEN
IMAGEN
Este gráfico de barras resalta los cinco programas educativos con mayor demanda en la institución.
1.     Ingeniero Agrónomo Especialista en Parasitología Agrícola: con una matrícula de 8,025 estudiantes.
2.     Ingeniería Agroindustrial: con 7,853 estudiantes.
3.      Ingeniero Agrónomo Especialista en Fitotecnia: con 6,913 estudiantes.
4.      Ingeniero en Irrigación: con 4,975 estudiantes.
5.      Ingeniero Mecánico Agrícola: con 3,354 estudiantes.
Estos cinco programas concentran gran parte de la demanda estudiantil, lo que evidencia la inclinación de los estudiantes hacia carreras relacionadas con la agronomía y las ingenierías especializadas en el sector agrícola. La sede de Chapingo se posiciona como un núcleo importante de formación académica en estas áreas, atendiendo a un gran número de estudiantes y fortaleciendo la oferta educativa de la institución.
- Mapa:Sede
Los gráficos visuales nos muestran que la unidad académica con el mayor ingreso es el Centro de Educación Continua, ubicado en la sede de Chapingo, con un 91.16% de los ingresos. Esta información se puede corroborar en la siguiente tabla, que presenta los diferentes porcentajes de ingreso de las diversas sedes de la universidad, destacando que Chapingo es la que registra el mayor porcentaje.
IMAGEN
IMAGEN
IMAGEN
- Gráfico lineal con predicción: # Alumnos por Año
Finalmente, se ha elaborado un gráfico de líneas con predicción que muestra la suma de alumnos en función del año, abarcando el período de 2005 a 2030. En este gráfico, se puede observar un incremento constante en la matrícula cada año, salvo en 2008 y 2015, donde se registraron disminuciones.
Dado el aumento en las matrículas, decidimos realizar una predicción para los próximos 10 años con el fin de analizar el comportamiento del número de matrículas. La tendencia proyectada es optimista, ya que, a pesar de ciertos factores que podrían haber afectado los ingresos, estos se mantuvieron estables con una tendencia al alza. Además, el periodo de COVID no tuvo un impacto significativo en el número de matrículas, como se ilustra en el gráfico.

##5.- Interpretación y Conclusiones.
Con respecto a nuestra primera hipótesis se descarta la idea de que el fenómeno COVID no fue significativo para los ingresos, por el contrario, fueron los años en los que más matriculados hubo.
Con respecto a la demanda de educación la Licenciatura es el nivel académico más demandado, lo que refleja una preferencia por la formación universitaria en la población estudiantil. Dentro de este nivel, el programa de Ingeniero Agrónomo Especialista se destaca como el más popular.
Se mantiene un crecimiento sostenido en  la matrícula de alumnos ha mostrado un incremento constante a lo largo de los años, con excepciones en 2008 y 2015. Esto sugiere una tendencia positiva en la captación de estudiantes, lo que puede ser indicativo de la calidad y relevancia de la oferta educativa.
Las proyecciones a 10 años indican un comportamiento ascendente en los ingresos, lo que es alentador. A pesar de fenómenos adversos, como la pandemia de COVID-19, la matrícula no se vio afectada de manera significativa lo que refuerza la capacidad de adaptación de la institución 
En resumen, los datos sugieren un panorama favorable para la institución en términos de matrícula y demanda educativa.

##6.-Recomendaciones para análisis futuros 
La baja representación en niveles de posgrado, como maestrías y doctorados, puede ser un área de oportunidad para la institución. Fomentar estos programas podría diversificar la oferta académica y atraer a más estudiantes interesados en formación avanzada.
Para incrementar el interés en los programas de nivel avanzado, la universidad podría diseñar campañas de promoción más intensivas y focalizadas, utilizando tanto medios tradicionales como digitales. Estas campañas podrían destacar los beneficios de obtener un grado de posgrado, como mayores oportunidades de investigación, desarrollo de habilidades especializadas, y el acceso a una red de profesionales y expertos en el área agrícola.

