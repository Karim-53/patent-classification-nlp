<h1 align="center">Fast Patent Classification from Abstracts 📄</h1>

<p align="center">
  <b>Can we tell what a patent is about from its abstract alone? This project benchmarks three NLP approaches — from classic word embeddings to GPT-2 — on binary patent classification.</b>
</p>

<p align="center">
  <img alt="Task" src="https://img.shields.io/badge/task-text%20classification-blueviolet">
  <img alt="Stack" src="https://img.shields.io/badge/stack-Keras%20%2F%20TensorFlow%202-orange">
  <img alt="Models" src="https://img.shields.io/badge/models-GloVe%20%7C%20Word2Vec%20%7C%20GPT--2-informational">
  <a href="LICENSE"><img alt="License" src="https://img.shields.io/badge/license-Unlicense-green"></a>
</p>

Given only the **abstract** of a patent, predict its category (a binary "class A vs. class B" problem). The goal is a lightweight classifier that works from short free-text alone — no full patent body, no metadata — and a head-to-head comparison of how different text representations perform on the same task.

## 🧪 Approaches compared
| # | Text representation | Idea |
|---|---------------------|------|
| 1 | **GloVe** (`glove.6B.50d`) | General-purpose pre-trained word embeddings. |
| 2 | **Domain Word2Vec** ([patent-domain vectors](https://www.kaggle.com/darshmso/w2vec-patent-domain)) | Embeddings trained on patent text — does domain adaptation help? |
| 3 | **GPT-2** (small, 124M) | Transfer learning from a pre-trained transformer language model. |

## 📊 Dataset
- **[WIPO-alpha](https://www.wipo.int/classifications/ipc/en/ITsupport/Categorization/dataset/wipo-alpha-readme.html)** — patents labelled with the International Patent Classification (IPC).
- ~5,000 patents, using the abstract field only.

## 🚀 Run it
The full pipeline — preprocessing, the three models, training and evaluation — lives in [`main.ipynb`](main.ipynb).

```bash
pip install "tensorflow>=2.1" "keras==2.3.1" jupyter
jupyter notebook main.ipynb
```

Download the GloVe (`glove.6B.50d.txt`), domain Word2Vec, and GPT-2 weights referenced in the notebook and point the paths accordingly.

## 🖥️ Environment
Trained on an NVIDIA GTX 1060 (CUDA) with TensorFlow 2.1 and Keras 2.3.1.

## 📄 License
Released into the public domain under the [Unlicense](LICENSE).
