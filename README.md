# 🗣️ Whisper ASR Fine-Tuning for Amharic

This project implements a full pipeline to fine-tune OpenAI's Whisper model on **Amharic speech data** using the Hugging Face `transformers` ecosystem. It includes data preprocessing, vocabulary generation, training configuration, evaluation metrics (WER/CER), and model pushing to the Hub with experiment tracking via Weights & Biases (W&B).

---

## 📌 Key Features

- Preprocesses and filters Amharic speech datasets (`KYAGABA_AMHARIC_ALFA_DATASET_100HRS`)
- Trims and splits data based on hours for train/dev
- Defines a custom vocabulary for Amharic characters
- Sets up Whisper tokenizer, processor, and feature extractor
- Fine-tunes `openai/whisper-small` for ASR transcription
- Evaluates performance using **WER** and **CER**
- Tracks experiments with W&B
- Pushes model, tokenizer, and processor to Hugging Face Hub

---

## 🗂️ Dataset

- **Train Set**: `KYAGABA/KYAGABA_AMHARIC_ALFA_DATASET_100HRS`
- **Dev Set**: `KYAGABA/amharic_cleaned_testset_verified`
- Filtered by:
  - Duration (1–30s)
  - Length ratio (CTC-friendly)
  - Token/character cleaning and normalization

---

## 🤖 Model

- Fine-tuned model: `openai/whisper-small`
- Output directory pattern:  
