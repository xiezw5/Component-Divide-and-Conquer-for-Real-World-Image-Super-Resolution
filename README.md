# Component Divide-and-Conquer for Real-World Image Super-Resolution(CDC)

This repository is an official PyTorch implementation of the paper **"Component Divide-and-Conquer for Real-World Image Super-Resolution
"** from **ECCV 2020**.

We provide full training and testing codes, pre-trained models and the large-scale dataset used in our paper. You can train your model from scratch, or use a pre-trained model to enlarge your images.

## Code
### Dependencies
* Python 3.6
* PyTorch >= 1.1.0
* numpy
* cv2
* skimage
* tqdm

### Quick Start
Clone this github repo.
```bash
git clone https://github.com/xiezw5/Component-Divide-and-Conquer-for-Real-World-Image-Super-Resolution
cd Component-Divide-and-Conquer-for-Real-World-Image-Super-Resolution/CDC
```
#### Training
1. Download our dataset and unpack them to any place you want. Then, change the ```dataroot``` and ```test_dataroot``` argument in ```./options/realSR_CDC.py``` to the place where images are located.
2. Run ```CDC_train_test.py``` using script file ```train_pc.sh```.
```bash
sh ./train_pc.sh cdc_x4 ./CDC_train_test.py ./options/realSR_HGSR_MSHR.py 1
```
3. You can find the results in ```./experiments/CDC-X4``` if the ```exp_name``` argument in ```./options/realSR_CDC.py``` is ```CDC-X4```

#### Testing
1. Download our pre-trained models to ```./models``` folder or use your pre-trained models
2. Change the ```test_dataroot``` argument in ```CDC_test.py``` to the place where images are located
3. Run ```CDC_test.py``` using script file ```test_models_pc.sh```.
```bash
sh test_models_pc.sh cdc_x4_test ./CDC_test.py ./models/HGSR-MHR_X4_SubRegion_GW_283.pth 1
```
4. You can find the enlarged images in ```./results``` folder

### Pretrained models
1. [2X Models]()
2. [3X Models]()
3. [4X Models]()

The above provided models are both trained on our dataset with our Gradient-weighted loss.

