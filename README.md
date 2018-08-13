# DataScience_AbsoluteFace

#### I make use of two methods for face recognition:
1. References from the [face recognition](https://github.com/thecodacus/Face-Recognition) repository on github.
 
##### Dependencies:
  * Python 2/3
  
  * OpenCV module for the respective python version
  
  * Numpy
         
##### Working

* We define **three** scripts for the face recognition:

* **data_set.py** : Before running, **make a folder "dataset" on the same path as the python script**. This script creates

     samples of user faces live from the webcam. This is a very fast process and you

     can enter multiple faces according to user number entered in the beginning.  You can also increase the count of               

     face samples to be taken at a time for a user. As default I have set it as 50. You can increase the number and it is 

     supposedly measured to work better for more number of training samples with also an hike in accuracy. Run the

     script by "python data_set.py". The dataset folder gets populated with images with names like "user1.1.jpg",

     "user1.2.jpg" for first user and similarly "user.2.1.jpg", user.2.2.jpg" for second user.

* **trainer.py** : **Create a folder namely Trainer in the same way you created dataset folder**. This script trains for 
     
     the number of users mentioned in the previous script. To run it, use 

     "python trainer.py" from the folder containing the script. We make use of LBPH(Local Binary Patterns

     Histograms) recognizer included in OpenCV. In the next section we make use of Deep Learning

* **recog.py** : By running this script using "python recog.py", we allow the webcam to start and thus recognise

     with a confidence level the users defined in the first script.
              
#### NOTE: We can get better performance by tweaking some of the parameters like increasing the condition of count and taking more samples of training data. The performance is also dependent on the GPU/CPU cores involved. Using a good GPU can significantly enhance the fps 
              
 
 2. Using [face_recognition](https://github.com/ageitgey/face_recognition) module developed by Adam Geitgey
