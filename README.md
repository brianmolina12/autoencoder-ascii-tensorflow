# 🧠 Autoencoders — Compresión, Denoising y Generación

Notebook en TensorFlow/Keras que implementa y compara tres tipos de
autoencoders aplicados a caracteres ASCII de 7×5 píxeles y emojis en
escala de grises.

---

## 📌 ¿Qué hace este proyecto?

### 1. Autoencoder básico (espacio latente 2D)
- Parsea 32 caracteres ASCII desde un archivo `.txt` como matrices binarias 7×5
- Entrena un autoencoder denso con espacio latente de **2 dimensiones**
- Visualiza cómo se distribuyen los caracteres en el espacio latente
- Genera nuevos caracteres interpolando puntos en el espacio latente

### 2. Autoencoder denoising
- Arquitectura más profunda: Dense 32 → 16 → 8 → latente 4
- Agrega ruido aleatorio (5–20%) a los caracteres en cada época
- La red aprende a reconstruir el original limpio desde la versión ruidosa
- Entrenamiento con tasa de aprendizaje variable y checkpoint para continuar

### 3. Autoencoder con emojis
- Extiende el concepto a imágenes 32×32 en escala de grises
- Widget interactivo con ipywidgets para explorar reconstrucciones

---

## 🛠 Tecnologías

- Python · TensorFlow · Keras · NumPy · Matplotlib · Pillow · ipywidgets

---

## 🚀 Cómo ejecutarlo

1. Abrí el notebook en Google Colab
2. Subí el archivo `datos.txt` con los caracteres ASCII
3. Ejecutá las celdas en orden

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1a4c9RJj6_TkgFHwJgzfSPOseR9XXi_oE?usp=sharing)

---

## 📊 Resultados

- El espacio latente 2D permite visualizar agrupaciones semánticas entre caracteres
- El denoising funciona correctamente con hasta ~20% de ruido por píxel
- Con datasets pequeños (32 muestras) la red tiende a memorizar — se documenta
  el comportamiento y las limitaciones encontradas
