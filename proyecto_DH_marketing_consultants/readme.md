# 📊 Proyecto Power BI – Dashboard de Marketing

## 📝 Descripción general  
Este proyecto consistió en el diseño y desarrollo de un dashboard de marketing interactivo utilizando Power BI, con el objetivo de analizar el rendimiento de campañas y canales digitales.

---

## ⚙️ Proceso técnico

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

- `Dim_Campaña`: información sobre nombre, tipo, objetivo y canal de cada campaña publicitaria.  
- `Dim_Calendario`: tabla calendario generada con DAX, con columnas para día, mes, trimestre, año, y jerarquías temporales.  
- `Dim_Fuente`: origen de los datos de tráfico o anuncios (por ejemplo, Google, YouTube, Instagram).  
- `Dim_Conversiones`: contiene el nombre de la categoría de conversión y el nombre de la acción asociada.  
- `Dim_GrupoAnuncios`: segmentación de audiencias objetivo (clientes frecuentes, leads potenciales, interesados, remarketing).

#### 🔗 Relaciones y optimización

- Relaciones uno a muchos entre las dimensiones y la tabla de hechos.  
- Uso de claves sustitutas para conexión robusta.  
- Ocultamiento de columnas técnicas y desactivación de relaciones innecesarias.  
- Uso de jerarquías temporales para una experiencia de usuario mejorada.

Este diseño permitió una navegación fluida, filtros cruzados efectivos y análisis rápidos, precisos y escalables para el área de marketing.

---

### 🔄 ETL (Power Query)  
Conexión a diversas fuentes de datos (Excel, CSV).

### 🧹 Limpieza, transformación y normalización de datos

Durante la fase de preparación de datos en Power Query, se realizaron los siguientes pasos:

- Eliminación de registros duplicados y valores nulos.  
- Unificación de formatos de fecha, moneda y texto.  
- Normalización de columnas categóricas (campañas, canales, dispositivos).  
- Conversión de tipos de datos para compatibilidad con DAX.  
- Creación de columnas derivadas (año, mes, día de la semana, etc.).  
- Filtrado de datos irrelevantes o inconsistentes.  
- Integración de múltiples fuentes de datos con correspondencia por ID y fecha.

Estos pasos aseguraron un modelo limpio, robusto y confiable para el análisis posterior en Power BI.

---

### 🧮 Cálculos con DAX  
- Definición de medidas personalizadas para análisis dinámico y comparativo.

---

### 📊 Visualización  
- Desarrollo de un dashboard claro e interactivo enfocado en KPIs de marketing.  
- Incorporación de filtros por fecha, canal y campaña para segmentaciones dinámicas.

---

## 📈 Indicadores clave (KPIs) calculados

### Totales:
- Gasto total  
- Total de impresiones  
- Total de visualizaciones  
- Total de clics  
- Total de conversiones  
- Valor total de conversiones  

### Métricas de rendimiento:
- Gasto medio por campaña  
- ROI (Return on Investment)  
- CTR (Click Through Rate)  
- CR (Conversion Rate)  
- CPA (Costo por Adquisición)  
- CPM (Costo por mil impresiones)  
- CPC (Costo por clic)  
- CPV (Costo por visualización)
