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
Hello! Welcome to Chapter 2.1, What are Pre-Trained models? In the first chapter, we studied about word emeddings, their importance and also introduced the Gensim Library. In this chapter, we will focus on Pre-Trained models, why to use them and how to load an existing pre-trained model.


---
## Pre-trained models

```yaml
type: "FullSlide"
key: "137cf4178b"
```

`@part1`
- Publicly available pre-trained models mostly by researchers or companies.

- Trained on large corpus like wikipedia, Google News, web corpus etc.{{1}}

- Created for multiple languages - EN, FR, ZH etc. {{2}}


`@script`
So, What are Pre-Trained models? As the name implies, these models are already trained. These models are made publicly available by researches or companies. Ideally, anyone can make it available. These models are trained on large corpus like Wikipedia, Google News or even the web corpus. They are also available on multiple languages like English, French, Chinese etc. So, you can easily find a word2vec pre-trained model present for French Wikipedia and straight away use it.


---
## Why to use Pre-trained models?

```yaml
type: "FullSlide"
key: "f1000300fa"
```

`@part1`
- Often models trained on generic datasets like wikipedia, works well for many NLP tasks like Natural language understanding, text classification etc.

- Training from scratch could take a lot of time (days) and requires complex machine set up like GPUs.{{1}}


`@script`



---
## KeyedVectors in gensim

```yaml
type: "FullSlide"
key: "58c79c1c80"
center_content: false
```

`@part1`
- Supports multiple embeddings like Word2Vec, FastText etc.

- Advantages: {{1}}

   - loads faster
   - Small in size{{2}}
   - Concurrent vector queries {{3}}
   - etc.{{4}}

_For more info: https://radimrehurek.com/gensim/models/keyedvectors.html_ {{5}}


`@script`



---
## load_word2vec_format()

```yaml
type: "FullCodeSlide"
key: "718d045990"
center_content: true
```

`@part1`
```
model = gensim.models.KeyedVectors.load_word2vec_format
         ('./data/GoogleNews-vectors-negative300.bin.gz', binary=True)
```{{1}}


`@script`



---
## Gensim downloader

```yaml
type: "FullSlide"
key: "ce3611842b"
center_content: false
```

`@part1`
Can load pre-trained models present in gensim data repository

```
import gensim.downloader as api

model = api.load("word2vec-google-news-300")
```{{1}}


`@script`



---
## Useful methods of Gensim Downloader

```yaml
type: "TwoColumns"
key: "d8dfcbc853"
center_content: false
```

`@part1`
```
api.info()
```


`@part2`
Retrieves information about all available datasets and models.


`@script`



---
## Useful methods of Gensim Downloader

```yaml
type: "TwoColumns"
key: "1d7adaafb8"
disable_transition: true
```

`@part1`
```
api.info("word2vec-google-news-300")
```


`@part2`
{'base_dataset': 'Google News (about 100 billion words)',
 'checksum': 'a5e5354d40acb95f9ec66d5977d140ef',
 'file_name': 'word2vec-google-news-300.gz',
 'file_size': 1743563840,
 'license': 'not found',
 'num_records': 3000000,
 'parameters': {'dimension': 300},
 'parts': 1,
}


`@script`



---
## Useful methods of Gensim Downloader

```yaml
type: "TwoColumns"
key: "2a1b741c3e"
disable_transition: true
```

`@part1`
```
api.load("wiki-en", return_path=True)
```


`@part2`
Downloads the dataset or model to local machine.


`@script`



---
## Let's practice!

```yaml
type: "FinalSlide"
key: "80989b47d1"
```

`@script`


