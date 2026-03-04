# Telecom X - Predicción de Evasión (Churn) - Parte 2

## Propósito del Análisis
El objetivo principal de este proyecto es desarrollar un modelo de Machine Learning capaz de predecir la cancelación (churn) de clientes de Telecom X. Al identificar los patrones que llevan a un cliente a abandonar la compañía, la empresa puede tomar decisiones proactivas para mejorar la retención y reducir pérdidas económicas.

## Estructura del Proyecto y Organización
- **telecom_ii.py**: Cuaderno principal que contiene el pipeline de ciencia de datos y entrenamiento de modelos.
- **datos_tratados.csv**: Dataset limpio y estandarizado (generado en la Parte 1) que sirve como base para este análisis.

## Preparación de los Datos
Para garantizar la eficacia del modelo, se realizaron los siguientes pasos:
1. Clasificación de Variables: Identificamos variables categóricas (como tipo de contrato, servicios) y numéricas (tenure, MonthlyCharges, TotalCharges).
2. Codificación y Normalización: 
    - Se aplicó One-Hot Encoding a las variables categóricas.
    - Se utilizó StandardScaler para normalizar las variables numéricas, asegurando que todas estén en la misma escala.
3. Separación de Datos: Los datos se dividieron en 80% entrenamiento y 20% prueba usando train_test_split.

## Modelización y Justificación
- Balanceo con SMOTE: Debido al desequilibrio en los datos (pocos clientes cancelados vs. muchos activos), se aplicó SMOTE para equilibrar las clases y mejorar la detección de fugas.
- Modelos Evaluados: Se compararon Regresión Logística y Random Forest. La Regresión Logística fue seleccionada por su equilibrio entre precisión y capacidad de interpretación para el negocio.

## Insights y Gráficos (EDA)
Durante el análisis exploratorio, se obtuvieron hallazgos críticos:
- Fibra Óptica: Es el servicio con mayor tasa de abandono, sugiriendo posibles problemas de precio o calidad.
- Tipo de Contrato: Los contratos "Mes a Mes" tienen una probabilidad de fuga significativamente mayor que los contratos de 1 o 2 años.

## Instrucciones de Ejecución
Para replicar este análisis o ejecutar el modelo en tu entorno local o en Google Colab, sigue estos pasos:

### 1. Instalación de Librerías
Ejecuta el siguiente comando para instalar las dependencias necesarias:

```bash
pip install pandas seaborn matplotlib scikit-learn imbalanced-learn
df = pd.read_csv('datos_tratados.csv')
