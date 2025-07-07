
# Efficient Speech-to-Text Summarization

![License](https://img.shields.io/badge/license-MIT-green)
![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![Model](https://img.shields.io/badge/model-Wav2Vec2%20%7C%20BERT%20%7C%20BART-yellow)

## 📌 Project Overview

This project presents a complete pipeline for **Speech-to-Text (STT) transcription and summarization** using modern deep learning models. It integrates:

- 🔊 **Wav2Vec2** for speech recognition
- 📄 **BERT-based** extractive summarization
- 🧠 **BART** for abstractive summarization

The hybrid summarization approach ensures factual accuracy (via extraction) and fluency (via abstraction).

---

## 🚀 Features

- 🔁 End-to-end pipeline: audio input to summary output
- 🎯 12.4% Word Error Rate (WER) using fine-tuned Wav2Vec2 on LibriSpeech (dev-clean)
- 📊 Summarization scores:
  - ROUGE-1: 21.1%
  - ROUGE-2: 0.0%
  - ROUGE-L: 10.5%
- ✅ Clean audio preprocessing (resampling, normalization)

---

## 🧠 Model Architecture

### 🔹 Transcription (STT)
- **Model:** Fine-tuned `Wav2Vec2`
- **Loss Function:** Connectionist Temporal Classification (CTC)

### 🔹 Summarization
- **Extractive:** Sentence embeddings with BERT + cosine similarity
- **Abstractive:** Generated summaries with BART
- **Hybrid:** Extractive → Abstractive pipeline

---

## 🛠️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/speech-summarizer.git
   cd speech-summarizer
