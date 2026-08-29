# Project page: Learning to Control PDEs with DPC and Time-Integrated Neural Operators

Source for the project website of
**"Learning to Control PDEs with Differentiable Predictive Control and Time-Integrated Neural Operators"**.

🌐 **[centrum-intelliphysics.github.io/PDEControl_DPC_website](https://centrum-intelliphysics.github.io/PDEControl_DPC_website/)**

| | |
|---|---|
| 📄 Paper | [arXiv:2511.08992](https://arxiv.org/abs/2511.08992) |
| 💻 Code | [Centrum-IntelliPhysics/PDEControl_DPC](https://github.com/Centrum-IntelliPhysics/PDEControl_DPC) |
| 🤗 Data | [huggingface.co/datasets/Centrum-IntelliPhysics/PDEControl_DPC](https://huggingface.co/datasets/Centrum-IntelliPhysics/PDEControl_DPC) |
| ▶️ Colab | [heat equation demo notebook](https://colab.research.google.com/github/Centrum-IntelliPhysics/PDEControl_DPC/blob/main/HE_TT/01_control_demo.ipynb) |

**Dibakar Roy Sarkar**, **Ján Drgoňa**\*, **Somdatta Goswami**\*
Johns Hopkins University, Whiting School of Engineering. \*Advised equally

## Local preview

Static site, no build step.

```bash
python -m http.server 8000
# open http://localhost:8000
```

## Layout

```
index.html                  # the whole page
static/
├── css/custom.css          # project styling layered over the template
├── js/index.js             # carousel + scroll behaviour
├── images/
│   ├── schematic.png       # method figure
│   ├── gifs/               # policy vs. zero-control animations, one pair per PDE
│   ├── results/            # closed-loop, physics-validation, error, and loss figures
│   └── extra/              # additional paper figures
└── pdfs/schematic.pdf      # vector method figure
```

## Colab links

The "Try it yourself" section and the hero **Colab** button link straight into the notebooks in
the [code repository](https://github.com/Centrum-IntelliPhysics/PDEControl_DPC), one badge per
notebook:

```
https://colab.research.google.com/github/Centrum-IntelliPhysics/PDEControl_DPC/blob/main/<EXPERIMENT>/<NOTEBOOK>.ipynb
```

where `<EXPERIMENT>` is `HE_TT`, `BE_shock` or `RD_TT`. They resolve against `main`, so renaming
or moving a notebook in the code repo breaks them — update both places together. The badge
grid is styled by `.colab-table` in `static/css/custom.css`.

## Adding a figure

1. Drop the image in `static/images/extra/`.
2. Copy the `result-block` pattern in `index.html`:

```html
<div class="result-block">
  <h3 class="title is-5">Figure title</h3>
  <img src="static/images/extra/your_figure.png" alt="Describe the figure" loading="lazy">
  <p class="caption">What it shows and why it matters.</p>
</div>
```

A commented-out template section near the end of `index.html` marks a good place for these.

## Deployment

GitHub Pages, **Settings → Pages → Deploy from a branch → `main` → `/ (root)`**.
Pushing to `main` redeploys. Keep `.nojekyll`, since without it Jekyll mangles asset paths.

## Credits

Built from the
[Academic Project Page Template](https://github.com/eliahuhorwitz/Academic-project-page-template)
by Eliahu Horwitz, licensed under
[CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/).
