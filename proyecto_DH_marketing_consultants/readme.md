# 📊 Proyecto Power BI – Dashboard de Marketing

## 📝 Descripción general
Este proyecto consistió en el diseño y desarrollo de un dashboard de marketing interactivo utilizando Power BI, con el objetivo de analizar el rendimiento de campañas y canales digitales.

## ⚙️ Proceso técnico

### 🔗 Fuente de datos y calidad
Los datos proporcionados provienen de una fuente de datos anonimizados que contiene información relacionada con la inversión en marketing realizada por una empresa durante un período de cuatro años. Tras la inspección, se determinó que los datos no contienen valores nulos ni vacíos, y son completamente coherentes con la descripción proporcionada en los nombres de las columnas. Los datos se presentaron en formato Excel y fueron transformados posteriormente en Power BI.

### 📐 Modelado de Datos
Se diseñó un modelo en estrella optimizado para análisis en Power BI, compuesto por una tabla de hechos central y cinco tablas dimensionales conectadas mediante claves ID. Este modelo permite análisis eficientes, segmentaciones dinámicas y visualizaciones interactivas.

#### 🔸 Tabla de hechos
Contiene los datos numéricos principales, como:

- Gasto
- Clics
- Impresiones
- Conversiones
- Métricas derivadas (CPC, CTR, ROI, entre otras)

Esta tabla actúa como núcleo del modelo para los cálculos en DAX y las visualizaciones.

#### 🔹 Tablas dimensionales

- **Dim_Campaña**: información sobre nombre, tipo, objetivo y canal de cada campaña publicitaria.
- **Dim_Calendario**: tabla calendario generada con DAX, con columnas para día, mes, trimestre, año, y jerarquías temporales.
- **Dim_Fuente**: origen de los datos de tráfico o anuncios (por ejemplo, Google, YouTube, Instagram).
- **Dim_Conversiones**: contiene el nombre de la categoría de conversión y el nombre de la acción asociada.
- **Dim_GrupoAnuncios**: segmentación de audiencias objetivo (clientes frecuentes, leads potenciales, interesados, remarketing).

#### 🔗 Relaciones y optimización

- Relaciones uno a muchos entre las dimensiones y la tabla de hechos.
- Uso de claves sustitutas para conexión robusta.
- Ocultamiento de columnas técnicas y desactivación de relaciones innecesarias.
- Uso de jerarquías temporales para una experiencia de usuario mejorada.

Este diseño permitió una navegación fluida, filtros cruzados efectivos y análisis rápidos, precisos y escalables para el área de marketing.

### 🔄 ETL (Power Query)
Conexión a diversas fuentes de datos (Excel, CSV).

### 🧹 Limpieza, transformación y normalización de datos
Durante la fase de preparación de datos en Power Query, se realizaron los siguientes pasos:

- Los datos fueron cargados desde un archivo Excel y posteriormente transformados en Power BI para su análisis.
- Se renombraron las columnas originales a nombres más cortos y representativos, facilitando su manejo y comprensión.
- Eliminación de registros duplicados y valores nulos.
- Unificación de formatos de fecha, moneda y texto.
- Normalización de columnas categóricas (campañas, canales, dispositivos).
- Conversión de tipos de datos para compatibilidad con DAX.
- Creación de columnas derivadas (año, mes, día de la semana, etc.).
- Filtrado de datos irrelevantes o inconsistentes.
- Integración de múltiples fuentes de datos con correspondencia por ID y fecha.

Estos pasos aseguraron un modelo limpio, robusto y confiable para el análisis posterior en Power BI.

### 🧮 Cálculos con DAX
- Definición de medidas personalizadas para análisis dinámico y comparativo.
- Cálculo de métricas financieras y de rendimiento como ROI, CTR, CR, CPC, CPA, CPV, CPM, entre otras.
- Análisis comparativo temporal (YTD, MoM, YoY) y segmentación por campañas, fuentes y dispositivos.
- Uso de funciones como **CALCULATE**, **FILTER**, **DIVIDE**, **RANKX**, **SELECTEDVALUE** para construir medidas robustas y dinámicas.

### 🧭 Interactividad y diseño del reporte
Se incorporaron elementos de navegación e interactividad avanzados para mejorar la experiencia del usuario:

- **Bookmarks (marcadores)**: vistas guardadas para mostrar datos del último mes de forma rápida.
- **Páginas dedicadas**: secciones específicas para análisis del último año, con filtros aplicados a nivel de página.
- **Botones de navegación**: enlaces entre páginas que facilitan la exploración del reporte.
- **Segmentadores sincronizados**: cuatro slicers sincronizados entre páginas para mantener el contexto del análisis.
- **Visualizaciones variadas**: uso de tarjetas, gráficos de barras, líneas, anillos, dispersión, mapas y otros tipos según el objetivo del análisis.

Estas funcionalidades permiten una exploración flexible, intuitiva y enfocada en los principales indicadores de rendimiento.

### 📈 Indicadores clave (KPIs) calculados

#### Totales:
- Gasto total
- Total de impresiones
- Total de visualizaciones
- Total de clics
- Total de conversiones
- Valor total de conversiones

#### Métricas de rendimiento:
- Gasto medio por campaña
- ROI (Return on Investment)
- CTR (Click Through Rate)
- CR (Conversion Rate)
- CPA (Costo por Adquisición)
- CPM (Costo por mil impresiones)
- CPC (Costo por clic)
- CPV (Costo por visualización)

## 📊 Análisis de los Datos

### 1. **Eficiencia de la campaña de marketing**
Los datos reflejan que la campaña de marketing actual ha sido bastante efectiva, logrando llegar a todos los tipos de audiencia de manera casi uniforme, utilizando diversas fuentes y canales de comunicación. Esta distribución equitativa en el alcance demuestra una estrategia bien implementada.

### 2. **Beneficio frente al coste**
El análisis de los costos y beneficios de las campañas revela que el beneficio de las campañas supera consistentemente el coste en todos los años analizados. Sin embargo, se observó un pico de intensa actividad en 2024, lo que resultó en un aumento significativo en las métricas de gasto (CPC, CPM, CPV, etc.).  
Por otro lado, el año 2022 mostró la menor actividad, lo que provocó un aumento en el gasto por clic, impresión y visualización, afectando negativamente el retorno de inversión de ese año y resultando en un beneficio menor para la empresa.





