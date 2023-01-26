# DisCoHead: Audio-and-Video-Driven Talking Head Generation by Disentangled Control of Head Pose and Facial Expressions
## [Geumbyeol Hwang](https://www.youtube.com/watch?v=bluhvpjWZOM), [Sunwon Hong](https://www.youtube.com/watch?v=pSUydWEqKwE), [Seunghyun Lee](https://www.youtube.com/@bankiszon/featured), [Sungwoo Park](https://www.youtube.com/watch?v=6yAmhBamecg), and [Gyeongsu Chae](https://www.youtube.com/watch?v=2f1Ny74_ou0).
<p align="center">
    <br>
    <img src='./demo2.gif' width=800>
    <br>
<p>


<p align="center">
    <br>
    <img src="https://assets.website-files.com/6392a785ccd80ebf6f060fbe/6392a7df8df82ba809d50347_Logo_Home.svg" width="400"/>
    <br>
<p>





# [Demo🕵️](https://deepbrainai-research.github.io/discohead)



## Requirements
- CUDA 10.2
- PyTorch 1.10.0
- Python 3.7

## Installation
You can install environements by 1. or 2.

1. Copy created conda environment
```
git clone  https://github.com/deepbrainai-research/discohead
cd discohead
conda env create -f discohead.yaml
conda activate discohead
```
2. Install requirements yourself
```
git clone  https://github.com/deepbrainai-research/discohead
cd discohead
conda env create -n discohead python=3.7
conda activate discohead
conda install pytorch==1.10.0 torchvision==0.11.1 torchaudio==0.10.0 cudatoolkit=10.2 -c pytorch
pip install -r requirements.txt
```

## Generate Demo Results

- Download the pre-trained checkpoints from [google drive](https://drive.google.com/drive/folders/1z2uuPkXEacVSY7Hd5k_QD7ZIrVd2_a28?usp=sharing) and put into `weight` folder
- Create the `dataset` folder.
- Unzip the `dataset_demo.zip` to `dataset`
- `DiscoHead` directory should have the following structure
```
DiscoHead/
├── dataset/
│   ├── obama/
│   │   ├──demo1/
│   │   ├──demo2/
│   ├── grid/
│   │   ├──demo1/
│   │   ├──demo2/
│   ├── koeba/
│   │   ├──demo1/
│   │   ├──demo2/
├── weight/
│   ├── obama.pt
│   ├── grid.pt
│   ├── koeba.pt
‥‥
```
- The `--mode` argument is used for specifying which demo you want to generate
- To reproduce demo1 of obama dataset, run command :
```
python test.py -m obama_demo1
```
