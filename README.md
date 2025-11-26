# Deep Learning Para El Procesamiento Del Lenguaje Natural

## Descripción

El objetivo de esta actividad es que el estudiante demuestre la capacidad de seleccionar, configurar y ejecutar el ajuste fino (fine-tuning) de un Modelo de Lenguaje (LM) preentrenado para una tarea específica de Procesamiento del Lenguaje Natural (NLP).

## Fecha y evaluación

La práctica es individual, debe entregarse antes del miércoles, 26 de noviembre de 2025, a las 10:00 a.m. Este proyecto práctico aporta un 10% a la nota final de la asignatura, sin nota mínima requerida (la entrega es opcional).

## Enunciado Abierto

Se solicita la implementación de un proyecto completo de ajuste fino de un LM. La elección del modelo base, la técnica de ajuste y el dataset de NLP a utilizar son libres, con las siguientes condiciones fundamentales:

- Se presenta un proyecto distinto los ya cubiertos en los notebooks del material de clase: clasificación de texto con una entrada mediante BERT o ajuste supervisado de Llama con QLORA.
- QUEDA PROHIBIDO presentar trabajos que hayan sido utilizados, o se vayan a utilizar, en cualquier otra asignatura de esta u otras titulaciones.

## Requisitos y Formato de Entrega

La práctica debe entregarse a través del medio oficial de la asignatura antes de la fecha y hora límite. La entrega debe constar de dos ficheros idénticos en contenido, pero en formato distinto:

- Apellido1_Apellido2_Nombre.ipynb: El notebook de Jupyter funcional. Se recomienda incluir enlaces (por ejemplo, a Google Drive o Hugging Face) para permitir la ejecución en Google Colab sin necesidad de cargar archivos locales.
- Apellido1_Apellido2_Nombre.pdf: Una impresión en PDF del notebook anterior.

El notebook debe documentarse en secciones de texto (Markdown), replicando el estilo de los notebooks del material de clase. El documento debe incluir, como mínimo, las siguientes secciones:

- Datos del Alumno y Título del Proyecto.
- Introducción: Descripción de la tarea de NLP, justificación de la elección del LM y la técnica de ajuste
  fino.
- Dataset: Descripción, fuente, estadísticas y preprocesamiento de los datos.
- Implementación: Código de carga del LM, detalles de los hiperparámetros de entrenamiento y
  ejecución del ajuste fino.
- Resultados y Discusión: Presentación de las métricas de evaluación obtenidas y un análisis crítico de
  los resultados y limitaciones.
- Conclusiones.

## Export environment

```
conda env export --from-history > environment.yml
```

## Recreate environment

```
conda env create -f environment.yml -p ./.conda
```
