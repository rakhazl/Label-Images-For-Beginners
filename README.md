# In Here Tutorial Label Images For Beginners with LabelImg
$~$
> [!WARNING]
> I'm using LabelImg 1.8.6 here
$~$

## Step 1 : Install Virtual Environment
### [Check Repositories For Install Vitual Environment Camera-Vision-YOLOv8-Project](https://github.com/rakhazl/Camera-Vision-YOLOv8-Project.git) :ok_person:

## Step 2 : Activate Virtual Environment
$~$
### For activate
    name_folder\Scripts\activate
$~$
## Step 3 : Install LabelImg
$~$
### 1. Open your virtual environment, and typing <code>pip install labelImg</code>
    pip install labelImg
### Please wait until it finishes 
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor.png)
$~$
### 2. Typing <code>labelImg</code> in CMD
    labelImg
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%202.png)
### 3. <code>Open Dir</code>, Select Folder
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%203.png)
### The example folder selected is <code>ex Images</code> as the source image folder
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%204.png)
$~$
### 4. Choose YOLO with click this icon and Anotate
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%205.png)
### Click Right your mouse, <code>Create RectBox</code>. *The example classification here is <code>helmet</code>*
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%208.png)
$~$
### 5. Save, Select Folder for result anotate
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%209.png)
### Click <code>view</code>, and then :ballot_box_with_check: <code>Auto Save Mode</code>
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%206.png)
$~$ 
### 6. Open CMD again, Typing <code>labelImg [IMAGE_PATH] [PRE-DEFINED CLASS FILE]</code>
    labelImg [IMAGE_PATH] [PRE-DEFINED CLASS FILE]
### example, 
    labelImg "C:\For Labeling\ex Images" "C:\For Labeling\ex Anotate\classes.txt" "C:\For Labeling\ex Anotate"
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%2011.png)
$~$
### 7. Open Folder Result Anotate, click file <code>classes.txt</code>
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%2010.png)
### Open File <code>classes.txt</code>, edit for your classification. *The example classification here is <code>helmet</code>*
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%2012.png)
$~$
### 8. Continue with annotating
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%2013.png)
### Check your Folder Result Anotate
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%2014.png)
### If everything is correct and as expected, then let's proceed :magic_wand:
$~$
## Step 4 : Manage Data
$~$
### 1. Create new folder for data collect. *The example folder here is <code>For Train</code>*
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%2015.png)
### Inside the <code>For Train</code> folder, create <code>train</code> and <code>valid</code> folders
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%2016.png)
### Inside each <code>train</code> and <code>valid</code> folder, create <code>image</code> and <code>labels</code> folders
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%2017%20.png)![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%2017-2.png)
$~$
### 2. In this example, there are 10 images. From the <code>ex Anotate</code> folder, move the files to <code>train\labels</code> and <code>valid\labels</code> folders
$~$
### For YOLO model or other machine learning models, you typically use the following data split:
#### Training Data:
- The training data usually comprises the largest portion of your dataset since the model will train itself with this data. Typically, you allocate around <code>60-80%</code> of your entire dataset for training data.
#### Validation Data:
- Validation data is used to evaluate the model's performance during training, allowing you to monitor overfitting and optimize model parameters. Typically, you allocate around <code>10-20%</code> of your entire dataset for validation data.
#### Testing Data (Opsional):
- Testing data is used to assess the performance of the trained and validated model on data it has never seen before. Reserve around <code>10-20%</code> of your entire dataset for testing data.
$~$
### In this example, using an <code>*80% training data*</code> and <code>*20% validation data*</code> split, there are <code>*8 images for training data*</code> and <code>*2 images for validation data*</code>
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%2018.png) ![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor18-2.png) ![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%2018-3.png) ![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor18-4.png)
### 3. Create file <code>.yaml</code>. The example here is <code>data.yaml</code>
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%2019.png)
### Edit <code>data.yaml</code>,
    train: path_folder_train_image
    val: path_folder_valid_image


    nc: number of classifications
    names: ['name of classifications.']

### example
![](https://github.com/rakhazl/Label-Images-For-Beginners/blob/main/Documentation%20Step/Ducomentation%20Tutor%2020.png)
### Save as <code>data.yaml</code>
$~$
## Step 5 : Train Your Data 
### ![This is for training YOLO](https://docs.ultralytics.com/modes/train/) :rocket:
$~$
### example for training <code>YOLOV8</code>, choose <code>yolov8n.pt</code> or <code>yolov8s.pt</code> or <code>yolov8l.pt</code> or etc
    yolo detect train data=coco128.yaml model=yolov8n.pt epochs=100 imgsz=640
### result training, do you use file <code>best.pt</code>, *you can find file like path this*
    \train\weights\best.pt"
