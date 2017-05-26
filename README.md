# TextAnalyzer

a text analizer that can analyze text. so far, it can extract hot words in a text segment by using tf-idf algorithm.

# features

***extracting hot words from a text.***
1. to gather statistics via frequence.
2. to gather statistics via by tf-idf algorithm
3. to gather statistics via a score factor additionally.

***synonym can be recognized***

***SVM Classificator***
this analyzer supports to classify text by svm. it involves vectoring the text. we can train the samples and then make a classification by the model.

# Dependence

https://github.com/sea-boat/IKAnalyzer-Mirror.git


# TODO
* term relationship.
* emotion analization.


# how to use 

***just simple like this***

1. indexing a document and get a docId.

```
long docId = TextIndexer.index(text);
```

2. extracting by docId.

```
 HotWordExtractor extractor = new HotWordExtractor();
 List<Result> list = extractor.extract(0, 20, false);
 if (list != null) for (Result s : list)
    System.out.println(s.getTerm() + " : " + s.getFrequency() + " : " + s.getScore());
```

a result contains term,frequency and score.

```
ʧҵ֤ : 1 : 0.31436604
���� : 1 : 0.30099702
��λ : 1 : 0.29152703
��ȡ : 1 : 0.27927202
��ȡ : 1 : 0.27581802
ְ�� : 1 : 0.27381304
�Ͷ� : 1 : 0.27370203
��ϵ : 1 : 0.27080503
���� : 1 : 0.27080503
��ֹ : 1 : 0.27080503
```