---
layout: post
title: "DBFace Light Detection"
date: 2019-04-17
excerpt: "DBFace Light Detection"
tags: Tech-writing
comments: true

---
## Project 
Here is the primary reference source: [Reference](https://blog.csdn.net/weixin_45192980/article/details/106485602)
1. Download the project original data from Github and unzip the data to Local. 
2. Download Anaconda that is Anaconda Prompt (Anaconda3), which is the Anaconda Client command line interface (CLI). 
3. Download Pycharm Community Edition (2020.3.5).
4. Download CUDA (NVIDIA Nsight Compute 2020.2.0). 
   Here are CUDA installation conditions: 
![]   (https://github.com/Kimwangqing/pictures/blob/master/CUDA%20installation%20conditions.png?raw=true)
   Here is the download source: [Download](https://developer.nvidia.com/zh-cn/cuda-downloads)    
5. Create a virtual environment with Anaconda,  
	1. In which python version is 3.6 or above.
   The name of the virtual envirnment is **py36**. 
   `conda create -n env_name python=xxx`, for example, `conda create -n py36 python=3.6`
    2. Activate the virtual environment. 
         `activate env_name`.
6. Download pytorch 1.5  in the virtual environment with conda command. Here is a reference sour: [Reference](https://blog.csdn.net/u014723479/article/details/103001861)
   1. Select installation conditions on Pytorch website. 
      PyTorch Build: Select **Stable()**
      Your OS: Select **Windows**
      Package: Select **Conda**
      Language: Select ** Python 3.xx** corresponding to the version python you are using in the virtual environment. 
      CUDA: Select the version you installed. 
   2. Then get the command, and copy the command into Anaconda to install pytorch. 
7. Download opencv-python4.2.0  in the virtual environment with conda command. 
8. Open the project with Pycharm, and then to set the interpreter for python. 
   1. Select **Add** to add a python interpreter. 
   2. Select python.exe in the py36 environment created. 
9. Find a picture that format is jpg, and put it into datas file. 
10. Add the jpg into image_demo(). 
11. Right click `main.py` to run `main`.
12. Check the result in `detect_result`. 

## 测试与结果展示
![successful vertification](https://github.com/Kimwangqing/pictures/blob/master/CUDA%20successful%20%20vertification.png?raw=true)

