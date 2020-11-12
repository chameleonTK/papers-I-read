## [Unsupervised Machine Translation Using Monolingual Corpora Only](https://arxiv.org/abs/1711.00043)


The authors proposed an MT model trained only with monolingual corpora. They firstly initialize a model with word-by-word translation model constructed by bilingual lexicon which also derived monolingual data. Then start iterative training processing by leveraging the previous MT model.

  

A new encoder-decoder model was trained with 3 loss functions

-   Denoising auto-encoding: a noise function is applied to a sentence then a decoder is tasked to reconstruct the original sentence from the given embedding of the noisy sentence. Min(diff(x, d(e(noise(x))))) where noise function does drop and shuffle words in the input sentence.
    
-   Cross domain training: aims to map sentences from source to target language by using back-translation. A sentence will be translated then applying the denoising objective but use an embedding from translated sentences.
    
-   Adversarial training: train a discriminator to classify languages of a given embedding vector.
    

The authors also proposed a new unsupervised metric to evaluate MT by averaging BLUE score from src-to-trg and trg-to-src MT models. It can be used as early stopping criteria and in hyper-parameter tuning.

  

The results show that this unsupervised model trained with 15M sentences achieved on par with NMT model trained on about 0.1M parallel sentences.


```
@article{lample2017unsupervised,
  title={Unsupervised machine translation using monolingual corpora only},
  author={Lample, Guillaume and Conneau, Alexis and Denoyer, Ludovic and Ranzato, Marc'Aurelio},
  journal={arXiv preprint arXiv:1711.00043},
  year={2017}
}
```







