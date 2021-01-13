
## The "Cats_vs_dogs_with_Image_Augmentation.ipynb" example shows how to add Image Augmentation.
## It is added only on the training set as below:

#### Image Augmentation on training set 
train_datagen = ImageDataGenerator(
      rescale=1./255,
      rotation_range=40,
      width_shift_range=0.2,
      height_shift_range=0.2,
      shear_range=0.2, # skewing
      zoom_range=0.2,
      horizontal_flip=True,
      fill_mode='nearest' # for the pixels around 
      )
     
For more info on Image Data Preprocessing for Keras see here: https://keras.io/api/preprocessing/image/

