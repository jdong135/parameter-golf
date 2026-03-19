This record captures `2026-03-19_Noob`.

Describe what changed in this run:
- model changes:
- optimization/schedule changes:
- systems/runtime changes:

Configuration:
- Layout: `VOCAB_SIZE=1024 NUM_LAYERS=9 MODEL_DIM=512 NUM_HEADS=8 NUM_KV_HEADS=4`
- MLP/embedding details:
- Batching details:

Command (track-relevant params):
```bash
RUN_ID=noob \
DATA_PATH=./data/datasets/fineweb10B_sp1024/ \
TOKENIZER_PATH=./data/tokenizers/fineweb_1024_bpe.model \
VOCAB_SIZE=1024 \
python3 train_gpt_mlx.py
```

Results (copy from your final logs):
- `val_loss`:
- `val_bpb`:
- `bytes_total`:
- `bytes_code`:
- train wallclock:
- notes:

Included files:
- `train_gpt_mlx.py` (code snapshot used for the run)
- `train.log` (exact training log)
- `submission.json` (leaderboard metadata)
