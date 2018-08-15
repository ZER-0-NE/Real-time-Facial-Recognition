# DataScience_AbsoluteFace

#### I make use of three methods for face recognition:
1. References from the [face recognition](https://github.com/thecodacus/Face-Recognition) repository on github.
 
##### Dependencies:
  * Python 2/3
  
  * OpenCV module for the respective python version
  
  * Numpy
         
##### Working

We define **three** scripts for the face recognition:

* [**data_set.py**](https://github.com/ZER-0-NE/DataScience_AbsoluteFace/blob/master/absolute_face_1/data_set.py) : Before running, **make a folder "dataset" on the same path as the python script**. This script creates

     samples of user faces live from the webcam. This is a very fast process and you

     can enter multiple faces according to user number entered in the beginning.  You can also increase the count of               

     face samples to be taken at a time for a user. As default I have set it as 50. You can increase the number and it is 

     supposedly measured to work better for more number of training samples with also an hike in accuracy. Run the

     script by "python data_set.py". The dataset folder gets populated with images with names like "user1.1.jpg",

     "user1.2.jpg" for first user and similarly "user.2.1.jpg", user.2.2.jpg" for second user.

* [**trainer.py**](https://github.com/ZER-0-NE/DataScience_AbsoluteFace/blob/master/absolute_face_1/trainer.py) : **Create a folder namely Trainer in the same way you created dataset folder**. This script trains for 
     
     the number of users mentioned in the previous script. To run it, use 

     "python trainer.py" from the folder containing the script. We make use of LBPH(Local Binary Patterns

     Histograms) recognizer included in OpenCV. In the next section we make use of Deep Learning

* [**recog.py**](https://github.com/ZER-0-NE/DataScience_AbsoluteFace/blob/master/absolute_face_1/recog.py ): By running this script using "python recog.py", we allow the webcam to start and thus recognise

     with a confidence level(0% = Perfect match) the users defined in the first script. We include an array for the names of 
     
     user. Make sure to modify it accordingly.
              
#### NOTE: We can get better performance by tweaking some of the parameters like increasing the condition of count and taking more samples of training data. The performance is also dependent on the GPU/CPU cores involved. Using a good GPU can significantly enhance the fps 

[LINK TO VIDEO](https://youtu.be/E5L5vEXQ9e0)
 
 2. Using Deep Metric Learning with references from [Adrian's Blog](https://www.pyimagesearch.com/2018/06/18/face-recognition-with-opencv-python-and-deep-learning/)
 
 ##### Dependencies:
  * Python 2/3
  
  * OpenCV module for the respective python version
  
  * Dlib
  
  * face_recognition module installed
  
  * A GPU is preferred but not necessary.
  
  ##### Working:
  
  * Create a dataset for the user faces(cropped properly) and store them in a folder 'dataset'. 
  The tree should look something like this:
  
  ├── dataset
  
│   ├── abhi [24 entries]

│   ├── sidmo [26 entries]

│   ├── chillar [25 entries]

  * We use the face_recognition module pretrained on ~3 million images and create 128-d images for our dataset using the [encode_faces.py](https://github.com/ZER-0-NE/DataScience_AbsoluteFace/blob/master/absolute_face_2/encode_faces.py) script.

 
 3. Using [face_recognition](https://github.com/ageitgey/face_recognition) module developed by Adam Geitgey
