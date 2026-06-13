# Plataforma Analytics CDR - Proyecto Final Big Data
<img width="1536" height="1024" alt="arquitectura_medallion" src="https://github.com/user-attachments/assets/e9dee650-2e7e-4ec0-80f1-5f261b130830" />

## Descripción

Este proyecto implementa una plataforma de analítica de datos para registros CDR (Call Detail Records) de telecomunicaciones utilizando Databricks y arquitectura Medallion.

La solución permite procesar más de 200.000 registros de llamadas, automatizar análisis operativos, detectar anomalías, optimizar procesos de facturación y generar información para la toma de decisiones.

---

## Caso de Negocio

Las empresas de telecomunicaciones generan grandes volúmenes de información diariamente. La explotación manual de estos datos genera:

* Baja visibilidad operativa.
* Dificultad para detectar fraude.
* Procesos de facturación lentos.
* Pérdida de oportunidades comerciales.
* Escasa capacidad de predicción de demanda.

La solución propuesta transforma los datos CDR en información accionable mediante una plataforma analítica escalable.

---

## Arquitectura

Se implementó una arquitectura Medallion utilizando Databricks y Delta Lake.

### Bronze

Datos crudos provenientes de archivos CDR.

### Silver

Datos limpios, normalizados y enriquecidos.

### Gold

Tablas analíticas para consumo de negocio:

* Métricas por cliente.
* Performance de proveedores.
* Detección de anomalías.
* Resumen de facturación.
* Segmentación de clientes.
* Predicción de demanda.

---

## Ciencia de Datos

Se implementaron los siguientes modelos:

### Prophet

Predicción de demanda futura.

### K-Means

Segmentación de clientes en diferentes grupos de consumo.

### Isolation Forest

Detección automática de anomalías y posibles eventos de fraude.

---

## Resultados

* 203.751 registros procesados.
* Pipeline automatizado Bronze-Silver-Gold.
* 6 tablas analíticas generadas.
* Detección automática de anomalías.
* Predicción de demanda a 30 días.
* Segmentación de clientes para estrategias comerciales.

---

## Tecnologías

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

## Autor

Angie Tatiana Salazar M.

Proyecto Final - Big Data 2026.
