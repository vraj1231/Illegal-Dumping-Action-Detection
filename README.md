# Smart City Community Watch - Camera-Based Community Watch for Traffic and Illegal Dumping
Master's project on detecting illegal dumping in modern cities using Computer Vision methods and helping society for better place.

# YOLOv5 + OCR + DEEPSORT
#### Calculating illegal dumping based on the distance between trash detection and human detection bounding box.

![image](https://github.com/vraj1231/Illegal-Dumping-Action-Detection/blob/Sub_branch/README/ezgif.com-gif-maker%20(2).gif)

## Data preprocess pipepline
1. About 2000 manually labels images and videos using labelImg and Roboflow. Will upload the link to drive and roboflow later.
2. For license plate detection we used pretrain ALPR-weights from https://github.com/pracool/ANPR-with-YoloV5. Thank you pracool for amazing repo and drawing easy steps for installation of weights and graphs. Also, I had own dataset for vehicles. TIP: you can find data on roboflow universe but it might take time.
3. Albumentation
![image](https://user-images.githubusercontent.com/60303995/195780781-28ce6549-92b5-4165-9d8b-8fe6f4d230a3.png)

## Model Overview
1. three models: human detection, car-license-plate detection and trash detection
2. All the model files with best weights are uploaded on the repo under model folder.
![image](https://user-images.githubusercontent.com/60303995/195782431-1c9bb537-f427-4b1c-8d19-767eca7baf01.png)


## results
1. Graph of trash_detection model below:
![image](https://user-images.githubusercontent.com/60303995/195781869-156f7653-4a6a-42e0-9e61-b1087f2e56eb.png)
2. Results on unseen data from robloflow universe. the confidence was set at 70%
![image](https://user-images.githubusercontent.com/60303995/195781934-40633098-e670-49f8-a4ac-7bb30ffc9189.png)

## Tracking
1. Deepsort algorithm will be used to track objects and human. Same ID will be assigned to both human and trash based on the distance. As human go far from the ojbect will be marked as illegal dumping.
