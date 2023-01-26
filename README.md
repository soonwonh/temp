# DisCoHead: Audio-and-Video-Driven Talking Head Generation by Disentangled Control of Head Pose and Facial Expressions
 
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





# [Demo🕵️](https://deepbrainai-research.github.io/discohead) | [KoEBA](https://github.com/deepbrainai-research/koeba)



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

## Generating Demo Videos

- Download the pre-trained checkpoints from [google drive](https://drive.google.com/drive/folders/1JOWwCVF8v2yNJ_n6a4BsaXuZZFKGo4je?usp=sharing) and put into `weight` folder
- Create the `dataset` folder.
- Unzip the `dataset_demo.zip` to `dataset`
- `DiscoHead` directory should have the following structure
```
DiscoHead/
├── dataset/
│   ├── fig2/
│   ├── fig3/
│   ├── fig4/
├── weight/
│   ├── obama.pt
│   ├── grid.pt
│   ├── koeba.pt
‥‥
```
- The `--fig_number` argument is used for specifying which figure you want to generate
- To reproduce fig. 2 of obama dataset, run command :
```
python test.py --fig_number 2
```

### [Geumbyeol Hwang], [Sunwon Hong], [Seunghyun Lee], [Sungwoo Park], and [Gyeongsu Chae].
