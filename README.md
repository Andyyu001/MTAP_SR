# MTAP_SR
This is an official implementation of _From Low to High: Cascade network for Restoring Low-resolution Face Image via Extracting and Transforming edge Feature_

## Dependenices
* python3.6
* pytorch = 1.2
* NVIDIA GPU + CUDA
* Python packages: pip install numpy opencv-python

## Dataset Preparation
The train and test dataset are obtained by using the above-constructed method from **CelebAMask HQ dataset**.        
To construct the low-quality face dataset, we process the HR face images by using the following method. 
* all face images are normalized as the size $256 \times 256$.
* these normalized images are blurred by randomly using blurry kernel from DeblurGAN.
* the LR face images can be produced by downsampling from the blurry face images. It is noted that the size of the LR face image is set as $<16 \times 16>.

## Train



## Test on Synthetic Images
