# Análisis estadístico sobre hábitos saludables en jóvenes universitarios

Este repositorio aloja el proyecto del **Módulo 5: Inferencia Estadística**, perteneciente al **"Bootcamp Fundamentos de Ciencias de Datos 2026"** de **Talento Digital para Chile - SENCE**.

## Introducción

El equipo de investigación, asumiendo el rol de analistas de datos, ha sido convocado por el área de salud universitaria de una institución pública. El objetivo principal es analizar los factores que influyen en los hábitos de sueño, alimentación y actividad física en jóvenes universitarios. Con base en esto, pretendemos identificar patrones comunes, causas probables y generar un informe científico validado empíricamente que oriente la creación de nuevas políticas de bienestar estudiantil, demostrando el aprendizaje integral de las herramientas de Inferencia Estadística.

## Estructura del Proyecto

Los siguientes archivos forman el núcleo del desarrollo del análisis:

- [`main.ipynb`](main.ipynb): Es el cuaderno interactivo principal donde se lleva a cabo todo el análisis, la generación de código y simulaciones probabilísticas, paso a paso, abarcando todas las lecciones del Módulo 5.
- [`technical_report.md`](technical_report.md): Informe técnico con el resumen ejecutivo de los hallazgos, explicaciones empíricas y recomendaciones.
- `data/simulated_students_health.csv`: Conjunto de datos base, generado sintéticamente en la Lección 2 del cuaderno, para evaluar la probabilidad, teoremas y ejecutar las inferencias estadísticas.

## Requisitos y Tecnologías

El proyecto fue desarrollado utilizando el entorno estándar de Python para análisis de datos científicos, con las siguientes bibliotecas:

- `numpy`: Para simulación numérica y operaciones estructurales.
- `pandas`: Para el modelado y manipulación del dataset estructurado.
- `scipy`: Herramienta central para las funciones probabilísticas, simulaciones de distribuciones y estadísticos de prueba (T-test).
- `matplotlib` y `seaborn`: Para la graficación y representación visual comparativa de distribuciones e histogramas.
- `ipykernel`: Para la ejecución del cuaderno en entorno Jupyter / VS Code.

---

## Instalación y Despliegue Local

### 1. Clonar el repositorio

```bash
git clone https://github.com/c-mena/dsb26-statistical-inference
cd dsb26-statistical-inference
```

### 2. Crear e inicializar el entorno virtual con `uv`

Para asegurar la máxima reproducibilidad y eficiencia en la gestión de entornos, se recomienda usar [uv](https://docs.astral.sh/uv/). Esto ayuda aislar y no contaminar tu versión global de Python de forma extremadamente veloz.

```bash
uv venv
```

### 3. Activar el entorno virtual

```bash
# Windows
.venv\Scripts\activate

# macOS / Linux
source .venv/bin/activate
```

### 4. Instalar dependencias

Recomendamos instalar y sincronizar las bibliotecas requeridas utilizando el archivo `pyproject.toml` incluido en el proyecto, garantizando operar con las dependencias exactas y probadas:

```bash
uv sync
```

### 5. Ejecutar el proyecto

La alternativa recomendada para inicializar y observar el proyecto es emplear **Visual Studio Code (VS Code)** con su extensión de **Jupyter** instalada. Sólo debes abrir la carpeta del repositorio en VS Code, seleccionar tu entorno virtual `.venv` como tu Kernel de ejecución, y abrir el archivo `main.ipynb` para ejecutar el código y visualizar sus correspondientes anotaciones en simultáneo.

*(Otra alternativa válida, desde la consola y con tu entorno activo, es ejecutar el comando `jupyter notebook` para levantar el servidor y entrar a `main.ipynb` directamente mediante tu navegador web).*

---
