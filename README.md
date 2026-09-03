# Morpho-Algo — Training Notebooks

Trading-decision LLM (SFT → DPO → GGUF → local CPU CLI), built on Phi-4-mini (3.8B).
Durable source of truth: **Hugging Face `bluemorpholimited/morpho-algo`** (data + drivers + code).

## ▶️ Run training in Google Colab

**QLoRA SFT — the version that fits a FREE Colab T4 (16 GB GPU)** *(recommended)*:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bluemorpholimited/morpho-algo/blob/main/MorphoAlgo_SFT_LoRA.ipynb)

**Full-parameter SFT (needs a large GPU, e.g. A100 40GB)** — for high-memory runtimes only:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bluemorpholimited/morpho-algo/blob/main/MorphoAlgo_SFT.ipynb)

### How to run (QLoRA path)
1. Click the **QLoRA SFT** badge above.
2. **Runtime → Change runtime type → Hardware accelerator: GPU** (a free T4 is fine).
3. Run the cells top-to-bottom.
4. Paste your **`bluemorpholimited` Hugging Face** write token when asked (HF token, not GitHub).
5. Run the SFT cell. It loads the 3.8B model in 4-bit, trains a LoRA adapter (low VRAM), and **uploads LoRA checkpoints to HF every 250 steps**. Interrupted? Just re-run the SFT cell — it resumes.

## Repos
- HF (data + `src/morpho_sft.py` full-param driver + `src/morpho_sft_lora.py` QLoRA driver): `huggingface.co/bluemorpholimited/morpho-algo`
- Compute is internal infrastructure — do not reference any sandbox in public artifacts.
