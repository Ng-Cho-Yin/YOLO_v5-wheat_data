# YOLO_v5 on Kaggle Competition

Competition: Global Wheat Detection

Link: https://www.kaggle.com/c/global-wheat-detection

GPU: Tesla T4 16GB

tips:  (for yolov5)

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
                 
#key commands:
To train: ! python /content/yolo/yolov5-master/train.py --img 1024 --batch 8 --epochs 20 --data /content/yolo/yolov5-master/wheat.yaml --cfg /content/yolo/yolov5-master/models/yolov5s.yaml --name wm_20e

To detect: ! python /content/yolo/yolov5-master/detect.py --source /content/wheat_data/input/test --weights /content/yolo/yolov5-master/runs/train/wm2/weights/best.pt

    
          
