# GPU-setup

This repo demonstrates how to setup GPU environment in your local machine

**Note: Make sure that your laptop is NVIDIA GPU compatable**

## Step1 : Installing the NVIDIA Driver in your machine 

a. Go to device manager and check the NVIDIA version <br>
![image](https://github.com/Tejanikhil/GPU-setup/assets/102232692/69748bb8-9f75-4110-9f84-fbcd6823479c)<br>
b. Go to the official page of NVIDIA for driver installation https://www.nvidia.com/download/index.aspx <br>
c. Select the appropriate hardware based on the nvidia version <br>
![image](https://github.com/Tejanikhil/GPU-setup/assets/102232692/c2324fae-0752-48d2-8ec2-497567e79666)<br>

## Step2 : Installing CUDA Toolkit

>> Go to https://developer.nvidia.com/cuda-downloads <br>
>> Select the appropriate options <br>
![image](https://github.com/Tejanikhil/GPU-setup/assets/102232692/f9ea1f13-c670-406f-9f1a-18657cdb0854)<br>
>> Click the .exe installation file and follow the instructions<br>
>> Setup the environment variables by creating the user variable called CUDA_HOME which consists of cuda directory<br>
![image](https://github.com/Tejanikhil/GPU-setup/assets/102232692/610a4db3-faa3-4b2a-8ac3-267e22b08755)

## Step3 : Installing cudann

>> Go to the official page of CUDANN for driver installation https://developer.nvidia.com/cudnn <br>
>> Select the appropriate versions of cudann based on NVIDIA version <br>
![image](https://github.com/Tejanikhil/GPU-setup/assets/102232692/5c3b6523-6fc5-4101-8427-1e4b0fc0eb4f) <br>
>> Once you installed cudann, it contains files as follows <br>
![image](https://github.com/Tejanikhil/GPU-setup/assets/102232692/8ccb7588-90dd-49ed-869f-bcece2a5fb30) <br>
Copy the 4 files and paste them in CUDA_HOME directory <br>
![image](https://github.com/Tejanikhil/GPU-setup/assets/102232692/5807dc4f-8ed0-4db1-b1a3-3411d795003e) <br>
**Note** : It asks for replacing the files, click on ok. <br>

## Step4 : Install anaconda and environment setup

>> Install anaconda from https://docs.anaconda.com/free/anaconda/install/windows/# <br>
>> Setup the environment variables as shown <br>
![image](https://github.com/Tejanikhil/GPU-setup/assets/102232692/0ab52f47-9dcf-4f6c-b28a-f35861eedc4c) <br>
>> Open anaconda prompt and create a new environment using `conda create gpu_env` <br>
>> Activate the environment using `conda activate gpu_env` <br>
>> Go to the pytorch page and select the appropriate versions for installations https://pytorch.org/get-started/locally/ <br>
![image](https://github.com/Tejanikhil/GPU-setup/assets/102232692/dbda5889-7e1a-4c3c-bda7-57086b6da2a8)<br>
>> install the pytorch packages using the command `conda install $LIBRARIES$`<br>

## Step5 : Ensuring that gpu environment is setup 

>> Open anaconda and select the environment that is created before<br>
>> You can see that the cuda compatable pytorch libraries are installed<br>
![image](https://github.com/Tejanikhil/GPU-setup/assets/102232692/35d744b7-78b2-4a1d-8ec2-174031542ffc)<br>
>> Open a python terminal in the environment and type the commands <br>
`import torch` <br>
`torch.cuda.is_available()` <br>
>> It returns the output as true which means that gpu is setup <br>
