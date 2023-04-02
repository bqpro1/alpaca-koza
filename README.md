## 🐐🌲KOZA: Low-Rank LLaMA Instruct-Tuning


KOZA 🐐 is an instruct model for Polish language with similar capabilities for LLMs like ChatGPT, but it can be run on a single machine 💻 with a strong GPU (RTX 4080/4090).
This repo was originally forked from [**alpaca-lora**](https://github.com/tloen/alpaca-lora).

Using this repo, you can reproduce the [**Stanford Alpaca**](https://github.com/tatsu-lab/stanford_alpaca) for the Polish language. Original paper from Stanford: [**low-rank adaptation (LoRA)**](https://arxiv.org/pdf/2106.09685.pdf).

### 1. Quick start

In your terminal clone repo:
```bash
git clone git@github.com:bqpro1/alpaca-koza.git
``` 
From repo folder install `requirements.txt`:
```bash
pip isntall -r requirements.txt
``` 
And run:
```bash
python generate.py
```
Go to  http://127.0.0.1:7860 in your browser. Enjoy **KOZA**!

### 2. Translation  

I used `translation_instructions.ipynb` for auto-translation instructions from `data/alpaca_data.json` to `data/alpaca_data_pl_verified.json`. Translation is far from perfect, might be improved. Translation took 12h. You can also find translated data on [huggingface🤗](https://huggingface.co/datasets/Lbuk/alpaca_data_pl.json) 


### 3. Training

Just run 
```bash
python finetune.py --base_model='decapoda-research/llama-7b-hf'
``` 
Weights for Polsih language are also on [huggingface🤗](https://huggingface.co/Lbuk/alpaca-koza-7b).
