# Hierarchical Model for Zero -shot Activity Recognition using Wearable Sensors

## Abstract 

> Unlike conventional models, the proposed framework does not need retraining for recognition of an unseen activity, if the activity can be represented by a combination of the predefined basic actions and objects.
>
> The experimental results showed that the proposed model could recognize three types of activities with precision of 77% and recall rate of 82%, which is comparable to a baseline method based on supervised learning.

## Gaze-Guided Object Recognition

![1570804465376](C:\Users\jiada\AppData\Roaming\Typora\typora-user-images\1570804465376.png)

> ### Access visual data by wearable sensors:
>
> - Attach a camera on head/body: 1st person view
> - Eye-tracking glasses: gaze point
>   - Cropping sub image only around the gaze point

> ### Training Set
>
> - When cropping, randomly change the size of cropping area. Obtain $ 60*fps*N_s*N_r $ data in 1 min. ($N_s$ is the different cropping size and $N_r$ is the different degrees of rotation)
> - When no objects in the cropped image, define the 'rejected class', which contains all the possible objects and back-ground scene other than the target objects. By this, the model is robust against the False Positive.

	> ### Model
	>
	> - GoogLeNet `Szegedy et al., 2015`
	>   - **Fine-tuning the last two layers** with above training data. 

## Action Recognition

> ### Training Set
>
> - All data collected by *Myo armband*: quaternion, acceleration, gyro and EMG data are utilized.
>   - Statistical features such as maximum, minimum, mean and standard deviation as well as the features in frequency domain, namely, amplitude spectrum obtained by applying fast Fourier transform (FFT) are used.
> - The “reject class” is defined in the action recognition model as well to deal with the case when no target action is performed.

## Activity Recognition

> ### Strategy
>
> ![1570807790395](C:\Users\jiada\AppData\Roaming\Typora\typora-user-images\1570807790395.png)
>
> - Define activities using name of object, name of action, and  the conjunction words.
>
> ### Model
>
> - a probabilistic framework
>
>   - The activity recognition module receives the array o f probabilities from basis recognition module, each  of which represents the likelihood of each target object or action.
>     $$
>     \begin{align*}
>     P(activity|s; def(activity)) &= p(activity|obj,act,def(activity))	\\
>     		& * p(obj|s)*p(act|s)
>     \end{align*}
>     $$

## Evaluation

> ### Experiment
>
> > #### Data collection procedure
> >
> > 1. Start recording data.
> >
> > 2. A subject performs one activity 3 to 5 times in a row with short interval between each performance.
> >
> > 3. Stop recording data.
> >
> > 4. Restart recording data.
> >
> > 5. The subject performs the 2nd activity 3 to 5 times in a row.
> >
> > 6. Stop recording data.
> >
> > 7. Iterate the same procedure for the last activity.
> >
> > 8. Iterate the same procedure for the other subjects.、
> >
> >    ![1570808830209](C:\Users\jiada\AppData\Roaming\Typora\typora-user-images\1570808830209.png)
> >
> >    ![1570808841214](C:\Users\jiada\AppData\Roaming\Typora\typora-user-images\1570808841214.png)
>
> Result
>
> - Each estimation was regarded as right if the IOU is more than a threshold.
>
>   - Baseline case is the normal supervised learning of SVM.
>
>   ![1570809196007](C:\Users\jiada\AppData\Roaming\Typora\typora-user-images\1570809196007.png)
>
> - ![1570809431447](C:\Users\jiada\AppData\Roaming\Typora\typora-user-images\1570809431447.png)

