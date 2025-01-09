# qwen-0.5b-finetune
Finetuning qwen2.5 0.5b

## Benchmarking for Hallucination

- NER to recognize entities in GT vs Response
  - Combine spacy NER (en_core_web_lg) and roberta NER (xlm-roberta-large-finetuned-conll03-English)
- Ratio between total entities vs hallucinated entities
- Precision over recall
  - Positive = response entity
  - Out of all predicted positive, how many are actually positive?
  
## Finetuning

- Start with LoRA w/ Unsloth
  - Using ChatGPT to generate synthetic training data
  - According to LoRA paper, best place to inject A and B matricies are W_q and W_v, as it does well even with small rank (r)
  - Small vs Large ranks have significant overlap between their subspaces of top singular vectors (i.e.most meaningful directions are shared between low and high rank adaptations)

