# 📡 Análisis de Evasión de Clientes (Churn) - TelecomX

Este proyecto aplica técnicas de **Ciencia de Datos y ETL** para identificar patrones de abandono en una empresa de telecomunicaciones. El objetivo es proporcionar *insights* accionables que permitan reducir la tasa de rotación y mejorar la retención de clientes de alto valor.

## 🎯 Objetivo del Proyecto
Analizar un conjunto de datos complejo (JSON anidado) para predecir el comportamiento de los clientes, identificando las variables financieras y de servicio que más influyen en la decisión de cancelar el contrato.

## 🛠️ Tecnologías Utilizadas
* **Python 3.x**
* **Pandas:** Para manipulación y limpieza de datos (ETL).
* **NumPy:** Procesamiento matemático y manejo de valores nulos (`NaN`).
* **Seaborn & Matplotlib:** Visualización de datos y análisis exploratorio (EDA).
* **Regex (Expresiones Regulares):** Limpieza de strings y detección de espacios vacíos.

## 📉 Hallazgos Principales (Insights)
Tras el análisis exploratorio de los datos, se identificaron los siguientes puntos críticos:
* **Tasa de Evasión:** El **26.4%** de la base de clientes ha cancelado el servicio.
* **El "Punto de Quiebre":** La mayor probabilidad de fuga ocurre durante los **primeros 12 meses** de antigüedad.
* **Sensibilidad al Precio:** Los clientes que cancelan pagan, en promedio, un **20% más** mensualmente que los clientes retenidos.
* **Fidelización por Contrato:** Los contratos mensuales presentan una volatilidad mucho mayor en comparación con los contratos anuales o bianuales.



## 🏗️ Estructura del Proceso (Pipeline)
1. **Extracción y Carga:** Procesamiento de archivos JSON mediante `json_normalize`.
2. **Limpieza (Data Wrangling):** - Conversión de tipos de datos (Strings a Floats).
   - Identificación y eliminación de 224 registros con espacios en blanco mediante Regex.
   - Traducción y estandarización de columnas al español.
3. **Ingeniería de Características:** Creación de la métrica `cuentas_diarias` para un análisis más granular.
4. **Análisis Exploratorio (EDA):** Visualización de distribuciones categóricas y numéricas mediante Boxplots, Countplots y mapas de calor (Heatmaps).

## 🚀 Cómo Ejecutar el Proyecto
1. Clona este repositorio.
2. Asegúrate de tener instaladas las dependencias: `pip install pandas seaborn matplotlib numpy`.
3. Ejecuta el notebook principal `Telecom_Churn_Analysis.ipynb`.

---
**Autor:** Giancarlos
**Especialidad:** Data Science & Machine Learning