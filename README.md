# Comparativa de Modelos para el Pronóstico de Series Temporales
Este proyecto tiene como objetivo comparar diferentes enfoques para el pronóstico de series temporales utilizando conjuntos de datos públicos de los ámbitos de salud pública, financiero y desempeño educativo. Para ello, trabajamos con modelos estadísticos clásicos, modelos de Deep Learning y un modelo basado en Inteligencia Artificial Generativa, con el fin de analizar su desempeño mediante distintas métricas de evaluación e incorporar un componente de explicabilidad que facilitara la interpretación de los resultados obtenidos.

## Objetivo
Evaluar y comparar el desempeño predictivo de modelos estadísticos clásicos, modelos Deep Learning y un modelo basado en Inteligencia Artificial Generativa (Gemini) para el pron+ostico de series temporales en distintos ámbitos de aplicación, con el propósito de identificar sus fortalezas, limitaciones e interpretabilidad utilizando diferentes conjuntos de datos públicos.

## Dataset
Para el desarrollo del proyecto trabajamos con 9 conjuntos de datos publicos organizados en tres ámbitos de aplicación.
### Salud Pública
- Life Expectancy
- Air Quality Data in India
- Health Nutrition and Population Statiscs

### Financiero
- Bitcoin Historical Data
- S&P 500 Historical Prices
- VIX Historical Daily

### Desempeño Educativo
- World Bank Education Statistics
- UNESCO - Tasa de Finalización (Secundaria básica, ambos sexos)
- Times World University Rankings

## Modelos evaluados
### Modelos estadísticos clásicos
- ARIMA
- Prophet

### Modelos de Deep Learning
- LSTM
- Transformer

### Modelo basado en Inteligencia Artificial Generativa
- Gemini mediante prompting estructurado

## Herramientas y tecnologías utilizadas
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- TensorFlow / Keras
- Prophet
- Google Colab
- Jupyter Notebook
- Gemini

## Metodología
Durante el desarrollo del proyecto trabajamos con diferentes conjuntos de datos públicos correspondientes a los ámbitos de salud pública, financiero y desempeño educativo. Este procedimiento se llevó a cabo  en cada uno de los cuadernos que trabajamos para los distintos dataset. Primero investigamos los conjuntos de datos que utilizaríamos, revisando su origen, el significado de cada una de sus variables entre otras características, esto nos permitió comprender mejor la información con la que trabajaríamos antes de comenzar el análisis.
Posteriormente, para casa dataset prepaaramos y realizamos un análisis exploratorio con el fin de conocer su estructura, verificar la calidad de la información y realizar el procesamiento necesario para su análisis. Una vez concluida esta etapa, implementamos los diferentes modelos del pronóstico de series temporales y generamos las predicciones correspondientes para cada conjunto de datos.
Después evaluamos el desempeño de cada modelo utilizando métricas como MAE, RMSE, MAPE y sMAPE, lo que nos permitió realizar una comparación entre los diferentes enfoques. Finalmente, analizamos e interpretamos los resultados obtenidos para identificar el comportamiento de cada modelo y comprender sus fortalezas y limitaciones en función de las caracterísricas de cada conjunto de datos.

## Explicabilidad (XAI)
