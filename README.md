# EDA-Diamonds
EDA diamonds seaborn

# EDA Diamonds / Análisis Exploratorio de Diamantes

## English Version

### Project Overview
This project presents an **Exploratory Data Analysis (EDA)** of the classic diamonds dataset.  
The goal is to understand the main patterns, relationships, and collinearity in the data before moving on to modeling.

### Dataset
- Contains numeric features: `carat`, `x`, `y`, `z`, `depth`, `table`, `price`.  
- Categorical features: `cut`, `color`, `clarity`.  
- Target variable: `price`.

### Key Findings
1. **Collinearity among numeric variables**  
   - Dimensions `x`, `y`, `z`, `depth`, `table`, and `volume` are highly collinear (very high VIF).  
   - `carat` summarizes size information and has the highest correlation with `price`.  
   - Recommendation: use only `carat` for numeric modeling.

2. **Categorical variables**  
   - `cut`, `color`, and `clarity` provide additional valuable information.  
   - Diamonds with better cut and clarity tend to have higher prices.

3. **Price distribution**  
   - Right-skewed distribution suggests potential log transformation for modeling.

4. **Outliers**  
   - Some diamonds have extremely high `carat` and `price`, as expected in this dataset.

5. **Additional relationships**  
   - `volume` is highly correlated with `carat`, confirming it as a derived feature.  
   - `depth` and `table` show low correlation with `price`.

### Recommendations for Modeling
- Keep `carat` and categorical variables (`cut`, `color`, `clarity`).  
- Drop `x`, `y`, `z`, `depth`, `table`, and `volume` to avoid multicollinearity.  
- Consider transforming `price` or `carat` for linear models.

### Suggested Plots
- Correlation heatmap for numeric variables.  
- Histogram and boxplot of `price`.  
- Scatter plot `carat` vs `price`.  
- Boxplots of `price` by `cut`, `color`, and `clarity`.

---

## Versión en Español

### Descripción del Proyecto
Este proyecto presenta un **Análisis Exploratorio de Datos (EDA)** del dataset clásico de diamantes.  
El objetivo es comprender los principales patrones, relaciones y colinealidad antes de avanzar a modelado.

### Dataset
- Variables numéricas: `carat`, `x`, `y`, `z`, `depth`, `table`, `price`.  
- Variables categóricas: `cut`, `color`, `clarity`.  
- Variable objetivo: `price`.

### Hallazgos Clave
1. **Colinealidad entre variables numéricas**  
   - Las dimensiones `x`, `y`, `z`, `depth`, `table` y `volume` presentan alta colinealidad (VIF muy alto).  
   - `carat` resume la información de tamaño y tiene la mayor correlación con `price`.  
   - Recomendación: usar solo `carat` como variable numérica.

2. **Variables categóricas**  
   - `cut`, `color` y `clarity` aportan información adicional relevante.  
   - Los diamantes con mejor corte y claridad tienden a tener precios más altos.

3. **Distribución de `price`**  
   - Distribución sesgada a la derecha, lo que sugiere aplicar log-transformación en modelos lineales.

4. **Outliers**  
   - Algunos diamantes presentan valores muy altos de `carat` y `price`, esperados en este dataset.

5. **Relaciones adicionales**  
   - `volume` está altamente correlacionado con `carat`.  
   - `depth` y `table` tienen baja correlación con `price`.

### Recomendaciones para Modelado
- Mantener `carat` y variables categóricas (`cut`, `color`, `clarity`).  
- Excluir `x`, `y`, `z`, `depth`, `table` y `volume` para evitar colinealidad.  
- Considerar transformaciones de `price` o `carat` para modelos lineales.

### Gráficos sugeridos
- Heatmap de correlación para variables numéricas.  
- Histograma y boxplot de `price`.  
- Scatter plot de `carat` vs `price`.  
- Boxplots de `price` por `cut`, `color` y `clarity`.
