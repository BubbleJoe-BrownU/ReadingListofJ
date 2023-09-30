# ReadingListofJ

Currently, each item is structured as Title + Summary + Citation. 

## CSP | Learning to compose soft prompts for compositional zero-shot learning

### Summary

### citation
```
@inproceedings{
  csp2023,
  title={Learning to Compose Soft Prompts for Compositional Zero-Shot Learning},
  author={Nihal V. Nayak and Peilin Yu and Stephen H. Bach},
  booktitle={International Conference on Learning Representations},
  year={2023}
}
```

## Alfred | A system for prompted weak supervision

### Summary
Alfred is the first second-generation of Programmatic Weak Supervision (WPS) system that generates traininig data by prompting large language models (e.g., GPT, T5, T0++) or vision-language models (e.g. CLIP). Alfred adopts a dynamic batching strategy that groups inputs with similar sequence length together to minimize padding and therefore increase memory utilization and increase throughput.

### citation
```
@inproceedings{yu2023alfred,
  title = {Alfred: A System for Prompted Weak Supervision},
  author = {Yu, Peilin and Bach, Stephen H.}, 
  booktitle = {ACL Demo}, 
  year = 2023, 
}
```

## NegCLIP | When and why vision-language models behave like bags-of-words, and what to do about it?

### Summary
Creted the Attribution, Relation and Order (ARO) benchmark, on which state-of-the-art VLMs behave like bags-of-words. The authors reveal that training on large-scale datasets is not enough for models to learn compositional understanding, and evaluting on these datasets does not surface this deficiency. The authors proposed composition-aware hard negative mining to improve OpenCLIP's understanding of compositionality and order.

### Citation
```
@inproceedings{
  yuksekgonul2023when,
  title={When and why Vision-Language Models behave like  Bags-of-Words, and what to do about it?},
  author={Mert Yuksekgonul and Federico Bianchi and Pratyusha   Kalluri and Dan Jurafsky and James Zou},
  booktitle={International Conference on Learning Representations},
  year={2023},
  url={https://openreview.net/forum?id=KRLUvxh8uaX}
}
```
