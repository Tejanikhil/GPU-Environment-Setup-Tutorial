# GPU Setup

This repository demonstrates how to set up a GPU environment on your local machine.

**Note: Make sure that your laptop is NVIDIA GPU compatible.**

## Step 1: Installing the NVIDIA Driver on Your Machine 

### a. Check NVIDIA Version
Go to Device Manager and check the NVIDIA version.  

![NVIDIA Version](https://github.com/Tejanikhil/GPU-setup/assets/102232692/69748bb8-9f75-4110-9f84-fbcd6823479c)

### b. Download NVIDIA Driver
Go to the official [NVIDIA driver download page](https://www.nvidia.com/download/index.aspx) and select the appropriate driver based on your NVIDIA version.  

![NVIDIA Driver Installation](https://github.com/Tejanikhil/GPU-setup/assets/102232692/c2324fae-0752-48d2-8ec2-497567e79666)

## Step 2: Installing CUDA Toolkit

### a. Download CUDA Toolkit
Navigate to the [CUDA Toolkit download page](https://developer.nvidia.com/cuda-downloads) and select the appropriate options.  

![CUDA Toolkit](https://github.com/Tejanikhil/GPU-setup/assets/102232692/f9ea1f13-c670-406f-9f1a-18657cdb0854)

### b. Setup Environment Variables
After installation, set up the environment variables by creating the user variable called CUDA_HOME, which consists of the CUDA directory.  

![CUDA Environment Variables](https://github.com/Tejanikhil/GPU-setup/assets/102232692/610a4db3-faa3-4b2a-8ac3-267e22b08755)

## Step 3: Installing cuDNN

### a. Download cuDNN
Visit the official [cuDNN download page](https://developer.nvidia.com/cudnn) and select the appropriate version based on your NVIDIA version.  

![cuDNN Installation](https://github.com/Tejanikhil/GPU-setup/assets/102232692/5c3b6523-6fc5-4101-8427-1e4b0fc0eb4f)

### b. Copy Files to CUDA_HOME
After installation, copy the files and paste them into the CUDA_HOME directory.  

![cuDNN Files](https://github.com/Tejanikhil/GPU-setup/assets/102232692/8ccb7588-90dd-49ed-869f-bcece2a5fb30)

**Note**: It may ask for replacing the files, click "OK".

## Step 4: Install Anaconda and Set Up Environment

### a. Install Anaconda
Download and install Anaconda from [here](https://docs.anaconda.com/free/anaconda/install/windows/#).

### b. Create and Activate Environment
Open Anaconda prompt and create a new environment using `conda create gpu_env`. Then, activate the environment using `conda activate gpu_env`.

### c. Install PyTorch
Visit the [PyTorch installation page](https://pytorch.org/get-started/locally/) to select and install the appropriate versions of PyTorch packages.  

![PyTorch Installation](https://github.com/Tejanikhil/GPU-setup/assets/102232692/dbda5889-7e1a-4c3c-bda7-57086b6da2a8)

## Step 5: Ensuring GPU Environment is Set Up

### a. Verify Installation
Open Anaconda, select the created environment, and verify that the CUDA-compatible PyTorch libraries are installed.  

![PyTorch Libraries](https://github.com/Tejanikhil/GPU-setup/assets/102232692/35d744b7-78b2-4a1d-8ec2-174031542ffc)

### b. Test GPU Availability
Open a Python terminal in the environment and type the following commands:
```python
import torch
torch.cuda.is_available()
