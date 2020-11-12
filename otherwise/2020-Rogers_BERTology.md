## [A Primer in BERTology: What we know about how BERT works](https://arxiv.org/abs/2002.12327)

-   BERT’s contextualised embeddings form clear clusters corresponding to word senses -- (Wiedemann et al, 2019)
-   Wordpiece tokenizer might be part of the issue where BERT doesn’t understand number very well
-   BERT cannot reason several steps (It cannot merge knowledge from many facts to inference the new one)
-   Most of the attention patterns are trivial patterns (attention to the next word, [CLS], [SEP] etc)
-   Attention to [SEP] might be no-op signal -- Clark et al. 2019.
-   Fine-tuning might be a process that BERT learns what not to do
    

#### Knowledge in BERT
-   Syntactic information is likely to be in the middle layers
-   Syntactic structure is not directly encoded in self-attention weights (Cannot extract full parse tree from BERT head alone)

-   **Middle layers are more transferable**
    
-   While semantics is spread across the entire model
-   BERT does not understand negation and is insensitive to malformed input (Its prediction were not altered even with shuffled word order, truncated sentences, remove subject/objects) -- Ettinger, 2019
    
-   **Final layers are the most task-specific**
    
-   Knowledge in BERT does not necessarily get used in down-stream tasks
-   Pre-training weights widen and flatten the error region of the fine-tuned BERT -- Hao et al. 2019. Visualizing and understanding the effectiveness of BERT.
    
#### Architecture
-   The number of heads was less important than the number of layers
-   Larger batch is helpful
-   Adapter modules???
    
-   Dropout might cause redundant heads/layers -- Clark et al. 2019
-   BERT compression: knowledge distilling/quantization

#### Cross-lingual BERT
-   BERT seems to learn high-quality cross-lingual word alignments -- Libovicky et al. 2019.
-   Adding language-id in pre-training was not helpful
-   Cross-lingual transfer can be achieved by only re-training the input embedding -- Artetxe et al. 2019
-   Freezing the bottom layers helps fine-tuning on multilingual datasets -- Wu and Dredze, 2019
    


```
@article{rogers2020primer,
  title={A primer in bertology: What we know about how bert works},
  author={Rogers, Anna and Kovaleva, Olga and Rumshisky, Anna},
  journal={arXiv preprint arXiv:2002.12327},
  year={2020}
}
```

