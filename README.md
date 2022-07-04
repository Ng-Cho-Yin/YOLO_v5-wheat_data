# YOLO_v5 on Kaggle Competition

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

    
          
