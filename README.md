# DataScience_AbsoluteFace

#### I make use of two methods for face recognition:
 1. Refernces from the [face recognition](https://github.com/thecodacus/Face-Recognition) repoitory.
 
     *Dependencies:
     
         *Python 2/3
         *OpenCV module for the respective python version
         *Numpy
         
      *Working
      
          * We define three scripts for the face recognition:
          
              * data_set.py : This creates samples of user faces live from the webcam. This is a very fast process and you can  
              enter multiple faces according to user number entered in the beginning.  You can also increase the count of face
              
              samples to be taken at a time for a user. As default I have set it as 50. You canincrease the number and it is 
              
              supposedly measured to work better for more number of training samples with also an hike in accuracy. Run the
              
              script by "python data_set.py". Before running, make a folder "dataset" on the same path as the python script.
              
              * trainer.py : This script trains for the number of users mentioned in the previous script. To run it, use 
              
              "python trainer.py" from the folder containing the script.
 
 
 
 
 
 
 
 2. Using [face_recognition](https://github.com/ageitgey/face_recognition) module developed by Adam Geitgey
