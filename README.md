# GenHash
This flask-based web application uses CNN and LSTM as the base models to generate the Hashtags for the uploaded image.
This web application uses a pre-trained model on the COCO dataset. The COCO (Common Objects in Context) dataset is a large-scale image recognition dataset for object detection, segmentation, and captioning tasks. It contains over 330,000 images, each annotated with 80 object categories.
# Stepwise Implementation of the Model
1. First step is to load the dataset. This is done in the Data loader.py file. 
2. Next is to generate the vocabulary to train the dataset. Code for this can be found in build vocab.py
3. Two models are defined in the model.py. One is CNN, and the other is LSTM. Both models are used to encode and then decode the images to generate the hashtags for the given image.
4. Train.py is run to combine all three files and train the model. The trained model is then saved in the same directory.
# Flask web application 
Flask is a tool used to make web applications using Python. This flask application has these files:
1. model.py
2. build_vocab.py
3. data_loader.py
4. saved models
5. vocab.pkl
6. app.py
The app.py has four primary functions which define the flow of the application. First is load_image(); it loads the image and resizes it according to the model. The second is the process() function which does all the image preprocessing. It transforms the image and loads the vocabulary wrapper using the save pkl file. Then the model is loaded with the defined weights and layers. The features are encoded using these models, and the hashtags are generated. The predict() function includes all the paths for the files and is called when the upload() function uploads the image.
The encoder and decoder files are big therefore providing the drive link for them here.
encoder: https://drive.google.com/file/d/1-ZT7IeR9hdpJjFClldUWIr-Bpm3o3UYt/view?usp=sharing
decoder: https://drive.google.com/file/d/1ypyJZ8AAZwcSE3nBiPJ3wGuYh-2K24Ni/view?usp=sharing
Link of the Screen recording of the code and the Web application: https://drive.google.com/drive/folders/1oz2IglnHGvDT_zXILTmdakJDgMBVWNpM?usp=sharing
