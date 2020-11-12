## [Cross-lingual Language Model Pretraining](https://arxiv.org/abs/1901.07291)


The authors suggest that LM can improve cross-lingual tasks by using it to initial a model. They proposed a model called "XLM".

-   TLM (train with sentence pairs which construct from parallel data) improves accuracy by 3% on average (on XNLI)
    
-   MT can utilise XLM both in unsupervised and supervised manner; found an improvement over 7-9 BLEU (MLM is significant better than CLM)
    
-   XLM trained with closer languages family can improve LM perplexity (Nepali+Hindi LMs > Nepali+English)
    


```
@article{lample2019cross,
  title={Cross-lingual language model pretraining},
  author={Lample, Guillaume and Conneau, Alexis},
  journal={arXiv preprint arXiv:1901.07291},
  year={2019}
}
```

