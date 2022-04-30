This repo is released for Deep Learning AI702 course at MBZUAI by Aidana Nurakhmetova and Imane Hilal. The project is about blood cells detection and is based on a single stage detector YOLOV5. The BCCD dataset link is https://github.com/Anay21110/BloodCell-Detection-Datatset. The dataset must be placed in a parallel directory to 'datasets' folder.

To setup the environment and libraries, go to demo.ipynb notebook, and run the corresping cells. You can see visual results, test results by running the following cell commands in the notebook file under Detect and Evaluate. 
You can also train yourself.


TRAIN SCRIPT:
python train.py --img 500 --batch 16  --data bccd.yaml --weights yolov5m6.pt --cfg models/yolov5l.yaml --hyp data/hyps/hyp.aug.yaml


TEST SCRIPT (with the best model weight):
python val.py  --img 500 --batch 16 --data bccd.yaml --weights runs/train/exp98/weights/best.pt  --task 'test'


April 30, 2022. All rights reserved.