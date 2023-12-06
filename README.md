# Optimización de campaña para depósito a plazo fijo
Se analizó un conjunto de datos público para optimizar un campaña de marketing de deposito a plazo fijo. Para esto se utilizaron tecnicas de machine learning para buscar las caracterísitcas que permitieran predecir si un cliente se suscribiria a un deposito a plazo fijo o no.

Para el análisis primero se visualizaón a las variables, se encontró que el conjunto de datos tenía clases desbalanceadas, por lo que a la variable objetivo (y) se le aplicó la técnica estadística de sobremuestreo SMOTE para crear muestras sintéticas y así equilibrar las clases. Con las muestras sintéticas en el conjunto se procedió a hacer un preprocesamiento de los datos, después se creó un modelo XGBoostClassifier para predecir la variable objetivo y se realizó un análisis de error. Se utilizó la técnica sequencial feature selection (SFS) para buscar características que mejoren la exactitud del modelo. También se utilizó la técnica SHAP y se comparó con la anterior técnica. Se encontró que debido al desbalance entre las clases la técnica SFS ignoraba características importantes para predecir la variable objetivo, mientras que al considerar todas las aportaciones con SHAP fue posible encontrar que los valores de las características: loan yes y default yes son una minoría entre las clases y estas son importantes para realizar una predicción sobre la variable objetivo.

Al final se encontró que la característica campaign, duration, contact, poutcome success, housing yes, loan yes, default yes, education primary, job housemaid, month mar, sep, oct y dec son las más importantes para hacer predicciones con el modelo.


Mas información en: https://www.kaggle.com/datasets/nelgiriyewithana/credit-card-fraud-detection-dataset-2023
Conjunto de datos by Ankush Singal (From Huggingface) https://huggingface.co/datasets/Andyrasika/banking-marketing
