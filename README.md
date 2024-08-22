# Adversarial Attacks and Defenses on BERT based NLU Tasks

For our project, we experimented with attacks and defenses and LLMs for NLU tasks.

The models we attacked are  - DeBERTa, Distilbert, and a BERT finetuned on a financial dataset.

All these models are trained on entailment tasks i.e. for a given premise and hypothesis pair, they determine if the hypothesis follows, contradicts, or is unrelated to the premise.

The datasets we experimented with are from GLUE - specifically, the RTE, MRPC, MNLI and QNLI subsets.

## Finetuning

To establish a baseline, we finetuned each model (DeBERTa and Distilbert) on each dataset. This brought up the accuracy from around 65% before finetuning, to 86% after finetuning. We did not have to finetune the third BERT model since it was already finetuned.

You can find the notebooks for finetuning at `/Finetuning_and_attacks/`.

## Attacks

We ran 5 attacks on most models - Textbugger, Textfooler, Deepwordbug, PWWS, IGA.

You can find the notebooks for Attacks at `/Finetuning_and_attacks/`

## Defenses

We also implemented 2 defenses - Adversarial Training, Multi-Model Adversarial Differential Defense (MMADD)

You can find the notebooks for Adversarial Training at `/Defense 1 - Adversarial_training/`

You can find the notebooks for MMADD at `/Defense 2 - MMADD/`

## Organization

All work was done in .ipynb files organized into the following folders:
- Finetuning_and_Attacks : Contains 7 notebooks (4 for DeBERTa (MRPC, RTE, MNLI, QNLI); 2 for DistilBERT (MRPC, RTE) ; 1 for financial BERT)
- Defense 1 - Adversarial Training : Contains 3 notebooks (1 for all DeBERTa models, 1 for all DistilBERT models, 1 for financial BERT)

There is a third log folder that contains .csv files with details on every datapoint's attacks and defenses.

These are also stored in a drive link for easy interfacing with google colab. The finetuned models are stored at these links:

- [Adversarially trained DeBERTa models](https://drive.google.com/drive/folders/1FBP_DZnPgIsqwtqv-x2UfoygrJAE37jE?usp=sharing)
- [Adversarially trained Distilbert models](https://drive.google.com/drive/folders/102PtOH1J3_cTnZdF3AJfs6Jqt6EoSpu2?usp=sharing)
- [Adversarially trained FinBERT models](https://drive.google.com/drive/folders/1PZZHKw4Xp-PQ6wizXFGoQXR_S27UytTO?usp=sharing)

These links are set to be viewable by anyone with the link, do let us know if you have any trouble accessing them!