## Experimenting with Neural Machine Translation for Thai

The author experimented NMT with different approaches for tokenization.
-   Word-level: apply tokenization before building model   
-   Character level
-   Byte-Pair Encoding (BPE)
-   Thai Character Cluster (TCC)

GRU encoder-decoder with global attention was trained with TED subtitle parallel corpus. Word-level model achieves the highest BLEU score 10.7 but relatively on par with TCC model. However, the architecture difference in the experiments might influence the results.

-   TCC using only 1/10 the vocabulary size of the word level model
-   CNN for charecter-level model while GRU for others

The author also pointed out an interesting question: Can close languages improve translation quality?
-   VN and KR are used but no analytic evaluation presented in the article
    
[https://medium.com/@petepeeradejtanruangporn/experimenting-with-neural-machine-translation-for-thai-1681fd2b375a](https://medium.com/@petepeeradejtanruangporn/experimenting-with-neural-machine-translation-for-thai-1681fd2b375a)