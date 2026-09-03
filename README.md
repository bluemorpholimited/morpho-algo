# Morpho-Algo — Training Notebooks

Trading-decision LLM (SFT → DPO → GGUF → local CPU CLI), built on Phi-4-mini (3.8B).
Durable source of truth: **Hugging Face `bluemorpholimited/morpho-algo`** (data + fixed driver + code).
This GitHub repo holds the **Google Colab** training notebooks.

## ▶️ Open in Colab

**SFT (the main training run)** — full-parameter bf16, auto-resume, checkpoints uploaded to HF every 300 steps:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bluemorpholimited/morpho-algo/blob/main/MorphoAlgo_SFT.ipynb)

### How to run
1. Click the badge above (opens in Colab).
2. **Runtime → Change runtime type → Hardware accelerator: GPU** (A100 recommended; T4 works but slower).
3. Run the cells top-to-bottom.
4. In the token cell, paste your **`bluemorpholimited` Hugging Face write token** (HF, not GitHub).
5. Run the **SFT** cell. Watch progress. Checkpoints auto-upload to HF.

## Repository
- Data (P1_v1 splits + DPO pairs) and the fixed SFT driver: `huggingface.co/bluemorpholimited/morpho-algo`
- Molab/GPU compute is internal infrastructure — do not reference the sandbox in any public artifact.
