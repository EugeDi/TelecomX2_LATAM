# Análisis Predictivo con Machine Learning de Evasión de Clientes en TelecomX (Challenge de Alura LATAM)

Este proyecto analiza el comportamiento de los clientes de la empresa TelecomX con el objetivo de predecir la **cancelación del servicio (churn)**. A través de distintas etapas de procesamiento, modelado y evaluación de modelos supervisados de machine learning, se busca identificar **factores clave** que influyen en la baja de clientes y proponer **estrategias de retención efectivas**.

---

## Descripción del Proyecto

Se utilizó un dataset pretratado, disponible públicamente en GitHub:

```
https://raw.githubusercontent.com/EugeDi/TelecomX2_LATAM/main/datos_tratados.csv
```

Contiene información de 7032 clientes de TelecomX, incluyendo variables demográficas, de servicios contratados y de facturación.

---

## Librerías utilizadas

- `pandas`, `numpy`
- `plotly`, `seaborn`, `matplotlib`
- `scikit‑learn` (`sklearn`) para preprocesamiento, modelos, métricas y validación
- `imblearn` (SMOTE para balanceo)

---

## Etapas del proyecto

1. **Preparación de los datos**

   - Clasificación de variables (categóricas binarias, multiclase, numéricas)
   - _One‑hot encoding_ a variables multiclase
   - Split en **train**, **val** y **test**
   - Balanceo del set de entrenamiento con **SMOTE**

2. **Análisis exploratorio**

   - Matriz de correlación (variables numéricas)
   - Boxplots segmentados por `Churn`

3. **Modelado**

   - **DummyClassifier** (baseline)
   - **DecisionTreeClassifier**
   - **KNeighborsClassifier** (con normalización `MinMaxScaler`)
   - **LogisticRegression**
   - **RandomForestClassifier**
   - **LinearSVC**

4. **Evaluación**
   - Exactitud, Precisión, Recall, F1‑score
   - Matrices de Confusión comparativas

---

## Conclusiones clave

- **Tenure** es el predictor más consistente: mayor antigüedad ⇒ menor churn.
- Contratos **“month‑to‑month”** y clientes de **fibra óptica** presentan mayor riesgo.

---

## Recomendaciones de negocio

- **Fidelización temprana** (primeros 3‑6 meses).
- Incentivar migración a **contratos anuales**.
- Monitoreo proactivo de usuarios con **servicio de internet** y **fibra óptica**.

---

> Proyecto realizado en el marco del **Challenge de Ciencia de Datos – Alura LATAM**.
