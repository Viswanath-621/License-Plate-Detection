# License-Plate-Detection
Automated Vehicle entry system using machine learning and Computer networks.

we used computer vision and machine learning for this project. 
( research )
By using sequential model from tensorflow.keras.models we created a model for training and the model gives best results at epoch 23.


Process:

for read the frames in the video we used cv2.read() function 

and then we pass every frame or image to the funtion called extract_image. This funtion chooses the particular dimensions in the form of rectangle 
where the number plate of the vehicle present in the frame is selected and returns the extracted number plate image.

now this extracted image is passed to another function called segment characters. this function converts the image into grayscale and 
highlights the characters/text in the image with the help of the funtion find_contours and splits the image into each character. it returns 
the particular image containg a single char .

now this each image is passed through show_results function. in this function we predict the character using model.predict function. and return 
that char. 

now these characters are grouped to a string and now this string is compared with the data in the file and displays whether that vehicle can 
pass or not .

