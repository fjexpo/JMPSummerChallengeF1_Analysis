<div align="center">

# 🏎️💨 JMP Summer Challenge: F1 Race Strategy Analysis 🏁

### _Análisis Predictivo del Ritmo de Carrera en la Fórmula 1_

</div>

<div align="center">

<!-- Banner: Crea una imagen de 1280x400px, súbela a imgur.com o similar y pega el enlace aquí -->
<img src="https://i.imgur.com/your-banner-image.png" alt="Project Banner">

</div>

---

### **Autor: [Tu Nombre] (`fjexpo`)**
[![LinkedIn](https://img.shields.io/badge/LinkedIn-fjexpo-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/tu-perfil/)  [![GitHub](https://img.shields.io/badge/GitHub-fjexpo-lightgrey?style=flat&logo=github)](https://github.com/fjexpo)

---

## 🎯 1. Resumen del Proyecto

Este repositorio documenta un análisis profundo de datos de carrera de Fórmula 1, realizado para el **JMP Summer Challenge**. El objetivo principal fue trascender el análisis de promedios para construir un **modelo predictivo robusto 🤖**, capaz de cuantificar los factores clave que determinan el tiempo de vuelta en condiciones de carrera.

El proyecto se abordó desde dos frentes, combinando lo mejor de ambos mundos:

*   **JMP Standard 📊:** Para una exploración visual rápida, limpieza de datos interactiva y modelado inicial.
*   **Python (Scikit-Learn & Pandas) 🐍:** Para replicar el análisis, asegurando la reproducibilidad y demostrando un control detallado del flujo de trabajo.

El modelo final, validado rigurosamente, logró explicar el **72.97%** de la variabilidad en los tiempos de vuelta, desvelando insights cruciales para la estrategia de carrera.

---

## 📂 2. Estructura del Repositorio

```
JMPSummerChallengeF1_Analysis/
│
├── 📁 data/
│   └── 📄 JMPSummerChallengeDataset.csv     # Conjunto de datos original
│
├── 📁 notebooks/
│   └── 📓 F1_Lap_Time_Prediction_Analysis.ipynb # Notebook con el análisis en Python
│
├── 📁 reports/
│   └── 📈 JMP_Summer_Challenge_Report.pdf   # Informe visual del proyecto
│
├── 📄 .gitignore
├── 📄 README.md
└── 📄 requirements.txt
```

---

## 🛠️ 3. Metodología y Herramientas

El análisis se basó en un flujo de trabajo disciplinado para garantizar resultados fiables y de alta calidad.

| Paso | Descripción | Herramientas Clave |
| :--- | :--- | :--- |
| **1. Limpieza de Datos** | 🧹 Se aplicó un filtro para aislar el ritmo puro, excluyendo vueltas anómalas (pits, SC, etc.). | `JMP Data Filter`, `pandas` |
| **2. Ingeniería de Características** | 🔬 Se creó la variable `LapsOnStint` para medir la degradación de forma consistente. | `JMP Formula Editor`, `pandas .groupby().cumcount()` |
| **3. Modelado Predictivo** | 🧠 Se construyó un modelo de **Regresión Lineal Múltiple** para predecir `LapTimeSeconds`. | `JMP Fit Model`, `scikit-learn LinearRegression` |
| **4. Validación Robusta** | 🛡️ El dataset se dividió en **75% Entrenamiento / 25% Validación** para evitar sobreajuste y medir el rendimiento real. | Proceso manual en JMP, `train_test_split` en Python |

---

## 🏆 4. Resultados y Conclusiones Clave

El modelo final demostró ser robusto y útil, con un **RSquare de 72.97%** en el conjunto de datos de validación. Los hallazgos más importantes son:

| Conclusión | Descripción Detallada | Insight Estratégico |
| :--- | :--- | :--- |
| **1. 👨‍✈️ El Talento del Piloto es Rey** | El `Driver` y las `Velocidades` en pista son los predictores estadísticamente dominantes. El modelo cuantifica el "delta" de ritmo base entre pilotos, incluso controlando por el coche. | Permite una evaluación objetiva del rendimiento del piloto y la identificación de sus puntos fuertes en el circuito. |
| **2. 🛞 El Efecto del Neumático es Indirecto** | La degradación (`LapsOnStint`) y el compuesto (`Compound`) no son dominantes estadísticamente *porque* su efecto se manifiesta a través de la velocidad que el piloto puede mantener. | El modelo nos enseña a mirar la velocidad en curva como el mejor indicador del estado real de los neumáticos. |
| **3. 🧠 Modelo como Herramienta Estratégica** | El modelo permite simular escenarios "what-if". Podemos cuantificar el delta de rendimiento entre compuestos y estimar el "punto de inflexión" para una parada en boxes óptima. | Transforma la estrategia de carrera de una intuición a un cálculo preciso y basado en datos. |

---

## 🚀 5. Cómo Ejecutar el Código

Para poner en marcha el análisis en Python, sigue estos pasos:

1.  **Clona el repositorio:**
    ```bash
    git clone https://github.com/fjexpo/JMPSummerChallengeF1_Analysis.git
    cd JMPSummerChallengeF1_Analysis
    ```

2.  **Crea y activa un entorno virtual (recomendado):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # En Windows: venv\Scripts\activate
    ```

3.  **Instala las dependencias:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Lanza Jupyter y explora el notebook:**
    ```bash
    jupyter notebook
    ```
    Navega a la carpeta `notebooks/` y abre el archivo `F1_Lap_Time_Prediction_Analysis.ipynb`.

---
<div align="center">

_¡Gracias por revisar este proyecto! El análisis de datos es la nueva carrera por la pole position._

</div>
