# 📡 TelecomX: Predicción de Evasión de Clientes (Churn Prediction)

Este proyecto utiliza técnicas de **Machine Learning** para identificar a los clientes con mayor probabilidad de abandonar los servicios de **TelecomX**. A través de un análisis exhaustivo y el entrenamiento de modelos predictivos, el objetivo es proponer estrategias de retención basadas en datos reales de comportamiento.

## 📋 Resumen del Proyecto
El abandono de clientes es un desafío crítico en las telecomunicaciones. Este análisis se centra en factores como el tipo de contrato, la antigüedad del cliente y los cargos mensuales para predecir la evasión.

### 🛠️ Tecnologías Utilizadas
* **Lenguaje:** Python 🐍
* **Librerías principales:** Pandas, Scikit-learn, Seaborn, Matplotlib, Imbalanced-learn (SMOTE).

## ⚙️ Pipeline de Procesamiento
Para asegurar la calidad de las predicciones, el flujo de trabajo incluyó:
1. **Limpieza de Datos:** Eliminación de variables redundantes como `diarias` y `cargos_totales` (evitando multicolinealidad).
2. **Preprocesamiento:** One-Hot Encoding para variables categóricas y `StandardScaler` para normalizar las magnitudes.
3. **Balanceo de Clases:** Aplicación de **SMOTE** para compensar el desbalance entre clientes leales y los que evaden.
4. **Modelado:** División 80/20 del dataset para entrenamiento y prueba.

## 📊 Comparativa de Modelos
Se evaluaron dos modelos principales, priorizando el **Recall** (capacidad de detectar fugas reales):

| Modelo | Recall (Evasión) | Accuracy |
| :--- | :---: | :---: |
| **Regresión Logística (Ganador)** | **0.69** | **0.78** |
| Random Forest (Optimizado) | 0.68 | 0.77 |



## 🔍 Hallazgos Clave
* **Factores de Riesgo:** El primer año de antigüedad (0-10 meses) y los contratos "mes a mes" son los mayores disparadores de fuga.
* **Impacto del Precio:** Los clientes que cancelan tienen cargos mensuales significativamente más altos (mediana de \$80).
* **Servicios Críticos:** La acumulación excesiva de servicios (`total_servicios`) aumenta la probabilidad de abandono según el modelo de regresión.



## 🚀 Estrategias de Retención Sugeridas
1. **Programas de Lealtad:** Incentivos especiales para clientes en sus primeros 12 meses.
2. **Incentivos Contractuales:** Promociones para migrar de contratos mensuales a anuales.
3. **Optimización de Cobro:** Automatizar pagos para reducir el riesgo asociado al uso de cheques electrónicos.

---
**Desarrollado por:** Giancarlos