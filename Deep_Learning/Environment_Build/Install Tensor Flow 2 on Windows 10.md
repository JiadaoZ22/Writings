# Install Tensor Flow 2.0.0 on Windows 10

## Download and Install Anaconda

> - Create ur own virtual environment
> - ```pip install tensorflow-gpu``` 

## Visual Studio

> - download VS 2017 from here <a>https://www.techspot.com/downloads/6278-visual-studio.html</a>
> - **Cuda 10.0 doesn't support VS 2019!!!**

## Nvidia Driver

> - Just use the latest one from the website: <a>https://www.nvidia.com/Download/index.aspx?lang=en-us#</a>

## Cuda Tool Kit

> - Ok, use CUDA TK **10.0** instead of 10.1
> - Download it from here: <a>https://developer.nvidia.com/cuda-toolkit-archive</a>
> - Install from the `.exe`

## Cudnn

> - Download the library for CUDA TK 10.0: <a>https://developer.nvidia.com/rdp/cudnn-download</a>

## Set the Environment Variables

> - search for `Environment Variables`, `edit` -> `path` in the `system vaiables` 
>
>   ![https://user-images.githubusercontent.com/4515120/52910032-06803880-32d5-11e9-87f2-a4a7627d0c30.png](https://user-images.githubusercontent.com/4515120/52910032-06803880-32d5-11e9-87f2-a4a7627d0c30.png)
>
>   ![image-20191124164223550](Install%20Tensor%20Flow%202%20on%20Windows%2010.assets/image-20191124164223550.png)
>

## Test It

> - open a cmd console in `anaconda navigator`
>
> - ```python
>  from __future__ import absolute_import, division, print_function, unicode_literals
>  import tensorflow as tf
>  print("GPU Available: ", tf.test.is_gpu_available())
>  ```
>  ```
> -  All set, if return `True`
>  ```

