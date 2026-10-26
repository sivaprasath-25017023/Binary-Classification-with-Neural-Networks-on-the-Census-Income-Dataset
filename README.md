# Census Income Binary Classification with PyTorch

This project trains a neural network to predict whether an individual earns more than $50,000 annually using the Census Income dataset.

## Dataset

Download `income.csv` from the provided Google Drive link:

https://drive.google.com/file/d/1ay5vOv2YiOwjKIWnXFT6sptW0gqew0oa/view?usp=sharing

Place `income.csv` in the repository root. The notebook also attempts an automatic download if the file is publicly accessible.

## Project files

- `notebooks/census_income_workshop.ipynb` — data preparation, model, training, evaluation, and optional prediction function.
- `requirements.txt` — Python dependencies.
- `README.md` — project overview and setup instructions.

## Setup

Python 3.10 or newer is recommended.

```bash
python -m venv .venv
```

Activate the environment:

- Windows: `.venv\Scripts\activate`
- macOS/Linux: `source .venv/bin/activate`

Install dependencies:

```bash
pip install -r requirements.txt
```

Start Jupyter:

```bash
jupyter notebook
```

Open `notebooks/census_income_workshop.ipynb` and run all cells from top to bottom.

## Model details

- Binary target: `<=50K` (class 0) or `>50K` (class 1)
- Categorical features: ordinal-encoded and passed through learned embeddings
- Continuous features: standardized and batch-normalized
- Hidden layer: 50 neurons with ReLU
- Dropout: 0.4
- Loss: CrossEntropyLoss
- Optimizer: Adam, learning rate 0.001
- Epochs: 300
- Split: 25,000 training rows and 5,000 test rows

The notebook prints the actual test loss, accuracy, and classification report after training. Do not report results until you have run the notebook.

## Upload to GitHub

1. Create a new GitHub repository.
2. Upload the `notebooks/` folder, `requirements.txt`, and `README.md`.
3. If the dataset is permitted to be shared, include `income.csv`; otherwise keep it out of the public repository and use the authorized dataset link.
4. Copy the repository URL and submit it in the Moodle workshop submission box.
