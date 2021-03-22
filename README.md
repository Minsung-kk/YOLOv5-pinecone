# yolov5-noise
YOLOv5 Object Detection in Noisy Images
* Brief instruction using Google Colaborator
  * original video link: https://www.youtube.com/watch?v=T0DO1C8uYP8
  * can use free provided GPU (Runtime - Change runtime type - GPU)
  * make a new folder and name it as dataset and upload dataset
  * change directory to content by typing %cd /content/
  * clone YOLOv5 by !git clone https://github.com/ultralytics/yolov5.git
  * install requirements
    * %cd /content/yolov5/
    * !pip install -r requirements.txt
  * split dataset into train and validation (only if dataset isn't splitted into two)
    * %cd /
    * from glob import glob
    * img_list = glob('/content/dataset/(location of images)/*.jpg')
    * from sklearn.model_selecion import train_test_split
    * train, val = train_test_split(img_list, test_size=0.2, random_state=2000)
  * save locations of train and val
    * with open('/content/dataset/train.txt', 'w') as f:
      * f.write('\n'.join(train) + 'n')
    * with open('/content/dataset/val.txt', 'w') as f:
      * f.write('\n'.join(val) + 'n')
  * change data.yaml to indicate above train and val locations
    *  import yaml
    *  with open('content/dataset/data.yaml', 'r') as f:
       * data = yaml.load(f)   
