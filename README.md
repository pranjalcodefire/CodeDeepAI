# codedeepai
OpenCV utility functions 

### pip install codedeepai

## Write Video Class 

OpenCV provides a lot of useful functions to work with images and video files. One such operation is saving video using OpenCV. However, saving video with OpenCV, although is a straightforward operation, but at times it becomes very time consuming to debug because of some silly mistakes. Any time there is any issue, the frames do not get added to video file, and the video thus generated does not work. For example if the extension of video file saved does not match the encoding that we are using, the video file does not get written. Similarly, if there is issue with fps or frame size, the video file does not get written to and hence does not work. This class adds a few validations like that to make saving videos smooth. 

### Usage example 

#### Constructor

initialise write Video object. Notice if you do not have the video frame yet, you need not pass the same. Which means actual writer object will be created when we start saving.

vw = writeVideo(savePath, capture)

savePath (for example "./vid/temp.mp4") is the path where Video file will be saved. Based on the extension used for file naming, a compatible video encoding will automatically be selected. 

Here is the default signature of Ctor

__init__(self, filepath, capture, currentframe = None, fps = None )



#### The Video Save function

This is the most important fuction with following signature
save(self, currentframe, starttime = 0, elapsedtime = -1)
currentframe: Is the current frame of video that needs to be saved
starttime: time in milleseconds from where video saving needs to start
elapsedtime: Delta time in milli seconds for which the video needs to be saved. -1 (default) for up to end of video

Blog Post with detailed code explaination and usage 
https://codedeepai.com/save-video-with-opencv-python/
