## PERSON FACE RECOGNITION - PROJECT OVERVIEW

![alt text](https://github.com/Rahul-Khairnar/Person_Face_Recognition/blob/master/Photos/cover_photo.png "Localities Explore")

* Model to predict the person based on face recognition
* SVC is used to predict the person having an accuracy of about 94%.

## RESOURCES USED
* Programming Language - Python
* Modules used - Matplotlib, Pandas, Numpy, Seaborn, OS, Shutil, Sklearn, Pywt
* Tools used - Anaconda

## ABOUT THE DATASET
* The dataset consists of images of 5 different personalities
    * Maria Sharapova
    * Virat Kohli
    * Serena Williams
    * Lionel Messi
    * Roger Federer
* All images are collected from google images using Fatkun Chrome Extension
* Faces are extracted from the images using harr classifiers and saved separately.

## DATA CLEANING
* Faces are extracted from the images obtained from google images.


![alt text](https://github.com/Rahul-Khairnar/Person_Face_Recognition/blob/master/Photos/face_extract.PNG "Localities Explore")


* Faces are extracted using face and eye classifiers. 


![alt text](https://github.com/Rahul-Khairnar/Person_Face_Recognition/blob/master/Photos/eyes_detect.PNG "Localities Explore")


![alt text](https://github.com/Rahul-Khairnar/Person_Face_Recognition/blob/master/Photos/eyes_detect.PNG "Localities Explore")


* Once the new images are obtained, the image files consisting of side views of the faces are deleted.
* Since some photos had multiple faces in them, the extracted images containing faces which are not required are deleted manually.
* The images obtained are now passed through a function because of which wavelet transform is performed on all of them. 
* The wavelet transform of the images are joined to the extracted images by vertically stacking them together.


![alt text](https://github.com/Rahul-Khairnar/Person_Face_Recognition/blob/master/Photos/wavelet_transform.PNG "Localities Explore")


## MODEL DEVELOPMENT
* A database is obtained by using the vertically stacked images and is then divided into test and train datasets.
* The test dataset is used to train the different models. Different models tested are:
    * Random forests
    * Logistic Regression
    * Support vector machine
* SVM and Logistic regression performed the best with an almost identical accuracy of about 94%, whereas Random forests performed badly with an accuracy of 64%.


![alt text](https://github.com/Rahul-Khairnar/Person_Face_Recognition/blob/master/Photos/accuracy.PNG "Localities Explore")


* Confusion matrix is obtained for the same


![alt text](https://github.com/Rahul-Khairnar/Person_Face_Recognition/blob/master/Photos/confusion_matrix.PNG "Localities Explore")


### Hence SVM can be used for the further development.
