# Photo Reconstruction Kaggle Challenge
## Pix2Pix Model

### Group 7
- Vibhu (20CS10072)
- Tanmay Mohanty (20CS10089)
- Shruti Pandey (21CS60R40)

### Requirements
    torch>=1.13.1
    torchvision>=0.14.1
    opencv-python>=4.7.0
    pandas>=1.5.3
    dominate>=2.7.0
    visdom>=0.2.4
    wandb>=0.14.2



### Preparing for Training
- Unzip the photo-reconstruction.zip to get the images.
- Run the Images.ipynb notebook to create and augment the dataset as required by the pix2pix model.

### Training the Model
    python train.py --dataroot .\..\Dataset --phase Train --model pix2pix --name pix2pix_animals --direction AtoB --batch_size 32
For training the pix2pix model, cd into the "pix2pix" directory and run:


### Generating Output on Test Data
    python test.py --dataroot .\..\Dataset\ --phase Test --model pix2pix --name pix2pix_animals --direction AtoB --eval --num_test 200

### Creating the submission csv from output images
- Run the submission.ipynb notebook to generate the csv