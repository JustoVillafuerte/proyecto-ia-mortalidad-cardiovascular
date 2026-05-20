# Predicción de la Tasa de Mortalidad por Enfermedades Cardiovasculares en Adultos Mayores de 35 años en EE. UU. (2017)

## 📋 Información del Curso y Grupo
* **Institución:** Universidad Andina del Cusco
* **Facultad:** Ingeniería y Arquitectura
* **Escuela Profesional:** Ingeniería de Sistemas
* **Curso:** Inteligencia Artificial Aplicada
* **Docente:** Felix Estanislao Vargas Quispe
* **Semestre:** 2026-I
* **Grupo:** N° 03

### 👥 Integrantes:
* Revilla Castro Riguel
* Vargas Palma Harley Abanto
* Villafuerte Andrade Justo Cristobher

---

## 📌 Descripción del Proyecto
Este proyecto de inteligencia artificial busca predecir la tasa de mortalidad continua ajustada por edad (por cada 100,000 habitantes) asociada a enfermedades del corazón en los Estados Unidos a nivel poblacional (condados y estados). A diferencia de los enfoques clínicos tradicionales basados en diagnósticos individuales binarios, este modelo integra variables demográficas (sexo, raza/etnia) y geoespaciales (coordenadas geográficas, condados) para aportar una herramienta predictiva útil en la gestión de salud pública y la planificación territorial.

---

## 🏗️ Arquitectura de IA Propuesta
El proyecto se divide en dos fases tecnológicas:
1. **Modelo Base (Fase 1 y 2):** **Random Forest Regressor** (Scikit-Learn). Seleccionado por su capacidad para manejar interacciones no lineales entre variables epidemiológicas y su robustez frente al ruido y desbalance de los datos.
2. **Modelo Avanzado (Fase 2 y 3):** Arquitectura de Deep Learning basada en **Transformers para datos tabulares** (ej. TabTransformer / FT-Transformer) usando TensorFlow/PyTorch, con el fin de capturar dependencias espaciales complejas a través de mecanismos de atención.

### 📊 Métricas de Evaluación:
* Coeficiente de determinación ($R^2$)
* Error Cuadrático Medio (RMSE)
* Error Absoluto Medio (MAE)

---

## 📁 Estructura del Repositorio
* `data/`: Contiene el dataset original en formato CSV provisto por el CDC/NVSS.
* `docs/`: Informes escritos y documentación teórica de cada fase.
* `notebooks/`: Jupyter Notebooks con el código fuente en Python (limpieza de datos, entrenamiento y evaluación).

---

## 🔧 Tecnologías Utilizadas
* **Lenguaje:** Python 3.x
* **Librerías principales:** Scikit-Learn, TensorFlow / PyTorch, Pandas, NumPy, Matplotlib/Seaborn.
* **Control de Versiones:** Git & GitHub

---

## ⚖️ Consideraciones Éticas y Sesgos
* **Privacidad:** El dataset utiliza registros completamente anonimizados y agregados a nivel de condado por el NVSS, garantizando el cumplimiento ético de no identificación.
* **Sesgo de Agregación:** Se reconoce el riesgo de falacia ecológica (aplicar conclusiones poblacionales a nivel clínico individual).
* **Sesgo de Representación:** Se identifica un fuerte desbalance de datos en minorías étnicas (como nativos americanos), lo cual será mitigado mediante técnicas de remuestreo en la Fase 2 para evitar predicciones injustas o imprecisas.
