# Framework Adaptativo para la Medición de Brechas Salariales y Distribución del Ingreso

Este repositorio contiene el prototipo funcional del Framework Adaptativo diseñado para la detección, análisis y visualización de brechas salariales y desigualdad en la distribución del ingreso, utilizando como caso de estudio datos sociolaborales estructurados. 

El proyecto integra capacidades avanzadas de procesamiento analítico con **Python** y visualización interactiva con **Power BI**, bajo el ciclo metodológico **CRISP-DM**.

---

## 🚀 Arquitectura del Prototipo

El framework opera bajo una arquitectura de tres capas que asegura la escalabilidad y el soporte eficiente del modelo de datos:

1. **Capa de Ingesta y Procesamiento (Python):** Limpieza de datos, manejo de valores nulos, detección de outliers y cálculo algorítmico automatizado de métricas de concentración mediante aproximación por trapecios.
2. **Capa de Persistencia y Almacenamiento:** Los datos procesados se estructuran en archivos planos de alta eficiencia (`.csv` / `.parquet`) optimizados para su consumo masivo.
3. **Capa de Presentación (Power BI):** Consumo del modelo de datos optimizado, cálculo de métricas dinámicas mediante DAX y despliegue de dashboards interactivos.

---

## 📂 Estructura del Repositorio

```text
├── data/
│   ├── raw/                  # Datos sintéticos originales (1,000 registros)
│   └── processed/            # Datos limpios y enriquecidos con métricas
├── notebooks/
│   └── eda_brechas_gini.ipynb # Script maestro en Python (Análisis Exploratorio y Algoritmo de Gini)
├── src/
│   └── data_processing.py    # Scripts modulares de Python para automatización
├── dashboard/
│   └── brechas_salariales.pbix # Archivo origen de Power BI con las métricas DAX
└── README.md                 # Documentación principal del proyecto

## 🛠️ Tecnologías y Librerías Utilizadas

* **Lenguaje de Programación:** Python 3.x
* **Procesamiento de Datos:** `pandas`, `numpy`
* **Cálculo Matemático:** `scipy` (regla del trapecio)
* **Visualización:** `matplotlib`, `seaborn`
* **Business Intelligence:** Power BI Desktop (DAX)

---

## 📊 Métricas Core Implementadas

* **Coeficiente de Gini (Python):** Calculado mediante la integración numérica de la Curva de Lorenz con la regla del trapecio:
  $$\text{Gini} = 1 - \sum_{i=1}^{n} (x_i - x_{i-1})(y_i + y_{i-1})$$
  *Resultado del Prototipo:* **0.3722** (Muestra de 1,000 registros).
* **Métricas Dinámicas (DAX):** `Ingreso Acumulado Relativo` y `Población Acumulada Relativa`.

---

## ⚙️ Instrucciones de Ejecución

### 1. Procesamiento de Datos (Python)
```bash
pip install pandas numpy scipy matplotlib seaborn
```
