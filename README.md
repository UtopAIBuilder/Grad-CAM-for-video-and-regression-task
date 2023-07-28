# Grad-CAM-for-video-and-regression-task
Generating explanations for the decision taken by deep models
has recently gained significant attention by the research
community. One of the work in this direction is Grad-CAM
which offers visual explanations for the decisions taken by
the large class of CNN based models. While Grad-CAM has
given landmark results for image based tasks, it has not been
explored much for video dataset. In this project, we have explored the use of Grad-CAM for video based classification
task. We have explored 3 different models, first model uses
3D convolution over time and space, second uses LSTM over
2D CNN model without attention and the third model uses attention over the second model. In another trajectory we have
tried to explore Grad-CAM for image based regression tasks.
Given a set of images captured from the camera of a moving vehicle, we need to predict the ego-motion. In this task,
we take gradient of the negative of the regression loss with
respect to the activation maps of the last layer.
For further details see the report

## Instructions to run the code for LSTM using Attention grad cam:
Sample dataset is available at: https://serre-lab.clps.brown.edu/resource/hmdb-a-large-human-motion-database/#Downloads
click on the highlighted part:
![image](https://github.com/UtopAIBuilder/Grad-CAM-for-video-and-regression-task/assets/18072434/34988e6c-08a5-47ad-bb7e-9b213dbcf2ab)

- Dataset of video should be organized in this structure: ./data/hmdb51_org/swing_baseball/xyx.avi (swing_baseball contains a set of videos having the label swing_baseball)
- First run DataPrepLSTMConv.ipynb. This will sample 16 frames from each video and will create directory in this way: ./data/hmdb51_jpg/swing_baseball/xyx/*.jpg.
- Once this is done, run LSTMConvMainWithAttention.ipynb to train and save a model checkpoint to be later used for GradCam inference.
- After this run GradCamWithAttention.ipynb to get the final output
