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
2.  
