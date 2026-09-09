# 📊 Análisis Estadístico y Segmentación de Clientes — ConnectaTel

## 📌 Objetivo del Proyecto
El propósito de este proyecto es realizar un análisis exploratorio y estadístico integral de la base de usuarios de la empresa de telecomunicaciones *ConnectaTel*. A través del tratamiento de datos, cálculo de rangos intercuartílicos (IQR) y la segmentación por comportamiento de uso y variables demográficas, se identificaron patrones clave para optimizar la oferta comercial y mejorar la rentabilidad de la red.

---

## 🛠️ Datasets Utilizados
El análisis se fundamenta en dos conjuntos de datos principales:

* *user_profile (users):* Información demográfica y contractual de los clientes.
  * user_id: Identificador único de usuario.
  * age: Edad del usuario (18 - 80 años).
  * city: Ciudad de residencia.
  * plan: Plan contratado (Básico o Premium).
  * churn_date: Fecha de cancelación del servicio (88.35% nulos correspondiente a usuarios activos).
* *usage:* Registros de consumo de la red.
  * call_count: Cantidad de llamadas realizadas.
  * call_duration: Duración acumulada de llamadas en minutos.
  * message_count: Cantidad de mensajes de texto enviados.

---

## 🔄 Etapas del Análisis
1. *Limpieza y Preparación de Datos:*
   * Diagnóstico de valores ausentes (churn_date, city, duration, length).
   * Verificación y eliminación de registros duplicados.
   * Tratamiento de tipos de datos y consolidación en una estructura analítica única.

2. *Análisis Exploratorio e Identificación de Outliers:*
   * Visualización de distribuciones mediante gráficos de caja (Boxplots).
   * Cálculo estadístico del límite superior $IQR = Q3 + 1.5 \times (Q3 - Q1)$.
   * Evaluación de valores extremos en duración de llamadas (límite IQR: 61.87 min, máx: 155.69 min) y mensajes (límite IQR: 11.5, máx: 17.0).

3. *Segmentación de Clientes:*
   * *Por Uso:* Categorización en Bajo uso, Uso medio y Alto uso según volumen de llamadas y mensajes.
   * *Por Edad:* Clasificación etaria en Joven (<30 años), Adulto (30-59 años) y Adulto Mayor (>=60 años).

4. *Síntesis Ejecutiva y Recomendaciones:*
   * Formulación de estrategias comerciales basadas en el comportamiento del consumidor y patrones de consumo masivo (heavy users).

---

## 🚀 Guía de Reproducción

### Requisitos Previos
* Python 3.8+
* Librerías requeridas: pandas, numpy, matplotlib, seaborn

  ### Pasos para Ejecutar
1. *Clonar el repositorio:*
   git clone https://github.com/leonardomolanocuervo-sketch/Telecom_analysis.git
2. *Abrir el archivo:*
   Abrir S7 Version-Estudiante-Project-ConnectaTel.ipynb en Jupyter Notebook o Google Colab.
3. *Ejecutar el análisis:*
   Correr todas las celdas en orden secuencial (Shift + Enter).
