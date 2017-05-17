# TextAnalyzer
a text analizer that can analyze text. so far, it can extract hot words in a text segment by using tf-idf algorithm.

# Dependence

https://github.com/sea-boat/IKAnalyzer-Mirror.git

# TODO
optimize hot-word extract by tf-idf.


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