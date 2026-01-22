# Fine-Tuning Phi-3 with QLoRA & Unsloth

This repository contains a specialized implementation for fine-tuning the **Microsoft Phi-3-mini** model using the **QLoRA** (Quantized Low-Rank Adaptation) technique.

## Key Features

- **Model:** Phi-3-mini-4k-instruct.
- **Technique:** **QLoRA** (4-bit quantization) for memory-efficient training.
- **Optimization:** Powered by **Unsloth**, providing 2x faster training and 70% less memory consumption.
- **Format:** Native Chat Template integration (Phi-3 tags: `<|user|>`, `<|assistant|>`, `<|end|>`).
- **Hardware:** Compatible with NVIDIA T4 GPUs (Free tier Google Colab).

## Dataset & Task

The model was fine-tuned on a custom dataset of 500 samples specifically designed for **HTML Data Extraction**.

- **Input:** Raw HTML snippets or web content.
- **Output:** Structured JSON data.

## Installation & Usage

You can run this project directly in your browser using the provided Google Colab notebook.

Click the link below to access the full training pipeline: 👉 [![Open In Colab](https://img.shields.io/badge/Google_Colab-F9AB00?logo=googlecolab&logoColor=white)](https://colab.research.google.com/drive/1chO1LBnY4d3l0kxTWCCHaXXOYRsxZjSi)

## Model Access

The final merged model and adapters are available on my Hugging Face profile:

- **Model Repository:** [Hedi-Bk/Phi-3_FT_with_500_Data_SFT](https://huggingface.co/Hedi-Bk/Phi-3_FT_with_500_Data_SFT)



*Created by [Hedi-Bk](https://github.com/Hedi-Bk) - Exploring efficient LLM fine-tuning.*
