# Exploring Optimisation of YOLOv5 for Real Time Threat Detection in Surveillance Systems

Welcome to the repository for this study. My name is Levent and I will be guiding you through how to use it to minmise confusion. There are a lot of files in this repository as I cloned it from the original YOLOv5 Ultralytics GitHub repository which can be found [here](https://github.com/ultralytics/yolov5).

To be clear, the only folder that has been created/edited by me is the Scripts and Notebooks folder which, as the name suggests, contains the scripts and notebooks that I used in this study. This has two folders, one to run on your local device to sort/filter the datasets and one to run on Google Colab for training.

The reason for using Google Colab was due to my laptop giving me an expected time of one training run being 60 hours due to poor resource allocation of CPUs, whereas on the A100 40GB GPU on Google Colab, it took a fraction of this time, coming to around 2 hours per training run. Google Colab is a paid service (to use those higher end GPUs, like the A100).

**IMPORTANT**: Type ```source yolov5_env/bin/activate``` in the terminal to activate the virtual environment with every package you will need for this task.

In terms of the rest of it, the only files you should concern yourself with for the study is in the Scripts and Notebooks folder.

**NOTE**: You may need to create some directories such as, assuming you are in the yolov5 default directory, a datasets folder which will contain all of your datasets but also additional folders, depends on if the code covers it. You can always run the code then create the directories using ```mkdir``` commands in the terminal, or manually make them if using an IDE. Below is attached an image of what my structure looks like.


![alt text](image.png)

Below is another image attached of what the inside of a folder looks like structurally, some scripts may require you to create these yourself, but this is as far as it will go.

![alt text](image-1.png)


## Dataset Downloads
The only thing that is required of you is to run these commands in the terminal:

```
# Create folders if needed
mkdir -p yolov5/datasets/coco

# Move into the directory
cd yolov5/datasets/coco

# Download the image and annotation zips
wget http://images.cocodataset.org/zips/train2017.zip
wget http://images.cocodataset.org/zips/val2017.zip
wget http://images.cocodataset.org/annotations/annotations_trainval2017.zip
```

Once you have obtained these you just simply run this next command again in the terminal:

```
unzip train2017.zip -d images/
unzip val2017.zip -d images/
unzip annotations_trainval2017.zip -d annotations/
```

This command will simply just unzip them ready for you to work with the data.

## Order of Scripts
Once you have loaded the COCO dataset, in terms of the final result, it was obtained by running the scripts which have been number ordered. The Google Colab script is absolute last thing you run in Colab, then I personally copied over the weights at the end of that script and ran the program to obtain results, which is explained in the Google Colab notebook.

That's all from me and I hope you find what you're looking for.

Levent