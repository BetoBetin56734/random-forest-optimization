# Random Forest Optimization

Este repositorio contiene un proyecto de optimización de un modelo de Random Forest Regressor utilizando GridSearchCV y RandomizedSearchCV. El objetivo principal es predecir la variable Speed a partir de los atributos de un conjunto de datos de personajes ficticios.

## 📁 Contenido del repositorio

- **random_forest_optimization.ipynb**: Cuaderno con todo el código para cargar datos, entrenar el modelo, optimizar hiperparámetros y evaluar el desempeño del modelo.
- **best_random_forest_model.pkl**: Modelo entrenado con los mejores hiperparámetros obtenidos a través de RandomizedSearchCV.
- **LICENSE**: Licencia MIT que permite el uso, modificación y distribución del código.
- **README.md**: Explicación del contenido del repositorio, los datos utilizados y los resultados obtenidos.

## 📊 Datos utilizados

Los datos utilizados provienen de la base pública disponible en el siguiente enlace:

[Characters Stats Dataset](https://raw.githubusercontent.com/BetoBetin56734/BaseAprendizajeAutomatico/refs/heads/main/charcters_stats.csv)

### Columnas principales:
- *Características numéricas*: Intelligence, Strength, Durability, Power, Combat.
- *Variable categórica*: Alignment (codificada como dummy variables).
- *Variable objetivo*: Speed.

## ⚙ Resultados

### Modelos evaluados:

- *Modelo Base Random Forest*:
  - *MSE en prueba*: 304.47

- *Optimización con GridSearchCV*:
  - *Mejores hiperparámetros*: {'max_depth': 5, 'min_samples_split': 2, 'n_estimators': 50}
  - *MSE en validación cruzada*: 283.39
  - *MSE en prueba*: 287.83

- *Optimización con RandomizedSearchCV*:
  - *Mejores hiperparámetros*: {'n_estimators': 300, 'min_samples_split': 8, 'min_samples_leaf': 2, 'max_features': 'sqrt', 'max_depth': None}
  - *MSE en validación cruzada*: 276.39
  - *MSE en prueba*: 270.61 (Mejor modelo)

### Mejor modelo:
El modelo optimizado con *RandomizedSearchCV* tiene el mejor desempeño y está guardado como best_random_forest_model.pkl.

## 🛠 Reproducir el análisis

1. Clona este repositorio:
   ```bash
   git clone https://github.com/[TuUsuario]/random-forest-optimization.git
