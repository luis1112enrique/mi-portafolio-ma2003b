
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

Incluye:

* Histogramas y distribuciones.
* Matriz de correlación.
* Diagramas de dispersión.
* Gráficos para identificar patrones entre variables financieras y la aprobación del crédito.

### **5. Ingeniería de Características**

* Creación de nuevas variables relevantes para el modelo.
* Normalización o estandarización si se requiere.
* Transformaciones para mejorar el rendimiento del modelo.

### **6. Modelado Predictivo**

Se implementan modelos de clasificación para predecir la aprobación del préstamo (según tu notebook pueden incluirse: Logistic Regression, Decision Tree, Random Forest, SVM, etc.)

Cada modelo incluye:

* Separación de datos en train/test.
* Entrenamiento del modelo.
* Predicciones.
* Evaluación mediante métricas como:

  * Accuracy
  * Precision
  * Recall
  * F1-score
  * Matriz de confusión
* Comparación final de desempeño entre modelos.

### **7. Conclusiones**

Resúmen de los hallazgos claves del análisis, como:

* Variables más influyentes en la aprobación.
* Desempeño del modelo más adecuado.
* Recomendaciones para el negocio.

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
