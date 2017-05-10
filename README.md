# TextAnalyzer
a text analizer that can analyze text. so far, it can extract hot words in a text segment by using tf-idf algorithm.

# Dependence

https://github.com/sea-boat/IKAnalyzer-Mirror.git

# TODO
optimize hot-word extract by tf-idf.


# how to use 

***just simple like this***

```
 HotWordExtractor extractor = new HotWordExtractor();
 List<Result> list = extractor.extract(0, 20, false);
 if (list != null) for (Result s : list)
    System.out.println(s.getTerm() + " : " + s.getFrequency() + " : " + s.getScore());
```

a result contains term,frequency and score.

```
һ��һ· : 15 : 0.10496296
���ɷ��� : 12 : 0.08397037
���� : 9 : 0.062977776
���� : 8 : 0.055980247
���� : 8 : 0.055980247
���� : 7 : 0.048982713
���� : 6 : 0.041985184
��ѧ : 6 : 0.041985184
���� : 5 : 0.034987655
��� : 5 : 0.034987655
��̳ : 5 : 0.034987655
�й� : 4 : 0.027990123
�о� : 4 : 0.027990123
��ҵ : 3 : 0.020992592
ǧ���� : 3 : 0.020992592
ʵ�� : 3 : 0.020992592
�� : 3 : 0.020992592
�о����� : 3 : 0.020992592
�׶� : 3 : 0.020992592
5�� : 2 : 0.013995062
```