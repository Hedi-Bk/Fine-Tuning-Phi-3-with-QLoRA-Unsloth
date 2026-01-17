# Fine-Tuning Phi-3 with QLoRA & Unsloth

This repository contains a specialized implementation for fine-tuning the **Microsoft Phi-3-mini** model using the **QLoRA** (Quantized Low-Rank Adaptation) technique. The project is optimized for high efficiency and low VRAM usage thanks to the **Unsloth** library.

## 🚀 Key Features

- **Model:** Phi-3-mini-4k-instruct.
- **Technique:** **QLoRA** (4-bit quantization) for memory-efficient training.
- **Optimization:** Powered by **Unsloth**, providing 2x faster training and 70% less memory consumption.
- **Format:** Native Chat Template integration (Phi-3 tags: `<|user|>`, `<|assistant|>`, `<|end|>`).
- **Hardware:** Compatible with NVIDIA T4 GPUs (Free tier Google Colab).

## 📊 Dataset & Task

The model was fine-tuned on a custom dataset of 500 samples specifically designed for **HTML Data Extraction**.

- **Input:** Raw HTML snippets or web content.
- **Output:** Structured JSON data.

## 🛠️ Installation & Usage

You can run this project directly in your browser using the provided Google Colab notebook.

### 1. Open in Google Colab

Click the link below to access the full training pipeline: [👉 Access the Colab Notebook](https://colab.research.google.com/drive/1chO1LBnY4d3l0kxTWCCHaXXOYRsxZjSi)

### 2. Implementation Details

The training process includes:

- Loading the model in **4-bit precision**.
- Adding **LoRA adapters** to specific target modules (`q_proj`, `k_proj`, `v_proj`, etc.).
- Using **Gradient Checkpointing** for maximum memory efficiency.
- Exporting the final model via **16-bit merging** for production use.

## 📦 Model Access

The final merged model and adapters are available on my Hugging Face profile:

- **Model Repository:** [Hedi-Bk/Phi-3_FT_with_500_Data_SFT](https://huggingface.co/Hedi-Bk/Phi-3_FT_with_500_Data_SFT)

## 📜 Requirements

- `unsloth`
- `xformers`
- `bitsandbytes`
- `peft`
- `transformers`
- `trl`

*Created by [Hedi-Bk](https://www.google.com/search?q=https://github.com/Hedi-Bk) - Exploring efficient LLM fine-tuning.*
