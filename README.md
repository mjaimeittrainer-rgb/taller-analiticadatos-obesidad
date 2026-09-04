# Taller Práctico de Analítica de Datos: Hábitos de Vida y Niveles de Obesidad

Repositorio práctico centrado en el análisis de datos de salud, alimentación y estilo de vida[cite: 1, 2], diseñado para explorar **qué factores pesan más allá del propio peso y la altura**[cite: 1, 2].

---

## 🎯 Pregunta Clave del Taller

> **¿Qué hábitos de vida y factores sociodemográficos están más asociados con el nivel de obesidad de una persona, más allá del propio peso y la altura?[cite: 1, 2]**

Para responderla de forma rigurosa, el proyecto aborda un problema crítico en ciencia de datos: **la fuga de información (*data leakage*)**[cite: 1, 2]. Se demuestra por qué incluir peso y altura arruina el propósito analítico del modelo al limitarse a recalcular el Índice de Masa Corporal (IMC), contraponiéndolo a un modelo predictivo basado exclusivamente en hábitos y demografía[cite: 1, 2].

---

## 📊 Dataset Utilizado

* **Origen:** *Estimation of Obesity Levels Based on Eating Habits and Physical Condition* (UCI Machine Learning Repository, ID 544)[cite: 1, 2].
* **Muestra:** 2.111 registros de personas de **Colombia, Perú y México** (edades entre 14 y 61 años)[cite: 1, 2]. 
* **Composición:** 23% de datos reales obtenidos mediante encuesta web y 77% de datos sintéticos generados mediante la técnica SMOTE para balancear las clases[cite: 2].
* **Variables (17 atributos + 1 objetivo):** Incluye datos antropométricos (`Gender`, `Age`, `Height`, `Weight`), antecedentes familiares (`family_history_with_overweight`), hábitos alimenticios (`FAVC`, `FCVC`, `NCP`, `CAEC`, `CH2O`, `SCC`, `CALC`), estilo de vida (`SMOKE`, `FAF`, `TUE`, `MTRANS`) y la variable objetivo con 7 categorías de obesidad (`NObeyesdad`)[cite: 1, 2].

---

## 🛠️ Tecnologías y Herramientas

* **Entorno:** Anaconda Web (Jupyter Notebooks en la nube, sin instalaciones locales obligatorias)[cite: 1, 2].
* **Lenguaje:** Python[cite: 1, 2].
* **Librerías principales:** 
  * `pandas` & `numpy` (manipulación y limpieza de datos)[cite: 3]
  * `matplotlib` & `seaborn` (visualización estadística y gráficos de calor/distribución)[cite: 3]
  * `scikit-learn` (codificación, partición de datos, modelos de clasificación `RandomForestClassifier` y métricas)[cite: 3]
  * `ucimlrepo` (descarga automatizada desde el repositorio oficial de la UCI)[cite: 1]

---

## ⚙️ Estructura del Proyecto

1. **Preparación del entorno:** Verificación e importación de librerías en Jupyter[cite: 1, 2].
2. **Adquisición de datos:** Conexión directa a la UCI o mediante respaldo CSV alternativo[cite: 1, 2].
3. **Limpieza y preprocesamiento:** Control de valores nulos, eliminación de duplicados exactos e inspección de rangos cuantitativos[cite: 1, 2].
4. **Análisis Exploratorio de Datos (EDA):** Distribuciones de clases, diagramas de caja del IMC y matrices de correlación[cite: 1, 2].
5. **Ingeniería de características:** Codificación de variables binarias, ordinales y *one-hot encoding* para medios de transporte[cite: 1, 2].
6. **Modelado Comparativo:**
   * **Modelo A (Control):** Incluye peso y altura ($\approx 95.9\%$ de exactitud debido a la fuga de datos por el cálculo directo del IMC)[cite: 2].
   * **Modelo B (Hábitos y Demografía):** Excluye peso, altura e IMC ($\approx 84.0\%$ de exactitud, demostrando que los hábitos contienen una señal predictiva real y útil)[cite: 2].
7. **Importancia de variables:** Extracción de los factores de estilo de vida más determinantes (edad, consumo de vegetales, comidas principales, actividad física, pantallas, agua, género y antecedentes familiares)[cite: 2].

---

## 🚀 Cómo Ejecutar el Taller

1. Clona o descarga este repositorio en tu equipo.
2. Accede a [anaconda.cloud](https://anaconda.cloud) e inicia sesión con tu cuenta gratuita[cite: 1, 2].
3. Abre una sesión de **Jupyter Notebook** en la nube[cite: 1, 2].
4. Sube el archivo del notebook (`Taller_Analitica_Datos_Obesidad.ipynb`)[cite: 1, 2].
5. Ejecuta las celdas de forma secuencial de arriba hacia abajo[cite: 1, 2].

---

## 📈 Conclusiones Principales

* Las intervenciones de salud pública enfocadas en fomentar el consumo de vegetales, el ejercicio físico regular, la reducción del sedentarismo digital y la estructuración de horarios de comidas principal poseen una asociación directa y sólida con niveles de obesidad más bajos[cite: 2].
* Las conclusiones deben interpretarse estrictamente como asociaciones descubiertas dentro de esta muestra poblacional específica y no como leyes causales universales[cite: 2].

---

## 📄 Licencia

Este contenido se distribuye bajo la licencia **Creative Commons Atribución-NoComercial-CompartirIgual 4.0 Internacional (CC BY-NC-SA 4.0)**[cite: 2, 3]. Queda excluido el contenido de terceros (imágenes, logotipos y marcas registradas)[cite: 2, 3].
