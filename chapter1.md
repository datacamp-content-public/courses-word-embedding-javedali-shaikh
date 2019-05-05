---
title: 'Chapter Title Here'
description: 'Chapter description goes here.'
free_preview: true
---

## What are pre-trained models?

```yaml
type: VideoExercise
key: d7821c846c
xp: 50
```

`@projector_key`
6bed2faf6b0fd7522a6aba3babdffac1

---

## Hello Gensim!

```yaml
type: NormalExercise
key: a10981b25e
xp: 100
```

In this exercise, we are going to load the gensim package we introduced in last lesson, and try to create a very naive word2vec model. After creating the model, we will use a simple function 'most_similar' to find most similar words. Don't worry at this point if you don't fully understand the details of how 'most_similar' function work, we will cover in detail in next chapter.

`@instructions`
1. Create a word2vec model by passing a list of sentences, this will build the vocabulary.
2. Train the model by passing the sentences.
3. Find the most similar word for word 'Man'.

`@hint`


`@pre_exercise_code`
```{python}
import gensim
```

`@sample_code`
```{python}

```

`@solution`
```{python}
sentences = [['Man is a king'], ['Women is queen'], ['Man and women are together']]
model = gensim.models.Word2Vec(sentences)
model.train(sentences, total_examples=len(sentences))

w1 = "Man"
model.wv.most_similar(positive=w1)
```

`@sct`
```{python}

```
