# Python companion materials

This course is taught in R. These notebooks follow the R lectures section by section, using Python (`pandas`, `scikit-learn`, `matplotlib`).

| Week | Notebook | R lecture |
|---|---|---|
| 2 | [evaluationMetrics.ipynb](week2/evaluationMetrics.ipynb) | `lectures/week2/evaluationMetrics.Rmd` |
| 2 | [crossValidation.ipynb](week2/crossValidation.ipynb) | `lectures/week2/crossValidation.Rmd` |
| 3 | [advanced_regression.ipynb](week3/advanced_regression.ipynb) | `lectures/week3/advanced_regression.Rmd` |
| 3 | [regularization.ipynb](week3/regularization.ipynb) | `lectures/week3/regularization.Rmd` |

## Setup
From the repo root, create a virtual environment and install the requirements:
```bash
python3 -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r python/requirements.txt
jupyter lab
```
Run `source .venv/bin/activate` again in each new terminal before `jupyter lab`.

macOS doesn't include a bare `pip` command (you'll see `zsh: command not found: pip`), and Homebrew Python blocks system-wide installs. The venv handles both problems. If `python3` itself isn't found, install it first with `xcode-select --install` or `brew install python`.

Or open a notebook in Google Colab. The notebooks load data from GitHub automatically if `python/data/` isn't found.

## Data
`data/` holds CSV exports of the R datasets used in lecture, so R and Python use identical data: `heights` and `mnist_27` (dslabs), `GaltonFamilies` (HistData), `QuickStartExample` and `BinomialExample` (glmnet), and batting tables derived from the Lahman package.

Note: Python and R use different random number generators, so splits and some numbers will differ slightly from the R slides.
