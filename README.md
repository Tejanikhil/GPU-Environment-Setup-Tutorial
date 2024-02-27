# GPU Setup

This repository demonstrates how to set up a GPU environment on your local machine.

**Note: Make sure that your laptop is NVIDIA GPU compatible.**

## Step 1: Installing the NVIDIA Driver on Your Machine 

a. Go to Device Manager and check the NVIDIA version.  

![NVIDIA Version](https://github.com/Tejanikhil/GPU-setup/assets/102232692/69748bb8-9f75-4110-9f84-fbcd6823479c)

b. Go to the official page of NVIDIA for driver installation [here](https://www.nvidia.com/download/index.aspx).

c. Select the appropriate hardware based on the NVIDIA version.  

![NVIDIA Driver Installation](https://github.com/Tejanikhil/GPU-setup/assets/102232692/c2324fae-0752-48d2-8ec2-497567e79666)

## Step 2: Installing CUDA Toolkit

- Go to [CUDA Downloads](https://developer.nvidia.com/cuda-downloads).
- Select the appropriate options.
  
![CUDA Toolkit](https://github.com/Tejanikhil/GPU-setup/assets/102232692/f9ea1f13-c670-406f-9f1a-18657cdb0854)
- Click the .exe installation file and follow the instructions.
- Set up the environment variables by creating the user variable called CUDA_HOME, which consists of the CUDA directory.
   
![CUDA Environment Variables](https://github.com/Tejanikhil/GPU-setup/assets/102232692/610a4db3-faa3-4b2a-8ac3-267e22b08755)

## Step 3: Installing cuDNN

- Go to the official page of cuDNN for driver installation [here](https://developer.nvidia.com/cudnn).
- Select the appropriate versions of cuDNN based on the NVIDIA version.
  
![cuDNN Installation](https://github.com/Tejanikhil/GPU-setup/assets/102232692/5c3b6523-6fc5-4101-8427-1e4b0fc0eb4f)
- Once installed, copy the files and paste them into the CUDA_HOME directory.
  
![cuDNN Files](https://github.com/Tejanikhil/GPU-setup/assets/102232692/8ccb7588-90dd-49ed-869f-bcece2a5fb30)

**Note**: It may ask for replacing the files, click "OK".

## Step 4: Install Anaconda and Set Up Environment

- Install Anaconda from [here](https://docs.anaconda.com/free/anaconda/install/windows/#).
- Set up the environment variables as shown.  

![Anaconda Environment Variables](https://github.com/Tejanikhil/GPU-setup/assets/102232692/0ab52f47-9dcf-4f6c-b28a-f35861eedc4c)

- Open Anaconda prompt and create a new environment using `conda create gpu_env`.
- Activate the environment using `conda activate gpu_env`.
- Go to the PyTorch page and select the appropriate versions for installation [here](https://pytorch.org/get-started/locally/).  

![PyTorch Installation](https://github.com/Tejanikhil/GPU-setup/assets/102232692/dbda5889-7e1a-4c3c-bda7-57086b6da2a8)

- Install the PyTorch packages using the command `conda install $LIBRARIES$`.

## Step 5: Ensuring GPU Environment is Set Up

- Open Anaconda and select the environment that was created before.
- You can see that the CUDA-compatible PyTorch libraries are installed.  

![PyTorch Libraries](https://github.com/Tejanikhil/GPU-setup/assets/102232692/35d744b7-78b2-4a1d-8ec2-174031542ffc)

- Open a Python terminal in the environment and type the commands:

```python
import torch
torch.cuda.is_available()
