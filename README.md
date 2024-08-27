# transfuserOnCarlaColaTruck

Reproducing results from Tubingen AI's transfuser and evaluating the model on a bigger vehicle. 


## System Specifications:

1.  Operating System:   Ubuntu 20.04.6 LTS
2.  GPUs:               2x NVIDIA A10-8Q
3.  RAM:                62.79 GBs
4.  Storage:            1 TB

## Driver Versions and Environment

1.  CUDA Version: 11.3 (the others didn't work so well for me)
2.  Virtual Environment Manager: Conda
3.  Python Version: 3.7.13
4.  My pip list can be found in requirements.txt
```python
pip install -r requirements.txt
```

## Follow the following steps to evaluate on your system

### 1.  Setup
```python
git clone https://github.com/autonomousvision/transfuser.git
cd transfuser
git checkout 2022
chmod +x setup_carla.sh
./setup_carla.sh
conda env create -f environment.yml
conda activate tfuse
```
**CUDA Compatibility issues took me a while to fix. I started with the ones provided by the developers and ended with the ones mentioned in requirements.txt. If installing those doesn't work, run the following to get the torch, torch-scatter and mmcv that worked for me.**
```python
pip3 install torch==1.12.0 torchvision==0.13.0 torchaudio==0.12.0 --extra-index-url https://download.pytorch.org/whl/cu113
pip install torch-scatter -f https://data.pyg.org/whl/torch-1.12.0+cu113.html
pip install mmcv-full==1.6.0 -f https://download.openmmlab.com/mmcv/dist/cu113/torch1.12.0/index.html
```
### 2.  Getting Pre-Trained Agents
```python
mkdir model_ckpt
wget https://s3.eu-central-1.amazonaws.com/avg-projects/transfuser/models_2022.zip -P model_ckpt
unzip model_ckpt/models_2022.zip -d model_ckpt/
rm model_ckpt/models_2022.zip
```
