# Machines Are Poets Too: An Introduction To Generative Text

Brent Bailey. Accompanying slides can be viewed [here](https://docs.google.com/presentation/d/1Ehy15d3MboG5IJ1t316ijKwP8llZBkOacEmipcWwSbk/edit?usp=sharing), along with [a recording](https://stars.library.ucf.edu/elo2020/live/workshops/6/) of the most recent version of the workshop given at the Electronic Literature Conference in July 2020.

This repo contains resources for learning about a small set of the myriad avilable methods to create generative text with code. Below are a few code samples inside the p5.js editor to toy with, plus a longer list of available resources to explore - this is just a small taste of the wide world of text generation tools available.

For some of the code samples (especially the ml5 stuff), it’s easiest if you have Python installed because running them in the p5 web editor gets tricky. Don’t worry, you don’t have to learn Python for this workshop! We’ll just be using it to run a local server. If you do have Python installed, just run `python -m SimpleHTTPServer -8000` (for Python 2) or `python -m http.server -8000` (for Python 3). From there, navigate to `localhost:8000` in your browser (all work best in Chrome).

## Basic Javascript Text Generation
A simple way of generating random text strings with p5 and an Amiri Baraka poem: [p5 sketch](https://editor.p5js.org/brondle/sketches/nvSxWVJS3)

And a slightly more complicated one that loads an external text corpus taken from the works of James Baldwin: [p5 sketch](https://editor.p5js.org/brondle/sketches/p6caUhGel).

## Tracery

[Tracery](http://tracery.io/) is a JavaScript library used to create “grammars”: basically a top-level sentence structure then sets of words that meet each sentence component. We’ll use [Allison Parrish](https://www.decontextualize.com/)’s p5 example [here](https://editor.p5js.org/allison.parrish/sketches/ByfvClyTg).

## Word vectors with ml5

Word vectors is basiclly the use of complex math to determine the similarity of different words. [ml5](https://ml5js.org/reference/api-Word2vec/) has a simple-to-use model built on top of [Tensorflow](https://www.tensorflow.org/) that we’ll use here. The code sample is located in the `word2vec` folder.

## Rita.js

[Rita.js](https://rednoise.org/rita/index.php) is an incredible tool for any kind of computational work with text, but we’ll be focusing specifically on some potential generative applications of it.

If you want to mess around with the examples, you may find its [documentation](https://rednoise.org/rita/reference/index.php) useful, as well as its [list of PENN part-of-speech tags](https://rednoise.org/rita/reference/PennTags.html).

These examples are made with Rita’s “full” lexicon - if you get into doing more serious work with it, you may want [a smaller version](https://rednoise.org/rita/download.php).

Code samples are located in the `rita` folder. A few of them are also online if you have issues running them locally:
- [intro showing how to extract parts of speech](https://editor.p5js.org/bront/sketches/BbritBXTT)
- [rhyme generator](https://editor.p5js.org/bront/sketches/FXYKtd0EC)
- [Markov chains](https://editor.p5js.org/bront/sketches/Cf0WltgW7).

## LSTM (CharRNN)

[CharRNN](https://ml5js.org/reference/api-charRNN/) is a LSTM (Long Short-Term Memory) neural network available in the ml5 library. RNNs are, uh, hard to explain, but there’s more information in the slides and resources. You can find code samples in the `char-rnn` folder, or play with a model I trained on James Baldwin [here](https://brondle.github.io/baldwin-rnn/).

## Transformers (GPT-2)

Transformers are even harder to explain! You can read more about them [here](https://towardsdatascience.com/transformers-141e32e69591).

The easiest way to train your own GPT-2 model is with [Runway](https://runwayml.com/). If you want to get closer to the metal, you can use Max Woolf’s [Colab Notebook](https://colab.research.google.com/drive/1VLG8e7YSEwypxU-noRNhsv5dW4NfTGce#scrollTo=H7LoMj4GA4n__) or [GPT-2-simple python package](https://github.com/minimaxir/gpt-2-simple).


## Resources

#### “Simple” Stuff
[How To Make A Dadaist Poem](https://www.writing.upenn.edu/~afilreis/88v/tzara.html)

[Botnik](https://botnik.org/apps/writer/?source=92f3bdc2396ae56487ae6b34df5effc3) - a predictive keyboard generator.

[Dadaist NLP text from in-class exercise](https://docs.google.com/document/d/1naZepmap0vkanRLAX_ytP53oynT3Zm3j9L4m3ub4iT0/edit?usp=sharing)

[ConceptNet, a semantic network](http://conceptnet.io)

[Cheap Bots Done Quick](https://cheapbotsdonequick.com/) - quick bot creation with Tracery.

[Free AIML Bots](https://github.com/pandorabots/Free-AIML)

[Runway ML](https://runwayml.com/) - basically PhotoShop for AI - plug and play machine learning with minimal setup. Currently in free and open beta!

#### Markov Chains

[A visual explanation of Markov chains](http://setosa.io/ev/markov-chains/)

[Towards data science on Markov chains](https://towardsdatascience.com/introduction-to-markov-chains-50da3645a50d) - honestly just start reading Towards Data Science if you’re into ML/AI.

#### Machine Learning

[Allison’s Understanding Word Vectors](https://github.com/aparrish/rwet/blob/master/understanding-word-vectors.ipynb) - it’s in Python, but the principles are the same.


[Publicly available nlp datasets](https://github.com/niderhoff/nlp-datasets) - if you don’t want to deal with making your own, there are tons out there!


[Recurrent Neural Networks Tutorial](http://www.wildml.com/2015/09/recurrent-neural-networks-tutorial-part-1-introduction-to-rnns/) - the most beginner-friendly explanation of RNNs I’ve seen

[The Unreasonable Effectiveness Of Recurrent Neural Networks](http://karpathy.github.io/2015/05/21/rnn-effectiveness/) - really useful intro to RNNs

[Better Language Models and Their Implications (GPT-2)](https://openai.com/blog/better-language-models/) - scary but cool!

[GPT-2](https://github.com/openai/gpt-2) - source code for GPT-2

[Can A Machine Write For The New Yorker?](https://www.newyorker.com/magazine/2019/10/14/can-a-machine-learn-to-write-for-the-new-yorker) - article on GPT-2 and the future of writing.


#### Text Resources

[Project Gutenberg](https://www.gutenberg.org/) - hella books.

[Gutenberg-dammit](https://github.com/aparrish/gutenberg-dammit) - A download of everything on Project Gutenberg.

[Gutenberg-poetry](https://github.com/aparrish/gutenberg-poetry-corpus) - The above, but for poetry.

Libgen - The Pirate Bay for books. I’m not linking here because they change URLs constantly, but look hard and you’ll find it. There’s a scraper for it in the post linked below.

### Data Gathering and Preparation

Inside this very GitHub, you can use the python script `clean_text.py` to quickly remove nonalphanumeric characters from a file. Simply type `python clean_text.py {your_file_name}` in your working directory. This script is a handy little way to get started with text manipulation in Python.

[My quick and dirty web scraping resources](https://medium.com/@brentbailey/a-brief-guide-to-finding-missing-data-ac0a4cb93fa1) - contains links to a couple potentially useful scrapers I’ve written, plus a guide to cracking DRM protection if you’d like to get a protected corpus (fOr ReSeArcH pUrpOseS OnLy).

[My intro to web scraping with scrapy](https://github.com/brondle/webscraping4good)

[An are.na channel dedicated to web scraping](https://github.com/brondle/webscraping4good)

[Effectively Pre-Processing Text Data](https://towardsdatascience.com/effectively-pre-processing-the-text-data-part-1-text-cleaning-9ecae119cb3e)


#### Other Fun Stuff

[NaNoGenMo](https://nanogenmo.github.io/) - national novel generation month. Every November. Generate a novel!
