# TelecomX_2
# 📊 Telecom X – Predicción de Cancelación (Churn)

## 📣 Objetivo
Predecir qué clientes tienen mayor probabilidad de cancelar sus servicios (churn) para implementar estrategias de retención proactivas.

---

## 🧰 Herramientas
- Python, Pandas, NumPy  
- Scikit-learn, Imbalanced-learn (SMOTE)  
- Matplotlib, Seaborn  

---

## 🔹 Preprocesamiento
- Se codificaron variables categóricas (One-Hot Encoding).  
- Se eliminó información irrelevante (`customerID`, `Churn`).  
- Se balancearon las clases con **SMOTE**.  
- Se normalizaron variables para modelos sensibles a la escala (KNN, Regresión).  

---

## 🔹 Modelos Evaluados
| Modelo            | Exactitud | Precisión | Recall | F1-score | Observaciones |
|------------------|-----------|-----------|--------|----------|---------------|
| Dummy Classifier  | 74,28%    | 0,0       | 0,0    | 0,0      | Línea base, no identifica cancelaciones |
| Árbol de Decisión | 69,12%    | 0,44      | 0,78   | 0,57     | Overfitting en profundidad alta |
| KNN               | 73,24%    | 0,48      | 0,64   | 0,55     | Mejor equilibrio precisión/recall |
| Random Forest     | 78,40%    | 0,58      | 0,56   | 0,57     | Mejor desempeño global |

**Conclusión:** Random Forest es el modelo más confiable.

---

## 🔹 Factores Clave de Cancelación
1. **tenure (antigüedad)** – Clientes recientes son más propensos a cancelar.  
2. **Charges.Monthly (costo mensual)** – Tarifas altas aumentan churn.  
3. **Contract (tipo de contrato)** – Mes a mes → más cancelaciones.  
4. **TechSupport** – Ausencia de soporte aumenta la probabilidad de churn.  

Otros factores: servicios adicionales (OnlineSecurity, OnlineBackup), presencia de familia (Partner, Dependents).



## 🔹 Estrategias de Retención
- Fidelización temprana: descuentos y promociones en los primeros meses.  
- Mejorar soporte técnico y servicios adicionales.  
- Incentivar contratos a largo plazo con beneficios y bonificaciones.  
- Identificar clientes de riesgo mediante Random Forest y contacto proactivo.  
- Ajuste de precios y planes flexibles según perfil del cliente.  


## 📌 Conclusión
Random Forest permite identificar clientes propensos a cancelar de manera confiable.  
La combinación de análisis de datos y estrategias de retención puede reducir significativamente la tasa de churn y aumentar la lealtad del cliente.



## 📂 Enlaces
- Notebook del proyecto: [`final_de_TelecomX_LATAM_2.ipynb`](./final_de_TelecomX_LATAM_2.ipynb)  
- Dataset limpio: [`empresa_limpia.csv`](./empresa_limpia.csv)  
