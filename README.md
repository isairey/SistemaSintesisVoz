<div align="center">

<img width="220" src="https://cdn-icons-png.flaticon.com/512/4712/4712109.png" />

# 🎙️ TransformerTTS

### Sistema de Síntesis de Voz basado en Transformers y TensorFlow 2 🚀

<p align="center">
  <b>TransformerTTS</b> es una implementación moderna de Text-to-Speech (TTS) basada en arquitecturas Transformer no autoregresivas, diseñada para generar voz natural, rápida y controlable mediante redes neuronales profundas.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/TensorFlow-2.x-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white">
  <img src="https://img.shields.io/badge/Transformer-TTS-blueviolet?style=for-the-badge">
  <img src="https://img.shields.io/badge/Python-AI-3776AB?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/DeepLearning-Speech-green?style=for-the-badge">
</p>

<p align="center">
  <a href="#-acerca-del-proyecto">Acerca</a> •
  <a href="#-características">Características</a> •
  <a href="#-arquitectura-del-sistema">Arquitectura</a> •
  <a href="#-tecnologías-utilizadas">Tecnologías</a> •
  <a href="#-instalación">Instalación</a>
</p>

</div>

---

# 🌌 Acerca del proyecto

**TransformerTTS** es una solución avanzada de síntesis de voz desarrollada con TensorFlow 2 que transforma texto en habla natural utilizando arquitecturas Transformer de última generación.

El proyecto toma inspiración de investigaciones reconocidas como:

* Neural Speech Synthesis with Transformer Network
* FastSpeech
* FastSpeech 2
* FastPitch

Su diseño no autoregresivo permite una generación de voz significativamente más rápida que modelos tradicionales, manteniendo una alta calidad y estabilidad durante la inferencia.

---

# ✨ Características

## 🎙️ Conversión Texto a Voz

* Conversión de texto en audio natural
* Síntesis neuronal de voz
* Generación de espectrogramas Mel
* Compatible con múltiples vocoders
* Soporte para inferencia rápida

---

## ⚡ Arquitectura No Autoregresiva

* Mayor velocidad de inferencia
* Eliminación de repeticiones
* Atención más estable
* Menor tiempo de procesamiento
* Mejor escalabilidad

---

## 🎚️ Control de Voz

* Control de velocidad de habla
* Ajuste de tono (Pitch)
* Duraciones personalizadas
* Generación flexible de audio
* Producción de voz más natural

---

## 🔊 Compatibilidad con Vocoders

* MelGAN
* HiFiGAN
* WaveRNN (versiones anteriores)

Permite transformar espectrogramas generados por el modelo en audio de alta calidad.

---

# 🧠 Arquitectura del sistema

## 🤖 Aligner Model

Módulo encargado de aprender la alineación entre texto y audio.

### Funcionalidades

* Extracción de duraciones
* Alineación fonética
* Procesamiento previo al entrenamiento
* Optimización de sincronización

---

## 🎙️ Forward Transformer

Modelo principal encargado de la síntesis de voz.

### Funcionalidades

* Generación de espectrogramas Mel
* Predicción de pitch
* Control de velocidad
* Producción de voz paralela

---

## 🔊 Vocoder Layer

Convierte espectrogramas Mel en audio reproducible.

### Compatibilidad

* MelGAN
* HiFiGAN
* Griffin-Lim
* WaveRNN

---

# 🚀 Ventajas del modelo

## ⚡ Fast Speech Generation

* Inferencia paralela
* Baja latencia
* Producción eficiente

---

## 🛡️ Robustez

* Menos errores de atención
* Menos repeticiones
* Mejor estabilidad

---

## 🎛️ Controlabilidad

* Modificación del pitch
* Control de duración
* Ajuste de velocidad

---

# 🛠️ Tecnologías utilizadas

## 🤖 Inteligencia Artificial

<p>
  <img src="https://skillicons.dev/icons?i=tensorflow,python" />
</p>

* TensorFlow 2
* Deep Learning
* Transformers
* Neural Networks

---

## 🎵 Procesamiento de Audio

* Mel Spectrograms
* Speech Synthesis
* Vocoders
* Audio Reconstruction

---

## 🧰 Herramientas

<p>
  <img src="https://skillicons.dev/icons?i=git,github,vscode" />
</p>

* Git
* GitHub
* VS Code
* TensorBoard

---

# 📂 Estructura del proyecto

```bash
TransformerTTS/
│
├── config/
│   ├── training_config.yaml
│
├── data/
│   ├── audio.py
│   ├── metadata_readers.py
│
├── model/
│   ├── factory.py
│   ├── models.py
│
├── notebooks/
│
├── docs/
│
├── create_training_data.py
├── train_aligner.py
├── train_tts.py
├── predict_tts.py
├── extract_durations.py
├── requirements.txt
└── README.md
```

---

# 📚 Dataset

## 🎵 LJSpeech Dataset

El proyecto utiliza principalmente el conjunto de datos LJSpeech para entrenar modelos de síntesis de voz.

### Contenido

* Archivos WAV
* Transcripciones
* Metadatos
* Información fonética

---

## 📂 Estructura esperada

```bash
dataset_folder/
│
├── metadata.csv
└── wavs/
    ├── file1.wav
    ├── file2.wav
    └── ...
```

---

# ⚡ Instalación

## 📋 Requisitos

* Python 3.6+
* TensorFlow 2
* Git
* Espeak
* Pip

---

# 🚀 Configuración del proyecto

## 1️⃣ Clonar repositorio

```bash
git clone https://github.com/as-ideas/TransformerTTS.git
```

---

## 2️⃣ Entrar al proyecto

```bash
cd TransformerTTS
```

---

## 3️⃣ Instalar Espeak

Ubuntu/Debian:

```bash
sudo apt-get install espeak
```

macOS:

```bash
brew install espeak
```

---

## 4️⃣ Instalar dependencias

```bash
pip install -r requirements.txt
```

---

# 🎓 Entrenamiento

## Crear dataset de entrenamiento

```bash
python create_training_data.py --config config/training_config.yaml
```

---

## Entrenar modelo Aligner

```bash
python train_aligner.py --config config/training_config.yaml
```

---

## Extraer duraciones

```bash
python extract_durations.py --config config/training_config.yaml
```

---

## Entrenar modelo TTS

```bash
python train_tts.py --config config/training_config.yaml
```

---

# 🎙️ Predicción

## Desde línea de comandos

```bash
python predict_tts.py -t "Please, say something."
```

---

## Con pesos personalizados

```bash
python predict_tts.py -t "Please, say something." -p /path/to/weights/
```

---

# 📊 Monitoreo

Visualizar métricas de entrenamiento mediante TensorBoard:

```bash
tensorboard --logdir /logs/directory/
```

Permite monitorear:

* Loss
* Attention Maps
* Training Progress
* Learning Curves

---

# 🌟 Funcionalidades principales

## 🎙️ Síntesis de voz neuronal

* Text-to-Speech
* Espectrogramas Mel
* Generación paralela
* Producción de audio natural

---

## 🤖 Inteligencia Artificial

* Transformers
* Deep Learning
* Pitch Prediction
* Duration Prediction

---

## 🔊 Audio de alta calidad

* MelGAN
* HiFiGAN
* Griffin-Lim
* Audio Reconstruction

---

# 🧠 Objetivos del proyecto

## 🎯 Investigación y desarrollo

* Síntesis de voz moderna
* Modelos Transformer
* Procesamiento de lenguaje natural
* Deep Learning aplicado al audio
* Generación de voz controlable
* Producción de voz en tiempo real

---

# 🚧 Roadmap

## 🔮 Próximas mejoras

* 🌍 Soporte multilenguaje
* 🎙️ Clonación de voz
* 🤖 Integración con LLMs
* ☁️ API en la nube
* 📱 Aplicaciones móviles
* ⚡ Inferencia optimizada GPU
* 🧠 Fine-Tuning personalizado

---

# 🤝 Contribuciones

Las contribuciones son bienvenidas ❤️

## Cómo contribuir

1. Fork del proyecto

```bash
git checkout -b feature/nueva-funcionalidad
```

2. Commit

```bash
git commit -m "✨ Nueva funcionalidad"
```

3. Push

```bash
git push origin feature/nueva-funcionalidad
```

4. Crear Pull Request 🚀

---

# 👨‍💻 Desarrollador original

<div align="center">

## Francesco Cardinale

Investigador y desarrollador enfocado en Deep Learning, Speech Synthesis y arquitecturas Transformer para generación de voz.

</div>

---

# 🙏 Agradecimientos

A los proyectos y comunidades que inspiraron y contribuyeron al desarrollo:

* MelGAN
* HiFiGAN
* WaveRNN
* Mozilla TTS
* TensorFlow Community

---

# 🌟 Apoya el proyecto

⭐ Dale una estrella

🍴 Haz Fork

📢 Comparte el proyecto

🤝 Contribuye con mejoras

---

# 📜 Licencia

Proyecto Open Source distribuido bajo licencia MIT para investigación, aprendizaje y desarrollo de sistemas avanzados de síntesis de voz basados en Inteligencia Artificial.

---

<div align="center">

### 🎙️ TransformerTTS — Generando voces naturales con el poder de los Transformers 🚀

</div>
