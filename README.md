# Análisis de Sentimientos en Tweets con Python

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Programa completo para realizar **análisis de sentimientos** en tweets en español utilizando **NLTK**, **Scikit-learn** y la **API de Twitter**.

## ✨ Características

- 📱 Recolección automática de tweets en tiempo real
- 🔤 Preprocesamiento avanzado de texto en español
- 🤖 Clasificación de sentimientos con Naive Bayes
- 📊 Evaluación completa del modelo (precisión, recall, F1-score)
- ⚡ Pipeline optimizado con Scikit-learn
- 🌍 Soporte completo para texto en español

## 📋 Requisitos Previos

```bash
pip install tweepy nltk scikit-learn pandas
```

**Credenciales de Twitter API necesarias:**
- API Key
- API Secret Key
- Access Token
- Access Token Secret

> **Nota**: Crea una cuenta de desarrollador en [Twitter Developer Portal](https://developer.twitter.com/)

## 🚀 Instalación y Uso

1. **Clona el repositorio**
```bash
git clone https://github.com/tu-usuario/analisis-sentimientos-tweets.git
cd analisis-sentimientos-tweets
```

2. **Configura tus credenciales** en el archivo principal:
```python
API_KEY = 'tu_api_key'
API_SECRET_KEY = 'tu_api_secret_key'
ACCESS_TOKEN = 'tu_access_token'
ACCESS_TOKEN_SECRET = 'tu_access_token_secret'
```

3. **Descarga recursos NLTK**
```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

4. **Ejecuta el programa**
```bash
python analisis_sentimientos.py
```

## 📖 Ejemplo de Salida

```
              precision    recall  f1-score   support
    negativo       0.85      0.82      0.83        50
   positivo       0.84      0.87      0.85        50
    accuracy                           0.84       100
   macro avg       0.84      0.84      0.84       100

Precisión: 0.84

Tweet: Me encanta este producto - Sentimiento: positivo
Tweet: No estoy satisfecho con el servicio - Sentimiento: negativo
```

## 🛠️ Estructura del Proyecto

```
├── analisis_sentimientos.py     # Script principal
├── requirements.txt            # Dependencias
├── README.md                  # Este archivo
└── datos/                     # Carpeta para datasets (opcional)
```

## 🔍 Funcionalidades Técnicas

### 1. **Recolección de Datos**
```python
tweets = obtener_tweets('tu_tema', 100)
```

### 2. **Preprocesamiento**
- Tokenización con NLTK
- Eliminación de stopwords en español
- Normalización a minúsculas
- Filtrado de caracteres no alfabéticos

### 3. **Modelo ML**
- **Vectorizador**: CountVectorizer
- **Clasificador**: Multinomial Naive Bayes
- **Pipeline**: make_pipeline para optimización

### 4. **Evaluación**
- Train/Test split (80/20)
- Classification Report completo
- Accuracy Score

## ⚙️ Personalización

```python
# Cambiar tema de búsqueda
tweets = obtener_tweets('elecciones2026', 500)

# Modificar cantidad de tweets
tweets = obtener_tweets('tu_tema', 1000)

# Usar dataset etiquetado real
df['sentimiento'] = cargar_dataset_etiquetado()
```

## 📈 Mejoras Futuras

- [ ] Integración con Twitter API v2
- [ ] Modelos más avanzados (BERT, RoBERTa)
- [ ] Análisis de emociones múltiples
- [ ] Interfaz web con Streamlit/Flask
- [ ] Guardado automático de datasets
- [ ] Visualizaciones con Matplotlib/Seaborn

## ⚠️ Consideraciones Importantes

1. **API de Twitter**: Respeta los límites de rate limiting
2. **Datos etiquetados**: Usa datasets reales para producción
3. **Privacidad**: No almacenes tweets sin permiso
4. **Idioma**: Optimizado para español, adaptable a otros idiomas

## 📄 Licencia

Este proyecto está bajo la [Licencia MIT](LICENSE). ¡Siéntete libre de usarlo y modificarlo!

## 🤝 Contribuir

¡Contribuciones son bienvenidas! Lee el [CONTRIBUTING.md](CONTRIBUTING.md) para más detalles.

---

**Hecho con ❤️ para la comunidad Data Science en español**
```

¿Te gustaría que ajuste alguna sección específica o agregue más detalles técnicos sobre el modelo de machine learning?
