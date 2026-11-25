# Comparativa de Modelos para el Pronóstico de Series Temporales
En este proyecto comparamos distintos enfoques para el pronóstico de series temporales usando conjuntos de datos públicos de salud pública, finanzas y desempeño educativo. Evaluamos modelos estadísticos clásicos, redes de Deep Learning y un modelo de Inteligencia Artificial Gnerativa bajo las mismas condiciones. midiendi su precisión y analizando qué tan fácil es interpretar sus resultados (XAI).

## Objetivo
Evaluar y comparar el desempeño predictivo de modelos estadísticos clásicos, modelos Deep Learning e Inteligencia Artificial Generativa (Gemini 2.5 Flash) en distintos ámbitos de aplicación, identificando sus fortalezas, limitaciones y nivel de interpretabilidad.

## Dataset
Trabajamos con **9 conjuntos de datos publicos** organizados en tres ámbitos de estudio:
### Salud Pública
- **Life Expectancy** Esperanza de vida al nacer en México.
- **Air Quality Data in India** Mediciones diarias de material particulado PM2.5.
- **Health Nutrition and Population Statiscs** Tasa de fertilidad en adolescentes.

### Financiero
- **Bitcoin Historical Data** Precio diario de cierre en USD.
- **S&P 500 Historical Prices** Cotización diaria del índice bursátil.
- **VIX Historical Daily** índice diario de volatilidad del mercado.

### Desempeño Educativo
- **World Bank Education Statistics** Tasa de inscripción en educación primaria.
- **UNESCO - Tasa de Finalización (Secundaria básica, ambos sexos)** Porcentaje de finalización en secundaria básica (ambos sexos).
- **Times World University Rankings** Puntuación longitudinal de instituciones educativas.

## Modelos evaluados
**Modelos estadísticos clásicos**
- Media Móvil Simple
- ARIMA
- Prophet

**Modelos de Deep Learning**
- LSTM
- Transformer

**Modelo basado en Inteligencia Artificial Generativa**
- Gemini mediante *prompting* estructurado (*zero-shot*)

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
Aplicamos el mismo flujo de trabajo de manera independiente en cada uno de los cuadernos correspondientes a los 9 datasets:

1. **Revisión y exploración:** Analizamos el origen y las variables de cada serie, ordenamos los registros cronológicamente y limpiamos valores faltantes.
2. **Preparación:** Realizamos particiones cronológicas estrictas (80 % entrenamiento / 20 % prueba) y escalamos los datos (0 a 1) con ventanas deslizantes de 50 observaciones para las redes neuronales.
3. **Implementación:** Entrenamos y ejecutamos los modelos clásicos, las redes de Deep Learning y las consultas estructuradas hacia Gemini.
4. **Evaluación:** Medimos el error de cada enfoque con **MAE, RMSE, MAPE y sMAPE (%)** para compararlos de forma justa entre distintas escalas.

## Explicabilidad (XAI)
Para complementar las métricas de error, analizamos qué tan transparente es cada familia de modelos:

* **Modelos estadísticos:** Interpretación directa a partir de sus coeficientes, tendencia y estacionalidad.
* **Deep Learning:** Estimación de la importancia de los datos pasados mediante los pesos de la última capa densa.
* **IA Generativa:** Revisión de las explicaciones cualitativas en lenguaje natural generadas junto con cada estimación.

## Resultados
Tomando el **sMAPE (%)** como métrica principal de comparación entre dominios:

* **Salud Pública:** ARIMA logró el menor error en series anuales estables como esperanza de vida (**0.14 %**) y fertilidad (**0.21 %**), mientras que LSTM lideró en calidad del aire (**12.60 %**).
* **Financiero:** Ante alta volatilidad, LSTM obtuvo los mejores resultados en Bitcoin (**1.75 %**) y VIX (**4.29 %**), mientras que Prophet destacó en el S&P 500 (**1.00 %**).
* **Desempeño Educativo:** ARIMA obtuvo errores mínimos en las series anuales de UNESCO (**0.024 %**) y Banco Mundial (**0.29 %**), y LSTM lideró en *Times University Rankings* (**0.42 %**).
* **Gemini 2.5 Flash:** Alcanzó errores muy bajos en pronósticos puntuales de un solo paso (**0.14 %** en Bitcoin), aunque sin acumular incertidumbre multipaso como el resto de modelos.

## Conclusiones
* **No existe un modelo único para todo:** La mejor opción depende de qué tan estable sea la serie y de cuánto se necesite explicar el resultado.
* **Series estables:** En datos anuales con cambios graduales, los modelos clásicos como **ARIMA** son más precisos, ligeros y fáciles de interpretar.
* **Alta volatilidad:** En mercados y variables con cambios bruscos, las redes **LSTM** se adaptan mucho mejor que los métodos tradicionales.
* **Aporte de la IA Generativa:** **Gemini** suma valor al acompañar sus estimaciones con explicaciones claras en lenguaje natural, funcionando como un buen complemento interpretativo.

## Reporte
El repositorio incluye un reporte técnico donde se documenta con mayor detalle la metodología utilizada, el análisis individual por conjunto de datos, las gráficas comparativas y las conclusiones finales del estudio.
