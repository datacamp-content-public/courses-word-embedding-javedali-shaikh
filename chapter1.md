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

## Toy model!

```yaml
type: NormalExercise
key: a10981b25e
xp: 100
```

In this exercise, we are going to build a toy word2vec model. We will use the gensim package we introduced in this lesson. We will learn important steps in creating a word2vec model. Though here we are building a toy model using a toy dataset, but with same steps a proper model can also be built. After creating the model, we will use a simple function 'most_similar' to find most similar words. Don't worry at this point if you don't fully understand the details of how 'most_similar' function work, we will cover in detail in next chapter.

`@instructions`
1. Instantiate a word2vec model by passing the toy dataset. This builds the vocabulary.
2. Train the model by passing the the toy dataset, len of dataset and number of epochs to train the model.
3. Find the most similar word for word 'Man'.

`@hint`
You need to pass the len of 'sentences' as parameter to train method
Pass the word as positive to find its most similar.

`@pre_exercise_code`
```{python}
import gensim
```

`@sample_code`
```{python}
sentences = [['man is a king. man and women live together.'], ['women is queen and they live together'], ['man and women are meant to live with each other']]

model = gensim.models.____(sentences)
model.____(____, total_examples=len(____))

w1 = "man"
model.wv.____(positive=____)
```

`@solution`
```{python}
sentences = [['man is a king. man and women live together.'], ['women is queen and they live together'], ['man and women are meant to live with each other']]
model = gensim.models.Word2Vec(sentences)
model.train(sentences, total_examples=len(sentences))

w1 = "man"
model.wv.most_similar(positive=w1)
```

`@sct`
```{python}

```
