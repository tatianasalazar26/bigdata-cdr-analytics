# 📊 Plataforma Analytics CDR para Infraestructura de Telecomunicaciones


## Proyecto Final - Big Data 2026

### Autor

**Angie Tatiana Salazar M.**

### Tecnología Principal

* Databricks
* Apache Spark
* Delta Lake
* Unity Catalog
* Python
* Scikit-Learn
* Prophet
* MLflow

---

# Arquitectura de la Solución

<img width="1536" height="1024" alt="arquitectura_medallion" src="https://github.com/user-attachments/assets/cfb95d03-0639-4e81-aa4f-0b329e41f68a" />


La solución implementa una arquitectura Medallion sobre Databricks para procesar registros CDR (Call Detail Records) de telecomunicaciones, transformando datos operativos en información estratégica para la toma de decisiones empresariales.

---

# Resumen Ejecutivo

Las empresas de telecomunicaciones generan diariamente grandes volúmenes de información relacionados con llamadas, duración, costos, proveedores, destinos y patrones de consumo.

El presente proyecto desarrolla una plataforma analítica empresarial capaz de procesar más de 200.000 registros de llamadas, permitiendo automatizar procesos operativos, detectar anomalías, optimizar la facturación y generar modelos predictivos para mejorar la toma de decisiones.

La solución utiliza Databricks como plataforma unificada de ingeniería de datos, analítica avanzada y ciencia de datos, implementando una arquitectura Medallion compuesta por capas Bronze, Silver y Gold.

---

# 1. Caso de Negocio

## Situación Actual

La organización provee infraestructura de telecomunicaciones para clientes corporativos y enfrenta los siguientes desafíos:

* Limitada visibilidad sobre el comportamiento del tráfico de llamadas.
* Procesos manuales de análisis y facturación.
* Dificultad para detectar anomalías y posibles fraudes.
* Baja capacidad para anticipar la demanda futura.
* Retrasos en la generación de reportes gerenciales.
* Dificultad para identificar oportunidades comerciales basadas en patrones de consumo.

## Objetivo General

Implementar una plataforma analítica basada en Big Data que permita transformar registros CDR en información estratégica para optimizar la operación y apoyar la toma de decisiones.

## Objetivos Específicos

* Procesar más de 200.000 registros de llamadas.
* Automatizar la consolidación y transformación de datos.
* Detectar anomalías mediante modelos de Machine Learning.
* Segmentar clientes según comportamiento de consumo.
* Generar predicciones de demanda.
* Construir indicadores para gestión ejecutiva.

---

# 2. Relación Beneficio / Coste

## Costos Actuales del Proceso Manual

| Recurso                      | Horas/Mes | Costo Mensual   |
| ---------------------------- | --------- | --------------- |
| Analistas de Datos           | 320       | $8.000          |
| Especialistas de Facturación | 160       | $4.800          |
| Ingenieros de Soporte        | 80        | $3.200          |
| **Total**                    |           | **$16.000/mes** |

## Inversión del Proyecto

| Concepto                    | Valor       |
| --------------------------- | ----------- |
| Infraestructura Databricks  | $15.000     |
| Desarrollo e Implementación | $8.000      |
| Capacitación                | $2.000      |
| **Total Inversión**         | **$25.000** |

## Beneficios Esperados

### Ahorros Operativos

* Automatización de procesos manuales.
* Reducción de errores de facturación.
* Optimización del uso de infraestructura.

### Nuevos Ingresos

* Identificación de oportunidades de upselling.
* Mejora en la experiencia del cliente.
* Incremento en la precisión de la facturación.

## Indicadores Financieros

| Indicador                  | Resultado |
| -------------------------- | --------- |
| Beneficio Anual Proyectado | $288.000  |
| Inversión Inicial          | $25.000   |
| ROI Estimado               | 1.052%    |
| Recuperación de Inversión  | 1 mes     |

---

# 3. Arquitectura Propuesta

La solución utiliza una arquitectura Medallion implementada sobre Databricks y Delta Lake.

## Flujo General

CDR Files → Auto Loader → Bronze → Silver → Gold → Machine Learning → Dashboards

## Componentes Tecnológicos

### Fuente de Datos

* Archivos CDR
* Formatos CSV
* Más de 203.000 registros procesados

### Ingesta

* Databricks Auto Loader
* Procesamiento automatizado
* Escalabilidad horizontal

### Almacenamiento

* Delta Lake
* ACID Transactions
* Versionamiento
* Data Governance

### Gobierno de Datos

* Unity Catalog
* Control de acceso
* Trazabilidad

---

# 4. Pipeline de Ingesta de Datos

## Estrategia Medallion

### Bronze Layer

Tabla:

```text
cdr_analytics.bronze.cdr_raw
```

Características:

* Datos originales.
* Sin transformaciones.
* Conservación histórica.
* Auditoría de ingestión.

Registros procesados:

```text
203.751 registros
```

---

### Silver Layer

Tabla:

```text
cdr_analytics.silver.cdr_cleaned
```

Transformaciones aplicadas:

* Limpieza de datos.
* Conversión de tipos.
* Eliminación de duplicados.
* Normalización de campos.
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

Total:

```text
6 tablas analíticas
```

---

# Resultados de Implementación

<img width="617" height="372" alt="Captura de pantalla 2026-06-12 211729" src="https://github.com/user-attachments/assets/88f16628-8c66-4d8c-9ee6-2136315090fe" />


La plataforma implementada logró:

* Procesamiento exitoso de más de 203 mil registros.
* Construcción de arquitectura Medallion.
* Automatización de transformaciones.
* Generación de tablas analíticas listas para negocio.

---

# 5. Ciencia de Datos

## Modelo 1 - Prophet

Objetivo:

Predecir la demanda futura de tráfico de llamadas.

Aplicación:

* Planeación de capacidad.
* Optimización de recursos.
* Gestión preventiva.

---

## Modelo 2 - K-Means

Objetivo:

Segmentar clientes según patrones de comportamiento.

Segmentos:

* Premium
* Standard
* Basic

Beneficio:

Personalización de estrategias comerciales.

---

## Modelo 3 - Isolation Forest

Objetivo:

Detectar anomalías y posibles eventos de fraude.

Resultado:

```text
33.734 anomalías detectadas
```

Beneficios:

* Reducción de pérdidas.
* Detección temprana de comportamientos atípicos.
* Mejora del control operativo.

---

# 6. Visualización y Consumo

La información procesada puede ser consumida mediante:

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

---

# Resultados Obtenidos

| Indicador               | Resultado |
| ----------------------- | --------- |
| Registros Procesados    | 203.751   |
| Registros Curados       | 203.733   |
| Tablas Gold             | 6         |
| Modelos ML              | 3         |
| Anomalías Detectadas    | 33.734    |
| Horizonte de Predicción | 30 días   |

---

# Conclusiones

La implementación de la Plataforma Analytics CDR permitió construir una solución integral de Big Data basada en Databricks para el procesamiento masivo de registros de telecomunicaciones.

La arquitectura Medallion garantizó calidad, trazabilidad y escalabilidad en el procesamiento de datos, mientras que los modelos de Machine Learning aportaron capacidades avanzadas de segmentación, predicción y detección de anomalías.

Los resultados obtenidos demuestran el potencial de las tecnologías Big Data para transformar datos operativos en información estratégica, mejorando la eficiencia operativa, la capacidad de análisis y la toma de decisiones basada en datos.

