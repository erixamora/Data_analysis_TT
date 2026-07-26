# GDP vs. Urban Traffic Correlation — Latin America

# Objective

This project investigates whether a country's level of economic development — measured as GDP per capita — correlates with the intensity of urban traffic congestion in its major cities. The assumption is that higher GDP enables greater investment in infrastructure and public transportation, which should reduce congestion; this analysis tests how well that assumption holds.

# Data

- Source: TomTom Traffic Index (traffic congestion metrics) and the OECD Cities database (economic indicators).
- Coverage: 2024 data for 15 cities across 7 Latin American countries: Belo Horizonte, Bogotá, Brasília, Buenos Aires, Curitiba, Fortaleza, Lima, Mexico City, Montevideo, Porto Alegre, Recife, Rio de Janeiro, Salvador, Santiago, and São Paulo.
- Key variables: `jams_delay` (average traffic delay time) and `city_gdp_capita` (city-level GDP estimate).

  # Methodology

  1. Load the TomTom traffic dataset and the OECD city-economy dataset.
  2. Standardize column names to snake_case and fix data types (dates, and numeric fields containing symbols such as `%`).
  3. Group and merge both datasets by city and year using an inner join on the key variables.
  4. Validate the merge and transformations at each step.
  5. Visualize the relationship between GDP per capita and traffic delay to identify overall trends and outliers.
 
  # Tools & Libraries

  Python, `pandas`, `numpy`, `seaborn`, `matplotlib`.

  # Key Findings

   - Cities in countries with higher GDP per capita tend to show lower traffic intensity, supporting the general hypothesis.
   - Mexico City stands out as an outlier that cannot be modeled the same way as the rest of the sample; the relevant question there is whether congestion growth is outpacing infrastructure expansion, which suggests a time-series analysis as a next step.
   - Bogotá shows the strongest correlation between high traffic congestion and low economic productivity, making it the top candidate city for priority investment in transportation infrastructure.
    
  # Limitations

   - The sample size (7 countries) is too small for robust statistical inference.
   - A single year of data does not allow distinguishing correlation from causation.
      
  # Repository Contents

   - `ladb_mobility_economy_project.ipynb` — main analysis notebook.
   - `ladb_mobility_economy_2024_clean.csv` — cleaned dataset used for the analysis.
   - `Executive_summary` — written summary of context, methodology, and findings.
        
  # How to Run

   1. Open `ladb_mobility_economy_project.ipynb` in Google Colab or a local Jupyter environment.
   2. Make sure the required CSV files are available at the path referenced in the notebook (or adjust the path).
   3. Install dependencies: `pip install pandas numpy seaborn matplotlib`.
   4. Run all cells in order from top to bottom.
          
            ---

  # Correlación entre el PIB y el tráfico urbano — América Latina

   # Objetivo

       Este proyecto investiga si el nivel de desarrollo económico de un país — medido como PIB per cápita — se correlaciona con la intensidad del tráfico urbano en sus principales ciudades. El supuesto es que un mayor PIB permite mayor inversión en infraestructura y transporte público, lo que debería reducir la congestión; este análisis pone a prueba qué tan bien se cumple ese supuesto.

  # Datos

      - Fuente: TomTom Traffic Index (métricas de congestión de tráfico) y la base de datos OECD Cities (indicadores económicos).
      - Cobertura: datos de 2024 para 15 ciudades en 7 países de América Latina: Belo Horizonte, Bogotá, Brasília, Buenos Aires, Curitiba, Fortaleza, Lima, Ciudad de México, Montevideo, Porto Alegre, Recife, Río de Janeiro, Salvador, Santiago y São Paulo.
      - Variables clave: `jams_delay` (tiempo promedio de retraso por tráfico) y `city_gdp_capita` (estimación del PIB de la ciudad).
             
  # Metodología

      1. Cargar el dataset de tráfico de TomTom y el dataset de economía de ciudades de la OCDE.
      2. Estandarizar los nombres de columnas a snake_case y corregir los tipos de datos (fechas, y campos numéricos con símbolos como `%`).
      3. Agrupar y combinar ambos datasets por ciudad y año mediante un inner join sobre las variables clave.
      4. Validar la combinación y las transformaciones en cada paso.
      5. Visualizar la relación entre el PIB per cápita y el retraso por tráfico para identificar tendencias generales y valores atípicos.
               
  # Herramientas y librerías

      Python, `pandas`, `numpy`, `seaborn`, `matplotlib`.

  # Hallazgos principales

      - Las ciudades en países con mayor PIB per cápita tienden a mostrar menor intensidad de tráfico, lo que respalda la hipótesis general.
      - Ciudad de México destaca como un valor atípico que no puede modelarse de la misma forma que el resto de la muestra; la pregunta relevante ahí es si el crecimiento de la congestión supera la expansión de la infraestructura, lo que sugiere un análisis de series de tiempo como siguiente paso.
      - Bogotá muestra la correlación más fuerte entre alta congestión de tráfico y baja productividad económica, siendo la ciudad candidata principal para inversión prioritaria en infraestructura de transporte.
                  
  # Limitaciones

       - El tamaño de la muestra (7 países) es insuficiente para una inferencia estadística robusta.
       - Un solo año de datos no permite distinguir correlación de causalidad.
                    
  # Contenido del repositorio

        - `ladb_mobility_economy_project.ipynb` — notebook principal del análisis.
        - `ladb_mobility_economy_2024_clean.csv` — dataset limpio utilizado para el análisis.
        - `Executive_summary` — resumen escrito del contexto, la metodología y los hallazgos.
                      
  # Cómo ejecutar

        1. Abre `ladb_mobility_economy_project.ipynb` en Google Colab o en un entorno Jupyter local.
        2. Asegúrate de que los archivos CSV requeridos estén disponibles en la ruta referenciada en el notebook (o ajusta la ruta).
        3. Instala las dependencias: `pip install pandas numpy seaborn matplotlib`.
        4. Ejecuta todas las celdas en orden de arriba hacia abajo.
