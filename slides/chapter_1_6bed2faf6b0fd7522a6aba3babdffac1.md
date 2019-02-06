---
title: Insert title here
key: 6bed2faf6b0fd7522a6aba3babdffac1

---
## What are pre-trained models?

```yaml
type: "TitleSlide"
key: "cda9794d19"
```

`@lower_third`

name: Javedali Shaikh
title: Data Scientist


`@script`



---
## What are Pre-trained models?

```yaml
type: "FullSlide"
key: "137cf4178b"
```

`@part1`
Trained on large corpus like wikipedia, web                            

Created for multiple languages - EN, FR, ZH etc.


`@script`



---
## Popular pre-trained models

```yaml
type: "FullSlide"
key: "6c3436ae32"
```

`@part1`
1. GoogleNews-vectors-Negative-300 

      - Trained on Google news, 300D (Dimension)

2. glove-wiki-gigaword-100

      - Trained on wikipedia, 100D


`@script`



---
## KeyedVecors

```yaml
type: "FullSlide"
key: "58c79c1c80"
```

`@part1`
Supports multiple embeddings like Word2Vec, FastText etc.

Advantages:
Faster load
Smaller objects
Concurrency
Shared RAM
etc.

_https://radimrehurek.com/gensim/models/keyedvectors.html_


`@script`



---
## load_word2vec_format()

```yaml
type: "FullCodeSlide"
key: "718d045990"
center_content: false
```

`@part1`
`model = gensim.models.KeyedVectors.load_word2vec_format
         ('./data/GoogleNews-vectors-negative300.bin.gz', binary=True)`


`@script`



---
## api.load()

```yaml
type: "FullSlide"
key: "ce3611842b"
center_content: false
```

`@part1`
Can load pre-trained models present in gensim data repository

`model = api.load("word2vec-google-news-300")`


`@script`



---
## Let's practice!

```yaml
type: "FinalSlide"
key: "80989b47d1"
```

`@script`


