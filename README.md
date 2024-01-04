# DMD-Unofficial

Unofficial Implementation of [One-step Diffusion with Distribution Matching Distillation](https://arxiv.org/abs/2311.18828)

## Usage

- Build Regression Dataset

```bash
python build_regression_data.py --gpus 0,1
python build_regression_data.py --gpus "0,1" --model_id PixArt-alpha/PixArt-XL-2-512x512 --save_dir data/diffusion_db_pixart_xl_2_512x512
```

- Train 

```bash
bash train.sh
```

- Gradio demo

```bash
python gradio_dmd.py --model_path lykon/dreamshaper-8 --unet_path saved/dmd/checkpoint-1000/student_unet
```

## Citation

```bibtex
@article{yin2023one,
  title={One-step Diffusion with Distribution Matching Distillation},
  author={Yin, Tianwei and Gharbi, Micha{\"e}l and Zhang, Richard and Shechtman, Eli and Durand, Fredo and Freeman, William T and Park, Taesung},
  journal={arXiv preprint arXiv:2311.18828},
  year={2023}
}
```