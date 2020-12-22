# Install Tensor Flow 2.4 on Windows 10

## Download and Install Anaconda

> ```shell
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
> - Be awared of `cuda` and `cuDNN`
>
>   ![https://user-images.githubusercontent.com/4515120/52910032-06803880-32d5-11e9-87f2-a4a7627d0c30.png](https://user-images.githubusercontent.com/4515120/52910032-06803880-32d5-11e9-87f2-a4a7627d0c30.png)
>
>   ![image-20191124164223550](Install%20Tensor%20Flow%202%20on%20Windows%2010.assets/image-20191124164223550.png)
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

