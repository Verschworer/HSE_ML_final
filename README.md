# HSE_ML_final
our team rep for final ML task

We have multiclass classification problem with this case

dataset with 3 columns:
  - cuisine is cuisine category, target column;
  - id is some object identificator;
  - ingredients are ingredients in recipe, features. Stringtype

we have classes, they are imbalanced:
  - italian - 7838
  - mexican - 6438
  - southern_us - 4320
  - indian - 3003
  - chinese - 2673
  - french - 2646
  - cajun_creole - 1546
  - thai - 1539
  - japanese - 1423
  - greek - 1175
  - spanish - 989
  - korean - 830
  - vietnamese - 825
  - moroccan - 821
  - british - 804
  - filipino - 755
  - irish - 667
  - jamaican - 526
  - russian - 489
  - brazilian - 467

there are 6714 unique ingredients, and 3074 unique words in ingredients column

classification problem in this case have different ways to solve:
  - onehot encoding;
  - nlp text preprocessing and vectorizing techniques;
  - class balance;
  - different models;
  - hyperparametrs tuning;
  - try some deep learning.

we have try spyci nlp and spark nlp, try tensorflow with lstm 

#BASELINE, two tries on Kaggle.com - 0.28278 & 0.27544

sparknlp ClassifierDLApproach with embeddings

vectorozation is done using the UniversalSentenceEncoder.pretrained model from the sparknlp toolkit
(The Universal Sentence Encoder encodes text into high-dimensional vectors that can be used for text classification, semantic similarity, clustering and other natural language tasks. The model is trained and optimized for greater-than-word length text, such as sentences, phrases or short paragraphs),
which, in turn, did not count on the listing of unrelated words, but on the presence of sentences and is expected for full-fledged texts. the mathematical representation of the text obtained in this way of preprocessing was transferred to the ClassifierDLApproach - a deep learning tool also from the sparknlp composition.
(ClassifierDL uses the state-of-the-art Universal Sentence Encoder as an input for text classifications. The ClassifierDL annotator uses a deep learning model (DNNs) we have built inside TensorFlow and supports up to 100 classes)

#two tries on Kaggle.com - 0.28278 & 0.27544

##then I had to look at the logs

sparknlp ClassifierDLApproach training logs:

  Training started - epochs: 30 - learning_rate: 0.01 - batch_size: 256 - training_examples: 35797 - classes: 20, Kaggle.com 

  - Epoch 0/30 - 10.02s - loss: 391.01025 - acc: 0.29464805 - val_acc: 43.02238 - batches: 140
  - Epoch 1/30 - 9.30s - loss: 368.92258 - acc: 0.4756007 - val_acc: 50.138294 - batches: 140
  - Epoch 2/30 - 9.87s - loss: 363.7496 - acc: 0.5127525 - val_acc: 51.898415 - batches: 140
  - Epoch 3/30 - 9.31s - loss: 363.78198 - acc: 0.5221782 - val_acc: 52.225296 - batches: 140
  
  ...
  
  - Epoch 26/30 - 9.45s - loss: 356.01282 - acc: 0.5420299 - val_acc: 53.43224 - batches: 140
  - Epoch 27/30 - 9.41s - loss: 355.9558 - acc: 0.54219854 - val_acc: 53.43224 - batches: 140
  - Epoch 28/30 - 9.15s - loss: 355.9018 - acc: 0.5423109 - val_acc: 53.40709 - batches: 140
  - Epoch 29/30 - 9.28s - loss: 355.84833 - acc: 0.54250765 - val_acc: 53.45738 - batches: 140

  Training started - epochs: 1000 - learning_rate: 1.0E-4 - batch_size: 256 - training_examples: 35797 - classes: 20

  - Epoch 0/1000 - 9.82s - loss: 417.42383 - acc: 0.19734961 - val_acc: 19.58763 - batches: 140
  - Epoch 1/1000 - 5.69s - loss: 408.16028 - acc: 0.19864231 - val_acc: 19.58763 - batches: 140
  - Epoch 2/1000 - 5.88s - loss: 405.27988 - acc: 0.19864231 - val_acc: 19.58763 - batches: 140
  - Epoch 3/1000 - 5.72s - loss: 404.9568 - acc: 0.19864231 - val_acc: 19.58763 - batches: 140

  ...
  
  - Epoch 996/1000 - 9.16s - loss: 391.82648 - acc: 0.33264804 - val_acc: 33.31657 - batches: 140
  - Epoch 997/1000 - 9.28s - loss: 391.82486 - acc: 0.33264804 - val_acc: 33.31657 - batches: 140
  - Epoch 998/1000 - 9.49s - loss: 391.82343 - acc: 0.33264804 - val_acc: 33.31657 - batches: 140
  - Epoch 999/1000 - 9.19s - loss: 391.822 - acc: 0.33264804 - val_acc: 33.31657 - batches: 140

It seem like model is undertrained, too less information by our vectors - “Never use a shotgun when a flyswatter will do”

so, in jupyter notebooks classic ML and some Tensor Flow with simply vectorization

