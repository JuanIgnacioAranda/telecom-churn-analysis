# Análisis Estratégico de Evasión de Clientes (Churn) - Telecom X

Este proyecto realiza un diagnóstico profundo sobre la pérdida de usuarios en la compañía Telecom X. A través de un proceso de ciencia de datos, identifiqué no solo quiénes se van, sino los fallos operativos y psicológicos que disparan la cancelación del servicio.

<div align="center">
  ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
  ![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
  ![Matplotlib](https://img.shields.io/badge/Matplotlib-ffffff?style=for-the-badge&logo=python&logoColor=black)
  ![Seaborn](https://img.shields.io/badge/Seaborn-4C4C4C?style=for-the-badge&logo=python&logoColor=white)
</div>

---

## 🔹 Metodología de Trabajo
Para asegurar la calidad de las conclusiones, el análisis siguió este rigor técnico:
1.  **ETL y Limpieza:** Extracción desde API JSON, aplanamiento de datos anidados y corrección de errores de formato en cargos financieros.
2.  **Ingeniería de Datos:** Traducción total al español y creación de métricas personalizadas como el gasto diario y perfiles de hogar.
3.  **Análisis Multivariable:** Cruce de factores demográficos con métodos de pago y niveles de soporte técnico.

---

## 🔹 Hallazgos y Descubrimientos

### 1. El Impacto Financiero Real
La evasión no es solo un porcentaje; es una fuga de capital. El análisis determinó que la empresa pierde **$139,130 USD mensuales**, lo que representa el **30.5%** de los ingresos potenciales totales.

<div align="center">
  <img src="imagenes/distribucion_churn.png" alt="Distribución general" width="500px">
</div>

### 2. Factores de Riesgo Categóricos
Descubrí que el tipo de contrato es el mayor predictor de fuga. Los clientes con planes mensuales ("Month-to-month") no tienen barreras de salida. Además, identificamos que la **Fibra Óptica** parece ser un problema, pero los datos revelaron que la causa real es la **falta de soporte técnico** asociado a esa tecnología.

<div align="center">
  <img src="imagenes/evasion_categoricas.png" alt="Evasión por Categorías" width="800px">
</div>

### 3. El Factor Tiempo (Permanencia)
Al analizar las variables numéricas con diagramas de caja, la evidencia fue clara: los clientes que cancelan tienen una mediana de permanencia drásticamente menor. La mayoría de las bajas ocurren en los **primeros meses de servicio**, evidenciando un problema en la experiencia inicial del cliente.

<div align="center">
  <img src="imagenes/evasion_numericas.png" alt="Evasión Numérica" width="800px">
</div>

### 4. La Brecha Digital en Adultos Mayores
Este fue uno de los descubrimientos más impactantes: la tasa de abandono en **Adultos Mayores (+65)** llega al **45.4%** cuando se les impone la facturación digital. Forzar este canal en este segmento genera frustración y desconexión inmediata.

<div align="center">
  <img src="imagenes/evasion_brecha_digital.png" alt="Brecha Digital" width="800px">
</div>

### 5. Fricción en el Pago y el "Ancla" Familiar
Los datos nos contaron dos historias opuestas:
* **Fricción:** Pagar manualmente (Cheque Electrónico) eleva la fuga al **45.3%**. Al tener que realizar el trámite cada mes, el cliente cuestiona el gasto.
* **Retención:** Los clientes con familia (pareja e hijos) son mucho más leales (solo 14.3% de fuga) debido al alto costo de cambio que implica mudar un hogar completo a otro proveedor.

<div align="center">
  <img src="imagenes/evasion_oculta.png" alt="Factores de pago y familia" width="800px">
</div>

### 6. El "Escudo" de Servicios y Sensibilidad al Precio
Cruzando datos avanzados, encontramos el "Escudo de Retención": a mayor cantidad de servicios adicionales (seguridad, respaldo, soporte), la evasión cae casi a cero. Sin embargo, descubrimos que los clientes de **Gasto Premium** son más propensos a irse que los económicos si no perciben valor por su dinero.

<div align="center">
  <img src="imagenes/insights_avanzados.png" alt="Insights Avanzados" width="1000px">
</div>

### 7. Evidencia Matemática (Correlaciones)
Para validar todo lo anterior, el Mapa de Calor confirmó que la variable que más ayuda a retener es el tiempo de permanencia (`tenure`), mientras que los cargos mensuales altos son el principal motor de salida.

<div align="center">
  <img src="imagenes/mapa_calor.png" alt="Mapa de calor de correlaciones" width="600px">
</div>

---

## 🔹 Recomendaciones para el Negocio

1.  **Automatización Obligatoria de Pagos:** Ofrecer incentivos agresivos para que los usuarios de "Cheque Electrónico" migren a débito automático, eliminando la fricción mensual de pago.
2.  **Inclusión Analógica:** Desactivar la facturación digital por defecto para mayores de 65 años. El regreso al papel podría reducir su deserción en más de un 15%.
3.  **Soporte Técnico como Estrategia de Venta:** Incluir soporte técnico gratuito durante los primeros 3 meses en todas las ventas de Fibra Óptica para asegurar el *onboarding*.
4.  **Fidelización de Cartera Antigua:** Atender a los más de 1,000 clientes que llevan 2 años sin contrato formal, ofreciéndoles planes anuales con beneficios para evitar su fuga inesperada.

---
<div align="center">
  Análisis desarrollado por **Juan Ignacio Aranda**
</div>