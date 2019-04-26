# Baseline model
## Training
```
allennlp train baseline.json \
    --serialization-dir baseline-model \
    --include-package package.baseline
```

## Evaluating
```
allennlp evaluate baseline-model/model.tar.gz \
    data/stanfordSentimentTreebank/trees/dev.txt \
    --include-package package.baseline
``` 

# Elmo model
## Training
```
allennlp train elmo.json \
    --serialization-dir elmo-model \
    --include-package package.baseline
```

## Evaluating
```
allennlp evaluate elmo-model/model.tar.gz \
    data/stanfordSentimentTreebank/trees/dev.txt \
    --include-package package.baseline
```


# Bert model
## Training
```
allennlp train bert.json \
    --serialization-dir bert-model \
    --include-package package.baseline
```

## Evaluating
```
allennlp evaluate bert-model/model.tar.gz \
    data/stanfordSentimentTreebank/trees/dev.txt \
    --include-package package.baseline
```

# My test sample:
```
allennlp predict elmo-model/model.tar.gz test.json \
    --include-package package.baseline \
    --predictor sentence_classifier_predictor
```
