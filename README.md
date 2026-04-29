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
El dashboard ejecutivo fue construido en Power BI e incorpora visualizaciones clave e interactivas con filtros dinámicos por año,       género, plataforma y región.



* Fase 6: Análisis, validación y storytelling
## 1) Contexto
* Se analizaron \*\*16,598 registros\*\* de videojuegos del dataset `vgsales.csv` para identificar patrones de ventas por año, género, plataforma, publisher y región.
* \## 2) ¿Qué pasó en el mercado?
* Las ventas globales alcanzan su mayor nivel entre \*\*2007 y 2010\*\*, con pico en \*\*2008\*\*, mostrando una etapa de alta adopción de consolas.
* \## 3) ¿Qué se vende más?
* Los géneros con mayor volumen histórico son:
* \- \*\*Action\*\* (\~1751 M)
* \- \*\*Sports\*\* (\~1331 M)
* \- \*\*Shooter\*\* (\~1037 M)
* Esto indica que estos géneros concentran la mayor demanda del mercado.
* \## 4) ¿En qué plataformas conviene enfocarse?
* Las plataformas con mayores ventas acumuladas son:
* \- \*\*PS2\*\* (\~1256 M)
* \- \*\*X360\*\* (\~980 M)
* \- \*\*PS3\*\* (\~958 M)
* \- \*\*Wii\*\* (\~927 M)
* Esto sugiere priorizar plataformas con mayor tracción comercial.
* \## 5) ¿Quién domina el mercado?
* En publishers, destacan:
* \- \*\*Nintendo\*\* (\~1787 M)
* \- \*\*Electronic Arts\*\* (\~1110 M)
* \- \*\*Activision\*\* (\~727 M)
* Estos actores funcionan como benchmark para estrategias de portafolio y posicionamiento.
* \## 6) ¿Cómo se comportan las regiones?
* La distribución regional muestra que:
* \- \*\*Norteamérica (NA)\*\* concentra la mayor parte de ventas.
* \- \*\*Europa (EU)\*\* ocupa el segundo lugar.
* \- \*\*Japón (JP)\*\* mantiene una participación relevante con dinámica propia.
* Conclusión regional: conviene una estrategia principal para NA/EU y adaptación específica para JP.
* \---
* \## Conclusiones
* 1\. El mercado histórico presenta su etapa más fuerte entre 2007-2010.
* 2\. Action, Sports y Shooter son los géneros más demandados.
* 3\. PS2, X360, PS3 y Wii concentran gran parte de las ventas históricas.
* 4\. NA y EU lideran comercialmente, con JP como mercado diferenciado.
* 5\. Nintendo, EA y Activision destacan como referencias competitivas.
* \---
* \## Decisiones basadas en datos
* 1\. \*\*Priorizar géneros líderes\*\* (Action/Sports/Shooter) en lanzamientos y campañas.
* 2\. \*\*Segmentar estrategia regional\*\*: foco comercial en NA y EU; localización y propuesta diferenciada para JP.
* 3\. \*\*Seleccionar plataformas de mayor alcance\*\* para maximizar volumen y retorno.
* 4\. \*\*Usar publishers líderes como benchmark\*\* en pricing, marketing y timing de lanzamiento.
* 5\. \*\*Monitorear evolución anual\*\* para alinear decisiones de inversión con ciclos del mercado.
* \---
* \## Limitaciones del análisis
* 1\. El dataset es \*\*histórico\*\*, no refleja condiciones de mercado en tiempo real.
* 2\. Existen datos faltantes en campos como `Year` y `Publisher`.
* 3\. No incluye variables de negocio clave (costos, márgenes, presupuesto de marketing, reseñas, retención).
* 4\. El análisis mide \*\*ventas agregadas\*\*, no rentabilidad ni desempeño post-lanzamiento.
* \---
* \## Cierre ejecutivo
* Con base en los datos, la mejor estrategia combina:
* \- enfoque en géneros de alta demanda,
* \- priorización de plataformas con mayor tracción,
* \- y ejecución regional diferenciada.
* Esto permite tomar decisiones más sólidas y orientadas a resultados medibles.
* 

