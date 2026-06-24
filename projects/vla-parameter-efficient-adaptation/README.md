# Parameter-Efficient Adaptation of Vision–Language–Action Policies for Long-Horizon Manipulation

**Jinglei Liang** · Preprint, 2026

## Abstract
We study how to adapt a large pre-trained vision–language–action (VLA) policy to
long-horizon manipulation tasks **without full fine-tuning**. A compact,
five-component recipe improves success on a standard manipulation benchmark while
training only a small fraction of parameters.

## Method
1. **Selective LoRA placement** — low-rank adapters on the layers that matter
   most for action decoding.
2. **LLM-based instruction augmentation** — paraphrase and diversify language
   conditioning to improve grounding.
3. **Test-time action-chunk fusion** — overlap-average successive action chunks
   for smoother, more reliable rollouts.
4. **EMA weight averaging** — exponential moving average of adapter weights for
   stability.
5. **Failure-case resampling** — re-weight the hardest episodes during training.

## Results
| Split | Baseline | Ours |
|---|---|---|
| Mean success | 92.2% | **94.2%** |
| Long-horizon | 85.2% | **88.8%** (+3.6 pt) |

Flow-matching loss reduced by **80%** over **2,000** evaluation episodes.

## Notes
Benchmark and base-model names follow public conventions. Internal training
infrastructure and dataset provenance are intentionally omitted.
