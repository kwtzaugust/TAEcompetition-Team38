# Team 38 TAEcompetition
Members: Seah Ee Song, Ku Wee Tiong  

https://www.kaggle.com/c/2019tae/overview  

# Dependencies  
```R
if(!require(tm)){
  install.packages("tm")
  library(tm)
}

if(!require(RWeka)){
  install.packages("RWeka")
  library(RWeka)
  # We realised a little late that RWeka may have some Java dependencies >.<
  # Please note that we only used the function NGramTokenizer from RWeka
  # as a utility fn, not as part of the model.
  # in hindsight, we found several pure R packages which could achieve the same utility
  # e.g. https://www.rdocumentation.org/packages/tokenizers/versions/0.2.1/topics/ngram-tokenizers
  # we should have used this instead, but we didn't due to time constraints
  # apologies for the oversight; we seek your understanding to please permit this
  # the main bulk of the model is k means clustering and randomforest!
}

if(!require(caret)){
  install.packages("caret")
  library(caret)
}

if(!require(flexclust)){
  install.packages("flexclust")
  library(flexclust)
}

if(!require(randomForest)){
  install.packages("randomForest")
  library(randomForest)
}

```

# Orientation  
`Generate csv w cluster k1_1_3.ipynb` is the notebook that produced our final `submission.csv`.  
`Generate csv w cluster k1_1_3.html` provides an imperfect snapshot of it post-run. We accidentally reran some parts so the output may not be totally accurate, apologies! It would take too long to rerun (~4 hours on a Macbook Pro 2017).  
`submission_k1_1_3_500b.csv` was the file outputted and submitted to Kaggle.  
`Trainer w cluster mod stop k1_1_3.ipynb` was the notebook we used to train and validate our models prior to running `Generate csv w cluster k1_1_3.ipynb`.  
The accompanying `Trainer w cluster mod stop k1_1_3.html` provides an imperfect snapshot of post-run state (again, we accidentally reran some cells!).  

