# YOLO_v5 on Kaggle Competition

![348a992bb](https://user-images.githubusercontent.com/56172862/177117517-7152591b-763f-433d-907d-d98a13bd275e.jpeg)
(20 epochs/models/yolov5s.yaml)

![348a992bb](https://user-images.githubusercontent.com/56172862/177136681-8b0aeace-7dee-4a07-bc77-98c986c8ec75.jpeg)
(20 epochs/models/yolov5s.yaml)with pretained model

Competition: Global Wheat Detection

Kaggle link: https://www.kaggle.com/c/global-wheat-detection

Data: https://www.kaggle.com/competitions/global-wheat-detection/data

GPU: Tesla T4 16GB

    --yolov5-master
      |
      --wheat_data
            |
            --labels
                  |
                  --train
                  --validation
            --images
                  |
                  --train
                  --validation
                  
      wheat.yaml:
            train: /content/yolo/yolov5-master/wheat_data/images/train
            
            val: /content/yolo/yolov5-master/wheat_data/images/validation
            
            nc: 1
            
            names: ['wheat']
                 
#key commands:

To train: ! python /content/yolo/yolov5-master/train.py --img 1024 --batch 8 --epochs 20 --data /content/yolo/yolov5-master/wheat.yaml --cfg /content/yolo/yolov5-master/models/yolov5s.yaml --name wm_20e

To detect: ! python /content/yolo/yolov5-master/detect.py --source /content/wheat_data/input/test --weights /content/yolo/yolov5-master/runs/train/wm2/weights/best.pt

    
          
