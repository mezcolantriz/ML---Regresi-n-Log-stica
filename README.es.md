# Proyecto de Ciencia de Datos

Esta plantilla está diseñada para impulsar proyectos de ciencia de datos proporcionando una configuración básica para conexiones de base de datos, procesamiento de datos, y desarrollo de modelos de aprendizaje automático. Incluye una organización estructurada de carpetas para tus conjuntos de datos y un conjunto de paquetes de Python predefinidos necesarios para la mayoría de las tareas de ciencia de datos.

## Estructura

El proyecto está organizado de la siguiente manera:

- `app.py` - El script principal de Python que ejecutas para tu proyecto.
- `explore.py` - Un notebook para que puedas hacer tus exploraciones, idealmente el codigo de este notebook se migra hacia app.py para subir a produccion.
- `utils.py` - Este archivo contiene código de utilidad para operaciones como conexiones de base de datos.
- `requirements.txt` - Este archivo contiene la lista de paquetes de Python necesarios.
- `models/` - Este directorio debería contener tus clases de modelos SQLAlchemy.
- `data/` - Este directorio contiene los siguientes subdirectorios:
  - `interim/` - Para datos intermedios que han sido transformados.
  - `processed/` - Para los datos finales a utilizar para el modelado.
  - `raw/` - Para datos brutos sin ningún procesamiento.

## Configuración

**Prerrequisitos**

Asegúrate de tener Python 3.11+ instalado en tu máquina. También necesitarás pip para instalar los paquetes de Python.

**Instalación**

Clona el repositorio del proyecto en tu máquina local.

Navega hasta el directorio del proyecto e instala los paquetes de Python requeridos:

```bash
pip install -r requirements.txt
```

# Comprensión Empresarial

## Descripción del Proyecto

Este proyecto tiene como objetivo ayudar al banco portugués a identificar a los clientes con mayor probabilidad de contratar un depósito a largo plazo. Los depósitos a largo plazo permiten a los bancos retener dinero durante un período específico, lo que les permite utilizar esos fondos para mejorar sus inversiones. Las campañas de marketing para este producto se basan en llamadas telefónicas; si un usuario no está disponible en un momento dado, se le volverá a llamar en otro momento.

## Descripción del Problema

El banco portugués está experimentando una disminución en sus ingresos, por lo que desean identificar a los clientes existentes que tienen una mayor probabilidad de contratar un depósito a largo plazo. Esto permitirá enfocar los esfuerzos de marketing en esos clientes y evitará perder tiempo y recursos en aquellos que probablemente no se suscribirán.

Para abordar este problema, se desarrollará un algoritmo de clasificación que ayude a predecir si un cliente contratará o no un depósito a largo plazo.

## Datos

El conjunto de datos se encuentra en el archivo `bank-marketing-campaign-data.csv` y se puede cargar directamente desde el siguiente enlace: https://raw.githubusercontent.com/4GeeksAcademy/logistic-regression-project-tutorial/main/bank-marketing-campaign-data.csv


El conjunto de datos contiene las siguientes variables:

- **age:** Edad del cliente (numérico)
- **job:** Tipo de trabajo (categórico)
- **marital:** Estado civil (categórico)
- **education:** Nivel de educación (categórico)
- **default:** ¿Tiene crédito actualmente? (categórico)
- **housing:** ¿Tiene un préstamo de vivienda? (categórico)
- **loan:** ¿Tiene un préstamo personal? (categórico)
- **contact:** Tipo de comunicación de contacto (categórico)
- **month:** Último mes en el que se le ha contactado (categórico)
- **day_of_week:** Último día en el que se le ha contactado (categórico)
- **duration:** Duración del contacto previo en segundos (numérico)
- **campaign:** Número de contactos realizados durante esta campaña (numérico)
- **pdays:** Número de días desde la última campaña hasta que fue contactado (numérico)
- **previous:** Número de contactos realizados durante la campaña anterior (numérico)
- **poutcome:** Resultado de la campaña de marketing anterior (categórico)
- **emp.var.rate:** Tasa de variación del empleo (numérico, indicador trimestral)
- **cons.price.idx:** Índice de precios al consumidor (numérico, indicador mensual)
- **cons.conf.idx:** Índice de confianza del consumidor (numérico, indicador mensual)
- **euribor3m:** Tasa EURIBOR a 3 meses (numérico, indicador diario)
- **nr.employed:** Número de empleados (numérico, indicador trimestral)
- **y (TARGET):** El cliente contrata un depósito a largo plazo o no (categórico)

## Pasos del Proyecto

### Paso 1: Carga del Conjunto de Datos

Carga el conjunto de datos desde el enlace proporcionado o descárgalo manualmente e inclúyelo en el repositorio.

### Paso 2: Análisis Exploratorio de Datos (EDA)

Realiza un análisis exploratorio completo para:
- Identificar y seleccionar las variables relevantes.
- Eliminar aquellas variables que no aportan información significativa.
- Dividir el conjunto de datos en conjuntos de entrenamiento y prueba, siguiendo las mejores prácticas.

Utiliza el Notebook de ejemplo y adáptalo a este caso de uso.

### Paso 3: Construcción del Modelo de Regresión Logística

Crea un modelo de regresión logística para predecir la probabilidad de que un cliente contrate un depósito a largo plazo. Comienza con los parámetros por defecto y evalúa el rendimiento del modelo.

### Paso 4: Optimización del Modelo

Si los resultados iniciales no son satisfactorios, aplica técnicas de optimización (como ajuste de hiperparámetros o selección de variables) para mejorar el rendimiento del modelo.

## Requisitos

- Python 3.x
- Bibliotecas: `pandas`, `numpy`, `scikit-learn`, `matplotlib`/`seaborn` (u otras para visualización)


