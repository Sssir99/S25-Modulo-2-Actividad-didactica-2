# 🕵️‍♂️ Detección de Fraude en Transacciones Financieras con HMM

Este proyecto implementa un sistema automatizado para la simulación y detección de fraudes en transacciones financieras utilizando **Modelos Ocultos de Markov (HMM)** y el **Algoritmo de Viterbi**.

El código ha sido diseñado para generar transacciones simuladas, aplicar inferencia probabilística sobre los estados ocultos de la transacción y proporcionar un dashboard completo de métricas de seguridad para su análisis.

> 🤖 **Nota:** Este proyecto fue desarrollado con la asistencia del modelo **Gemini 3.1 Pro**.

## ✨ Características Principales

* **Modelo HMM Personalizado**: Simula transacciones basándose en un sistema de tres estados ocultos (Legítima, Sospechosa, Fraudulenta) y tres tipos de observaciones de monto (Bajo, Medio, Alto).
* **Decodificación con Viterbi**: Infiere de forma automática la secuencia de estados más probables a partir de las observaciones de montos monetarios de las transacciones.
* **Sistema de Scoring de Riesgo**: Asigna un puntaje dinámico (0-100) a cada transacción basándose en la probabilidad del estado oculto inferido y agravantes asociados al monto económico involucrado.
* **Métricas de Seguridad (Dashboard)**: Cálculo en tiempo real de métricas importantes como:
  * Tasa de detección de fraude.
  * Tasa de falsos positivos.
  * Monto total de dinero en riesgo.
  * Tiempo promedio para detectar fraude.
* **Visualizaciones y Alertas**: Gráficos claros utilizando `matplotlib` y `seaborn` para la visualización de datos de las anomalías en línea temporal, distribución y comportamiento del fraude.

## 🛠️ Tecnologías y Librerías

El Jupyter Notebook requiere las siguientes librerías de Python:
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`

## 🚀 Cómo Ejecutar el Proyecto

Este proyecto está diseñado para ejecutarse directamente en **Google Colab** o en cualquier entorno local de **Jupyter Notebook**.

### Opción 1: Ejecutar en Google Colab (Recomendado)
1. Abre [Google Colab](https://colab.research.google.com/).
2. Haz clic en **Archivo** -> **Subir bloc de notas** y selecciona el archivo `HMM_Deteccion_Fraude.ipynb`.
3. Ve a **Entorno de ejecución** -> **Ejecutar todas** para simular los datos y visualizar el dashboard generado.

### Opción 2: Ejecutar de manera local
1. Clona o descarga este repositorio en tu máquina.
2. Instala las dependencias necesarias:
   ```bash
   pip install numpy pandas matplotlib seaborn jupyter
   ```
3. Inicia Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Abre `HMM_Deteccion_Fraude.ipynb` y ejecuta las celdas secuencialmente.

## 📄 Estructura del Proyecto

```text
├── HMM_Deteccion_Fraude.ipynb   # Código principal del simulador de fraude
├── README.md                    # Documentación del proyecto
└── .gitignore                   # Archivos ignorados por Git
```

## 📝 Especificaciones del Modelo

El HMM está configurado con las siguientes matrices de probabilidad:
- **Estados ocultos:** `Transacción Legítima`, `Transacción Sospechosa`, `Transacción Fraudulenta`
- **Observaciones:** `Monto Bajo`, `Monto Medio`, `Monto Alto`
- **Distribución Inicial:** 70% Legítima, 20% Sospechosa, 10% Fraudulenta.
