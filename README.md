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
