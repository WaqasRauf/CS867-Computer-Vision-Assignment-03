# CS867-Computer-Vision-Assignment-03
Semantic Segmentation


Semantic image segmentation is the task of classifying each pixel in an image from a predefined set of classes. In the following example, different entities are classified.

<p align="center">
  <img src="sample_images/1_input.jpg" width="350" title="hover text">
  <img src="sample_images/1_output.png" width="350" alt="accessibility text">
</p>


In the above example, the pixels belonging to the bed are classified in the class “bed”, the pixels corresponding to the walls are labeled as “wall”, etc.
In particular, our goal is to take an image of size W x H x 3 and generate a W x H matrix containing the predicted class ID’s corresponding to all the pixels.
Usually in an image with various entities, we want to know which pixel belongs to which entity, For example in an outdoor image, we can segment the sky, ground, trees, people, etc.
Semantic segmentation is different from object detection as it does not predict any bounding boxes around the objects. We do not distinguish between different instances of the same object. For example, there could be multiple cars in the scene and all of them would have the same label.
ASSIGNMENT 03
     CS 867 COMPUTER VISION, FALL 2021 1|Page
In order to perform semantic segmentation, a higher level understanding of the image is required. The algorithm should figure out the objects present and also the pixels which correspond to the object. Semantic segmentation is one of the essential tasks for complete scene understanding.
1.1 Datasets for semantic segmentation
The first step in training our segmentation model is to prepare the dataset. We would need the input RGB images and the corresponding segmentation images. If you want to make your own dataset, a tool like labelme or GIMP can be used to manually generate the ground truth segmentation masks.
Assign each class a unique ID. In the segmentation images, the pixel value should denote the class ID of the corresponding pixel. This is a common format used by most of the datasets




The convolutional neural network (CNN) is a class of deep learning neural networks. CNNs represent a huge breakthrough in image recognition. They’re most commonly used to analyze visual imagery and are frequently working behind the scenes in image classification. They can be found at the core of everything from Facebook’s photo tagging to self-driving cars. They’re working hard behind the scenes in everything from healthcare to security.
Image classification is the process of taking an input (like a picture) and outputting a class (like “cat”) or a probability that the input is a particular class (“there’s a 90 percent probability that this input is a cat”).
A CNN has
• Convolutional layers
• ReLU layers
• Pooling layers
• Batch Normalization layer
• A Fully connected layer (optional)
A CNN convolves (not convolutes...) learned features with input data and uses 2D convolutional layers. This means that this type of network is ideal for processing 2D images. Compared to other image classification algorithms, CNNs use very little preprocessing. This means that they can learn the filters that have to be hand-made in other algorithms. CNNs can be used in tons of applications from image and video recognition, image classification, and recommender systems to natural language processing and medical image analysis. CNNs have an input layer, and output layer, and hidden layers. The hidden layers usually consist of convolutional layers, ReLU layers, pooling layers, and batch normalization layers.
A CNN works by extracting features from images. This eliminates the need for manual feature extraction. The features are not trained! They’re learned while the network trains on a set of images. This makes deep learning models extremely accurate for computer vision tasks. CNNs learn feature detection through tens or even hundreds of hidden layers.

## Task : Implement an image classification pipeline using CNN to classify the given two datasets into different classes.

Human Detection is a branch of Object Detection. Object Detection is the task of identifying the presence of predefined types of objects in an image. This task involves both identification of the presence of the objects and identification of the rectangular boundary surrounding each object (i.e. Object Localisation). An object detection system which can detect the class “Human” can work as a Human Detection System.
Human detection is an essential and significant task in any intelligent video surveillance system, as it provides the fundamental information for semantic understanding of the video footages. It has an obvious extension to automotive applications due to the potential for improving safety systems. Many car manufacturers (e.g. Volvo, Ford, GM, Nissan) offer this as an ADAS option in 2017. Some of the applications be given as;
o Self-driving cars: Identifying pedestrians on a road scene
o Security: Restrict access for certain people to certain places o Retail: Analysing visitors behaviour within a supermarket
o Fashion: Identify specific brands and persons who wear them

### Dataset-1 : Chest X-Ray Images (Pneumonia) Classification

According to the World Health Organization (WHO), pneumonia kills about 2 million children under 5 years old every year and is consistently estimated as the single leading cause of childhood mortality (Rudan et al., 2008), killing more children than HIV/AIDS, malaria, and measles combined (Adegbola, 2012). The WHO reports that nearly all cases (95%) of new- onset childhood clinical pneumonia occur in developing countries, particularly in Southeast Asia and Africa. Bacterial and viral pathogens are the two leading causes of pneumonia (Mcluckie, 2009) but require very different forms of management. Bacterial pneumonia requires urgent referral for immediate antibiotic treatment, while viral pneumonia is treated with supportive care. Therefore, accurate and timely diagnosis is imperative. One key element of diagnosis is radiographic data since chest X-rays are routinely obtained as standard of care and can help differentiate between different types of pneumonia.

## Dataset-2 : 315 Bird Species - Classification

Data set of 315 bird species. 45980 training images, 1575 test images(5 images per species) and 1575 validation images(5 images per species). All images are 224 X 224 X 3 color images in jpg format. Data set includes a train set, test set and validation set. Each set contains 315 sub directories, one for each bird species. The data structure is convenient if you use the Keras ImageDataGenerator.flowfromdirectory to create the train, test and valid data generators. The data set also include a file Bird Species.csv. This cvs file contains three columns. The filepaths column contains the file path to an image file. The labels column contains the class name associated with the image file. The Bird Species.csv file if read in using df= pandas.birdscsv(Bird Species.csv) will create a pandas dataframe which then can be split into train the data into train, test and valid data sets.df, testdf and valid df dataframes to create your own partitioning of All files were also numbered sequential starting from one for each species. So test images are named 1.jpg to 5.jpg. Similarly for validation images. Training images are also numbered
sequentially with "zeros" padding. For example 001.jpg, 002.jpg ....010.jpg, 011.jpg.....099.jpg, 100jpg, 102.jpg etc. The zero's padding preserves the file order when used with python file functions and Keras flow from directory.
