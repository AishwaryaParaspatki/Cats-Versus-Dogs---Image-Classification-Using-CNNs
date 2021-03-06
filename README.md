# Cats Versus Dogs - Image Classification Using CNNs

### This notebook consists of 3 parts:<br>
Image Augmentation<br>
CNN Model<br>
VGG16 Model<br>

### Technology stack:<br>
Python<br>
Keras - TensorFlow<br>
matplotlib<br>
Numpy<br>
piexif<br>
shutil<br>

The dataset for this project is hosted by Microsoft.<br>
https://www.microsoft.com/en-us/download/details.aspx?id=54765
<br>

### Notebooks:

1. visualize.ipynb:<br>

<p align = 'center'>Cats:<br>
  
  ![Cats](/images/Cat.png)

  Dogs:
  ![Dogs](/images/Dog.png)
</p><br>


2. Image Augmentation:<br>
<p align = 'center'>
  An example on a random image from the dataset.<br>

  ![Augmented_Image](/images/Image_aug.png)
</p>
<br>


3. CNN Model:<br>
The Hyper Parameters used:<br>
FILTER_SIZE = 3<br>
NUM_FILTERS = 32<br>
INPUT_SIZE  = 32<br>
MAXPOOL_SIZE = 2<br>
BATCH_SIZE = 16<br>
STEPS_PER_EPOCH = 20000//BATCH_SIZE<br>
EPOCHS = 20<br>
<br>
<p align = 'center'>The CNN model layer sequence goes like:<br>
Conv2D -> MaxPooling -> Conv2D -> MaxPooling -> Flatten -> Dense -> Dropout -> Output<br>
with sigmoid activation for the output layer and relu activation for the rest of the layers with adam optimizer and accuracy as the evaluation metric.<br>
  Output:<br>
  loss: 0.7063166499137878<br>
  accuracy: 0.778124988079071
</p>
<br>
<br>

4. VGG 16:<br>
Taking the input size of 128 with a batch size of 16 examples, I have trained the VGG16 model from keras, by freezing the pretrained layers, for 3 epoches with 200 steps per epoch using imagenet dataset's pretrained weights.<br>
<p align = 'center'>loss: 0.47205138206481934<br>
accuracy: 0.8762500286102295</p>
