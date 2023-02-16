# Traffic-Sign-Classification-LeNet
Traffic sign image Classification using LeNet architecture. 

Classes are defined like:
- 0 - Speed limit (20km/h)
- 1 - Speed limit (30km/h)
- 2 - Speed limit (50km/h)
- 3 - Speed limit (60km/h)
- 4 - Speed limit (70km/h)
- 5 - Speed limit (80km/h)
- 6 - End of speed limit (80km/h)
- 7 - Speed limit (100km/h)
- 8 - Speed limit (120km/h)
- 9 - No passing
- 10 - No passing for vehicles over 3.5 metric tons
- 11 - Right-of-way at the next intersection
- 12 - Priority road
- 13 - Yield
- 14 - Stop
- 15 - No vehicles
- 16 - Vehicles over 3.5 metric tons prohibited
- 17 - No entry
- 18 - General caution
- 19 - Dangerous curve to the left
- 20 - Dangerous curve to the right
- 21 - Double curve
- 22 - Bumpy road
- 23 - Slippery road
- 24 - Road narrows on the right
- 25 - Road work
- 26 - Traffic signals
- 27 - Pedestrians
- 28 - Children crossing
- 29 - Bicycles crossing
- 30 - Beware of ice/snow
- 31 - Wild animals crossing
- 32 - End of all speed and passing limits
- 33 - Turn right ahead
- 34 - Turn left ahead
- 35 - Ahead only
- 36 - Go straight or right
- 37 - Go straight or left
- 38 - Keep right
- 39 - Keep left
- 40 - Roundabout mandatory
- 41 - End of no passing
- 42 - End of no passing by vehicles over 3.5 metric tons

## How to run
1. Datasets are too heavy (can be shared upon request)
2. Clone repo and place dataset in directory
3. Run `main.ipynb` file

## Highlights
- Fast computation (even with CPU)
- Good performance with only 200 epochs (can be enhanced with more iterations)
- Built on Keras + Tensorflow
- Model included in the `./saved_model` directory
- Used Architecture (LeNet Based):
```
Model: "sequential_8"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_15 (Conv2D)           (None, 28, 28, 6)         156       
_________________________________________________________________
batch_normalization_5 (Batch (None, 28, 28, 6)         24        
_________________________________________________________________
average_pooling2d_15 (Averag (None, 14, 14, 6)         0         
_________________________________________________________________
dropout_1 (Dropout)          (None, 14, 14, 6)         0         
_________________________________________________________________
conv2d_16 (Conv2D)           (None, 10, 10, 16)        2416      
_________________________________________________________________
batch_normalization_6 (Batch (None, 10, 10, 16)        64        
_________________________________________________________________
average_pooling2d_16 (Averag (None, 5, 5, 16)          0         
_________________________________________________________________
dropout_2 (Dropout)          (None, 5, 5, 16)          0         
_________________________________________________________________
flatten_8 (Flatten)          (None, 400)               0         
_________________________________________________________________
dense_22 (Dense)             (None, 120)               48120     
_________________________________________________________________
batch_normalization_7 (Batch (None, 120)               480       
_________________________________________________________________
dropout_3 (Dropout)          (None, 120)               0         
_________________________________________________________________
dense_23 (Dense)             (None, 84)                10164     
_________________________________________________________________
batch_normalization_8 (Batch (None, 84)                336       
_________________________________________________________________
dense_24 (Dense)             (None, 43)                3655      
=================================================================
Total params: 65,415
Trainable params: 64,963
Non-trainable params: 452
```
## Demo Images

### Training vs Validation (Loss & Accuracy)
![image](https://user-images.githubusercontent.com/87340855/219429581-4252dabf-e4b2-4694-a44d-04ce5040ff66.png)

### Random sample evaluation
![image](https://user-images.githubusercontent.com/87340855/219429640-96d2c9ce-f8c4-4b30-a27b-89667cc49773.png)

### Confusion Matrix
![image](https://user-images.githubusercontent.com/87340855/219429708-084f9820-d68c-4c99-90d2-4f351959dd27.png)


## References
- LeNet: http://yann.lecun.com/exdb/publis/pdf/lecun-01a.pdf
