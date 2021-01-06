# Persian Digit Image Classifier
Two neural network models, Multilayer Perceptron Neural Network (MLP-NN) and Convolutional Neural Network (CNN) , that classify image of Persian digits.

## Datasets

### Persian digits
Due to privacy issues, the models are presented here for HODA handwringing Persian digits dataset. The trained models are re-trained for images of Persian digits.<br>

[HODA dataset](http://farsiocr.ir/%D9%85%D8%AC%D9%85%D9%88%D8%B9%D9%87-%D8%AF%D8%A7%D8%AF%D9%87/%D9%85%D8%AC%D9%85%D9%88%D8%B9%D9%87-%D8%A7%D8%B1%D9%82%D8%A7%D9%85-%D8%AF%D8%B3%D8%AA%D9%86%D9%88%DB%8C%D8%B3-%D9%87%D8%AF%DB%8C/)<br>
HODA dataset is the first dataset of handwritten Farsi digits that has been developed during an MSc. project in Tarbiat Modarres University entitled: Recognizing Farsi Digits and Characters in SANJESH Registration Forms. This project has been carried out in cooperation with Hoda System Corporation. It was finished in summer 2005 under supervision of Prof. Ehsanollah Kabir. Samples of the dataset are handwritten characters extracted from about 12000 registration forms of university entrance examination in Iran. The dataset specifications is as follows:

  * Resolution of samples: 200 dpi<br>
  * Total samples: 102,352 samples<br>
  * Training samples: 60,000 samples<br>
  * Test samples: 20,000 samples<br>

10% of training data are used for validation purpose.
  
A function reading images in HODA dataset is developed by Amir Saniyan and is available here which is used in this work
[HodaDatasetReader](https://github.com/amir-saniyan/HodaDatasetReader)

<p align="center">
<img  align="center" src="https://github.com/saniaki/digit-classifier/blob/master/images/Persian/HODA-dataset._Persian.jpg" width="300"/>
<br>

### English digits
Same models are applied to SVHN data set which includes images of real word English digits.
[SVHN dataset](http://ufldl.stanford.edu/housenumbers/) <br>
<p align="center">
<img  align="center" src="https://github.com/saniaki/digit-classifier/blob/master/images/English/Numbers.jpg" width="300"/>
 
Both neural networks are trained on a subset of SVHN dataset including 73257 training data and 26032 test data. In each case, 10% of training data are used for validation purpose.
Input images are 32*32*3. The training is applied to the grey scale images of 32*32*1 obtained through preprocessing of data.


## Neural Networks 

CNN Model:
* l2 regularization
* He weights initializer
* ones bias initializer
* batchnrmalization
* dropout
* relu and softmax activations
* test accuracy, Persian digits = 0.983, English digits = 0.898 

<p align="center">
<img  align="center" src="https://github.com/saniaki/digit-classifier/blob/master/images/English/CNN_Summary.jpg" width="450"/>
 
 
MLP Model:
* l2 regularization
* He weights initializer
* ones bias initializer
* relu and softmax activations
* test accuracy, Persian digits = 0.966, English digits = 0.779 

<p align="center">
<img  align="center" src="https://github.com/saniaki/digit-classifier/blob/master/images/English/MLP_Summary.jpg" width="450"/>
 

## Predictions
For HODA Persian dataset, both models makes highly accurate predictions.  For SVHN English dataset, CVV model is more accurate.  <br>
 
**Accuracy of CNN model - Persian Digits** 
<p align="center">
<img  align="center" src="https://github.com/saniaki/digit-classifier/blob/master/images/Persian/CNN%20accuracy_Persian.jpg" width="450"/>
 
**Accuracy of MLP model- Persian Digits** 
<p align="center">
<img  align="center" src="https://github.com/saniaki/digit-classifier/blob/master/images/Persian/MLP%20accuracy_Persian.jpg" width="450"/>
<br>

**Accuracy of CNN model - English Digits** 
<p align="center">
<img  align="center" src="https://github.com/saniaki/digit-classifier/blob/master/images/English/CNN_accuracy.jpg" width="450"/>
 
**Accuracy of MLP model- English Digits** 
<p align="center">
<img  align="center" src="https://github.com/saniaki/digit-classifier/blob/master/images/English/MLP_accuracy.jpg" width="450"/>
<br>
 
Some sample predictions of models for Persian or Enlish digits: <br>
1- **Both models predict Persian number 2 correctly:** <br>
<p align="center">
<img  align="center" src="https://github.com/saniaki/digit-classifier/blob/master/images/Persian/Predictions_01_Persian.jpg" width="700"/>
<br> 

2- **Only CNN model predicts English number 5 correctly:**  <br>
<p align="center">
<img  align="center" src="https://github.com/saniaki/digit-classifier/blob/master/images/English/Sample_output_2.jpg" width="700"/>
 <br> 
 
 3- **Only CNN model predicts English number 4 correctly:** <br>
<p align="center">
<img  align="center" src="https://github.com/saniaki/digit-classifier/blob/master/images/English/Sample_output_3.jpg" width="700"/>
<br>
  
4- **Both models predict Persian number 0 correctly:** <br>
<p align="center">
<img  align="center" src="https://github.com/saniaki/digit-classifier/blob/master/images/Persian/Predictions_02_Persian.jpg" width="700"/>
<br>
  
5- **Both models predict Persian number 5 correctly:** <br>
<p align="center">
<img  align="center" src="https://github.com/saniaki/digit-classifier/blob/master/images/Persian/Predictions_03_Persian.jpg" width="700"/>
<br>

**Acknowledgement** <br>
This model is developed with support of <br>
<br>
<img  align="center" src="https://github.com/saniaki/digit-classifier/blob/master/images/Logo.jpg" width="200"/> 


