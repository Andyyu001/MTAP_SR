# MTAP_SR
This is an official implementation of _From Low to High: Cascade network for Restoring Low-resolution Face Image via Extracting and Transforming edge Feature_

## codes and dataset
All dataset and codes could be downloaded by following website:
链接：https://pan.baidu.com/s/1KUPHAk0h0v89GfXC_lirZQ 
提取码：8itz

## Dependenices
* python3.6
* pytorch = 1.2
* NVIDIA GPU + CUDA10.0
* Python packages: pip install numpy opencv-python os pandas


## Dataset Preparation
The train and test dataset are obtained by using the above-constructed method from **CelebAMask HQ dataset**.        
To construct the low-quality face dataset, we process the HR face images by using the following method. 
* all face images are normalized as the size $256 \times 256$.
* these normalized images are blurred by randomly using blurry kernel from DeblurGAN.
* the LR face images can be produced by downsampling from the blurry face images. It is noted that the size of the LR face image is set as $<16 \times 16>.

### how to create the datafile
* 1. opening code _Get_data.py_ 
* 2. changing the path of your dataset, and labelfile
* 3. getting the labelfile, e.g. _data/label10000.csv_

## Train
* 1. opening code _train_16times_GAN.py_
* 2. changing the Dataset loader by _data/label10000.csv_
* 3. changing the save_path on your path, e.g. _Model_study/P16times/GAN_8/netG_B8_D1W_vggImgGAN_284.pth_
* 4. python --cuda --batchSize 10  

## Test on Synthetic Images
evaluation methods including GMSE,LPIPS, PSNR, SSIM, OIM
* 1. opening code _test_16times.py_
* 2. changing the save_path on your path
* 3. python --cuda --generator Model_study/P16times/GAN_8/netG_B8_D1W_vggImgGAN_284.pth

## Acknowledgment
The auothor would like to thank the opening-source codes from DeblurGAN, SFT_SR, and so on.
