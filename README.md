# Analítica de Datos para la Detección Temprana del Riesgo Cardiovascular

Proyecto académico de la asignatura **Gestión de Proyectos de Datos**, orientado al análisis de información clínica y al desarrollo de modelos de Machine Learning para la detección de enfermedad cardíaca. El trabajo utiliza el conjunto de datos `controles_cardiovasculares_los_robles.csv` e implementa las etapas analíticas de la metodología **CRISP-DM** hasta la evaluación de modelos.

## Objetivo de la implementación técnica

Desarrollar y comparar modelos de **clasificación binaria** que predigan la presencia (`target = 1`) o ausencia (`target = 0`) de enfermedad cardíaca, priorizando el *recall* de la clase positiva para reducir los falsos negativos.

Los algoritmos implementados son **Árbol de Decisión** y **Random Forest**, con selección del modelo a partir de sus métricas de evaluación.

## Estructura del repositorio

```text
.
├── data/
│   └── controles_cardiovasculares_los_robles.csv
├── docs/                     # Documentación de apoyo
├── modelos/                  # Directorio reservado para artefactos de modelos
├── notebooks/
│   └── deteccion_riesgo_cardiovascular.ipynb
├── resultados/
│   └── plots/                # Gráficos del análisis y la evaluación
├── src/                      # Directorio reservado para código reutilizable
├── requirements.txt          # Dependencias para ejecutar el notebook
└── README.md
```

## Requisitos de software

| Función | Tecnología |
|---|---|
| Lenguaje | Python (el notebook registra la versión 3.13.1) |
| Análisis y manipulación de datos | `pandas`, `numpy` |
| Machine Learning | `scikit-learn` |
| Visualización | `matplotlib`, `seaborn` |
| Entorno de ejecución | `JupyterLab`, `ipykernel` |
| Control de versiones | `Git` |

Las bibliotecas utilizadas se enumeran en `requirements.txt`. Sus versiones exactas deben registrarse tras comprobar una ejecución completa en el entorno elegido.

## Instalación y ejecución

Es recomendado, pero no obligatorio, comprobar la ejecución desde un entorno limpio para acreditar la reproducibilidad técnica. Sin embargo, el proyecto se puede ejecutar en un entorno existente.


**1. Clonar el repositorio:**

```bash
git clone https://github.com/david-ramirezl/deteccion-riesgo-cardiovascular.git
cd deteccion-riesgo-cardiovascular
```

**2. Crear y activar un entorno virtual (recomendado):**

En Windows PowerShell:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

En macOS o Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

**3. Instalar las dependencias:**

```bash
python -m pip install -r requirements.txt
```

**4. Iniciar JupyterLab:**

```bash
jupyter lab
```

Abrir `notebooks/deteccion_riesgo_cardiovascular.ipynb` y ejecutar las celdas en orden, desde el inicio.

## Fuente de datos

El archivo utilizado es **`controles_cardiovasculares_los_robles.csv`**. Una copia se encuentra en `data/` dentro del repositorio.

La versión actual del notebook carga los datos desde:

[controles_cardiovasculares_los_robles.csv — fuente utilizada por el notebook](https://raw.githubusercontent.com/david-ramirezl/data/refs/heads/main/controles_cardiovasculares_los_robles.csv)

## Contenido del notebook

El desarrollo sigue las siguientes etapas de **CRISP-DM**:

1. **Comprensión del negocio:** contexto, objetivos y enfoque del análisis.
2. **Comprensión de los datos:** descripción de variables y análisis exploratorio (EDA).
3. **Preparación de los datos:** revisión y transformación de características para el modelado.
4. **Modelado:** entrenamiento y optimización de Árbol de Decisión y Random Forest.
5. **Evaluación:** métricas de clasificación, matrices de confusión, curvas ROC-AUC y comparación de modelos.

El notebook concluye con la interpretación de resultados y selección del modelo.

## Autores

- David Ramírez Luna
- Felipe Huincaman
