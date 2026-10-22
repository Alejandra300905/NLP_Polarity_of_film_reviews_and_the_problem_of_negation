## Análisis de Sentimientos en Reseñas de IMDb
Este proyecto aborda el análisis de sentimientos en reseñas de películas, utilizando técnicas de Procesamiento de Lenguaje Natural (NLP) y modelos de aprendizaje automático para clasificar opiniones como positivas o negativas.

Se trabaja con el conjunto de datos IMDb Large Movie Review Dataset, que contiene reseñas de películas etiquetadas según su polaridad. A partir del texto, se construyen representaciones numéricas que permiten a los modelos identificar patrones asociados con cada sentimiento.

El proyecto comienza con un modelo baseline basado en Naive Bayes Multinomial y evoluciona hacia representaciones de texto y modelos más avanzados, con el propósito de comparar resultados y comprender las ventajas y limitaciones de distintos enfoques.

---
## El problema de la negación

Uno de los desafíos del análisis de sentimientos es que el significado de una expresión depende del contexto y del orden de las palabras.

Por ejemplo, “the movie was good” y “the movie was not good” comparten varias palabras, pero expresan sentimientos diferentes. Una representación basada únicamente en unigramas no modela explícitamente la relación entre las palabras ni cómo la negación modifica el significado de una expresión.

Por esta razón, el proyecto explora estrategias como el uso de bigramas y el marcado de negación, además de representaciones semánticas mediante vectores de palabras.

---

##  Etapas del Proyecto

### Etapa 1: Análisis, Representación y Baseline
* **Representación:** Bolsa de palabras (BoW) de unigramas (matriz dispersa).
* **Modelo Baseline:** Naive Bayes (MultinomialNB).
* **Métricas:** Exactitud, F1-Score, AUC-ROC.

### Etapa 2: Primera Aproximación
* **Representación:** TF-IDF de unigramas y bigramas + Marcado de negación (heurística `NEG_`).
* **Modelo:** Regresión Logística.

### Etapa 3: Mejora
* **Representación:** Promedio de vectores Word2Vec preentrenados.
* **Modelo:** Perceptrón Multicapa (MLP) con back-propagation.
  
---

## Referencias
* Corpus: [IMDb Large Movie Review Dataset](https://ai.stanford.edu/~amaas/data/sentiment/)
