# Positive/Negative Classification CNN

## Environment
모든 작업이 Google Colab Notebooks에서 진행되었습니다. 

## Dataset
구글 크롤링을 이용해 데이터셋을 만들었습니다.

**Positive Keyword** : Happy, Beautiful Environment, love, 행복, 웃음, 가족

**Negative Keyword** : Sad, Crying, Depression, Spooky, 자연재해, 외로움


    ├── datasets
    |   ├── train              # Train
    |   |   ├── 0              # Positive images (i.e. Happy)
    |   |   └── 1              # Negative images (i.e. Sad)
    |  
    |   ├── valid              # Validation
    |   |   ├── 0              # Positive images (i.e. Love)
    |   |   └── 1              # Negative images (i.e. Spooky)
    | 
    |   ├── test               # Test images

다음 링크를 통해 다운받으실 수 있습니다.

[Datasets](https://drive.google.com/drive/folders/14hvvYNGkppzlFY7WcNSp_wj9gpH9Uj1-?usp=sharing) 



## Setup
<code> Google Colab Notebooks</code> 에서 <code> git clone</code> 커맨드를 입력합니다.

    !git clone https://github.com/KKN18/Pos-Neg-CNN.git

1. **train.ipynb** : pretrained Resnet 101을 fine tuning 하여 학습을 진행 및 saved_model 폴더에 저장합니다.
2. **eval.ipynb** : test 폴더에 있는 사진들에 대해 긍정/부정을 평가합니다. 
