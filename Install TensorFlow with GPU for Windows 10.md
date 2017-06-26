# Install tensorflow with gpu in windows 10

## Requirements

- Python 3.5
- Nvidia CUDA GPU. You can check [here](https://developer.nvidia.com/cuda-gpus) if your GPU is CUDA compatible.

## Setting up your Nvidia GPU

You need to install Cuda Toolkit 8.0 and cuDNN v5.1 as the GPU version works best with these.



### Download and install CUDA Toolkit

Toolkit version 8.0 or above: https://developer.nvidia.com/cuda-downloads

![](https://ooo.0o0.ooo/2017/06/26/59508e1f45633.png)

Example installation directory: `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0`

### Download and install cuDNN

cuDNN version 5.1 library for Windows 10: https://developer.nvidia.com/cudnn

![](https://ooo.0o0.ooo/2017/06/26/59508de8afd9a.png)

You would need to signup at Nvidia in order to download these files. Now extract the cuDNN files into your Toolkit directory.

![](https://ooo.0o0.ooo/2017/06/24/594dd1ea6ab0a.jpg)
 
### Environmental variables
Ensure after installing CUDA toolkit, the CUDA_HOME is set in the environmental variables. If not then you need to add it manually..

![](https://ooo.0o0.ooo/2017/06/24/594dcb90118c2.png)

And path variables as..

![](https://ooo.0o0.ooo/2017/06/24/594dcbf8eb6ac.png)

## Install Anaconda

We will install Anaconda as it helps us to easily manage separate environments for specific distributions of Python, without disturbing the version of python installed on your system.

### Download and install 

[Anaconda](https://www.continuum.io/downloads)

### Create conda environment

Create new environment, with the name tensorflow-gpu and python version 3.5.2
`conda create -n tensorflow-gpu python=3.5.2`

![](https://ooo.0o0.ooo/2017/06/24/594dd073b87d8.png)

Activate the environment activate tensorflow-gpu

![](https://ooo.0o0.ooo/2017/06/24/594dd0df09aaa.png)

### Install tensorFlow

`pip install tensorflow-gpu`

![](https://ooo.0o0.ooo/2017/06/24/594dd10d769a5.png)
 

Done. You have successfully installed TensorFlow with GPU on your Windows machine.
Now lets test if it is using GPU…

### Activate environment we created

`activate tensorflow-gpu`

### Test GPU

Enter into python shell

```bash
python
```



![](https://ooo.0o0.ooo/2017/06/24/594dd238eb3e4.png)


That’s all. Time to play with it.

## ISSUE

I get error such as `ImportError: No module named '_pywrap_tensorflow_internal'`. and I refer some website, finnally I got solutions.

Try to rename `cudnn64_6.dll` to `cudnn64_5.dll` in `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\bin`.
