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
Repository를 불러오고 현재 경로를 변경합니다.

    git clone https://github.com/KKN18/Pos-Neg-CNN.git
    cd Pos-Neg-CNN

원하는 epochs만큼 CNN 모델을 학습시켜 save_dir에 저장합니다.

    python train.py --epochs 20 --train_root '/content/drive/MyDrive/Colab Notebooks/CNN_Project/datasets/train' --valid_root '/content/drive/MyDrive/Colab Notebooks/CNN_Project/datasets/valid' --save_dir '/content/drive/MyDrive/Colab Notebooks/GitHub/Pos-Neg CNN/saved_model'
    
학습한 모델로 test폴더의 사진들에 대해 긍정/부정을 평가합니다.

    python eval.py --test_root '/content/drive/MyDrive/Colab Notebooks/GitHub/Pos-Neg CNN/datasets/test' --save_dir '/content/drive/MyDrive/Colab Notebooks/GitHub/Pos-Neg CNN/saved_model'

## Result
<img src = "https://github.com/KKN18/Pos-Neg-CNN/blob/main/test/1.jpg">

**>>Negative**

<img src = "https://github.com/KKN18/Pos-Neg-CNN/blob/main/test/2.jpg">

**>>Positive**

<img src = "https://github.com/KKN18/Pos-Neg-CNN/blob/main/test/3.jpg">

**>>Negative**

<img src = "https://github.com/KKN18/Pos-Neg-CNN/blob/main/test/4.jpg">

**>>Positive**

<img src = "https://github.com/KKN18/Pos-Neg-CNN/blob/main/test/5.jpg">

**>>Negative**

<img src = "https://github.com/KKN18/Pos-Neg-CNN/blob/main/test/6.jpg">

**>>Positive**

<img src = "https://github.com/KKN18/Pos-Neg-CNN/blob/main/test/7.jpg">

**>>Positive**
