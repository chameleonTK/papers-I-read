## [XNLI: Evaluating Cross-lingual Sentence Representations](https://arxiv.org/abs/1809.05053)


The authors present a new benchmark for inference task (entail, contradiction, neutral) -- Thai included. 7500 samples from MNLI are translated by experts as test and dev datasets.

-   Since it is obtained by translation, it might be different when people from different cultures conduct sentences in real-world.
    

They provide 4 baselines
1. Machine translation-based:
    - Translation-train: training data is translated into target language then use it to train a mdel
    - Translation-test: test data will be translated at test time to English then apply a model that trained on English
    

2. Cross-lingual approach:
    - CBOW: English fasttext embedding is fixed then fine-tuning sentences embedding from other languages to have closer values using MUSE
    - Bi-LSTM: an English encoder was trained with MNLI then target language encoders are trained to match the output of the English encoder

Translation-based are limited by the quality of the translation system. The results are strongly-correlated with BLUE. However, in general, trainalation-test performs consistently better than Trainalation-train.

Cross-lingual model can be beaten by translation-test model (6% differences). The accuracy has strong-correlated with alignment loss. Fine-tuning the embeddings does not significantly impact the overall performance.



```
@article{conneau2018xnli,
  title={XNLI: Evaluating cross-lingual sentence representations},
  author={Conneau, Alexis and Lample, Guillaume and Rinott, Ruty and Williams, Adina and Bowman, Samuel R and Schwenk, Holger and Stoyanov, Veselin},
  journal={arXiv preprint arXiv:1809.05053},
  year={2018}
}
```





