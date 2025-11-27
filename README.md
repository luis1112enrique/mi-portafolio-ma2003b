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
- **Víctor Ángel Martínez Vidaurri**  
- **Alejandro Martínez Ochoa**  
*(Opcional)*: Enlaces a perfiles de LinkedIn

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
| **LendSmart – Credit Risk Analysis** | Discriminant Analysis | ¿Cómo clasificar aplicantes de crédito según riesgo de default? | LDA predice correctamente **100%** de los defaulters; principales predictores: credit utilization, DTI, payment history. | [Ver caso →](./case-02-discriminant-analysis) |
| **MegaMart – Customer Segmentation** | Cluster Analysis | ¿Qué segmentos naturales existen entre los clientes? | 4–5 clusters con comportamiento distinto; un segmento High-Value genera una parte desproporcionada de ingresos. | [Ver caso →](./case-03-cluster-analysis) |

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

