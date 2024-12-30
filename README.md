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

