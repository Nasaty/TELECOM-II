#  Predicción de Evasión (Churn) - Telecom X

Este repositorio contiene la fase avanzada de ciencia de datos para la empresa Telecom X. El objetivo es predecir qué clientes tienen mayor probabilidad de cancelar su servicio utilizando modelos de Machine Learning.

##  Estructura del Proyecto
- `datos_tratados.csv`: Dataset procesado en la Parte 1, con limpieza de nulos, normalización de campos anidados y estandarización de tipos de datos.
- `telecom_ii.py`: Script principal de Python que ejecuta el pipeline de Machine Learning.

## 🛠️ Procesos Implementados
Para garantizar la eficacia del modelo, se realizaron los siguientes pasos técnicos:
1. **Carga Continua:** Uso del archivo CSV procesado según estándares de Trello.
2. **Balanceo de Datos:** Implementación de **SMOTE** para equilibrar la clase minoritaria (clientes que cancelan).
3. **Escalado:** Uso de `StandardScaler` para normalizar las variables numéricas.
4. **Modelado:** Entrenamiento y comparación entre **Regresión Logística** y **Random Forest**.

##  Resultados y Conclusiones
El modelo de **Regresión Logística** demostró ser el más efectivo para este caso de negocio:
- **Recall (Sensibilidad): 68%** - Capacidad de detectar correctamente a los clientes en riesgo.
- **Factor de Riesgo Identificado:** Los clientes con contrato "Mes a Mes" y servicio de "Fibra Óptica" son los más propensos a la fuga.
- **Factor de Retención:** Los contratos a largo plazo (1 o 2 años) reducen drásticamente la evasión.

##  Cómo ejecutarlo
1. Clona este repositorio.
2. Asegúrate de tener instaladas las librerías: `pandas`, `sklearn`, `imblearn`, `seaborn`, `matplotlib`.
3. Ejecuta el archivo `telecom_ii.py`.
Modelo predictivo de evasión de clientes para Telecom challenge Alura
