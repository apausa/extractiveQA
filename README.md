# Fine-tuning DistilBERT for Extractive Question Answering Using Stanford QA Dataset with Sliding Window Preprocessing

To do: 
- La posibilidad de cambiar el dataset
- la posibilidad de cambiar el modelo
- Ver también el accuracy del modelo base (sin fine-tuning)
- Cambiar la parte de los ejemplos
- Cambiar el markdown para que tenga relación con web science

Este proyecto demuestra el fine-tuning de DistilBERT para el _extractive question-answering_ usando el Stanford Question Answering Dataset (SQuAD) con preprocesamiento de ventanas deslizantes. A diferencia de los enfoques generativos que crean texto, esta tarea identifica y extrae el fragmento exacto del texto a partir del contexto en el que se enmarca una pregunta.

## DistilBERT

Se ha seleccionado DistilBERT en lugar de modelos como BERT por razones de eficiencia computacional: al desarrollar desde cero es importante valorar la capacidad para iterar rápido y hacer muchas pruebas. DistilBERT es una versión destilada que retiene el 97% del rendimiento de BERT mientras reduce el número de parámetros en un 40% y aumenta la eficiencia en un 60% **(Sanh et al., 2020)**. Esta optimización permite entrenar el modelo de manera más rápida sin sacrificar calidad en las predicciones.

Las arquitecturas basadas exclusivamente en codificador como BERT, destacan al responder cuestiones directas, pero presentan limitaciones ante preguntas abiertas (para estas situaciones que requieren elaboración, las arquitecturas de codificador-decodificador resultan más apropiadas ya que pueden generar respuestas más elaboradas).

## *Fine-tuning*

El _fine-tuning_ consiste en adaptar un modelo preentrenado a una tarea específica para mejorar su rendimiento. En este caso, mientras que el preentrenamiento le proporciona al modelo una comprensión general del lenguaje, el _fine-tuning_ lo especializa para identificar las posiciones de inicio y fin de las respuestas dentro de un contexto dado, **consiguiendo un 77.22% en EM y 85.34% de F1 accuracy**.

## Estructura

El notebook se estructura en las siguientes fases:

- **3. Preparación de los datos**: SQuAD, preprocesamiento con ventanas deslizantes, mantenimiento de alineación de carácter a token y generación de etiquetas a nivel de token.
- **4. Entrenamiento**: Ajuste fino de DistilBERT para predecir fragmentos de respuesta sobre 87,735 características en aproximadamente 40.5 minutos.
- **5. Evaluación**: Posprocesamiento de predicciones, agregación de características, cálculo de métricas de SQuAD.
- **6. Análisis de Rendimiento**: Demostración de mejora sobre el modelo base en preguntas específicas sobre las diapositivas de clase.
