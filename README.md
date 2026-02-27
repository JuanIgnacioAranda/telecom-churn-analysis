# telecom-churn-analysis
TELEXOM X1 Juan Aranda
# Análisis de Evasión de Clientes (Churn) - Telecom X

## Descripción del Proyecto
Telecom X se enfrenta a una alta tasa de cancelación de servicios por parte de sus clientes (Churn). En este proyecto, analicé la base de datos de la empresa para comprender los factores demográficos, técnicos y financieros que impulsan esta pérdida. A través del procesamiento de datos con Python, se extrajo información de alto valor que sirve como base para el diseño de estrategias de retención y futuros modelos predictivos.

## Objetivo
Identificar las principales causas de abandono de clientes mediante un Análisis Exploratorio de Datos (EDA) avanzado y multivariable, generando conclusiones accionables que permitan a los equipos de negocio tomar decisiones fundamentadas para reducir la fuga de capital.

## Desarrollo del Proyecto

1. Recolección y preparación de datos
Se importó la base de datos desde una API en formato JSON. Se realizó un proceso de transformación (aplanamiento de diccionarios anidados) y limpieza profunda, identificando y eliminando valores nulos que se encontraban ocultos como espacios en blanco en la facturación.

2. Ingeniería de características (Feature Engineering)
Para habilitar el análisis matemático avanzado, se transformaron las variables categóricas de texto (como "Yes" y "No") en variables numéricas binarias (1 y 0). Se ajustaron los tipos de datos de las variables continuas como el tiempo de permanencia y los cargos mensuales.

3. Análisis Exploratorio de Datos (EDA)
Se analizaron las distribuciones de variables individuales y se aplicaron cruces multivariables. Se utilizó una matriz de correlación (Heatmap) para identificar las relaciones matemáticas más fuertes con la variable de abandono, complementado con un análisis de impacto financiero bruto.

## Principales Hallazgos

Tras el análisis exhaustivo, se identificaron patrones críticos en el comportamiento de los usuarios:

- El impacto financiero del Churn: La fuga de clientes representa un riesgo financiero grave. La empresa pierde aproximadamente $139.130 dólares mensuales debido a cancelaciones, lo que equivale al 30.5% de sus ingresos mensuales potenciales.

- Riesgo en la etapa de Onboarding: La gran mayoría de las cancelaciones ocurren de forma prematura, específicamente durante los primeros 1 a 5 meses. Si el cliente supera este umbral temporal, su lealtad a largo plazo aumenta drásticamente.

- La trampa del plan mensual: El abandono está fuertemente concentrado en los contratos de renovación mensual (Month-to-month). Por el contrario, los contratos de uno o dos años actúan como una barrera de retención altamente efectiva.

- El falso problema de la Fibra Óptica: Inicialmente, el servicio de fibra óptica mostraba una tasa de abandono alarmante. Sin embargo, al segmentar los datos, se descubrió que el problema real es la falta de asistencia. Los clientes de fibra óptica sin soporte técnico contratado tienen una tasa de fuga del 49.4%, mientras que aquellos con soporte la reducen a más de la mitad (22.6%).

- Fricción en los pagos: El método de pago manual "Electronic check" presenta una tasa de abandono del 45.3%. Esto contrasta drásticamente con los métodos de pago automáticos (tarjeta de crédito o transferencia bancaria), cuya evasión ronda apenas el 15%.

- El efecto del Ancla Familiar: Se comprobó la existencia de altos "costos de cambio" logísticos en grupos familiares. Los clientes solitarios (sin pareja ni dependientes) cancelan a una tasa del 34.2%, mientras que los clientes con un núcleo familiar reducen su evasión al 14.3%.

## Recomendaciones Estratégicas

Para mitigar la pérdida del 30% de los ingresos, se sugiere transicionar hacia un modelo de retención proactivo mediante las siguientes acciones:

1. Estrategia de Onboarding: Implementar un plan de retención y seguimiento intensivo durante los primeros 5 meses del ciclo de vida del cliente.
2. Cross-selling técnico: Ofrecer el servicio de Soporte Técnico con un fuerte descuento (o de forma gratuita temporalmente) a todos los nuevos clientes de Fibra Óptica para evitar la frustración tecnológica temprana.
3. Automatización de pagos: Crear campañas para incentivar la migración de clientes que pagan manualmente hacia métodos de pago automáticos, ofreciendo pequeños descuentos en la factura mensual.
4. Fomento de lealtad: Diseñar "Planes Familiares" o promover la transición hacia contratos anuales, ya que estos perfiles han demostrado ser los más estables y rentables a largo plazo.

## Tecnologías Utilizadas
- Lenguaje: Python.
- Librerías principales: Pandas, Matplotlib, Seaborn.
- Entorno de desarrollo: GitHub Codespaces / Jupyter Notebooks.