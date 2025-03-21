# EnlightenGAN

### Representitive Results
![representive_results](/assets/show_3.png)

### Overal Architecture
![architecture](/assets/arch.png)

## Environment Preparing
```
python3.5
```
You should prepare at least 3 1080ti gpus or change the batch size. 


```pip install -r requirement.txt``` </br>
```mkdir model``` </br>


EnlightenGAN/final_dataset/trainA   EnlightenGAN/final_dataset/trainB

 EnlightenGAN/test_dataset/trainA Low light EnlightenGAN/test_dataset/testB 
EnlightenGAN/ablation/enlightening 

### Training process
Before starting training process, you should launch the `visdom.server` for visualizing.

```nohup python -m visdom.server -port=8097```

then run the following command

```python scripts/script.py --train```

### Testing process

Create directories `../test_dataset/testA` and `../test_dataset/testB`. Put your test images on `../test_dataset/testA` (And you should keep whatever one image in `../test_dataset/testB` to make sure program can start.)

Run

```python scripts/script.py --predict```

### Dataset preparing

Training data [[Google Drive]](https://drive.google.com/drive/folders/1fwqz8-RnTfxgIIkebFG2Ej3jQFsYECh0?usp=sharing) (unpaired images collected from multiple datasets)

Testing data [[Google Drive]](https://drive.google.com/open?id=1PrvL8jShZ7zj2IC3fVdDxBY1oJR72iDf) (including LIME, MEF, NPE, VV, DICP)


