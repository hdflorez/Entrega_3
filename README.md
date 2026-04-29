# Entrega\_3

Análisis de Datos 2026-1 (190304018-1) | Entrega 3: Proyecto integral de Business Intelligence (BI)
Dataset: Video Game Sales, recuperado de: https://www.kaggle.com/datasets/gregorut/videogamesales

**Integrantes del equipo #8**:

* Mariana Villegas Ochoa
* Melisa Colorado Soto
* Jaider Santiago Villa David
* Hernán Darío Flórez Martínez

**Contenido del repositorio**:

* Notebook de Google Colab con enlace a la fuente de datos del dataset (VideoGameSales.ipynb)
* Dashboard en Power BI (Dashboard\_VideoGameSales.pbix)
* Archivo README.md (Con integrantes del equipo, Objetivo, Metodología, Resultados y Conclusiones)

**Objetivo**
La industria de los videojuegos ha atravesado una evolución notable en las últimas décadas: de máquinas de juego y cartuchos físicos a ecosistemas digitales de alcance global que generan ingresos anuales de miles de millones de dólares. En este marco, el presente proyecto se orienta a convertir datos históricos de ventas de videojuegos en inteligencia de negocio accionable, mediante la aplicación de técnicas de Business Intelligence (BI), análisis estadístico y herramientas de visualización interactiva.

De manera específica, el proyecto busca:

* Identificar los géneros y plataformas con mayor impacto comercial histórico.
* Determinar la distribución geográfica del mercado y sus implicaciones estratégicas.
* Validar estadísticamente hipótesis sobre el comportamiento del mercado.
* Construir indicadores clave (KPIs) que permitan monitorear el desempeño de la industria.
* Desarrollar un dashboard ejecutivo para la toma de decisiones informadas.

**Metodología**
El proyecto siguió una metodología estructurada de seis fases, alineada con los principios del ciclo de vida del dato en proyectos de BI:

* Fase 1: Comprensión del problema
Se analizó el dataset Video Game Sales de VGChartz, compuesto por 16.598 registros de videojuegos comercializados entre 1980 y 2020.    Se identificaron las variables disponibles, su naturaleza y los principales actores del mercado. A partir de este diagnóstico, se       formularon tres preguntas de negocio que orientaron el análisis:

  1. ¿Qué géneros generan mayores ventas y cómo varía esta tendencia por región?
  2. ¿Cómo ha evolucionado el volumen de ventas a lo largo del tiempo y qué plataformas dominaron cada era?
  3. ¿Qué tan concentrado está el mercado editorial?
* Fase 2: Formulación de hipótesis
H1: Los géneros Action y Sports, al ser los más producidos, generan ventas globales significativamente superiores al resto de géneros.
H2: Norteamérica es la región con mayores ventas, siendo su dominancia estadísticamente significativa frente a Europa y Japón.

  Cada hipótesis fue contrastada mediante pruebas no paramétricas: la prueba Mann-Whitney U para H1 y la prueba de Wilcoxon para H2,      dado que la distribución de ventas presenta una fuerte asimetría positiva, incompatible con supuestos paramétricos.

  * Fase 3: Preparación y modelado de datos
El proceso de preparación de datos comprendió una fase inicial de exploración para identificar tipos de datos, distribuciones y         posibles valores atípicos, seguida de la limpieza, donde se trataron valores nulos en Year (mediante imputación por mediana) y          Publisher (asignando la etiqueta “Unknown”), sin encontrarse registros duplicados. Posteriormente, se realizaron transformaciones       que incluyeron la creación de variables derivadas como top\_region, decade, is\_hit y success\_level, orientadas a enriquecer el           análisis. La validación aseguró la consistencia entre ventas regionales y globales, la coherencia en los rangos de años y la            ausencia de valores negativos. Como resultado, se obtuvo un dataset estructurado y listo para su análisis y visualización.
* Fase 4: Definición de KPIs
Se definieron cinco indicadores clave de desempeño (KPIs) para monitorear el comportamiento del mercado desde distintas dimensiones     estratégicas.

  Entre ellos están: Ventas globales totales (Buscando medir el tamaño total del mercado), Participación de mercado por género            (Identificar géneros dominantes en la industria), Participación regional de ventas (Definir mercados prioritarios), Tasa de éxito por   plataforma (Evaluar rentabilidad) e Índice de concentración HHI (Medir competitividad del mercado).

* Fase 5: Desarrollo del dashboard
El dashboard ejecutivo fue construido en Power BI e incorpora visualizaciones clave e interactivas con filtros dinámicos por año, género, plataforma y región.

* Fase 6: Análisis, validación y storytelling
  En esta fase se interpretaron los resultados obtenidos a lo largo del proyecto, se validaron formalmente las dos hipótesis mediante pruebas estadísticas y se     construyó una narrativa de negocio basada en evidencia. Ambas hipótesis fueron rechazadas con un p-value inferior a 0,0001, confirmando la ventaja comercial de   los géneros Action y Sports, y la dominancia sostenida de Norteamérica como mercado prioritario. A partir de estos hallazgos se formularon recomendaciones        estratégicas orientadas a decisiones de desarrollo, lanzamiento y posicionamiento en la industria, y se discutieron las limitaciones del dataset en términos de    cobertura temporal y ausencia del mercado digital.

**Resultados**
El análisis confirmó que los géneros Action y Sports lideran el mercado tanto en volumen de producción como en ventas acumuladas, concentrando el 34,4% del total global (1.722,84M y 1.309,24M de copias respectivamente). Esta ventaja fue validada estadísticamente mediante la prueba Mann-Whitney U (p < 0,0001), rechazando la hipótesis nula y confirmando que su superioridad comercial no es atribuible al azar. En el plano regional, Norteamérica concentra el 49,1% de las ventas globales (4.327,65M de copias), superando ampliamente a Europa (27,3%) y Japón (14,6%), diferencia confirmada por la prueba de Wilcoxon con p < 0,0001 en ambas comparaciones. El mercado alcanzó su pico histórico en 2008 con 678,90 millones de copias, impulsado por el auge de la Nintendo Wii y la madurez simultánea de múltiples plataformas. A nivel editorial, Nintendo lidera con 1.784,43M de copias, aunque el índice HHI de 800,90 indica que el mercado es competitivo y no presenta niveles de concentración que limiten la participación de nuevos actores.

**Conclusiones**
Los datos históricos de ventas de videojuegos permiten establecer patrones comerciales claros y estadísticamente respaldados. Apostar por géneros Action o Sports representa una ventaja real de rentabilidad frente al resto del mercado. Norteamérica es el territorio prioritario para cualquier estrategia de lanzamiento, dado que concentra prácticamente la mitad del mercado mundial de forma sostenida en el tiempo. El mercado editorial, pese al peso de grandes publishers, conserva niveles de competitividad que abren oportunidades para nuevos desarrolladores. No obstante, el análisis tiene limitaciones relevantes: el dataset excluye la distribución digital, el mercado móvil y está subrrepresentado después de 2016, por lo que sus conclusiones describen con precisión el mercado físico histórico, pero deben complementarse con fuentes actualizadas antes de aplicarse al contexto presente.
