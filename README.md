# MKFM

> The official implementation for Findings of the EMNLP 2023 paper *An Empirical Study on Multiple Knowledge from ChatGPT for Emotion Recognition in Conversations*.

<img src="https://img.shields.io/badge/Venue-EMNLP--23-blue" alt="venue"/> <img src="https://img.shields.io/badge/Status-Accepted-success" alt="status"/> <img src="https://img.shields.io/badge/Issues-Welcome-red">

## Requirements
* Python 3.7.11
* PyTorch 1.8.0
* Transformers 4.1.1
* CUDA 11.1

## Preparation
Download [**datasets**](https://drive.google.com/file/d/1Xxgp-D2idEcds023iPilyCXYY4kF9tm8/view?usp=drive_link) and save them in ./data.

## Training & Evaluation
You can train the models with the following codes:

For IEMOCAP:
```sh
python run.py --dataset IEMOCAP --gnn_layers 4 --lr 0.0005 --batch_size 16 --epochs 30 --dropout 0.2
```
For MELD: python run.py --dataset MELD --lr 0.00001 --batch_size 64 --epochs 70 --dropout 0.1

For DailyDialog: python run.py --dataset EmoryNLP --lr 0.00005 --batch_size 32 --epochs 100 --dropout 0.3

For EmoryNLP: python run.py --dataset DailyDialog --gnn_layers 3 --lr 0.00002 --batch_size 64 --epochs 50 --dropout 0.3

## Citation
If you find our work useful for your research, please kindly cite our paper as follows:
```
@article{,
  title={An Empirical Study on Multiple Knowledge from ChatGPT for Emotion Recognition in Conversations},
  author={Geng Tu, Bin Liang, Bing Qin, Kam-Fai Wong, Ruifeng Xu},
  booktitle={Findings of The 2023 Conference on Empirical Methods in Natural Language Processing, (EMNLP 2023)},
  year={2023}
}
```

## Credits
The code of this repository partly relies on [DAG-ERC](https://github.com/shenwzh3/DAG-ERC) and I would like to show my sincere gratitude to the authors behind these contributions.
