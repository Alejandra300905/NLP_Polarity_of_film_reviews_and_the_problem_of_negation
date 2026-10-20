
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

## 📚 Referencias
* Corpus: [IMDb Large Movie Review Dataset](https://ai.stanford.edu/~amaas/data/sentiment/)
