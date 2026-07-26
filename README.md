# ConnectaTel Customer Behavior and Usage Analysis – Sprint 7

Este repositorio contiene el análisis realizado durante el Sprint 7 para auditar la calidad de los datos de consumo, identificar perfiles de clientes y evaluar el uso de infraestructura de la compañía ConnectaTel. El proyecto trabaja con datos de 4,000 usuarios y 40,000 registros transaccionales de uso, los cuales se limpian, combinan y analizan para diseñar estrategias de fidelización, optimización de planes y planes tarifarios comerciales.

## Contenido del repositorio

* `S7 Version-Estudiante-Project-ConnectaTel.ipynb`: Notebook principal que incluye la carga de datos, detección de valores sentinel (-999, "?"), análisis de nulos condicionales (MAR) por tipo de servicio, corrección de fechas futuras (2026), agregación de consumo por usuario, segmentación demográfica/de uso y visualizaciones analíticas de distribución.

## Cómo abrir el notebook en Google Colab

Haz clic en el siguiente botón:

Haz clic en el siguiente botón:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1TvS8kGSfeLpiM5eM33fKQvNeBfYprN-h?usp=sharing)

O también puedes usar este enlace directo: [Abrir en Google Colab](https://colab.research.google.com/drive/1TvS8kGSfeLpiM5eM33fKQvNeBfYprN-h?usp=sharing)

## Objetivo del análisis

* **Auditar la calidad de los datos:** Construir un pipeline de limpieza reproducible para neutralizar valores sentinel numéricos (`age = -999`) y categóricos (`city = "?"`), además de corregir anomalías cronológicas de fechas futuras del año 2026.
* **Evaluar nulos estructurales (MAR):** Verificar matemáticamente que la ausencia de datos en `duration` (55.19% nulos) y `length` (44.74% nulos) está condicionada por la variable `type`, correspondientes de forma correcta a mensajes de texto y llamadas.
* **Segmentar la base de clientes:** Clasificar a los usuarios mediante funciones lógicas bajo enfoques demográficos (`grupo_edad`: Joven, Adulto, Adulto Mayor) y comportamientos transaccionales (`grupo_uso`: Bajo, Medio, Alto uso) para identificar el núcleo del negocio.
