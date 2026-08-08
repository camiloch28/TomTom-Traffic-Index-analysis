# TomTom Traffic Index Analysis: Movilidad, Economía y Contaminación en Ciudades del Mundo

📌 ¿De qué trata este proyecto?

Este proyecto analiza datos del TomTom Traffic Index, combinados con indicadores económicos y ambientales de distintas ciudades del mundo, para entender cómo se relacionan tres factores clave: la congestión del tráfico, la productividad económica (medida a través del PIB per cápita) y la calidad del aire (niveles de PM2.5).

La pregunta central que guía el análisis es simple, pero relevante para la toma de decisiones urbanas: ¿las ciudades con más tráfico y contaminación son también las que menos productividad económica muestran, o no hay una relación clara entre estas variables?

Para responderla, se trabajó con dos fuentes de datos independientes —una de tráfico y movilidad, y otra de indicadores económicos y ambientales— que se limpiaron, estandarizaron y combinaron en un solo dataset final, listo para análisis y visualización.

Este repositorio documenta todo el proceso: desde los datos crudos y desordenados, hasta un dataset limpio, unificado y con hallazgos claros sobre qué ciudades podrían ser prioritarias para inversión en infraestructura de transporte.

📂 ¿Qué contiene este repositorio?
TomTom_Traffic_Index_analysis.ipynb → El notebook principal, con todo el flujo de trabajo paso a paso: limpieza de datos, estandarización de columnas, conversión de formatos, filtrado por año, agregación por ciudad, unión de datasets y visualizaciones.
ladb_mobility_economy_2024_clean.csv → El dataset final, limpio y unificado, con las métricas de tráfico y economía por ciudad para el año 2024. Es el resultado directo del proceso documentado en el notebook.
Gráficos generados dentro del notebook:
📦 Boxplot de jams_delay — para observar la distribución de la congestión y detectar ciudades con valores atípicos.
📊 Histograma de city_gdp_capita — para entender cómo se distribuye la riqueza económica entre las ciudades analizadas.
📈 Gráfico de barras comparativo — para visualizar, ciudad por ciudad, la relación entre congestión y PIB per cápita.
▶️ ¿Cómo abrir el notebook en Google Colab?

No necesitas instalar nada en tu computador para revisar o ejecutar este análisis. Sigue estos pasos:

Entra a Google Colab.
Haz clic en Archivo > Abrir notebook.
Selecciona la pestaña GitHub.
Pega la URL de este repositorio (o busca el nombre de usuario/repositorio).
Selecciona el archivo TomTom_Traffic_Index_analysis.ipynb de la lista que aparece.
El notebook se abrirá directamente en tu entorno de Colab, listo para ejecutar.

💡 Alternativa rápida: si el repositorio es público, muchas veces basta con hacer clic en el botón "Open in Colab" que puedes agregar al inicio del notebook, o pegar directamente esta estructura de URL en tu navegador: https://colab.research.google.com/github/<usuario>/<repositorio>/blob/main/TomTom_Traffic_Index_analysis.ipynb

🔁 ¿Cómo reproducir este análisis?

El notebook está diseñado para ejecutarse de principio a fin, en orden, sin pasos manuales adicionales. Así es como debes hacerlo:

Abre el notebook (TomTom_Traffic_Index_analysis.ipynb) en Google Colab o Jupyter, siguiendo la sección anterior.
Ejecuta todas las celdas en orden, usando Kernel/Entorno de ejecución > Reiniciar y ejecutar todo. Esto es importante porque el análisis depende de que cada paso se construya sobre el anterior (limpieza → filtrado → agregación → unión → visualización).
La carga de los datasets ya está incluida dentro del notebook — no necesitas descargar ni subir archivos manualmente antes de empezar. Las primeras celdas se encargan de cargar los datos originales de tráfico (traffic) y economía (eco).
Sigue el flujo tal como está documentado en las celdas y comentarios, que corresponde a estas etapas:
Limpieza y estandarización de nombres de columnas.
Corrección de formatos numéricos y de fecha.
Extracción del año y filtrado de registros de 2024.
Cálculo de promedios de tráfico por ciudad.
Unión (merge) de los datasets de tráfico y economía.
Visualización de relaciones entre variables.
Exportación del dataset final limpio.
El resultado final (ladb_mobility_economy_2024_clean.csv) se genera automáticamente al ejecutar la última celda del notebook, y queda disponible para descarga o análisis posterior.

⚠️ Si al ejecutar alguna celda ves un error de tipo KeyError o NameError, casi siempre significa que se corrió una celda fuera de orden o que el entorno se reinició a mitad de camino. La solución es siempre la misma: reiniciar el entorno y ejecutar todas las celdas nuevamente desde el inicio.

📝 Nota

Este README fue redactado como parte del proyecto del curso de Análisis de Datos, basado en el notebook TomTom_Traffic_Index_analysis.ipynb. Los nombres de columnas y variables mencionados corresponden a los que se estandarizaron durante el proceso de limpieza (por ejemplo, jams_delay, city_gdp_capita, pm25, population), documentado paso a paso dentro del notebook.
