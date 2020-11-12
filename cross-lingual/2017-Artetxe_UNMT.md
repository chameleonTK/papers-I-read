## [Unsupervised Neural Machine Translation](https://arxiv.org/abs/1710.11041)


The authors propose a new architecture which has 3 properties:
-   Dual structure: handle both translation directions in the same model
-   Shared encoder: aimed to produce a language independent representation
-   Fixed embeddings in the encoder, separate vocabularies
    

To train this model, they employ 2 strategies:
-   Denoising
-   On-the-fly backtranslation
    
These two training objectives are alternated from mini-batch to mini-batch.

They observed that this unsupervised approach can improve the semi-supervised setting with only 100k sentences to be on par with a supervised model trained on the full corpus.

💡 Opinion: they assume that using fixed cross-lingual embeddings in the encoder is necessary in the early stages of training but it might not be true or maybe relaxing version which progressive unfrozen might increase the accuracy.

  
💡💡 Idea: build an MT by using pre-trained BERT but connect from the middle layer instead because an analysis shows that BERT captures syntactic information in the layer 4-6. This is the only section that is language dependence.
    


```
@article{artetxe2017unsupervised,
  title={Unsupervised neural machine translation},
  author={Artetxe, Mikel and Labaka, Gorka and Agirre, Eneko and Cho, Kyunghyun},
  journal={arXiv preprint arXiv:1710.11041},
  year={2017}
}
```

