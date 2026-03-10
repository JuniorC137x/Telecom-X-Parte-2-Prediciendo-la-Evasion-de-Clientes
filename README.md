# Telecom-X-Parte-2-Prediciendo-la-Evasion-de-Clientes
Prediciendo la Evasión de Clientes
# Telecom X — Parte 2: Prediciendo la Evasión de Clientes

## 1. Propósito del Análisis

Tras identificar los factores asociados a la evasión de clientes en la Parte 1, el siguiente paso es anticiparse al problema. El objetivo de este proyecto es construir modelos predictivos capaces de determinar qué clientes tienen mayor probabilidad de cancelar sus servicios en Telecom X.

Para lograrlo se desarrolló un pipeline completo de Machine Learning que incluye:

- Preparación y codificación de los datos para modelado
- Análisis de correlación y selección de variables relevantes
- Entrenamiento y evaluación de dos modelos de clasificación
- Interpretación de resultados con enfoque estratégico

---

## 2. Estructura del Proyecto
```
telecomx-parte2/
│
├── TelecomX_Parte2.ipynb      # Notebook principal con el pipeline completo de ML
├── datos_tratados.csv         # Datos limpios provenientes del challenge anterior
└── README.md                  # Este archivo
```

El notebook está organizado en tres bloques principales:

- **Preparación de datos:** limpieza adicional, encoding, verificación de balance de clases, estandarización
- **Correlación y selección de variables:** análisis de correlación con Churn y filtrado de variables relevantes
- **Modelado y conclusiones:** entrenamiento, evaluación con métricas, importancia de variables y recomendación estratégica

---

## 3. Gráficos e Insights Obtenidos

### Proporción de Cancelación (Churn)
Gráfico de barras mostrando la distribución entre clientes que se quedaron y los que cancelaron.
> **Insight:** Aproximadamente 1 de cada 4 clientes abandona la empresa, lo que confirma la necesidad de un modelo predictivo para actuar de forma preventiva.

### Correlación de Variables con Churn
Barras horizontales mostrando qué variables tienen mayor relación con la cancelación, diferenciando correlación positiva y negativa.
> **Insight:** El tipo de contrato, el cargo mensual y el tiempo de permanencia son las variables más correlacionadas con el Churn.

### Matriz de Confusión — Regresión Logística y Random Forest
Visualización de los aciertos y errores de cada modelo al clasificar clientes.
> **Insight:** El Random Forest reduce los falsos negativos, es decir, identifica mejor a los clientes que realmente se van a ir.

### Top 10 Variables más Importantes — Random Forest
Barras horizontales con el peso relativo de cada variable en las decisiones del modelo.
> **Insight:** El contrato mes a mes, el cargo mensual y la antigüedad (tenure) concentran la mayor parte del poder predictivo del modelo.

---

## 4. Instrucciones para Ejecutar el Notebook

### Opción A — Google Colab (recomendado)

1. Descarga `TelecomX_Parte2.ipynb` y `datos_tratados.csv`
2. Entra a [colab.research.google.com](https://colab.research.google.com)
3. Haz clic en **Archivo → Subir notebook** y selecciona el `.ipynb`
4. Sube el CSV al entorno de Colab arrastrándolo al panel de archivos de la izquierda
5. Ejecuta todas las celdas 

### Opción B — Localmente con Jupyter

Requisitos previos:
```bash
pip install pandas matplotlib seaborn scikit-learn jupyter
```

Pasos:
```bash
# 1. Clona este repositorio
git clone https://github.com/JuniorC137x/Telecom-X-Parte-2-Prediciendo-la-Evasion-de-Clientes.git

# 2. Entra a la carpeta

# 3. Abre el notebook
jupyter notebook TelecomX_Parte2(1).ipynb
```
