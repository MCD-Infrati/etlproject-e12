# Implementación de un Proceso ETL con Azure Data Factory para Análisis de Datos Inmobiliarios

## Resumen del Proyecto

Este repositorio contiene los artefactos y la documentación de un proyecto de ingeniería de datos enfocado en la implementación de un proceso de **Extracción, Transformación y Carga (ETL)**. El objetivo principal fue consolidar datos heterogéneos sobre propiedades inmobiliarias de la ciudad de Ames (Iowa, EE. UU.) para facilitar su posterior análisis.

El pipeline orquestado en **Azure Data Factory** integra datos desde tres fuentes distintas:
1.  Archivos planos **CSV**.
2.  Una base de datos relacional **PostgreSQL**.
3.  Una base de datos NoSQL **MongoDB**.

El resultado final es un único archivo CSV (`salida.csv`), limpio, unificado y estructurado, listo para ser consumido por herramientas de análisis y modelos de Machine Learning.

**Institución:** Universidad Icesi  
**Maestría:** Ciencia de Datos  
**Curso:** Infraestructura de TI

## Arquitectura de la Solución

El proceso ETL se diseñó y ejecutó completamente en la nube de Microsoft Azure, siguiendo el siguiente flujo de trabajo:

1.  **Orquestación:** Se utiliza **Azure Data Factory (ADF)** para controlar y ejecutar el pipeline de datos de extremo a extremo.
2.  **Almacenamiento (Staging y Destino):** **Azure Blob Storage** funciona como área de almacenamiento intermedio para los datos extraídos (staging) y como destino final para el dataset procesado.
3.  **Transformación:** La lógica de transformación, que incluye joins entre las distintas fuentes, limpieza de valores nulos, selección y renombrado de columnas, se implementó de manera visual y escalable utilizando **Mapping Data Flows** dentro de ADF.
