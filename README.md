---
language:
- en
license: apache-2.0
datasets:
- Open-Orca/OpenOrca
- jackhhao/jailbreak-classification
metrics:
- accuracy
library_name: transformers
pipeline_tag: text-classification
tags:
- jailbreak
- security
- moderation
- prompt-injection
---

# Jailbreak Classifier

Classifies prompts as jailbreaks or benign. This is a fine-tune checkpoint of [bert-base-uncased](https://huggingface.co/bert-base-uncased) on the [jailbreak-classification](https://huggingface.co/datasets/jackhhao/jailbreak-classification) dataset.

## Training Details

### Training Data

Fine-tuned on the [jailbreak-classification](https://huggingface.co/datasets/jackhhao/jailbreak-classification) dataset.

### Training Procedure 

#### Training Hyperparameters

Fine-tuning hyper-parameters:
- learning_rate = 5e-5
- train_batch_size = 8
- eval_batch_size = 8
- lr_scheduler_type = linear
- num_train_epochs = 5.0