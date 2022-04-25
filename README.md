# Yolov5-musicscore-remote
Considering the use of local computers for deep learning training will waste a particularly long time, this repository is the Yolov5-musicscore-local repository written by myself to use a remote server for training, and establish corresponding exercises with the local. This method refers only to my own experience.



**Using the step：**


           
**1.Set up the data**

        You can use the my Yolov5-musicscore-local the repository.And download it 

        Please,use the voc_to_yolo file that can set up the data.Reference my repository of Yolov5-musicscore-local's README.md 
   
**3.data**

  	Modify the  classes/ TRAIN_RATIO/ file path
  
    VOCdevkt

       --images
           --train
           --val
       --labels
           --train
           --val
           
**4.data/voc.yaml**

	train path/ val path/ nc/ name

  	train path-->VOCdevkit/images/train/
  
  	val path--> VOCdevkit/images/val/
  
  	nc-->number of classes
  
  	name-->class names
  
**5.models/.yaml**

	Modify the  anchors/nc

**6.train**

  	weights-->initial weights path
  
  	cfg-->model.yaml path
  
  	data-->data.yaml path
  
  	hyp-->hyperparameters path
  
  	epochs
  
  	batch-size
  
  


# When you get to this point, you've done a lot

Then you need to upload your entire project to the remote server and establish a mapping between the remote server and the local server.


**Run the train file on your local server. Start training.**


When the training is complete, the result of the run will appear on the remote server, please download to the local, you will get the result of the remote training



**1.runs/train/exp/labels、train_batch、weights**

**2.detect  weights、source、conf-thres、iou-thres**

        Check the results of the training
