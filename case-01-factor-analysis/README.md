# 📘 Case 01 – Factor Analysis: TechnoServe Customer Satisfaction

Este caso aplica **Análisis Factorial** para identificar las dimensiones latentes que explican la satisfacción de clientes de TechnoServe Solutions. El objetivo es transformar un conjunto amplio de variables de percepción en un modelo compacto y accionable para la toma de decisiones estratégicas.

---

# 🧭 1. Contexto del Negocio

TechnoServe Solutions recopiló **3,400 encuestas de satisfacción** para evaluar la experiencia de sus clientes en áreas como soporte técnico, comunicación, transparencia y calidad del servicio. La empresa enfrentaba el reto de:

- Entender **qué factores realmente impulsan la satisfacción**.  
- Priorizar inversiones estratégicas basadas en impacto.  
- Conectar métricas internas con resultados de negocio como NPS, retención y crecimiento.

El análisis factorial permite **reducir dimensionalidad** y revelar patrones estructurales que no son visibles en análisis univariados.

---

# 🔬 2. Metodología

Se aplicó un **Análisis Factorial Exploratorio (AFE)**, siguiendo estos pasos:

### ✔️ 1. Pruebas de adecuación
- **KMO = 0.959**  
- **Test de Bartlett: p < 0.001**

Ambos indican que los datos son adecuados para Análisis Factorial.

### ✔️ 2. Método
- Extractor: **Principal Axis Factoring (PAF)**
- Rotación: **Varimax (ortogonal)**
- Número de factores retenidos: **5** (basado en Scree Plot y criterios de Kaiser)

### ✔️ 3. Herramientas
- Python  
- Pandas, FactorAnalyzer, Seaborn, Matplotlib  
- Jupyter Notebook  
- Visualizaciones generadas en `visualizations/`

> El notebook reproducible se encuentra en:  
`./notebooks/factor_analysis.ipynb`

---

# 🧪 3. Datos

El dataset contiene **3,400 observaciones** y más de 20 variables de percepción del cliente, incluyendo:

- Innovación técnica  
- Comunicación  
- Gestión de proyectos  
- Claridad financiera  
- Soporte postventa  
- Valor percibido  

### 📄 Diccionario de Datos  
Puedes consultar el diccionario completo en:  
`./data/DATA_DICTIONARY.md`

---

# 📊 4. Hallazgos Principales

El análisis factorial reveló **5 factores latentes** que explican **61.85 %** de la varianza total:

| Factor | Nombre Empresarial | Insight Clave |
|--------|--------------------|----------------|
| **F1** | Innovación y Excelencia Técnica | Capacidad técnica sólida y soluciones innovadoras |
| **F2** | Relación con el Cliente | Comunicación clara, confianza y seguimiento |
| **F3** | Gestión de Proyectos | Cumplimiento de tiempos, entregables y calidad |
| **F4** | Transparencia Económica | Claridad en costos, ROI y valor percibido |
| **F5** | Soporte y Capacitación | Eficiencia en soporte postventa |

Estos factores muestran consistencia estadística y relevancia estratégica.

### 📌 Visualización Destacada (Scree Plot)

![Scree Plot](../case-01-factor-analysis/visualizations/scree_plot.png)

### Otros hallazgos claves:

- F1, F2 y F4 explican la mayor parte del impacto sobre **NPS**, renovación y satisfacción general.  
- F5, aunque menos correlacionado con satisfacción inmediata, es clave para **retención**.  
- Las cargas factoriales muestran agrupamientos claros y sin multicolinealidad crítica.

Más visualizaciones en `visualizations/`.

---

# 💼 5. Recomendaciones de Negocio

Con base en las dimensiones identificadas:

### 🎯 1. **Reforzar Innovación Técnica (F1)**
- Invertir en capacidades técnicas y desarrollo de nuevas soluciones.  
- Documentar casos de éxito para fortalecer confianza de clientes.

### 📞 2. **Potenciar Relación y Comunicación (F2)**
- Capacitar a personal en comunicación consultiva.  
- Implementar seguimientos post-proyecto con protocolos estandarizados.

### 💰 3. **Optimizar Transparencia Económica (F4)**
- Crear dashboards de ROI visibles para el cliente.  
- Simplificar reportes financieros y propuestas económicas.

### 🎓 4. **Fortalecer Soporte y Capacitación (F5)**
- Ampliar bibliotecas de capacitación técnica y videos.  
- Medir tiempos de respuesta y mejorar SLA.

---