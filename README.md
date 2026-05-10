# The Illusion of Failure: Re-evaluating Zero-shot MT of LLMs

[![Python](https://img.shields.io/badge/Python-3.11-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-red.svg)](https://pytorch.org/)
[![Transformers](https://img.shields.io/badge/HuggingFace-Transformers-orange.svg)](https://huggingface.co/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> An empirical evaluation of Mistral-7B on English-Vietnamese translation, highlighting the "Chatbot Verbosity" phenomenon and the obsolescence of the BLEU score.

---

### Abstract

Large Language Models (LLMs) are increasingly blurring the lines between specialized Neural Machine Translation (NMT) and general-purpose text generation. However, evaluating these generative models using traditional n-gram metrics presents a significant challenge. This project investigates the zero-shot translation capabilities of an open-source LLM (Mistral-7B-Instruct, 4-bit quantized) on the IWSLT'15 English-Vietnamese parallel dataset. 

Initial automated evaluations yielded an abysmal BLEU score of 3.69. However, subsequent qualitative analysis using the Multidimensional Quality Metric (MQM) framework revealed that this low score was an "illusion of failure." The model did not mistranslate; rather, it suffered from "Chatbot Verbosity"—providing accurate translations wrapped in conversational context, over-generated explanations, and literal/figurative alternatives. This project demonstrates that traditional metrics like BLEU are inherently obsolete for evaluating modern generative LLMs, penalizing them for stylistic flexibility and instruction-following behavior. The findings emphasize the critical need for strict prompt engineering (Negative Constraints) and semantic-based evaluation metrics (like COMET) in the LLM era.

### Citation

If you use this evaluation methodology or code in your research, please cite:
```bibtex
@misc{thu-zeroshot-mt-2026,
  author = {Van Thi Minh Thu},
  title = {The Illusion of Failure: Re-evaluating Zero-shot Machine Translation of LLMs and the Obsolescence of BLEU Score},
  year = {2026},
  publisher = {GitHub},
  url = {[https://github.com/yourusername/llm-zeroshot-mt-evaluation](https://github.com/yourusername/llm-zeroshot-mt-evaluation)}
}
```
### Acknowledgments
- Dataset: [IWSLT'15 English-Vietnamese Parallel Corpus](https://www.kaggle.com/datasets/tuannguyenvananh/iwslt15-englishvietnamese)
- Pretrained Model: [Mistral-7B-Instruct-v0.2](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.2)

---
> **Note:** While this project's code is MIT licensed, the dataset and model may have their own specific usage terms.
