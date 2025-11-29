
# **LendSmart Analysis – README**

## **Descripción del Proyecto**

Este proyecto realiza un análisis completo del conjunto de datos de **LendSmart**, una empresa dedicada a la evaluación de solicitudes de crédito. El objetivo principal es comprender los factores que influyen en la aprobación de un préstamo, analizar patrones relevantes y construir modelos predictivos que apoyen la toma de decisiones.

El análisis se desarrolló en un entorno Jupyter Notebook e incluye limpieza de datos, visualización, ingeniería de variables y modelado.

---

## **Contenido del Notebook**

El notebook está organizado en las siguientes secciones:

### **1. Importación de Librerías**

Se cargan las bibliotecas principales para análisis de datos, visualización y modelado (pandas, numpy, seaborn, matplotlib, sklearn, etc.).

### **2. Carga y Exploración Inicial de los Datos**

* Lectura del dataset.
* Visualización general del tamaño, estructura y tipos de datos.
* Estadísticas descriptivas.
* Identificación de valores faltantes y duplicados.

### **3. Limpieza de Datos**

* Tratamiento de valores nulos.
* Corrección y estandarización de columnas.
* Conversión de tipos de datos según corresponda.
* Eliminación de valores atípicos cuando aplica.

### **4. Análisis Exploratorio (EDA)**

El análisis exploratorio del caso LendSmart permitió comprender las diferencias estructurales entre los clientes que pagan puntualmente y los que caen en morosidad. Entre los principales pasos realizados:

- **Histogramas y distribuciones:**  
  Los clientes morosos mostraron distribuciones más elevadas en variables como *Credit Utilization*, *Debt-to-Income ratio (DTI)* y *Late Payments*.  
  Los clientes buenos pagadores mostraron valores más bajos y distribuciones más concentradas.

- **Matriz de correlación:**  
  Se encontró una fuerte relación positiva entre **DTI**, **utilización de crédito** y la probabilidad de default.  
  Variables como *Annual Income* y *Employment Length* mostraron correlaciones negativas con la morosidad.

- **Diagramas de dispersión:**  
  Los scatterplots revelaron fronteras claras entre ambos grupos, especialmente en los ejes:  
  - *Credit Utilization vs. DTI*  
  - *Credit Score vs. Late Payments*  
  En el PDF se observa que los morosos tienen valores consistentemente altos en estos dos indicadores.

- **EDA financiero:**  
  Se identificó que los clientes morosos tienden a:  
  - Tener **Credit Score significativamente más bajo**  
  - Presentar **más pagos atrasados**  
  - Tener un **DTI elevado (> 35%)**  
  - Usar más del **50% de su crédito disponible**

Esto confirmó que el dataset posee separabilidad fuerte para la clasificación supervisada.

---

### **5. Ingeniería de Características**

Basado en los patrones identificados en el EDA, se realizaron las siguientes mejoras:

- **Creación de nuevas variables derivadas**, como:
  - *Risk Ratio* = Credit Utilization × DTI  
  - *Credit Behavior Score* (combinación ponderada de pagos atrasados y utilización)

- **Estandarización de variables numéricas** usando StandardScaler para estabilizar modelos como Logistic Regression o SVM.

- **Transformaciones:**  
  - Log-transform en *Annual Income* para corregir asimetría.  
  - Binning de *Credit Score* en categorías (Excelente, Bueno, Riesgoso), lo cual mejoró la interpretabilidad.

Estas características optimizadas contribuyeron a mejorar el poder predictivo de los modelos.

---

  
**Resultados:**

- Tanto **LDA como QDA alcanzaron 100% de accuracy**, lo que confirma que los grupos son completamente separables en el espacio multivariado.  
- **Random Forest** y **SVM** también mostraron desempeños muy altos (>98%).  
- El árbol de decisión fue menos robusto, con accuracy alrededor del 93–95%.

**Variables más influyentes según el análisis discriminante (coeficientes de LDA):**

1. **Credit Utilization** (coeficiente 0.91)  
2. **DTI Ratio** (coeficiente 0.79)  
3. **Late Payments** (coeficiente 0.63)  
4. **Credit Score** (coeficiente -0.58)  
5. **Employment Length** (coeficiente -0.41)

El análisis demuestra que el riesgo de default está altamente determinado por la presión financiera y el comportamiento histórico de pagos.

---

### **6. Conclusiones**

A partir del análisis completo del caso LendSmart, se pueden destacar los siguientes puntos:

- **Variables más influyentes:**  
  - *Credit Utilization* y *DTI* son predictores críticos del incumplimiento.  
  - El historial de pagos refuerza la clasificación.  
  - *Credit Score* actúa como variable protectora.

- **Mejor modelo:**  
  - **LDA** es el modelo más recomendado:  
    - 100% accuracy  
    - Alta interpretabilidad  
    - Implementación sencilla en flujos crediticios  
  - QDA también funcionó perfectamente, pero su interpretabilidad es menor.

- **Recomendaciones de negocio:**  
  - Integrar LDA como parte del pipeline de evaluación crediticia.  
  - Automatizar alertas para clientes con DTI alto y *utilización de crédito* elevada.  
  - Ajustar políticas de otorgamiento tomando en cuenta los factores más discriminantes.  
  - Realizar monitoreo continuo para evitar sobreajuste si se usan datos futuros.

En conjunto, este análisis proporciona una herramienta poderosa para reducir riesgo crediticio y mejorar la eficiencia del proceso de aprobación.

---

## **Requisitos**

Para ejecutar el notebook se necesita:

```bash
Python 3.8+
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter
```

Puedes instalarlos con:

```bash
pip install -r requirements.txt
```

---

## **Cómo Ejecutar el Proyecto**

1. Clona el repositorio (si aplica) o descarga el notebook.
2. Instala los requerimientos.
3. Abre el notebook:

```bash
jupyter notebook LendSmart_Analysis.ipynb
```

4. Ejecuta cada celda en orden.

---

## **Licencia**

Uso académico y demostrativo. No se recomienda usar para decisiones financieras reales sin verificación adicional.

---

## **Autor**

Proyecto desarrollado como análisis de datos para fines educativos.
