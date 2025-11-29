# mi-portfolio-ma2003b
# 📊 Portfolio Final – MA2003B: Métodos Multivariados en Ciencia de Datos  
Aplicación de Métodos Multivariados en Ciencia de Datos – Tecnológico de Monterrey (CCM)

Repositorio profesional que integra los tres análisis multivariados desarrollados durante el curso MA2003B, documentado, reproducible y presentado con estándares de la industria.

---

## 🏷️ Badges
![License](https://img.shields.io/badge/license-MIT-green.svg)  
![Python](https://img.shields.io/badge/python-3.10-blue.svg)  
![Status](https://img.shields.io/badge/status-active-brightgreen.svg)  
![Jupyter](https://img.shields.io/badge/made%20with-Jupyter-orange.svg)

---

## 👥 Equipo
- **Luis Enrique Hernández Torres** — A01662166  
- **Víctor Ángel Martínez Vidaurri** - A01657661 
- **Alejandro Martínez Ochoa** - A01657661

## 📚 Tabla de Contenidos
1. [Descripción General](#descripcion-general)
2. [Resumen de Casos de Estudio](#resumen-de-casos-de-estudio)
3. [Instrucciones de Reproducibilidad](#instrucciones-de-reproducibilidad)
4. [Estructura del Repositorio](#estructura-del-repositorio)
5. [Tools Used](#tools-used)

---

# 🧭 Descripción General
Este portfolio integra los tres casos de análisis multivariado desarrollados durante el curso **MA2003B – Aplicación de Métodos Multivariados en Ciencia de Datos**.

Su propósito es demostrar:  
- Dominio técnico de **Factor Analysis**, **Discriminant Analysis** y **Cluster Analysis**.  
- Capacidad para documentar proyectos de ciencia de datos con estándares profesionales.  
- Uso correcto de Git, GitHub y control de versiones.  
- Comunicación clara y ejecutiva de hallazgos técnicos complejos.  
- Integración metodológica y reflexión crítica sobre el proceso analítico.

La evaluación incluye repositorio, documentación técnica, notebooks reproducibles y una presentación ejecutiva de 15–20 minutos.

---

# 📁 Resumen de Casos de Estudio

| Caso | Método | Pregunta de Negocio | Hallazgo Clave | Link |
|------|--------|----------------------|-----------------|------|
| **TechnoServe – Customer Satisfaction** | Factor Analysis | ¿Qué dimensiones latentes explican la satisfacción del cliente? | 5 factores explican **61.85%** de la varianza; destacan Innovación Técnica, Relación con Cliente y Transparencia Económica. | [Ver caso →](./case-01-factor-analysis) |
| **LendSmart – Credit Risk Analysis** | Discriminant Analysis | ¿Cómo clasificar aplicantes de crédito según riesgo de default? | LDA predice correctamente **100%** de los defaulters; principales predictores: credit utilization, DTI, payment history. | [Ver caso →](./case-02-lendsmart-analysis) |
| **MegaMart – Customer Segmentation** | Cluster Analysis | ¿Qué segmentos naturales existen entre los clientes? | 4–5 clusters con comportamiento distinto; un segmento High-Value genera una parte desproporcionada de ingresos. | [Ver caso →](./case-03-cluster-analysis) |

---

## 🔍 Comparación Metodológica  
### Factor Analysis vs. Discriminant Analysis vs. Cluster Analysis

A continuación se presenta una comparación clara entre las tres metodologías aplicadas en el portafolio, basadas en los casos reales de satisfacción del cliente, riesgo crediticio y segmentación de clientes.

---

### 📘 1. Factor Analysis (Customer Satisfaction)
**Propósito:**  
Reducir la dimensionalidad y descubrir factores latentes que explican patrones entre variables correlacionadas.

**Aplicación en el proyecto:**  
- Se identificaron **5 factores principales** que explican el 61.85% de la varianza.  
- Los factores permitieron resumir más de 40 indicadores en componentes interpretables.  
- Factores clave: Innovación Técnica, Relación con el Cliente, Transparencia Económica, etc.

**Fortalezas:**  
- Simplifica datos complejos.  
- Identifica constructos estratégicos.  
- Útil para encuestas o bases con redundancia.

**Limitaciones:**  
- No clasifica ni segmenta.  
- Requiere interpretación experta.

---

### 📙 2. Discriminant Analysis (LendSmart Credit Risk)
**Propósito:**  
Clasificación supervisada: distinguir grupos conocidos (buenos vs. malos pagadores).

**Aplicación en el proyecto:**  
- Modelos LDA y QDA entrenados con variables financieras.  
- Ambos alcanzaron **100% accuracy** debido a la separación perfecta del dataset.  
- Variables discriminantes clave: DTI ratio, utilización de crédito, historial de pagos.

**Fortalezas:**  
- Alta interpretabilidad.  
- Clasificación robusta para decisiones crediticias.  
- Facilita conocer qué variables separan mejor los grupos.

**Limitaciones:**  
- Requiere etiquetas previas.  
- Supone normalidad y varianzas homogéneas (LDA).

---

### 📗 3. Cluster Analysis (MegaMart Segmentation)
**Propósito:**  
Agrupar observaciones similares sin necesidad de etiquetas → segmentación no supervisada.

**Aplicación en el proyecto:**  
- Combinación de clustering jerárquico + K-Means.  
- Validación con Elbow, Silhouette y PCA.  
- Se obtuvieron **4 segmentos** accionables para marketing.

**Fortalezas:**  
- Ideal para estrategias comerciales y segmentación.  
- Descubre patrones latentes en datos de clientes.

**Limitaciones:**  
- Sensible a outliers y escala.  
- Elección de k puede ser subjetiva.

---

### 📊 Conclusión Comparativa

| Técnica               | Tipo            | Objetivo                      | Uso en el Portafolio                    | Cuando Usarla                                  |
|----------------------|----------------|--------------------------------|------------------------------------------|------------------------------------------------|
| **Factor Analysis**   | Reducción      | Identificar factores ocultos   | Satisfacción del Cliente                 | Muchas variables correlacionadas               |
| **Discriminant**      | Supervisado    | Clasificar grupos conocidos    | Riesgo Crediticio                        | Clasificación predictiva                       |
| **Cluster Analysis**  | No supervisado | Descubrir grupos naturales     | Segmentación de Clientes (MegaMart)      | No hay etiquetas; buscar patrones comerciales  |

---

## 🎓 Lecciones Aprendidas (Reflexión Final)

---

### 1. El valor del análisis multivariado
El portafolio demuestra que estas técnicas permiten convertir bases de datos complejas en **decisiones accionables**.  
Cada técnica aporta un lente distinto: reducción, clasificación y segmentación.

---

### 2. Complementariedad entre métodos
Las tres técnicas se integran para crear una visión completa:

- **Factor Analysis** reduce complejidad.  
- **Discriminant Analysis** clasifica y permite decisiones operativas.  
- **Cluster Analysis** descubre oportunidades y segmenta clientes.

Combinadas, forman un toolkit esencial para problemas reales.

---

### 3. Aplicaciones profesionales
Este trabajo fortalece competencias claves:

- Evaluación crítica de modelos  
- Interpretación de métricas  
- Comunicación de insights complejos  
- Toma de decisiones basada en datos

Aplicable en marketing, riesgo, consultoría y ciencia de datos.

---

### 4. Cierre personal
El proyecto reforzó habilidades técnicas y estratégicas, demostrando el valor del análisis multivariado para **resolver problemas reales y generar impacto empresarial**.

---

# ⚙️ Instrucciones de Reproducibilidad

## 🔧 Requerimientos
- Python **3.10+**
- JupyterLab o Jupyter Notebook
- pip

---

## 📦 Instalación de dependencias
```bash
pip install -r requirements.txt
```

Clonar el repositorio:
```bash
git clone https://github.com/usuario/mi-portfolio-ma2003b.git
```
Acceder a un caso:
```bash
cd mi-portfolio-ma2003b/case-01-factor-analysis/notebooks
```

Abrir el notebook:
```bash
jupyter lab
```

```bash
## 🗂️ Estructura del Repositorio
mi-portfolio-ma2003b/
│
├── README.md
├── LICENSE
├── .gitignore
├── requirements.txt
│
├── case-01-factor-analysis/
│   ├── README.md
│   ├── data/
│   ├── notebooks/
│   ├── reports/
│   ├── src/
│   └── visualizations/
│
├── case-02-discriminant-analysis/
│   ├── README.md
│   ├── data/
│   ├── notebooks/
│   ├── reports/
│   └── visualizations/
│
├── case-03-cluster-analysis/
│   ├── README.md
│   ├── data/
│   ├── notebooks/
│   ├── reports/
│   └── visualizations/
│
├── portfolio-summary/
│   ├── PORTFOLIO_OVERVIEW.md
│   ├── LESSONS_LEARNED.md
│   └── METHODOLOGY_COMPARISON.md
│
└── presentation/
    └── final_portfolio_presentation.pdf
```

```


