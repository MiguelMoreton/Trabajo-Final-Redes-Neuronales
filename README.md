# 🧠 Trabajo Final - Redes Neuronales

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-ee4c2c?style=for-the-badge&logo=pytorch)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter)
![Optuna](https://img.shields.io/badge/Optuna-Optimization-purple?style=for-the-badge)

</div>

---

## 📌 Descripción

Este repositorio contiene el desarrollo de mi **Trabajo Final de Redes Neuronales**, centrado en la creación, entrenamiento y comparación de diferentes modelos de Deep Learning para un problema de **clasificación multiclase de imágenes**.

A lo largo del proyecto se prueban distintas arquitecturas y técnicas de entrenamiento, empezando por redes **Fully Connected** y evolucionando hacia modelos convolucionales tipo **ResNet18**, junto con optimización de hiperparámetros mediante **Optuna**.

El objetivo final es entrenar un modelo capaz de generar predicciones sobre un conjunto de test y guardarlas en formato `.npz`.

---

## 🚀 Objetivos del proyecto

- Implementar modelos de redes neuronales con **PyTorch**.
- Comparar diferentes arquitecturas.
- Aplicar técnicas de preprocesamiento y transformación de datos.
- Mejorar el entrenamiento mediante optimizadores y schedulers.
- Utilizar **Optuna** para búsqueda de hiperparámetros.
- Guardar el mejor modelo entrenado.
- Generar predicciones finales sobre datos de test.

---

## 🧠 Modelos desarrollados

Durante el proyecto se han explorado varias aproximaciones:

### 🔹 Redes Fully Connected

Modelos densos utilizados como primera aproximación al problema.

Notebooks principales:

- `Fully_Connected.ipynb`
- `Fully_Connected_torchTransforms.ipynb`
- `Fully_Connected_torchTransformsAdamyPlateau.ipynb`
- `Fully_Connected_torchTransformsAdamyPlateauyOptuna.ipynb`

---

### 🔹 Modelos tipo ResNet18

Posteriormente se desarrollan modelos convolucionales inspirados en **ResNet18**, más adecuados para trabajar con imágenes y extraer patrones espaciales.

Notebooks principales:

- `ResNet18_1.0.ipynb`
- `ResNet18_2.0.ipynb`
- `ResNet18_3.0.ipynb`
- `ResNet18_4.0.ipynb`
- `ResNet18_4.0_optuna.ipynb`

---

### 🔹 Modelo final

El mejor modelo entrenado se guarda en:

```text
Best_model.pth
```

Y se utiliza posteriormente para generar las predicciones finales mediante el notebook:

```text
Prediccion_Y_pred_GELU_manual.ipynb
```

---

## 📂 Estructura del repositorio

```text
.
├── Fully_Connected.ipynb
├── Fully_Connected_torchTransforms.ipynb
├── Fully_Connected_torchTransformsAdamyPlateau.ipynb
├── Fully_Connected_torchTransformsAdamyPlateauyOptuna.ipynb
│
├── ResNet18_1.0.ipynb
├── ResNet18_2.0.ipynb
├── ResNet18_3.0.ipynb
├── ResNet18_4.0.ipynb
├── ResNet18_4.0_optuna.ipynb
│
├── Prediccion_Y_pred_GELU_manual.ipynb
├── Best_model.pth
│
├── X_train.npz
├── Y_train.npz
├── X_test.npz
├── Y_pred.npz
└── README.md
```

---

## 📊 Datos

El proyecto trabaja con archivos en formato `.npz`:

| Archivo | Descripción |
|---|---|
| `X_train.npz` | Datos de entrenamiento |
| `Y_train.npz` | Etiquetas de entrenamiento |
| `X_test.npz` | Datos de test |
| `Y_pred.npz` | Predicciones finales generadas por el modelo |

---

## ⚙️ Tecnologías utilizadas

- Python
- PyTorch
- Torchvision
- NumPy
- Scikit-learn
- Matplotlib
- Optuna
- Jupyter Notebook

---

## 🛠️ Instalación

Clona el repositorio:

```bash
git clone https://github.com/MiguelMoreton/Trabajo-Final-Redes-Neuronales.git
cd Trabajo-Final-Redes-Neuronales
```

Instala las dependencias principales:

```bash
pip install numpy torch torchvision matplotlib scikit-learn optuna jupyter
```

Abre Jupyter Notebook:

```bash
jupyter notebook
```

---

## ▶️ Ejecución

Para seguir el desarrollo completo del proyecto, se recomienda revisar los notebooks en este orden:

```text
1. Fully_Connected.ipynb
2. Fully_Connected_torchTransforms.ipynb
3. Fully_Connected_torchTransformsAdamyPlateau.ipynb
4. Fully_Connected_torchTransformsAdamyPlateauyOptuna.ipynb
5. ResNet18_1.0.ipynb
6. ResNet18_2.0.ipynb
7. ResNet18_3.0.ipynb
8. ResNet18_4.0.ipynb
9. ResNet18_4.0_optuna.ipynb
10. Prediccion_Y_pred_GELU_manual.ipynb
```

Para generar las predicciones finales:

1. Asegúrate de tener `Best_model.pth` y `X_test.npz` en el directorio raíz.
2. Ejecuta el notebook `Prediccion_Y_pred_GELU_manual.ipynb`.
3. Se generará el archivo `Y_pred.npz`.

---

## 📈 Predicción final

Las predicciones finales se guardan en:

```text
Y_pred.npz
```

El archivo contiene una matriz con las probabilidades asignadas por el modelo a cada clase.

Se puede cargar con:

```python
import numpy as np

data = np.load("Y_pred.npz")
Y = data["Y"]

print(Y.shape)
```

---

## 🧪 Flujo del proyecto

```text
Datos
  ↓
Preprocesamiento
  ↓
Modelo Fully Connected
  ↓
Mejoras con transforms y regularización
  ↓
Modelos ResNet18
  ↓
Optimización con Optuna
  ↓
Selección del mejor modelo
  ↓
Predicción final
```

---

## 🎯 Aprendizajes

Este proyecto me ha permitido trabajar de forma práctica con conceptos clave de Deep Learning:

- Diseño de arquitecturas neuronales.
- Entrenamiento de modelos con PyTorch.
- Comparación experimental entre modelos.
- Uso de redes convolucionales para imágenes.
- Regularización y mejora del entrenamiento.
- Optimización de hiperparámetros.
- Exportación de modelos y predicciones.

---

## 👤 Autor

**Miguel Moretón**

Trabajo Final de la asignatura **Redes Neuronales**.

---

## 📄 Licencia

Este proyecto no especifica una licencia actualmente.
