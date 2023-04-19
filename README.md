# unpairedi2i
access the pretrained model file in the drive link mentioned below
https://drive.google.com/drive/folders/1yow7nIUbqBzxWp99daH7tDTN85lCiZZd?usp=share_link
upload this in your working directory , make necessary location changes while debugging

The link mentioned below is for data 
https://drive.google.com/drive/folders/1jBAk4nnCBqYRdFuaQN56eaLJ9d5vFFDm?usp=share_link
upload this in your working directory , make necessary location changes while debugging


----------------------------------------------------------------------------------------
## Dependencies
```
conda create -n EGSDE python=3.7
conda activate EGSDE
conda install pytorch==1.9.0 torchvision==0.10.0 torchaudio==0.9.0 cudatoolkit=10.2
pip install pyyaml
pip install scipy
```
run this file
$ python run_EGSDE.py


```
```task``` is which task to run and is chosen from ```cat2dog```.In cat2dog , the resutls will be saved in ```runs/cat2dog```. The default args is provided in ```profiles/cat2dog/args.py```.
* ```testdata_path``` is the path for source image. ```ckpt``` is the path for score-based diffusion model. ```dsepath``` is the path for domain-specific extractors. 
  ```diffusionmodel``` is the backbone of noise prediction network , where ```ADM``` support [guided-diffusion](https://github.com/openai/guided-diffusion) and ```DDPM``` support [ddim](https://github.com/ermongroup/ddim).

## Evaluation
```
$ python run_score.py

