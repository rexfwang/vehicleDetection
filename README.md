# Intro
In this project, I implemented two vehicle detectors using SVM with HOG (histogram of oriented gradient) and CNN on gti vehicle dataset (https://www.gti.ssr.upm.es/data/Vehicle_database.html) and data from Udacity. I train the SVM model with HOG feature, and CNN using with the raw image. In the target image, I use sliding window to go through different region of interest and use the model to predict if there's a vehicle within the window. After going through the whole image, a heatmap is generated and thresholded to generate the final bounding boxes of vehicles.

For video, besides generating heatmap for each frame, I applied IIR filter to heatmaps to stablize the result. The bouding boxes are generated based on filtered heatmap. Averaging 5 or 10 frames can also stablize the output but perform worse.   

This project uses Scikit-learn for HOG feature and SVM model. It also uses TensorFlow with Keras API for simple CNN model. OpenCV is used for image processing.
