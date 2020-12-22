# Install Tensor Flow 2.4 on Windows 10

## Download and Install Anaconda

> ```shell
> # update
> conda update conda
> # conda update anaconda=VersionNumber
> 
> # Create ur own virtual environment
> conda create --name tf24
> 
> # activate the environ
> conda activate tf24
> ```

## Install Tensorflow

> ```shell
> # update pip
> # pip install --upgrade pip
> python -m pip uninstall pip
> python -m ensurepip
> python -m pip install -U pip
> 
> # install tensorflow
> pip install tensorflow==2.4.0
> ```

## Visual Studio (Skipped, come with Driver)

> - download VS 2017 from here <a>https://www.techspot.com/downloads/6278-visual-studio.html</a>
> - **Cuda 10.0 doesn't support VS 2019!!!**

## Nvidia Driver

> - Just use the latest one from the [website](https://www.nvidia.com/Download/index.aspx?lang=en-us#)

## Cuda Tool Kit

> - TensorFlow supports [CUDA® 11](https://developer.nvidia.com/cuda-toolkit-archive) (TensorFlow >= 2.4.0)
>   - Install from the `.exe`

## Cudnn

> - Download the library for [cuDNN](https://developer.nvidia.com/rdp/cudnn-download) SDK 8.0.4
>   - **find the corresponding version with your Cuda package**

## Set the Environment Variables

> - search for `Environment Variables`, `edit` -> `path` in the `system vaiables` 
>
> - the pathes of `CUDA` are taken care by `CUDA`'s installation (skipped)
>
>   <img src="Install Tensor Flow 2_4 on Windows 10.assets/image-20201222142048362.png" alt="image-20201222142048362" style="zoom:50%;" />
>
> - add the pathes of `cuDNN ` (do it)
>
>   <img src="Install Tensor Flow 2_4 on Windows 10.assets/image-20201222141844362.png" alt="image-20201222141844362" style="zoom:50%;" />
>
>   
>   
>

## Test It

> - open a cmd console in `anaconda navigator
>
>    ```python
>    from __future__ import absolute_import, division, print_function, unicode_literals
>    import tensorflow as tf
>    print("GPU Available: ", tf.test.is_gpu_available())
>    ```
>
> -  All set, if return `True`

## Necessary Libraries

> ```shell
> pip install pandas
> pip install scipy
> pip install scikit-learn
> pip install numba
> 
> conda uninstall pydot
> conda uninstall pydotplus
> conda uninstall graphviz
> conda install pydot
> conda install pydotplus
> ```
>
> 

