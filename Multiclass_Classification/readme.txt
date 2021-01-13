http://www.laurencemoroney.com/rock-paper-scissors-dataset/

Rock Paper Scissors is a dataset containing 2,892 images of diverse hands in Rock/Paper/Scissors poses. 
It is licensed CC By 2.0 and available for all purposes, but it’s intent is primarily for learning and research.

Rock Paper Scissors contains images from a variety of different hands,  from different races, ages and genders,
posed into Rock / Paper or Scissors and labelled as such. 
Traning /test sets are available as well as few images to use for prediction. 
The images have all been generated using CGI techniques as an experiment in determining if a CGI-based dataset can be used for classification against real images.
All of this data is posed against a white background.

Each image is 300×300 pixels in 24-bit color


## To use multiclass classification the following must be done:
1) The "class_mode" parameter on the train generator should change to "categorical" (on train_datagen.flow_from_directory)
2) On model definition the output layer must be changed according to the # that we want to have as an output for e.g. in the case of rock/paper/scissors this
   will be 3 and the activation cannot be of course "sigmoid" since this is only for "binary" classification. Instead the activation can be for e.g. 'softmax'
   which turns all the values into probabilities that will sum up to one. 
3) The final change is when we compile the network. The loss_function should be changed for e.g. to "categorical_crossentropy"
   
   
