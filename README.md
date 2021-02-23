# Grad-CAM-for-video-and-regression-task
Generating explanations for the decision taken by deep models
has recently gained significant attention by the research
community. One of the work in this direction is Grad-CAM
which offers visual explanations for the decisions taken by
the large class of CNN based models. While Grad-CAM has
given landmark results for image based tasks, it has not been
explored much for video dataset. In this project, we have ex-
plored the use of Grad-CAM for video based classification
task. We have explored 3 different models, first model uses
3D convolution over time and space, second uses LSTM over
2D CNN model without attention and the third model uses at-
tention over the second model. In another trajectory we have
tried to explore Grad-CAM for image based regression tasks.
Given a set of images captured from the camera of a mov-
ing vehicle, we need to predict the ego-motion. In this task,
we take gradient of the negative of the regression loss with
respect to the activation maps of the last layer.
For further details see the report
