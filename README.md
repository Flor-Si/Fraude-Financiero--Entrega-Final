# Fraude-Financiero

🏦 Trabajo Final: Ingenia-2025
Detección de fraudes en transacciones bancarias
👥 Integrantes Grupo 4
Carpio, Vanessa
Huber, Anne Kathrin
Siarri, María Florencia
Introducción
Este proyecto es parte del Trabajo Final del curso de Ciencia de Datos dictado por Fundación YPF en 2025.
El pago en línea es el método de transacción más popular en el mundo, pero su aumento trae consigo un incremento de fraude.
El objetivo de este análisis es identificar pagos fraudulentos y no fraudulentos a partir de un conjunto de datos históricos provenientes de Kaggle.

🎯 Objetivos
Desarrollar un modelo que detecte transacciones potencialmente fraudulentas.
Analizar distintos tipos de transacciones ( CASH-IN, CASH-OUT, DEBIT, PAYMENT, TRANSFER).
Explorar comportamientos según:
Montos
Días y horarios
Cuentas afectadas y destinos de las transferencias.
🗄️ Descripción del conjunto de datos
Origen : Kaggle
Tamaño : CSV de más de 493 MB (se aloja en GitLab para facilitar la descarga).
Variables (11):
step– unidad de tiempo (1 hora; 744 pasos = 31 días).
type– tipo de transacción ( CASH-IN, CASH-OUT, DEBIT, PAYMENT, TRANSFER).
amount– monto en moneda local.
nameOrig– cliente que inicia la transacción.
oldbalanceOrg– saldo inicial del origen.
newbalanceOrig– saldo después de la transacción.
nameDest– cliente/destino de la transacción.
oldbalanceDest– saldo inicial del destino (no aplica a comerciantes “M…”).
newbalanceDest– saldo después en destino (no aplica a “M…”).
isFraud– indicador de fraude real.
isFlaggedFraud– marcado si monto > 200 000 en una sola transacción.
🧹 Limpieza de Datos(Pasos que se realizaron en la entrega anterior)
Carga del CSV
Visualización inicial
Identificación de tipos de variables
Dimensiones: filas y columnas
Estadística descriptiva
Detección y eliminación de nulos
Función discreppara valores atípicos
Registro de registros por tipo
Diagramas de caja e histogramas
Matriz de correlación
transformación de datos (normalización, codificación de variables categóricas).
Modelado y optimización de hiperparámetros
Evaluación de los modelos
🚀 Metodología
**Lenguaje, librerías y modelos**:

Python: pandas, numpy, matplotlib, seaborn, scikitlearn, RandomForestClassifier, scipy, sklearn.ensemble, XGboost,
Pasos :(Entrega Final)

Carga y Preprocesamiento (escalado, separación de etiquetas)
Reducción de Dimensionalidad con PCA
Búsqueda de Parámetros para K-Means (Elbow y Silhouette)
Entrenamiento Final de K-Means y evaluación de la tasa de fraude en cada cluster
Estimación de ε y Ejecución de DBSCAN, con gráfico de k-distancia para seleccionar eps
IsolationForest para puntuación de anomalías
Evaluación y Combinación de Señales de los métodos
🛠️ Herramientas
Google Colab
Cuaderno Jupyter
GitHub / GitLab
Excel (exploración rápida)
🔗 Enlaces útiles
🔍 Conjunto de datos en Kaggle:
https://www.kaggle.com/datasets/rupakroy/online-paids-fraud-detection-dataset
