# 📊 Plataforma Analytics CDR para Infraestructura de Telecomunicaciones

## Proyecto Final - Big Data 2026

### Autor

**Angie Tatiana Salazar M.**

### Tecnologías Utilizadas

* Databricks
* Apache Spark
* Delta Lake
* Unity Catalog
* Python
* Pandas
* Scikit-Learn
* Prophet
* MLflow

---

# Arquitectura de la Solución

<img width="1536" height="1024" alt="arquitectura_medallion" src="https://github.com/user-attachments/assets/564de503-204e-44dd-8b18-a59cd3264430" />


La solución implementa una arquitectura Medallion sobre Databricks para el procesamiento de registros CDR (Call Detail Records), permitiendo transformar grandes volúmenes de datos operativos en información estratégica para la toma de decisiones empresariales.

---

# Resumen 

Las empresas de telecomunicaciones generan diariamente grandes volúmenes de información asociados al tráfico de llamadas, duración, costos, proveedores, destinos y patrones de consumo.

Este proyecto desarrolla una plataforma analítica empresarial capaz de procesar más de 200.000 registros CDR mediante una arquitectura moderna de Big Data implementada sobre Databricks, integrando procesos de ingeniería de datos, analítica avanzada y ciencia de datos.

La solución permite automatizar la transformación de datos, optimizar procesos de facturación, detectar anomalías, segmentar clientes y generar predicciones de demanda para apoyar la toma de decisiones basada en datos.

---

# 1. Caso de Negocio

## Situación Actual

La organización presta servicios de infraestructura de telecomunicaciones para clientes corporativos y enfrenta los siguientes desafíos:

* Limitada visibilidad sobre el comportamiento del tráfico de llamadas.
* Procesos manuales de consolidación y análisis de información.
* Dificultad para detectar anomalías y posibles eventos de fraude.
* Baja capacidad para anticipar comportamientos futuros de demanda.
* Retrasos en la generación de reportes ejecutivos.
* Limitado aprovechamiento comercial de los datos generados por la operación.

## Objetivo General

Implementar una plataforma analítica basada en tecnologías Big Data que permita transformar registros CDR en información estratégica para optimizar la operación y fortalecer la toma de decisiones.

## Objetivos Específicos

* Procesar más de 200.000 registros de llamadas.
* Automatizar la consolidación y transformación de información.
* Detectar anomalías mediante algoritmos de Machine Learning.
* Segmentar clientes según patrones de comportamiento.
* Generar modelos predictivos de demanda.
* Construir indicadores ejecutivos para la gestión empresarial.

---

# 2. Relación Beneficio / Coste

## Costos Actuales del Proceso Manual

| Recurso                      | Horas/Mes |   Costo Mensual |
| ---------------------------- | --------: | --------------: |
| Analistas de Datos           |       320 |          $8.000 |
| Especialistas de Facturación |       160 |          $4.800 |
| Ingenieros de Soporte        |        80 |          $3.200 |
| **Total**                    |           | **$16.000/mes** |

## Inversión del Proyecto

| Concepto                    |       Valor |
| --------------------------- | ----------: |
| Infraestructura Databricks  |     $15.000 |
| Desarrollo e Implementación |      $8.000 |
| Capacitación                |      $2.000 |
| **Inversión Total**         | **$25.000** |

## Beneficios Esperados

### Ahorros Operativos

* Automatización de procesos manuales.
* Reducción de errores de facturación.
* Optimización del uso de infraestructura tecnológica.
* Disminución de tiempos de análisis.

### Incremento de Ingresos

* Identificación de oportunidades de upselling.
* Mejora en la experiencia del cliente.
* Mayor precisión en la facturación.
* Incremento en la retención de clientes.

## Indicadores Financieros

| Indicador                    | Resultado |
| ---------------------------- | --------: |
| Beneficio Anual Proyectado   |  $288.000 |
| Inversión Inicial            |   $25.000 |
| ROI Estimado                 |    1.052% |
| Recuperación de la Inversión |     1 mes |

---

# 3. Arquitectura Propuesta

La solución utiliza una arquitectura Medallion implementada sobre Databricks y Delta Lake.

## Flujo General

```text
CDR Files
    ↓
Auto Loader
    ↓
Bronze Layer
    ↓
Silver Layer
    ↓
Gold Layer
    ↓
Machine Learning
    ↓
Dashboards y Consumo
```

## Componentes Tecnológicos

### Fuente de Datos

* Archivos CDR.
* Formato CSV.
* Más de 203.000 registros procesados.

### Ingesta

* Databricks Auto Loader.
* Procesamiento automatizado.
* Escalabilidad horizontal.

### Almacenamiento

* Delta Lake.
* Transacciones ACID.
* Versionamiento.
* Data Governance.

### Gobierno de Datos

* Unity Catalog.
* Control de acceso.
* Trazabilidad.
* Gestión centralizada de activos de información.

---

# 4. Pipeline de Ingesta de Datos

## Estrategia Medallion

### Bronze Layer

Tabla principal:

```text
cdr_analytics.bronze.cdr_raw
```

Características:

* Datos originales sin transformación.
* Conservación histórica.
* Auditoría de ingestión.
* Trazabilidad completa.

Registros procesados:

```text
203.751 registros
```

---

### Silver Layer

Tabla principal:

```text
cdr_analytics.silver.cdr_cleaned
```

Transformaciones aplicadas:

* Limpieza de datos.
* Conversión de tipos.
* Eliminación de registros duplicados.
* Normalización de atributos.
* Enriquecimiento de información.

Registros procesados:

```text
203.733 registros
```

---

### Gold Layer

Tablas analíticas generadas:

```text
cdr_customer_metrics
cdr_vendor_performance
cdr_fraud_detection
cdr_billing_summary
cdr_customer_segments
cdr_ml_predictions
```

Resultado:

```text
6 tablas analíticas para consumo empresarial
```

---

# Resultados de Implementación

![Resultados Plataforma](docs/pipeline_completo.png)

La implementación permitió:

* Procesar exitosamente más de 203 mil registros CDR.
* Construir una arquitectura Medallion completa.
* Automatizar procesos de transformación de datos.
* Generar activos analíticos para consumo de negocio.
* Integrar modelos de Machine Learning dentro del flujo de datos.

---

# 5. Ciencia de Datos

## Modelo Prophet

Objetivo:

Predecir la demanda futura de tráfico de llamadas.

Aplicaciones:

* Planeación de capacidad.
* Optimización de recursos.
* Gestión preventiva de infraestructura.

---

## Modelo K-Means

Objetivo:

Segmentar clientes según patrones de comportamiento.

Segmentos identificados:

* Premium.
* Standard.
* Basic.

Beneficio:

Facilitar estrategias diferenciadas de atención y comercialización.

---

## Modelo Isolation Forest

Objetivo:

Detectar anomalías y posibles eventos de fraude.

Resultado obtenido:

```text
33.734 anomalías detectadas
```

Beneficios:

* Reducción de pérdidas operativas.
* Identificación temprana de comportamientos atípicos.
* Fortalecimiento de controles internos.

---

# 6. Visualización y Consumo

La información generada puede ser consumida mediante:

* Databricks SQL.
* Dashboards ejecutivos.
* Power BI.
* Tableau.
* APIs y Endpoints.
* Sistemas corporativos.

## Indicadores Disponibles

* Tráfico total de llamadas.
* Costos por proveedor.
* Clientes de mayor consumo.
* Tendencias históricas.
* Predicciones de demanda.
* Alertas de anomalías.
* Métricas operativas y financieras.

---

# Resultados Obtenidos

<img width="617" height="372" alt="Captura de pantalla 2026-06-12 211729" src="https://github.com/user-attachments/assets/bb9df010-041b-4610-896d-127c0b8d53fe" />


---

# Evidencias de Ejecución

Las evidencias completas del proyecto se encuentran disponibles dentro de este repositorio.

### Notebook Fuente

**Plataforma_Analytics_CDR.ipynb**

Contiene el desarrollo integral de la solución:

* Caso de negocio.
* Relación beneficio/coste.
* Arquitectura propuesta.
* Pipeline Medallion.
* Procesamiento de datos.
* Consultas analíticas.
* Implementación de modelos de Machine Learning.

### Evidencia Ejecutada

**Plataforma_Analytics_CDR_Ejecucion_Completa.html**

Contiene la ejecución completa del proyecto en Databricks, incluyendo:

* Resultados de procesamiento.
* Evidencias de las capas Bronze, Silver y Gold.
* Tablas generadas.
* Métricas calculadas.
* Resultados de Prophet.
* Resultados de K-Means.
* Resultados de Isolation Forest.
* Validaciones y salidas generadas por la plataforma.

La versión HTML constituye la evidencia integral de ejecución y permite revisar los resultados sin requerir acceso a Databricks.

---

# Conclusiones

La implementación de la Plataforma Analytics CDR permitió construir una solución integral de Big Data basada en Databricks para el procesamiento masivo de registros de telecomunicaciones.

La arquitectura Medallion garantizó calidad, trazabilidad, gobernanza y escalabilidad en el tratamiento de la información, mientras que los modelos de Machine Learning aportaron capacidades avanzadas de segmentación, predicción y detección de anomalías.

Los resultados obtenidos demuestran el potencial de las tecnologías Big Data para transformar datos operativos en información estratégica, optimizando procesos, fortaleciendo la toma de decisiones y generando valor a partir de los activos de información de la organización.
