This folder holds **local reference copies** of training scripts (not a leaderboard submission).

- **`train_gpt.py`** — CUDA `torchrun` trainer snapshot matching upstream-style features (e.g. sliding-window eval, LoRA TTT hooks, int8+zlib artifact path). Use as a backup while iterating on the root `train_gpt.py`.
- **`train_gpt_mlx.py`** — Apple MLX trainer snapshot for local smoke runs.

**CUDA reference** (from repo root, typical env):

```bash
torchrun --standalone --nproc_per_node=8 train_gpt.py
```

**MLX** (example):

```bash
RUN_ID=reference_mlx \
DATA_PATH=./data/datasets/fineweb10B_sp1024/ \
TOKENIZER_PATH=./data/tokenizers/fineweb_1024_bpe.model \
VOCAB_SIZE=1024 \
python3 train_gpt_mlx.py
```

Included files: `train_gpt.py`, `train_gpt_mlx.py`, `submission.json` (placeholder metadata from the old template).
