# ReadingListofJ

Currently, each item is structured as Title + Summary + Citation. 
# Deep Learning Algorithm papers

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
Alfred is the first second generation of Programmatic Weak Supervision (WPS) system that generates training data by prompting large language models (e.g., GPT, T5, T0++) or vision-language models (e.g. CLIP). Alfred adopts a dynamic batching strategy that groups inputs with similar sequence lengths together to minimize padding and therefore increase memory utilization and throughput.

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
Created the Attribution, Relation and Order (ARO) benchmark, on which state-of-the-art VLMs behave like bags-of-words. The authors reveal that training on large-scale datasets is not enough for models to learn compositional understanding, and evaluating on these datasets does not surface this deficiency. The authors proposed composition-aware hard negative mining to improve OpenCLIP's understanding of compositionality and order.

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

# Deep Learning System papers

## Flexgen | High-throughput Generative Inference of Large Language Models with a Single GPU

### Summary
Flexgen is an offloading framework for high-throughput LLM inference, which optimizes both GPU and CPU memory allocation as well as model quantization to allow for inference with higher throughput than previous offloading-based frameworks, such as DeepSpeed ZeRO inference and HuggingFace Accelerate, though at the cost of inference speed. Using Flexgen, one can run OPT-175B on a single GPU with 16GB memory with effective batch size of 144.

Flexgen's offloading strategy aims to minimize the I/O complexity of moving model weights back and forth between GPU, CPU, and disks. In order to reduce the I/O of moving KV cache from CPU to GPU, especially for inference with long sequence lengths, Flexgen delegates computation tasks to CPU when KV cache is already in CPU memory and model quantization is disabled. 

Flexgen's model compression strategy mainly has two parts, one is to quantize model weights and KV Cache in 4-bit integers in a group-wise manner, and convert them back to FP16 before computation, the other is to sparsify attention calculation by only loading the top 10% attention value cache on OPT-175B model. The model compression strategy only leads to a negligible loss drop for OPT-30B and OPT-175B on two next-word prediction tasks.

### Citation
```
@misc{sheng2023flexgen,
      title={FlexGen: High-Throughput Generative Inference of Large Language Models with a Single GPU}, 
      author={Ying Sheng and Lianmin Zheng and Binhang Yuan and Zhuohan Li and Max Ryabinin and Daniel Y. Fu and Zhiqiang Xie and Beidi Chen and Clark Barrett and Joseph E. Gonzalez and Percy Liang and Christopher Ré and Ion Stoica and Ce Zhang},
      year={2023},
      eprint={2303.06865},
      archivePrefix={arXiv},
      primaryClass={cs.LG}
}
```
