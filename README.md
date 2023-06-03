Create a directory called data that will be used to store the training dataset[The more the model is trained, the more accurate it becomes]

++++++++++++++++++++++ How it Works +++++++++++++++++++

1. Generate dataset function: This is the function that automatically generates the dataset that will
be used to train the learning model. This function opens the camera detects a person’s face and
takes 100 images of a person, crops them and stores them in a directory. Before it stores the
images into the directory, it first changes the images into gray scale images. The images are stored
in line with their identity, e.g. images for user 1 will be stored under user1 and images from user
2 will be stored under user2.

2. Create the learning mode and train the module: This is the function that has the learning model.
It is the function that will take input from the dataset created in the generate dataset function and
use it to train. The data in the dataset will be divided into two, training dataset and testing dataset.
This will increase the accuracy of the trained module. As the training is going on, this function
will also display the accuracy of the training.

3. Image collecting function: This function will open the camera and take images of the person
whom the system is going to predict whether his image is in the dataset. The user will manually
take images of him/herself and the system will automatically append the images in a directory.
This function is configured in a way that when another person collects images using this function,
the previous images get deleted.

4. Prediction function: This function automatically collects images from the directory created the
image collecting function and uses them as their input to predict the data. This prediction data
tells the user if he/she is verified or not verified. Verified users are the users of whom the
prediction module has positively predicted their images and those who are not verified are those
whom the system has negatively predicted their images.
