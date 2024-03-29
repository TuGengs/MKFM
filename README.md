# MKFM

> The official implementation for Findings of the EMNLP 2023 paper *An Empirical Study on Multiple Knowledge from ChatGPT for Emotion Recognition in Conversations*.

<img src="https://img.shields.io/badge/Venue-EMNLP--23-blue" alt="venue"/> <img src="https://img.shields.io/badge/Status-Accepted-success" alt="status"/> <img src="https://img.shields.io/badge/Issues-Welcome-red">

## Requirements
* Python 3.7.11
* PyTorch 1.8.0
* Transformers 4.1.1
* CUDA 11.1

## Preparation
Download [**datasets**](https://drive.google.com/file/d/1I47mbbHSc2vkNXZs_NjRng-7cglqDdSd/view?usp=drive_link) and save them in ./data.

Download [**knowledge**](https://drive.google.com/file/d/1w_9aFxQVKPkGIH2Gednb_JFoimZTJLZ1/view?usp=drive_link) and save them in ./.

## Training & Evaluation
You can train the models with the following codes:

* ```--TP ```: Using auxiliary label knowledge: topic
* ```--SC ```: Using auxiliary label knowledge: sarcasm
* ```--MP ```: Using auxiliary label knowledge: metaphor
* ```--EC ```: Using auxiliary utterance knowledge: emotional cause
* ```--CS ```: Using auxiliary utterance knowledge: commonsense knowledge
* ```--ACS ```: Using auxiliary utterance knowledge: affective commonsense knowledge
* ```--CR ```: Using auxiliary contextual knowledge: co-reference
* ```--CT ```: Using auxiliary contextual knowledge: context
* ```--EC2 ```: Using auxiliary contextual knowledge: emotional cause

For IEMOCAP: ```python run.py --dataset IEMOCAP --gnn_layers 4 --lr 0.0005 --batch_size 16 --epochs 30 --dropout 0.2 ```

For MELD: ```python run.py --dataset MELD --lr 0.00001 --batch_size 64 --epochs 70 --dropout 0.1 ```

For EmoryNLP: ```python run.py --dataset EmoryNLP --lr 0.00005 --batch_size 32 --epochs 100 --dropout 0.3 ```

## Citation
If you find our work useful for your research, please kindly cite our paper as follows:
```
@inproceedings{tu2023empirical,
  title={An Empirical Study on Multiple Knowledge from ChatGPT for Emotion Recognition in Conversations},
  author={Tu, Geng and Liang, Bin and Qin, Bing and Wong, Kam-Fai and Xu, Ruifeng},
  booktitle={Findings of the Association for Computational Linguistics: EMNLP 2023},
  pages={12160--12173},
  year={2023}
}
```

## Credits
The code of this repository partly relies on [DAG-ERC](https://github.com/shenwzh3/DAG-ERC) and I would like to show my sincere gratitude to the authors behind these contributions.
