## [Cross-lingual Projections between Languages from Different Families](https://www.aclweb.org/anthology/P13-2056/)

When dealing with a language pair that vastly different (En-Zh), building direct projection is difficult and tend to have lower accuracy than other methods. While projection based on word alignment works is more robust to language differences but its coverage (#words that this approach works) is limited by the diversity of the parallel corpus and the performance is limited by the accuracy of the word alignments.


They proposed two techniques that can enhance the latter projection:
-   use Brown clusters as features to build a model so it could utilize information from other labelled words from the cluster.
-   Removing noise with an assumption that words from the same cluster are likely to have the same labels so noise could be removed by removing word that inconsistent with other words from the same cluster.
      
**Direct projection**: words from both languages are projected into a common space

**Projection based on word alignment**: predictions from source sentences are projected into target sentences by existing word alignment then use the projected labels to build a new model for the target language.


💡 Opinion: this method might help to build En-Th model
-   This approach works only with word-level tasks.
-   Don’t know how well it is compared to fine-tuning approach.
-   Need parallel corpus and word alignment which might be a strong condition.
  

```
@inproceedings{yu2013cross,
  title={Cross-lingual projections between languages from different families},
  author={Yu, Mo and Zhao, Tiejun and Bai, Yalong and Tian, Hao and Yu, Dianhai},
  booktitle={Proceedings of the 51st Annual Meeting of the Association for Computational Linguistics (Volume 2: Short Papers)},
  pages={312--317},
  year={2013}
}
```

