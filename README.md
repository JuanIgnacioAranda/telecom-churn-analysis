<div align="center">
  <h1>Análisis Estratégico de Retención de Clientes (Churn)</h1>
  <h3>Telecom X | Proyecto de Ciencia de Datos Aplicada</h3>
  
  [![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)]()
  [![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)]()
  [![Matplotlib](https://img.shields.io/badge/Matplotlib-ffffff?style=for-the-badge&logo=python&logoColor=black)]()
  [![Seaborn](https://img.shields.io/badge/Seaborn-4C4C4C?style=for-the-badge&logo=python&logoColor=white)]()
</div>

---

## Resumen Ejecutivo

Telecom X enfrenta un desafío crítico de negocio: una alta tasa de atrición (Churn) que está erosionando significativamente su rentabilidad. Este proyecto aplica técnicas de Ciencia de Datos y Análisis Multivariable sobre la base de datos de clientes para identificar los factores subyacentes del abandono.

> **Impacto Financiero Cuantificado:** La fuga de clientes representa un riesgo financiero de **$139,130.85 USD mensuales**, lo que equivale a una pérdida del **30.5%** de los ingresos recurrentes potenciales de la compañía.

---

## Metodología y Desarrollo Técnico

El flujo de trabajo se desarrolló bajo un estricto rigor analítico, abarcando las siguientes fases:

1. **Extracción y Transformación (ETL):** Consumo de datos desde API (formato JSON). Aplanamiento de estructuras anidadas mediante diccionarios multinivel y limpieza de anomalías.
2. **Feature Engineering:** Binarización de variables categóricas (mapeo escalar 1-0) para viabilizar el cálculo de matrices de correlación y la estandarización de tipos de datos continuos.
3. **Análisis Exploratorio de Datos (EDA):** Evaluación de distribuciones univariantes, cruces bivariantes y mapas de calor para la detección de multicolinealidad.

---

## Hallazgos Basados en Datos

### 1. Panorama de Atrición General
Si bien la mayoría de la base de usuarios se mantiene activa, existe una proporción de cancelaciones lo suficientemente grande como para desestabilizar el modelo de ingresos.

<div align="center">
  <img src="imagenes/distribucion_churn.png" alt="Distribución general" width="600px">
  <br>
  <i>Figura 1: Distribución de evasión de clientes.</i>
</div>

### 2. La Barrera del Compromiso Contractual
Los clientes retenidos bajo esquemas de renovación mensual ("Month-to-month") presentan un riesgo de fuga crítico en comparación con los esquemas anuales o bianuales.

<div align="center">
  <img src="imagenes/evasion_contrato.png" alt="Evasión por tipo de contrato" width="700px">
  <br>
  <i>Figura 2: Proporción de retención vs. cancelación segmentada por contrato.</i>
</div>

### 3. Matriz de Correlaciones y Factores Latentes
El mapa de calor cuantifica las relaciones matemáticas entre variables. La permanencia correlaciona negativamente con el abandono (-0.35), actuando como el principal factor protector.

<div align="center">
  <img src="imagenes/mapa_calor.png" alt="Mapa de calor de correlaciones" width="750px">
  <br>
  <i>Figura 3: Matriz de correlación térmica evaluando la interacción entre variables.</i>
</div>

### 4. Riesgo Temporal y La Paradoja de la Fibra Óptica
Al analizar variables combinadas descubrimos dos factores críticos:
- **El Valle de la Muerte Temporal:** Existe una concentración crítica de cancelaciones durante los primeros **1 a 5 meses** de servicio (gráfico derecho).
- **El problema del Internet:** La fibra óptica presenta la mayor cantidad de bajas netas (gráfico izquierdo). El análisis profundo reveló que los clientes de fibra óptica sin soporte presentan una tasa de fuga del **49.4%**, mientras que aquellos con soporte la reducen a **22.6%**.

<div align="center">
  <img src="imagenes/internet_y_permanencia.png" alt="Servicio y Permanencia" width="800px">
  <br>
  <i>Figura 4: Evasión cruzada por tipo de servicio de internet y meses de permanencia acumulados.</i>
</div>

---

## Recomendaciones Estratégicas y Plan de Acción

1. **Reingeniería del proceso de Onboarding:** Establecer un protocolo de seguimiento y satisfacción intensivo durante los primeros 180 días.
2. **Cross-Selling Orientado a Retención:** Subsidiar u ofrecer agresivamente el servicio de Soporte Técnico a nuevas altas de Fibra Óptica para mitigar la frustración tecnológica temprana.
3. **Incentivos para Automatización:** Implementar reducciones marginales en la tarifa para forzar la migración de usuarios que pagan mediante cheques electrónicos hacia esquemas de débito automático.
4. **Arquitectura de Planes Agrupados:** Fomentar el anclaje familiar mediante la creación de planes que agrupen múltiples líneas.

---
<div align="center">
  <i>Análisis desarrollado por <b>Juan Ignacio Aranda</b></i>
</div>