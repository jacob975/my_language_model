# my_language_model
## Overview
There are my sample code of natural language generative models, and their objective is translation, usually from chinese to english. This is an interesting topic since the debate of MLE and GAN on NLP in [Caccia+18])(https://arxiv.org/abs/1811.02549.

## Model and algorithm
I use Transformer in [Vaswani+17](https://arxiv.org/abs/1706.03762) as my model, and the objective is maximize likelihood estimation(MLE). 

## Preprocessing
Before the training start, all sentences will be encoded as sequences of one-hot encoding. The length is limited by a certain number.

## Pretraining
I use self-supervised learning with objective of MLE as pretraining. Self-supervised learning can make a use of  monolingual sentences, which is usually cheaper than biligual sentences. Therefore, we can collect cheaper data for training.


## Experiments
I also implement other algorithms into my model as well as note on their name.
+ In the notebook named after 'LSTM', I replace Transformer by Long Short-Term Memory (LSTM) RNN.
+ In the notebook named after 'seqGAN', I use both MLE and Sequential Generative Adversarial Networks(seqGAN in [Yu+16](https://arxiv.org/abs/1609.05473)).
+ In the notebook named after 'TayPO', I use the concept of Taylor series to generalize the Proximal Policy Optimization and then implement it into my seqGAN ([Tang+20](http://proceedings.mlr.press/v119/tang20d/tang20d.pdf)).
+ In the notebook named after 'radam', I replace the optimizor Adam by RectifiedAdam in [Liu+19](https://arxiv.org/abs/1908.03265v1)
+ In the notebook named after 'slowMLE', I construct a model with two-stage learning rate, 10^-3 and 10^-5.