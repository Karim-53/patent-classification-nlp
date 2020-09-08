# patent-classification-nlp

**Fast patent classification from abstract**: I choose to work on a binary classification problem ( is the patent of class A or B ) using only the abstract as input

- Dataset: Wipo-alpha data https://www.wipo.int/classifications/ipc/en/ITsupport/Categorization/dataset/wipo-alpha-readme.html
- total size: 5'000 patents
- model 1: I use glove.6B.50d.txt
- model 2: I use W2Vec_Patent_Domain.txt from https://www.kaggle.com/darshmso/w2vec-patent-domain
- model 3: I use pre-trained openai GPT-2 (small 124M)
- Hardware:    Nvidia GTX 1060 with CUDA
- Keras:           v 2.3.1
- Tensorflow:   v 2.1 released on 08/01/2020 tensorflow pip package now includes GPU support by default (same as tensorflow-gpu)

