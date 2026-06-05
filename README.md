# FlashGS-Unofficial

> Unofficial PyTorch implementation starter for **FlashGS: Efficient 3D Gaussian Splatting for Large-scale and High-resolution Rendering** (CVPR 2025).
>
> If this repo saves you reading / reproduction time, please star it and follow [@StaryMoon](https://github.com/StaryMoon). I am building honest open reproduction starters for recent CVPR papers.

## Status

This repository is an **independent, unofficial, work-in-progress starter**.

- Paper: [FlashGS: Efficient 3D Gaussian Splatting for Large-scale and High-resolution Rendering](https://openaccess.thecvf.com/content/CVPR2025/html/Feng_FlashGS_Efficient_3D_Gaussian_Splatting_for_Large-scale_and_High-resolution_Rendering_CVPR_2025_paper.html)
- Venue: CVPR 2025
- Reproduction status: **benchmarks are not reproduced yet**
- Relationship to authors: this repo is not official and is not affiliated with the paper authors.

## What Is Implemented

This v0.1.0 starter implements a compact, readable scaffold inspired by the paper:

- image/token encoder
- Gaussian primitive prediction head
- opacity, scale, color, and position outputs
- toy regularization loss
- smoke-test script

The goal is to make the high-level idea easy to inspect, fork, and improve.

## What Is Not Implemented Yet

- CUDA splatting renderer
- exact scene representation
- real dataset loader
- official rendering metrics

## Quick Start

```bash
git clone https://github.com/StaryMoon/FlashGS-Unofficial.git
cd FlashGS-Unofficial
pip install -r requirements.txt
python scripts/smoke_test.py
```

Expected output includes:

```text
loss: ...
gaussians: torch.Size([2, 128, 11])
```

## Minimal Usage

```python
import torch
from flashgs_unofficial import UnofficialStarter

image = torch.rand(2, 3, 64, 64)
model = UnofficialStarter(kind="gaussian")
out = model(image)
```

## Roadmap

- [ ] Replace toy modules with a closer implementation of the paper.
- [ ] Add dataset loader and config files.
- [ ] Add metric scripts and visualization.
- [ ] Reproduce a small benchmark or ablation table.
- [ ] Add pretrained weights once experiments are stable.

## Search Tags

cvpr-2025, 3d-gaussian-splatting, rendering, pytorch, unofficial-implementation

## Citation

Please cite the original paper if you use the method. This repo is only an unofficial starter and does not replace the paper.

## License

MIT License. The original paper and official materials remain owned by their respective authors / publishers.
