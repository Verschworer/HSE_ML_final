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


sparknlp ClassifierDLApproach 30 epochs logs:

  Training started - epochs: 30 - learning_rate: 0.01 - batch_size: 256 - training_examples: 35797 - classes: 20

  Epoch 0/30 - 10.02s - loss: 391.01025 - acc: 0.29464805 - val_acc: 43.02238 - batches: 140
  Epoch 1/30 - 9.30s - loss: 368.92258 - acc: 0.4756007 - val_acc: 50.138294 - batches: 140
  Epoch 2/30 - 9.87s - loss: 363.7496 - acc: 0.5127525 - val_acc: 51.898415 - batches: 140
  Epoch 3/30 - 9.31s - loss: 363.78198 - acc: 0.5221782 - val_acc: 52.225296 - batches: 140
  Epoch 4/30 - 9.24s - loss: 363.12735 - acc: 0.5255167 - val_acc: 52.652752 - batches: 140
  Epoch 5/30 - 9.22s - loss: 362.68106 - acc: 0.52843934 - val_acc: 52.97963 - batches: 140
  Epoch 6/30 - 9.26s - loss: 362.2034 - acc: 0.5303503 - val_acc: 53.105354 - batches: 140
  Epoch 7/30 - 9.25s - loss: 361.48337 - acc: 0.53184545 - val_acc: 53.105354 - batches: 140
  Epoch 8/30 - 9.39s - loss: 360.599 - acc: 0.5334192 - val_acc: 53.1305 - batches: 140
  Epoch 9/30 - 9.27s - loss: 359.8706 - acc: 0.5342903 - val_acc: 53.155643 - batches: 140
  Epoch 10/30 - 9.16s - loss: 359.2229 - acc: 0.5349648 - val_acc: 53.18079 - batches: 140
  Epoch 11/30 - 9.33s - loss: 358.6243 - acc: 0.5359822 - val_acc: 53.205933 - batches: 140
  Epoch 12/30 - 9.48s - loss: 358.15625 - acc: 0.53685904 - val_acc: 53.256226 - batches: 140
  Epoch 13/30 - 9.32s - loss: 357.7255 - acc: 0.5375054 - val_acc: 53.306515 - batches: 140
  Epoch 14/30 - 10.03s - loss: 357.3251 - acc: 0.53806746 - val_acc: 53.381943 - batches: 140
  Epoch 15/30 - 10.14s - loss: 357.0393 - acc: 0.5386014 - val_acc: 53.40709 - batches: 140
  Epoch 16/30 - 9.28s - loss: 356.85745 - acc: 0.53919154 - val_acc: 53.356804 - batches: 140
  Epoch 17/30 - 9.27s - loss: 356.7212 - acc: 0.53950065 - val_acc: 53.331654 - batches: 140
  Epoch 18/30 - 9.45s - loss: 356.60748 - acc: 0.5398941 - val_acc: 53.40709 - batches: 140
  Epoch 19/30 - 9.41s - loss: 356.51703 - acc: 0.54023135 - val_acc: 53.356804 - batches: 140
  Epoch 20/30 - 9.38s - loss: 356.433 - acc: 0.5405686 - val_acc: 53.40709 - batches: 140
  Epoch 21/30 - 9.35s - loss: 356.35114 - acc: 0.5408777 - val_acc: 53.40709 - batches: 140
  Epoch 22/30 - 9.35s - loss: 356.27438 - acc: 0.5411025 - val_acc: 53.43224 - batches: 140
  Epoch 23/30 - 9.65s - loss: 356.20038 - acc: 0.54138356 - val_acc: 53.43224 - batches: 140
  Epoch 24/30 - 9.47s - loss: 356.13593 - acc: 0.5416927 - val_acc: 53.40709 - batches: 140
  Epoch 25/30 - 9.47s - loss: 356.07196 - acc: 0.54188937 - val_acc: 53.43224 - batches: 140
  Epoch 26/30 - 9.45s - loss: 356.01282 - acc: 0.5420299 - val_acc: 53.43224 - batches: 140
  Epoch 27/30 - 9.41s - loss: 355.9558 - acc: 0.54219854 - val_acc: 53.43224 - batches: 140
  Epoch 28/30 - 9.15s - loss: 355.9018 - acc: 0.5423109 - val_acc: 53.40709 - batches: 140
  Epoch 29/30 - 9.28s - loss: 355.84833 - acc: 0.54250765 - val_acc: 53.45738 - batches: 140
