# TEXT Project: WhatsApp Message Classification & Generation
# AUTHORS: Paula Echamendi & Carmen Miralles 

## Descripción

Este proyecto aplica técnicas de Procesamiento de Lenguaje Natural (NLP) sobre conversaciones reales de WhatsApp con dos objetivos principales:

* Clasificación de mensajes mediante modelos de Machine Learning y Deep Learning
* Generación de texto simulando mensajes y conversaciones entre usuarios

Se abordan tanto enfoques tradicionales (TF-IDF + ML) como modelos secuenciales (LSTM, GRU) y arquitecturas modernas basadas en Transformers.

---

## Objetivos

* Analizar conversaciones reales de WhatsApp
* Clasificar mensajes por usuario
* Comparar modelos de Machine Learning vs Deep Learning
* Generar texto coherente imitando el estilo conversacional
* Evaluar el rendimiento de modelos generativos

---

## Estructura del proyecto

El proyecto está organizado en notebooks secuenciales:

```
.
├── data/                  
├── models/                
│
├── 0. Data Loading.ipynb
├── 1. Data Cleaning & EDA.ipynb
├── 2. Vectorization & Text Representation.ipynb
├── 3. Machine Learning.ipynb
├── 4. Deep Learning.ipynb
├── 5. Generative Models (LSTM & GRU).ipynb
├── 6. Generative Transformers.ipynb
```
## SE OMITE LA SUBIDA DE LA CARPETA 'data/' POR PRIVACIDAD, en caso de querer recrearlo podeis utilizar vuestro propio .txt  exportando un chat de WhatsApp (sin archivos multimedia)

## La carpeta `models/` no se incluye en este repositorio debido a limitaciones de tamaño de GitHub.

### Descripción de cada notebook:

* **0. Data Loading**

  * Carga y estructuración inicial del dataset de WhatsApp

* **1. Data Cleaning & EDA**

  * Limpieza de texto
  * Análisis exploratorio (EDA)
  * Distribución de mensajes y usuarios

* **2. Vectorization & Text Representation**

  * Preparación de datos para clasificación
  * Representación del texto (Bag of words, TF-IDF, ...)

* **3. Machine Learning**

  * Modelos clásicos:

    * Logistic Regression
    * SVM
    * Otros clasificadores
  * Evaluación con métricas y matrices de confusión

* **4. Deep Learning**

  * Modelos secuenciales:

    * RNN
    * LSTM
    * GRU
    
  * Modelos basados en Transformers

* **5. Generative Models (LSTM & GRU)**

  * Entrenamiento de modelos generativos
  * Generación de texto por usuario

* **6. Generative Transformers**

  * Uso de modelos Transformer preentrenados
  * Generación de texto más coherente mediante atención
  * Simulación de conversaciones


---

## Datos

El dataset consiste en conversaciones de WhatsApp entre varios participantes, con las siguientes características:

* Mensajes de texto reales
* Identificación de usuario (persona)
* Timestamp
* Conversaciones multiusuario

Se realiza un proceso de limpieza para:

* Eliminar ruido (símbolos, formatos)
* Normalizar texto
* Preparar secuencias para modelos

---

## Metodología

### Preprocesamiento

* Tokenización
* Padding de secuencias
* Construcción de vocabulario

### Representación del texto

* TF-IDF (modelos clásicos)
* Embeddings (deep learning)

### Modelos de clasificación

* Machine Learning:
  * SVM
  * Regresión logística

* Deep Learning:
  * RNN, LSTM, GRU
  * Modelos basados en Transformers:

    * Fine-tuning de modelos preentrenados (DistilBERT)
    * Clasificación de texto mediante mecanismos de atención
    * Comparación con modelos secuenciales

### Modelos generativos

* LSTM y GRU para generación secuencial
* Transformers para generación avanzada basada en atención

---

## Resultados

* Los modelos de Machine Learning presentan limitaciones debido a la similitud léxica entre clases
* Los modelos de Deep Learning capturan mejor el contexto del lenguaje
* En generación de texto:

  * **GRU** genera frases más coherentes que LSTM
  * Ambos modelos pierden coherencia en secuencias largas
* Los **Transformers** mejoran significativamente la calidad del texto generado

---

## Uso del proyecto

1. Ejecutar los notebooks en orden:

   * Desde `0. Data Loading` hasta `6. Generative Transformers`

2. Requisitos:

```bash
pip install pandas numpy scikit-learn tensorflow keras matplotlib seaborn torch
```

3. (Opcional) Cargar modelos entrenados para generación sin reentrenar

---

## Conclusiones

Este proyecto muestra la evolución de técnicas en NLP:

* Los modelos clásicos funcionan bien como baseline
* El Deep Learning mejora la comprensión contextual
* Los modelos generativos permiten simular lenguaje natural
* Los Transformers representan el estado del arte en generación de texto

Como mejora futura, se podrían:

* Afinar hiperparámetros
* Usar una base de datos más grande
* Incorporar fine-tuning específico del dominio
* Transcribir los mensajes de audio y analizarlos


---

## Autoras
Carmen Miralles & Paula Echamendi
Proyecto académico de NLP aplicado a datos no estructurados.
