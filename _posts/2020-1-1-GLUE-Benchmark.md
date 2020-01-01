---
layout: post
title: GLUE Benchmark - The labours of Hercules!
published: true
---

# GLUE (General Language Understanding Evaluation) Benchmark 
Its a collection of 9 language understanding tasks - including q&A , textual entailments, sentiment prediction & grammar understanding

![_config.yml]({{ site.baseurl }}/images/Twelve_Labours_Altemps_Inv8642.jpg)



GLUE >> is model-agnostic but incentivizes sharing knowledge across tasks 
This is beneficial where data is not easily available---such tasks can benefit from knoweldge transfer. 

While current models excel where there are strong lexical signals, they struggle with tasks of logic. Some tasks like WNLI tasks which involves making inference from a sentence is still elusive
eg. "John couldn't fit the trophy in the suitcase because it was too big". Models struggle to identify that the "The trophy was too big"


The Nine tasks are listed below: 

<A> Single sentence tasks

CoLA: Corpus of Linguistic Acceptability 
Each example is a set of English words annotated with whether it's grammatically possible sentence in English 
Acceptability is based on expert judgement drawn from 22 books & journals on linguistic theory 

SST-2: The Stanford Sentiment Treebank
These are sentences extracted from movie reviews & their human annotation. There is a two-way split (positive/negative)


<B> Similarity & Paraphrase Tasks 

MRPC: Microsoft Research Paraphrase Corpus
Sentence pairs which are automatically extracted from online news sources. Task is to annotate if the two sentences are semantically equivalent. Accuracy & F1 scores are used


QQP: Quora Question Pairs
Given two questions the task is to identify whether they are semantically equivalent. Metrics: accuracy & F1 

STS-B: Semantic Textual Similarity Benchmark
The task is for determining the similarity on a continous scale
MEtric: PEarson & Spearman coeeficients

<C> Inference Tasks 

MNLI: Multi-genre Language Inference
Given a premise sentence & a hypothesis. The task is to predict if the sentence entails the hypothesis, contradicts or is neutral.
The SNLI dataset is also used for co-training the model 

QNLI: This is the SQuAD dataset Stanford Q&A dataset for inference
Qusetion & Paragraph pairs are present. The answer is a sentence in the paragraph 

RTE: Recognizing Textual Entailments
This is a task for premise entails hypothesis. The task is to annotate into entailment or non-entailment ( neutral & contradicts are collapsed into this class)

WNLI: Winograd Schema Challenge
This is a reading comprehension test. A sentence containing a pronoun & a list of possible referrants. Task is to choose the correct one. 


To create the benchmark we use a macro-average of all the metrics. 

