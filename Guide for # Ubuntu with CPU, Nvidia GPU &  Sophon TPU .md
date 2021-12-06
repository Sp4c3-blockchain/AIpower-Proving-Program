# AIpower-Proving-Program
AIPP(AIpower Proving Program) 1.01 supports some hardware(AI hardware,GPU and CUP) provides AI computing power for sp4c3 networks. 
This versions1 and support programs corresponding to more devices will be updated from time to time.

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

## Step.2 Download miner software and run

### Step 2.1 download 
$ cd [your created folder]
$ wget https://sp4.s3.ap-east-1.amazonaws.com/install/sp4ubuntu.tar-1.0.1.gz
$ tar -zxvf sp4ubuntu.tar.gz
$ cd sp4ubuntu

 
### Step 2.2 Install requirements
$ pip3 install -r requirements.txt 
Step 2.3 Run
$ python3 run.py



# Ubuntu with AI Machine Sophon TPU (E.g. Sophon TPU)
## Step 1. Configure AI Enviromnent
### step.1 Install docker 
How to install? Google it or follow the instructions:
 https://docs.docker.com/engine/install/ubuntu/

### Step.2 Download and Load Sophon docker
#### Step 2.1 Download Sophon Docker
Run command to download and unzip:
$ wget https://sophon-file.sophon.cn/sophon-prod-s3/sdk/bmnnsdk_ubuntu_docker.tar.gz
$ tar -zxvf bmnnsdk_ubuntu_docker.tar.gz
#### Step 2.2 Load docker
$ sudo docker load -i bmnnsdk2-bm1684-ubuntu.docker
(check if necessary $ sudo docker image ls)

### Step.3 Configure AI enviroment 
#### Step 3.1 Downlad Sophon SDK
$ wget https://sophon-file.sophon.cn/sophon-prod-s3/drive/21/11/12/10/bmnnsdk2-bm1684_v2.6.0.tar.gz
$ tar -zxvf bmnnsdk2-bm1684_v2.6.0.tar.gz

#### Step 3.2 Install TPU Driver
$ cd bmnnsdk2-bm1684_v2.6.0/scripts
$ sudo apt-get install make
$ sudo apt-get install make
$ sudo ./install_driver_pcie.sh

#### Step 3.3 Run in docker and configure enviroment
$ cd bmnnsdk2-bm1684_v2.6.0
$ sudo ./docker_run_bmnnsdk.sh

*** INSIDE Docker Now! ***
#### # python3 -m pip install paddlepaddle -i https://mirror.baidu.com/pypi/simple
#### # cd /workspace/scripts/
#### # ./install_lib.sh nntc
#### # source envsetup_pcie.sh
#### # cd ..
#### # cd lib/ffmpeg/x86 && export LD_LIBRARY_PATH=`pwd`:$LD_LIBRARY_PATH 
#### # cd ../../../
#### # cd lib/decode/x86 && export LD_LIBRARY_PATH=`pwd`:$LD_LIBRARY_PATH
#### # cd ../../../
#### # cd lib/sail/python3/pcie/py35 (* depends on your python version *)
#### # pip3 install sophon-2.6.0-py3-none-any.whl

### x # cd ../examples/SSD_object/cpp_cv_bmcv_bmrt/


## Step 2. Download miner software and run [Run in Docker]

### Step 2.1 download 
# cd [your created folder]
# wget https://sp4.s3.ap-east-1.amazonaws.com/install/sp4ubuntu.tar-1.0.1.gz
# tar -zxvf sp4ubuntu.tar.gz
# cd sp4ubuntu

 
### Step 2.2 Install requirements
# pip3 install -r requirements.txt 
### Step 2.3 Run
# python3 run.py
