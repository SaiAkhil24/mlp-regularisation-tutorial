# Taming Overfitting: Regularisation in Neural Networks

A hands-on tutorial for module **7PAM2021 – Machine Learning and Neural Networks**
(Individual Tutorial assignment). It teaches the three most useful regularisation
tools — **L2 weight decay, dropout and early stopping** — using a **Multilayer
Perceptron (MLP) written entirely from scratch in NumPy** on the two-moons problem.

> **GitHub:`https://github.com/SaiAkhil24/mlp-regularisation-tutorial`

## What's inside

| File | Description |
|------|-------------|
| `Regularisation_in_Neural_Networks_Tutorial.pdf` | The written tutorial (<2000 words) — submit this to CodeGrade |
| `Regularisation_in_Neural_Networks_Tutorial.docx` | Editable source of the tutorial |
| `mlp_regularisation_tutorial.ipynb` | Reproducible Jupyter notebook — run top to bottom to recreate every figure |
| `mlp_reg.py` | Stand-alone script version of the same code (`python mlp_reg.py`) |
| `figures/` | The figures used in the tutorial |
| `requirements.txt` | Python dependencies (numpy, matplotlib) |
| `LICENSE` | MIT licence |

## The focus

Rather than calling a library, the MLP (forward pass, back-propagation, Adam,
dropout and L2) is implemented by hand so every step is visible. The tutorial
shows overfitting as a jagged decision boundary and as a rising validation-loss
curve, then demonstrates how each regulariser fixes it and how to choose the
regularisation strength via a validation sweep.

## How to run

**Requirements:** Python 3.9+, `numpy`, `matplotlib` only (no scikit-learn/scipy).

```bash
pip install -r requirements.txt      # numpy + matplotlib
# Notebook:
jupyter notebook mlp_regularisation_tutorial.ipynb
# or the script (writes figures/ and prints a results summary):
python mlp_reg.py
```

Everything is seeded, so results are reproducible.

## Key results

| Model | Train acc. | Test acc. |
|-------|-----------|-----------|
| No regularisation | 1.00 | 0.87 |
| L2 weight decay (λ = 1) | 0.95 | 0.91 |
| Early stopping | 0.90 | 0.88 |
| Dropout (p = 0.6) | 0.98 | 0.89 |

## Accessibility

Figures use the Okabe–Ito colour-blind-safe palette and combine colour with
distinct markers and line styles, so they remain readable in greyscale.

## References (Harvard)

Goodfellow, I., Bengio, Y. and Courville, A. (2016) *Deep Learning*. Cambridge, MA: MIT Press. Available at: https://www.deeplearningbook.org/

Kingma, D.P. and Ba, J. (2015) 'Adam: a method for stochastic optimization', *Proceedings of the 3rd International Conference on Learning Representations (ICLR)*. Available at: https://arxiv.org/abs/1412.6980

Krogh, A. and Hertz, J.A. (1991) 'A simple weight decay can improve generalization', *Advances in Neural Information Processing Systems 4*, pp. 950–957. Available at: https://proceedings.neurips.cc/paper/1991/hash/8eefcfdf5990e441f0fb6f3fad709e21-Abstract.html

Pedregosa, F. et al. (2011) 'Scikit-learn: machine learning in Python', *Journal of Machine Learning Research*, 12, pp. 2825–2830. Available at: https://scikit-learn.org/stable/modules/generated/sklearn.datasets.make_moons.html

Prechelt, L. (1998) 'Early stopping – but when?', in Orr, G.B. and Müller, K.-R. (eds.) *Neural Networks: Tricks of the Trade*. Berlin: Springer, pp. 55–69. Available at: https://doi.org/10.1007/3-540-49430-8_3

Srivastava, N., Hinton, G., Krizhevsky, A., Sutskever, I. and Salakhutdinov, R. (2014) 'Dropout: a simple way to prevent neural networks from overfitting', *Journal of Machine Learning Research*, 15, pp. 1929–1958. Available at: https://jmlr.org/papers/v15/srivastava14a.html

## Licence

Released under the MIT Licence — see `LICENSE`.
