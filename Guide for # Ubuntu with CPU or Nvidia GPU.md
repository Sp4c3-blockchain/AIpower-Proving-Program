# AIpower-Proving-Program
The current program supports some AI device hardware, GPU and CUP, and provides AI computing power for sp4c3 networks. 
The versions and support programs corresponding to more devices will be updated from time to time.

# Ubuntu with CPU or Nvidia GPU
## Step 1. Configure AI Enviromnent
### step 1.1 Install CUDA and CUDNN (If you have GPU)
* Please install CUDA 10.2 or 11.3 according to your GPU
ref. : https://developer.nvidia.com/cuda-toolkit
* Install CUDNN according to your CUDA version
ref. : https://developer.nvidia.com/cudnn
https://docs.nvidia.com/deeplearning/cudnn/install-guide/index.html
* Please Choose the right version according to your GPU and OS.

### Step 1.2 Install AI base tools
* install python 3.8.x
$ sudo apt install python3.8
* install paddlepaddle : https://github.com/paddlepaddle/paddle
Please install GPU version if you have GPU
AND select the right CUDA version please.
* install tensorflow : https://www.tensorflow.org/install
Please install GPU version if you have GPU
AND select the right CUDA version please.
* install pytorch : https://pytorch.org/get-started/locally/
Please install GPU version if you have GPU
AND select the right CUDA version please.
* PLEASE choose the corresponding version according to your GPU and CUDA 
* Choose CPU version if you do not have a GPU

## Step.2 Download miner software and run (Using g)

### Step 2.1 download 
 git clone https://github.com/Sp4c3-blockchain/AIpower-Proving-Program.git
 cd sp4ubuntu
### Step 2.2 Install requirements
$ pip3 install -r requirements.txt 
Step 2.3 Run
$ python3 run.py
