## [Understanding Back-Translation at Scale](https://arxiv.org/abs/1808.09381)

Back-translation is data augmentation for parallel corpus which an initial MT model is trained with parallel corpus for target-to-source then the model is used to translate unlabelled sentences from the target language to build a new synthetic parallel corpus.

-   They found that synthetic corpus with noisy sampling has richer information than synthetic corpus based on beam/greedy search.
-   Back-translation could boost BLUE around 2-3 points.
-   In low-resource setup, the noise of sampling becomes harmful.
-   Synthetic data can be nearly as effective as real human-translated data when domains match

  
```
@article{edunov2018understanding,
  title={Understanding back-translation at scale},
  author={Edunov, Sergey and Ott, Myle and Auli, Michael and Grangier, David},
  journal={arXiv preprint arXiv:1808.09381},
  year={2018}
}
```