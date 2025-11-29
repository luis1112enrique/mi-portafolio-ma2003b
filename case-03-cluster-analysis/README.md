# 🛒 MegaMart Customer Segmentation Analysis  
**Data Science Project — Clustering, PCA & Behavioral Insights**

Este proyecto desarrolla una segmentación de clientes para MegaMart utilizando técnicas avanzadas de análisis multivariado, con el objetivo de mejorar la personalización del marketing, optimizar recursos y aumentar la retención y conversión de clientes.

---

## 📌 Objetivo del Proyecto
MegaMart actualmente opera sin una estrategia de segmentación formal, lo que conduce a campañas genéricas y gasto ineficiente.  
El objetivo del análisis es **identificar segmentos de clientes basados en comportamiento real** y generar **recomendaciones accionables** para el área de marketing.

---

## 📊 Dataset
- **3,000 clientes**
- **9 variables conductuales**, incluidas:
  - monthly_transactions  
  - avg_basket_size  
  - total_spend  
  - avg_session_duration  
  - email_open_rate  
  - product_views_per_visit  
  - return_rate  
  - customer_tenure_months  
  - recency_days

Todos los datos se encuentran limpios y sin valores faltantes.

---

## 🧹 1. Exploratory Data Analysis (EDA)
El EDA incluye:

- Histogramas por variable  
- Matriz de correlación  
- Boxplots de outliers  
- Scatterplots clave (ej. *total_spend vs monthly_transactions*)  
- Análisis de patrones de navegación, gasto y recencia

**Hallazgos clave:**
- Alta variabilidad en gasto y actividad.
- Correlación moderada entre *basket size* y *total spend*.
- Outliers controlados mediante análisis visual; no se removieron por su relevancia comercial.

---

## ⚙️ 2. Preprocesamiento  

### **Estandarización (StandardScaler)**
Todas las variables numéricas fueron estandarizadas:

\[
z = \frac{x - \mu}{\sigma}
\]

Esto evita que variables con rangos grandes (como *total_spend*) dominen la distancia euclidiana en los modelos de clustering.

---

## 🌲 3. Análisis de Cluster Jerárquico

Se evaluaron cuatro métodos de linkage:

- Single  
- Complete  
- Average  
- **Ward (mejor desempeño)**

**Conclusiones del dendrograma:**
- Ward presenta las separaciones más estables.
- Se observa una brecha vertical clara alrededor de **k = 4**, indicando cuatro grupos naturales.
- Los métodos Single y Average sufren *chaining effect*.

---

## 🔢 4. K-Means Clustering

### **Selección de k**
- **Elbow Method:** inflexión entre *k = 3 y 4*.  
- **Silhouette Score:** mejor valor práctico para *k = 4* (≈ 0.317).  
- **Validación cruzada con Ward:** también sugiere *k = 4*.

**Resultado final:**  
👉 **k = 4 clusters** como solución óptima.

---

## 🧭 5. PCA Visualization

Se redujo la dimensionalidad de 9 variables a 2 componentes principales (**PC1** y **PC2**).

- Varianza explicada por los dos primeros componentes: **≈62%**  
- Visualización clara de la separación entre clusters  
- Los centroides proyectados refuerzan la estructura de grupos

---

## 👥 6. Cluster Profiling

### **Cluster 0 — High-Value Loyalists**
- Alto gasto total  
- Frecuencia elevada de compras  
- Gran actividad de navegación  
- Baja tasa de devoluciones  
**→ Segmento más valioso**

### **Cluster 1 — Deal-Driven Inactive**
- Bajo gasto  
- Baja actividad en sitio  
- Alta recencia  
- Sensibles a precios y descuentos  
**→ Objetivo de reactivación**

### **Cluster 2 — Mid-Value Occasional**
- Cestas grandes  
- Compras ocasionales  
- Gasto moderado-alto  
**→ Potencial para crecer**

### **Cluster 3 — Engaged Browsers**
- Mucha navegación  
- Sesiones largas  
- Conversión moderada  
**→ Oportunidad de optimizar upselling**

---

## 📈 7. Recomendaciones Estratégicas

| Segmento | Objetivo | Estrategias |
|----------|----------|-------------|
| High-Value Loyalists | Retener y aumentar valor | Programas VIP, early access, cross-selling |
| Deal-Driven Inactive | Reactivar | Descuentos, cupones, incentivos de envío |
| Mid-Value Occasional | Incrementar frecuencia | Bundles, ofertas estacionales, “spend-more-save-more” |
| Engaged Browsers | Aumentar conversión | Recomendaciones personalizadas, ofertas por tiempo limitado |

---

## 🚀 8. Impacto Esperado

- **25% reducción** de churn en High-Value Loyalists  
- **40% aumento** en open rates con mensajes personalizados  
- **15–20% aumento** en conversiones en segmentos objetivo  
- Mejor ROI mediante campañas basadas en comportamiento

---

## 🧩 9. Conclusiones

Este análisis demuestra que MegaMart puede beneficiarse ampliamente de una estrategia basada en segmentación de clientes:

- Detecta patrones ocultos en comportamiento  
- Permite personalización y asignación eficiente de recursos  
- Proporciona insights accionables para marketing y retención  
- Sienta las bases para estrategias avanzadas como LTV o segmentación dinámica

---

## 📦 Archivos incluidos

- `notebook.ipynb` — Notebook completo del análisis  
- `models/` — Modelos y centroides  
- `plots/` — Gráficos EDA, dendrogramas, PCA, perfiles  
- `data/` — Dataset original (si aplica)


---

