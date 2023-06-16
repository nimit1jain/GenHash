# GenHash
This is a flask based web application which uses CNN and LSTM as the base moodels to generate the Hashtags for the uploaded image.
This web application uses a pre trained model on the HARRIOSN dataset. HARRISON dataset is a benchmark on hashtag recommendation for real world images in social networks. The HARRISON dataset is a realistic dataset, composed of 57,383 photos from Instagram.

# Stepwise Implemenetation of the Model
1. First step is to load the dataset. This is done in the Data loader.py file. 
2. Next is to generate the vocabulary to train the dataset. Code for this is can be found in build vocab.py
3. Two models are defined in the model.py. One is CNN and other is LSTM both models are used to encode and then decode the images to generate the hashtags for the given image.
4. Train.py is run to combine all the three files and train the model. The trained model is then saved in the same directory.

# Flask web application 
Flask is a tool used to make web applications using python. This flask application has these files:
1. model.py
2. build_vocab.py
3. data_loader.py
4. saved models
5. vocab.pkl
6. app.py

The app.py has four major functions which defines the flow of the application. First is load_image(), it loads the image nad resizes it according to the model. Second is process() function which do all the image preprocessing. It transforms the image and the loads the vocabulary wrapper using the save pkl file. Then the model is loaded with the defined weights and layers. Using these models the features are encoded and the caption is generated. The predict() function includes all the paths for the files and is called when the image is uploaded by the upload() function.
