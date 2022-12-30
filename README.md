---
license: apache-2.0
tags:
- generated_from_trainer
datasets:
- imagefolder
metrics:
- f1
model-index:
- name: vit-base-riego
  results:
  - task:
      name: Image Classification
      type: image-classification
    dataset:
      name: imagefolder
      type: imagefolder
      config: MaxP--agro_riego
      split: train
      args: MaxP--agro_riego
    metrics:
    - name: F1
      type: f1
      value: 0.9853801169590642
---

<!-- This model card has been generated automatically according to the information the Trainer had access to. You
should probably proofread and complete it, then remove this comment. -->

# vit-base-riego

This model is a fine-tuned version of [google/vit-base-patch16-224-in21k](https://huggingface.co/google/vit-base-patch16-224-in21k) on the imagefolder dataset.
It achieves the following results on the evaluation set:
- Loss: 0.0544
- F1: 0.9854

## Model description

More information needed

## Intended uses & limitations

More information needed

## Training and evaluation data

More information needed

## Training procedure

### Training hyperparameters

The following hyperparameters were used during training:
- learning_rate: 0.0002
- train_batch_size: 16
- eval_batch_size: 8
- seed: 42
- optimizer: Adam with betas=(0.9,0.999) and epsilon=1e-08
- lr_scheduler_type: linear
- num_epochs: 3
- mixed_precision_training: Native AMP

### Training results

| Training Loss | Epoch | Step | Validation Loss | F1     |
|:-------------:|:-----:|:----:|:---------------:|:------:|
| 0.0443        | 0.48  | 100  | 0.4737          | 0.8742 |
| 0.0349        | 0.95  | 200  | 0.0774          | 0.9733 |
| 0.003         | 1.43  | 300  | 0.0675          | 0.9794 |
| 0.002         | 1.9   | 400  | 0.0674          | 0.9810 |
| 0.0014        | 2.38  | 500  | 0.0431          | 0.9871 |
| 0.0011        | 2.86  | 600  | 0.0544          | 0.9854 |


### Framework versions

- Transformers 4.25.1
- Pytorch 1.13.0+cu116
- Datasets 2.8.0
- Tokenizers 0.13.2
