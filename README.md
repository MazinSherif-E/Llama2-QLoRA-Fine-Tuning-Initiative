# Llama2-QLoRA Fine-Tuning Initiative

## Overview
This project showcases the application of QLoRA (Quantized Low Rank Adaptation), a parameter-efficient fine-tuning technique, to optimize the Llama 2 language model for environments with limited computational resources. The initiative aims to demonstrate that large language models like Llama 2 can be efficiently fine-tuned and deployed on standard hardware, making advanced NLP capabilities more accessible.

## Objective
To fine-tune the Llama 2 model on a 15GB GPU, leveraging QLoRA for high efficiency and reduced VRAM usage, without significantly compromising the model's performance.

## Technologies Used
- Python
- PyTorch
- Hugging Face Transformers
- bitsandbytes (for 4-bit quantization)
- QLoRA

## Dataset
The model was fine-tuned using the `mlabonne/guanaco-llama2-1k` dataset, a curated set of 1,000 samples specifically reformatted for this project. This dataset aims to provide a diverse range of prompts and responses to ensure comprehensive fine-tuning.

## Fine-Tuning Process
The fine-tuning process involved the following steps:
1. Loading the `llama-2-7b-chat-hf` model along with its tokenizer.
2. Configuring 4-bit quantization for efficient memory usage.
3. Applying QLoRA with a rank of 64 and a scaling parameter of 16 to update the model parameters.
4. Training the model for one epoch on the selected dataset.

## Outcome
The project successfully fine-tuned the Llama 2 model, achieving effective training with limited VRAM without a significant loss in performance. This makes the model suitable for a wide range of NLP tasks while being accessible for users with standard computing resources.

## How to Use
Load the fine-tuned model from the Hugging Face Hub using the provided code snippets.

## Code & Model Access
The fine-tuned model, along with the training scripts and utility functions, is available on the Hugging Face Hub. You can access it [here](https://huggingface.co/Mazin100/Llama-2-7b-chat-finetune/commit/a3b378be85c3146e75159fa4e795a87a18657e64).
